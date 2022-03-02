# Rename core

A barebones project that provides the essentials for writing highly-optimized, reusable packages in Svelte using SvelteKit's [`package`](https://kit.svelte.dev/docs#packaging) feature.

All styles are component-scoped and preprocessed into minified and prefixed CSS during packaging using [cssnano](https://cssnano.co/) and [autoprefixer](https://github.com/postcss/autoprefixer). TypeScript type definitions are generated automatically from your components using [svelte2tsx](https://github.com/sveltejs/language-tools/tree/master/packages/svelte2tsx).

## Packaging and Publishing

### Packaging

To package your components, simply run the package command:

```bash
npm run package
```

This will preprocess the contents of [`src/lib`](/src/lib) into a `package` folder at the root of your project.

### Publishing to NPM

After you have generated the `package` folder, run `npm publish ./package` to publish your library to NPM.

Be sure to properly configure `package.json` with the correct data before publishing.

## Setting up Documentation

Most components will need documentation in some form. This template doesn't have any opinions on how documentation should be handled, however it does provide you with SvelteKit's `routes` folder which can be used for this. Below are some very useful svelte-focused tools that can make your life considerably easier when documenting components:

- [vite-plugin-svled](https://github.com/mattjennings/vite-plugin-sveld) is a vite port of [sveld](https://github.com/carbon-design-system/sveld/), which allows you to automatically generate API documentation for your svelte components using typescript types and JSDoc comments.
- [mdsvex](https://mdsvex.pngwn.io/) is a superset of markdown that allows the usage of Svelte components and interactive logic. Since mdsvex preprocesses your markdown files into Svelte components, it can also be used as SvelteKit routes.
- [mdsvex-sveld](https://github.com/mattjennings/mdsvex-sveld) is an mdsvex plugin that automatically outputs markdown tables for component API documentation using [sveld](https://github.com/carbon-design-system/sveld/).

## Setting up Theming

If you plan to develop a large amount of components, it may become necessary to have people import a theme stylesheet containing variables. This can be done by creating a `theme.css` file in [`src/lib`](/src/lib) and having people import it from `node_modules`.

Developers using your library could import the theme file like so:

```html
<script>
	import 'my-package/theme.css';
	import { ComponentThatUsesTheming } from 'my-package';
</script>

<ComponentThatUsesTheming />
```

Many modern bundlers support importing CSS as ES Modules. This is likely to be the best way of importing theme files, as they can be easily resolved from `node_modules`. Alternatively, you can use @import syntax with the postcss-import plugin or sass in your \<style> tags, or consider CDNS such as [unpkg](https://unpkg.com/).

## License

All Rename packages have MIT license.
