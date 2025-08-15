# `create-preact`

<h2 align="center">
  <img height="256" width="256" src="./src/assets/preact.svg">
</h2>

<h3 align="center">Get started using Preact and Vite!</h3>

-   Vite serves from public/ for static files that bypass the build process, while it serves from src/ for source files that are processed, bundled, and optimized during the build.
-   index.html is the entry point and it imports "/src/index.tsx" which is a processed and bundled version of the actual file src/index.tsx
-   /src/style.css styles the whole thing, served as /src/style.css which just quotes it escaped inside of const __vite__css which is imported into index.tsx

## Getting Started

-   `npm run dev` - Starts a dev server at http://localhost:5173/

-   `npm run dev -- --port 8992 --host` - Starts a dev server at http://0:8992/

-   `npm run build` - Builds for production, emitting to `dist/`

-   `npm run preview` - Starts a server at http://localhost:4173/ to test production build locally
