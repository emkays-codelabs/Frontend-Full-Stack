# Vite Quick Reference Guide

## Essential Commands

### Project Setup
```bash
# Create new Vite project
npm create vite@latest

# Install dependencies
npm install

# Start dev server (with HMR)
npm run dev
```

### Development
```bash
# Start dev server on custom port
npm run dev -- --port 3000

# Stop dev server
Ctrl + C
```

### Production
```bash
# Build for production
npm run build

# Preview production build locally
npm run preview

# Clean build output
rm -rf dist/
```

---

## Project Structure Reference

```
project/
├── index.html              # Entry point (served first)
├── vite.config.js          # Main configuration
├── package.json            # Dependencies & scripts
├── src/
│   ├── main.jsx            # App bootstrap
│   ├── App.jsx             # Root component
│   ├── App.css             # Styles
│   └── assets/             # Images, fonts (optimized)
├── public/                 # Static files (copied as-is)
├── dist/                   # Built output (created by build)
└── .env                    # Environment variables
```

---

## Configuration Snippets

### vite.config.js Template

```javascript
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'

export default defineConfig({
  plugins: [react()],
  
  server: {
    port: 5173,
    open: true,              // Auto-open browser
    host: '0.0.0.0',         // Expose to network
  },
  
  build: {
    outDir: 'dist',
    sourcemap: false,
    minify: 'terser',
  },
  
  resolve: {
    alias: {
      '@': '/src',
    }
  }
})
```

### Environment Variables (.env)

```bash
# Must start with VITE_ prefix
VITE_API_URL=https://api.example.com
VITE_APP_TITLE=My App
VITE_ENV=development
```

Access in code:
```javascript
const apiUrl = import.meta.env.VITE_API_URL
```

### TypeScript Config (tsconfig.json)

```json
{
  "compilerOptions": {
    "target": "ES2020",
    "useDefineForClassFields": true,
    "lib": ["ES2020", "DOM", "DOM.Iterable"],
    "module": "ESNext",
    "skipLibCheck": true,
    "strict": true
  }
}
```

---

## Common Tasks

### Adding TypeScript to JavaScript Project

1. Rename `main.jsx` → `main.tsx`
2. Update `index.html`:
   ```html
   <script type="module" src="/src/main.tsx"></script>
   ```
3. Create `tsconfig.json` (see template above)
4. Install `typescript`: `npm install -D typescript`

### Importing Static Assets

```javascript
// Optimized (hashed, inlined if small)
import logo from './assets/logo.svg'

// Static (copied as-is)
<img src="/vite.svg" alt="Vite" />
```

### Code Splitting & Lazy Loading

```javascript
import React, { lazy, Suspense } from 'react'

// Load component only when needed
const Heavy = lazy(() => import('./pages/Heavy'))

function App() {
  return (
    <Suspense fallback={<div>Loading...</div>}>
      <Heavy />
    </Suspense>
  )
}
```

### Path Aliases

In `vite.config.js`:
```javascript
resolve: {
  alias: {
    '@': '/src',
    '@components': '/src/components',
    '@utils': '/src/utils',
  }
}
```

Usage:
```javascript
import Button from '@components/Button'
import { helper } from '@utils/helpers'
```

### Installing & Using Plugins

```bash
# Example: QR code plugin for mobile testing
npm install -D vite-plugin-qrcode
```

In `vite.config.js`:
```javascript
import qrcode from 'vite-plugin-qrcode'

export default defineConfig({
  plugins: [qrcode()],
  server: {
    host: '0.0.0.0',  // Needed for QR scanning
  }
})
```

---

## Built-in Environment Variables

```javascript
// Development vs Production
import.meta.env.DEV        // boolean (true in dev)
import.meta.env.PROD       // boolean (true in prod)
import.meta.env.MODE       // 'development' or 'production'
import.meta.env.BASE_URL   // Base URL path

// Server-side rendering
import.meta.env.SSR        // boolean (true if SSR)

// Custom variables (prefixed with VITE_)
import.meta.env.VITE_API_URL
```

---

## Hot Module Replacement (HMR)

HMR is automatic for most frameworks. For vanilla JS:

```javascript
// Accept updates to this module
if (import.meta.hot) {
  import.meta.hot.accept((module) => {
    // Handle update
    console.log('Module updated')
  })
}
```

