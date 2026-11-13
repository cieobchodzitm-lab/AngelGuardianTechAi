# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) (or [oxc](https://oxc.rs) when used in [rolldown-vite](https://vite.dev/guide/rolldown)) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## React Compiler

The React Compiler is enabled on this template. See [this documentation](https://react.dev/learn/react-compiler) for more information.

Note: This will impact Vite dev & build performances.

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type-aware lint rules:

```js
export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...

      // Remove tseslint.configs.recommended and replace with this
      tseslint.configs.recommendedTypeChecked,
      // Alternatively, use this for stricter rules
      tseslint.configs.strictTypeChecked,
      // Optionally, add this for stylistic rules
      tseslint.configs.stylisticTypeChecked,

      // Other configs...
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```

You can also install [eslint-plugin-react-x](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-x) and [eslint-plugin-react-dom](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-dom) for React-specific lint rules:

```js
// eslint.config.js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...
      // Enable lint rules for React
      reactX.configs['recommended-typescript'],
      // Enable lint rules for React DOM
      reactDom.configs.recommended,
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```

## Status zrzutki AGT / PDS HU-SAR (2026-11-13)

Aktualny, publicznie bezpieczny status programu i zrzutki jest w [`STATUS.md`](STATUS.md). Skrót nowości: [`NEWS.md`](NEWS.md). Ślad audytu: [`AUDIT_TRAIL.md`](AUDIT_TRAIL.md).

- Zrzutka: [https://zrzutka.pl/hkkzyn](https://zrzutka.pl/hkkzyn) (cel 555 000 zł).
- Landing: [https://agt-lab-zrzutka.vercel.app/](https://agt-lab-zrzutka.vercel.app/).
- 12–13.11.2026: korekta treści landingu po audycie zgodności HSA-001; ponowny audyt tekstu 13.11.2026 — PASS.
- Program PDS HU-SAR obejmuje dwa odrębne elementy: kask RESCUE RECON i dwuwirnikowy dron zwiadowczy.
- Pozycjonowanie: AI dla ratownictwa (SAR), dual-use defensywne. Estońska spółka AGT jest w trakcie zakładania.
- Medal Benenati to imienny cyfrowy certyfikat. Medale NFT są 1/1 i nie dają praw do zysku. Zbiórka kapitałowa dopiero po prototypie.
- Kolekcja Stoic Matrix / Amor Fati Bene Nati na Solanie: nie wdrożona (NOT DEPLOYED).
