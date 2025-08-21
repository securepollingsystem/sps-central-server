# `create-preact`

<h2 align="center">
  <img src="blinding-notes-20250819.jpg">
</h2>

<h3 align="center">Secure Polling System: Central Server</h3>

-   Vite serves from public/ for static files that bypass the build process, while it serves from src/ for source files that are processed, bundled, and optimized during the build.
-   index.html is the entry point and it imports "/src/index.tsx" which is a processed and bundled version of the actual file src/index.tsx
-   /src/style.css styles the whole thing, served as /src/style.css which just quotes it escaped inside of const __vite__css which is imported into index.tsx

## Blinding
-   blinding using Schnorr is possible using libsodium but Schnorr requires a multi-step signing process which forbids concurrency, meaning the voter and registrar have to dance back and forth together before registrar can start dancing with someone else, lest the dancees collaborate to create an unearned signature https://nickler.ninja/slides/2018-bob.pdf see also https://github.com/jedisct1/libsodium/issues/831
-   pairing is required for the kind of blinding where there's no back-and-forth, but libsodium doesn't support pairing, so we might use ChainSafe which is very well reviewed https://github.com/ChainSafe/bls
-   There's also this https://www.npmjs.com/package/bls-signatures AKA https://github.com/Chia-Network/bls-signatures (in C++/Python and no longer maintained)

## Getting Started

-   `npm run dev` - Starts a dev server at http://localhost:5173/

-   `npm run dev -- --port 8992 --host` - Starts a dev server at http://0:8992/

-   `npm run build` - Builds for production, emitting to `dist/`

-   `npm run preview` - Starts a server at http://localhost:4173/ to test production build locally
