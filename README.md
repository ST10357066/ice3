# Ndaedzo Austin Mukhuba - Profile

A modern React application built with Vite, TypeScript, and SWC showcasing a personal profile page.

## Features

- ⚡ **Vite** - Fast build tool and development server
- ⚛️ **React 18** - Latest React with modern features
- 🔷 **TypeScript** - Type-safe JavaScript
- 🚀 **SWC** - Super-fast JavaScript/TypeScript compiler
- 📦 **ESLint** - Code linting and formatting

## Getting Started

### Prerequisites

- Node.js (version 16 or higher)
- npm or yarn

### Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd ice3
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

4. Open [http://localhost:3000](http://localhost:3000) in your browser

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

## 🚀 Deployment to Netlify

### Option 1: Deploy via Git (Recommended)

1. **Connect your repository to Netlify:**
   - Go to [Netlify](https://netlify.com)
   - Click "Add new site" → "Import an existing project"
   - Connect your GitHub repository
   - Netlify will automatically detect the build settings from `netlify.toml`

2. **Deploy automatically:**
   - Netlify will build and deploy your site automatically on every push
   - Your site will be live at a URL like: `https://amazing-site-name.netlify.app`

### Option 2: Manual Deploy via Drag & Drop

1. **Build the project locally:**
   ```bash
   npm run build
   ```

2. **Deploy via Netlify:**
   - Go to [Netlify](https://netlify.com)
   - Click "Sites" → "Deploy manually"
   - Drag and drop the entire `dist` folder
   - Your site will be deployed instantly

## 📁 Project Structure

```
├── public/                 # Static assets
│   ├── Profilepicture.jpg  # Your profile picture
│   ├── vite.svg           # Favicon
│   └── _redirects         # SPA routing rules
├── src/                   # Source code
│   ├── App.tsx            # Main React component
│   ├── App.css            # Component styles
│   ├── main.tsx           # App entry point
│   └── index.css          # Global styles
├── dist/                  # Build output (generated)
├── netlify.toml          # Netlify deployment config
├── vite.config.ts        # Vite configuration
├── tsconfig.json         # TypeScript configuration
└── package.json          # Project dependencies
```

## 🎯 Build Configuration

The project is configured for optimal Netlify deployment:

- **Build Command:** `npm run build` (runs `npx tsc && vite build`)
- **Publish Directory:** `dist`
- **Node Version:** 18.17.0
- **Environment:** NODE_ENV = "production"
- **SPA Routing:** Automatic redirects configured
- **Security Headers:** Added for better security
- **Asset Optimization:** Static assets cached for performance

## 🐛 Troubleshooting Deployment Issues

### Common Netlify Configuration Errors:

**1. "Can't redefine existing key" Error:**
- **Cause:** Duplicate environment variable definitions in `netlify.toml`
- **Solution:** Use only the `[build.environment]` table format (not inline format)

**2. "Command not found" Error:**
- **Cause:** Node/npm not available in build environment
- **Solution:** Ensure `NODE_VERSION` is set correctly in `netlify.toml`

**3. "tsc: not found" Error:**
- **Cause:** TypeScript compiler not available globally in Netlify environment
- **Solution:** Use `npx tsc` instead of `tsc` in build scripts

**4. "Build failed" Error:**
- **Cause:** Missing dependencies or build script issues
- **Solution:** Test locally with `npm run build` before deploying

### Deployment Checklist:

- ✅ `netlify.toml` exists with correct configuration
- ✅ Build command works locally (`npm run build`)
- ✅ All dependencies listed in `package.json`
- ✅ Static assets in `public/` folder
- ✅ No conflicting environment variable definitions
- ✅ Node version specified in `.nvmrc` and `netlify.toml`

### Manual Verification:

Run this command to check your deployment readiness:
```bash
node deploy-check.js
```

**If you encounter issues:**
1. Check the Netlify build logs for specific error messages
2. Verify all files are committed to your Git repository
3. Ensure your repository is public (or you have proper permissions)
4. Try a manual drag-and-drop deployment of the `dist` folder



## Technologies Used

- **Vite** - Build tool and dev server
- **React** - UI library
- **TypeScript** - Type safety
- **SWC** - Fast compiler
- **ESLint** - Code linting
