# svelte-components

Steps to create a library of reusable Svelte components:

1. Choose a library name that is not already registered in npm.
2. Create the library by entering
   `npx degit sveltejs/component-template` _`library-name`_.
3. `cd` _`library-name`_
4. Add a `name` property in `package.json`.

- `"name": "`_`library-name`_`",`

5. Add a version property in `package.json`.

- ex. `"version": "0.1.0",`

6. Change the value of the `main` property in `package.json`.

- `"main": "index.js",`

7. Rename `src/index.svelte` to `src/index.js`.
8. Replace the content of `src/index.js` with a line like the following for each component:

   - `export {default as MyComponentName} from './MyComponentName.svelte';`

9. Create the component `.svelte` files in the `src` directory.
10. Create a GitHub repository for the library.
11. Add this directory to the GitHub repository.
12. If not already logged into npm, enter `npm login`.
13. Publish this library to npm with `npm pub`.

- Every time changes need to be published,
  bump the version in `package.json`.
