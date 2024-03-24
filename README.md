# Atomic Design Methodology
- Folder structures with Atom ✅
```
📦src
 ┣ 📂components
 ┃ ┣ 📂atoms
 ┃ ┣ 📂molecules
 ┃ ┣ 📂organisms
 ┃ ┣ 📂pages
 ┃ ┗ 📂templates
 ┣ 📜App.tsx
 ┣ 📜main.tsx
 ┣ ...rest
 ┗ 📜vite-env.d.ts
 ```

 - Break Down

| <div style="width:150px">Folder</div>               | Description |
| -------------------- | ----------- |
| 📂 atoms     | The fundamental building blocks, like individual HTML elements (buttons, forms, labels) or basic design principles (color palettes, fonts). Think of them as the smallest, reusable units.       |
| 📂 molecules    | Groups of atoms that come together to form a more complex component. Imagine combining a button and a text field to create a search bar. Molecules are still reusable, but offer slightly more functionality.        |
| 📂 organisms   | Composed of various molecules (and sometimes atoms) to create a distinct section of your interface. A header with a logo, navigation menu, and search bar would be an organism. Organisms are self-contained and have a clear purpose.        |
| 📂 pages   | The final product –  unique instances of your templates filled with specific content.  Imagine a contact page using a header organism, a form molecule, and other components to create a functional page.        |
| 📂 templates   | Layouts that define the overall structure of your pages. Templates combine organisms to showcase how content will be organized. Think of them as blueprints for your final webpages.        |
 
# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type aware lint rules:

- Configure the top-level `parserOptions` property like this:

```js
export default {
  // other rules...
  parserOptions: {
    ecmaVersion: 'latest',
    sourceType: 'module',
    project: ['./tsconfig.json', './tsconfig.node.json'],
    tsconfigRootDir: __dirname,
  },
}
```

- Replace `plugin:@typescript-eslint/recommended` to `plugin:@typescript-eslint/recommended-type-checked` or `plugin:@typescript-eslint/strict-type-checked`
- Optionally add `plugin:@typescript-eslint/stylistic-type-checked`
- Install [eslint-plugin-react](https://github.com/jsx-eslint/eslint-plugin-react) and add `plugin:react/recommended` & `plugin:react/jsx-runtime` to the `extends` list
