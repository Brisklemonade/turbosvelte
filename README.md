<p align="center">
  <h1 align="center">Turborepo SvelteKit System starter</h1>
  <h3 align="center">This is an unofficial SvelteKit monorepo starter powered by Turborepo.</h3>
</p>

# What's inside?

This Turborepo includes the following packages and apps:

### Apps and Packages

- `docs`: A placeholder documentation site powered by [MdSvex](https://mdsvex.pngwn.io/docs/) (coming soon)
- `@rename/core`: core components
- `@rename/tsconfig`: shared `tsconfig.json`s used throughout the monorepo
- `eslint-preset-acme`: ESLint preset (coming soon)

Each package and app is 100% [Typescript](https://www.typescriptlang.org/).

### Utilities

This turborepo has some additional tools already setup for you:

- [Typescript](https://www.typescriptlang.org/) for static type checking
- [ESLint](https://eslint.org/) for code linting
- [Prettier](https://prettier.io) for code formatting

## Installation

Run the following command:

```bash
npx create-turbosvelte your-app
```

### Changing the NPM organization scope

The NPM organization scope for this design system starter is `@rename`. To change this, it's a bit manual at the moment, but you'll need to do the following:

- Rename folders in `packages/*` to replace `rename` with your desired scope
- Search and replace `rename` with your desired scope
- Re-run `npm install`

# Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

# License

[MIT](https://choosealicense.com/licenses/mit/)
