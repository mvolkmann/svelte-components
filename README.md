# svelte-components

## To create a library of reusable Svelte components

1. Choose a library name that is not already registered in npm.
1. Create the library by entering
   - `npx degit sveltejs/component-template library-name`
1. `cd library-name`
1. Change the `input` property in `rollup.config.js`
   from `src/index.svelte` to `src/index.js`.
1. Add a `name` property in `package.json`.

   - `"name": "library-name",`

1. Add a `version` property in `package.json`.

   - ex. `"version": "0.1.0",`

1. Change the value of the `main` property in `package.json`.

   - `"main": "index.js",`

1. Rename `src/index.svelte` to `src/index.js`.
1. Replace the content of `src/index.js` with a line like the following for each component:

   - `export {default as MyComponentName} from './MyComponentName.svelte';`

1. Create the component `.svelte` files in the `src` directory.
1. Create a GitHub repository for the library.
1. Add the contents of this directory to the GitHub repository.
1. If not already logged into npm, enter `npm login`.
1. Every time changes need to be published,
   bump the version in `package.json`
   and tag the GitHub repository.

   - `npm version patch|minor|major`
   - `git push --tags`
   - `git push`

1. Publish this library to npm with `npm pub`.

## To use these components in a Svelte application

1. Install the library by entering `npm install library-name`
1. Import the components to be used.

- ex. `import {LabeledInput, Select} from rmv-svelte-components;`

1. Use the components like any other Svelte component.

For example:

```html
<script>
  import {LabeledInput, Select} from 'rmv-svelte-components';
  let color = '';
  let name = 'Mark';
  let options = ['', 'red', 'green', 'blue'];
</script>

<main>
  <LabeledInput label="Name" bind:value="{name}" />
  <p>Hello, {name}!</p>
  <Select options={options} on:select={event => color = event.detail} />
  <p>You selected the color {color}.</p>
</main>
```