Preserve state across updates:
```javascript
// Your app state
let count = 0

export function increment() { count++ }
export function getCount() { return count }

// Preserve state on HMR
if (import.meta.hot) {
  import.meta.hot.accept()
}
```

---

## Performance Optimization

### Build Analysis

```bash
npm install -D rollup-plugin-visualizer
```

In `vite.config.js`:
```javascript
import { visualizer } from 'rollup-plugin-visualizer'

export default defineConfig({
  plugins: [visualizer()],
})
```

Run `npm run build` to generate `stats.html` showing bundle composition.

### Common Optimizations

| Task | Solution |
|------|----------|
| Large bundle | Code splitting with `React.lazy()` |
| Slow startup | Pre-bundle with esbuild (automatic) |
| Stale cache | Asset fingerprinting (automatic) |
| Find unused code | Tree-shaking (use named exports) |
| Slow builds | Check for heavy plugins, large assets |

---

## Deployment

### Vercel (Recommended)

```bash
npm install -g vercel
vercel
# Auto-detects Vite and deploys
```

### Netlify

```bash
npm run build
# Drag dist/ folder to Netlify or connect Git
```

### GitHub Pages

```javascript
// vite.config.js
export default defineConfig({
  base: '/your-repo-name/',
})
```

```bash
npm run build
# Deploy dist/ to gh-pages branch
```

### Traditional Hosting (VPS, Shared Hosting)

```bash
npm run build
# Upload dist/ folder via FTP/SSH
```

Configure for SPA routing (Nginx example):
```nginx
location / {
  try_files $uri $uri/ /index.html;
}
```

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| Port already in use | `npm run dev -- --port 3000` |
| Changes not appearing | Check HMR config in `vite.config.js` |
| Module not found | Check import paths, verify file exists |
| CSS not scoped | Use `.module.css` for CSS Modules |
| Large bundle | Run visualizer, remove unused deps |
| Slow builds | Check for heavy plugins, minify options |

### Common Errors

**"Cannot find module"**
- Check import path is correct
- Verify file exists at that location
- Restart dev server after adding files

**"Port 5173 already in use"**
```bash
npm run dev -- --port 3000
```

**"HMR not connecting"**
```javascript
// vite.config.js
server: {
  hmr: {
    host: 'your-machine-ip',
    port: 5173,
  }
}
```

---

## Plugin Ecosystem

Popular plugins for common tasks:

| Plugin | Purpose |
|--------|---------|
| `@vitejs/plugin-react` | React with HMR |
| `@vitejs/plugin-vue` | Vue 3 support |
| `vite-plugin-svelte` | Svelte support |
| `vite-plugin-qrcode` | QR code for mobile testing |
| `vite-plugin-svgr` | SVG as React components |
| `@vitejs/plugin-basic-ssl` | HTTPS in dev |
| `rollup-plugin-visualizer` | Bundle analysis |

Install and add to plugins array in `vite.config.js`.

---

## React-Specific Tips

### Fast Refresh Setup

```bash
npm install -D @vitejs/plugin-react
```

```javascript
// vite.config.js
import react from '@vitejs/plugin-react'

export default defineConfig({
  plugins: [react()],
})
```

Automatic! Changes to JSX appear instantly while preserving component state.

### Absolute Imports

```javascript
// vite.config.js
resolve: {
  alias: {
    '@': '/src',
  }
}

// tsconfig.json
"baseUrl": ".",
"paths": {
  "@/*": ["src/*"]
}
```

Usage:
```javascript
import Button from '@/components/Button'
```

---

## Resources

- **Official Docs:** https://vitejs.dev
- **GitHub:** https://github.com/vitejs/vite
- **Discord Community:** https://discord.gg/vite
- **Plugin Directory:** https://vitejs.dev/plugins/
- **Awesome Vite:** https://github.com/vitejs/awesome-vite

---

## Quick Wins Checklist

- [ ] Set up path aliases for cleaner imports
- [ ] Use `React.lazy()` for code splitting
- [ ] Enable source maps for debugging
- [ ] Configure environment variables
- [ ] Add QR code plugin for mobile testing
- [ ] Run visualizer to check bundle size
- [ ] Configure for SPA routing on your host
- [ ] Set up CI/CD for automatic deployment
- [ ] Use `.env.development` and `.env.production`
- [ ] Enable strict mode in tsconfig

---

Last updated: 2024
