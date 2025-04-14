# Node Scripts

```json
"scripts": {
  "prepare": "husky",
  "dev": "run-p -sr shopify:dev tailwind:watch",
  "dev:sync": "run-p -sr shopify:dev:sync tailwind:watch",
  "shopify:dev": "shopify theme dev -s pergolux-tyskland.myshopify.com",
  "shopify:dev:sync": "shopify theme dev -s pergolux-tyskland.myshopify.com --theme-editor-sync",
  "tailwind:watch": "npx tailwindcss -i ./assets/base.css -o ./assets/main.css -w",
  "build:css": "npx tailwindcss -i ./assets/base.css -o ./assets/main.css --minify",
  "pull:live": "shopify theme pull -l -n -o settings_data.json templates/*.json sections/*.json",
  "pull:dev": "shopify theme pull -d -n -o settings_data.json templates/*.json sections/*.json",
  "push:dev": "shopify theme push -d -o settings_data.json templates/*.json sections/*.json",
  "push:new": "shopify theme push -u -x .shopifyignore",
  "lint:all": "run-s -s prettier:fix eslint theme:check",
  "prettier": "prettier -c . --config .prettierrc.json --config-precedence file-override",
  "prettier:fix": "prettier -w . --config .prettierrc.json --config-precedence file-override",
  "eslint": "eslint assets/*.js --config ./.eslintrc.js",
  "theme:check": "shopify theme check"
}
```

## TL;DR - Dev Flow

```bash
npm run dev        # Start dev server + tailwind watcher
npm run dev:sync   # Same, but keeps theme editor in sync
npm run push:dev   # Push local theme to Shopify dev theme
npm run lint:all   # Format & lint everything
```

## Prepare

```js
{
  "prepare": "husky"
}

/*
1. This runs when you install dependencies.
2. Used to setup Husky, which is for managing Git hooks (like pre-commit linting or tests).
*/
```

## Development Scripts

```js
{
  "dev": "run-p -sr shopify:dev tailwind:watch",
  "dev:sync": "run-p -sr shopify:dev:sync tailwind:watch",
}

/*
1. run-p -sr = run scripts in parallel (-p), stream output (-s), and kill all if one fails (-r).

These spin up:
  - Shopify’s theme development server.
  - Tailwind in watch mode to auto-build CSS on file changes.

dev uses basic theme dev, dev:sync adds the --theme-editor-sync flag (helps sync changes with Shopify’s editor live).
*/
```

## Shopify Scripts

```js
{
  "shopify:dev": "shopify theme dev -s pergolux-tyskland.myshopify.com",
  "shopify:dev:sync": "shopify theme dev -s pergolux-tyskland.myshopify.com --theme-editor-sync",
}

/*
1. Spin up a local dev server and tunnel it to the Shopify store.
2. The sync variant also lets the Shopify theme editor stay in sync with your local changes.
*/
```

## Tailwind Scripts

```js
{
  "tailwind:watch": "npx tailwindcss -i ./assets/base.css -o ./assets/main.css -w",
  "build:css": "npx tailwindcss -i ./assets/base.css -o ./assets/main.css --minify",
}

/*
1. tailwind:watch: Watches your base.css file for changes and outputs a full CSS file.
2. build:css: One-time minified build—used for production.
*/
```

## Theme Sync Scripts

```js
{
  "pull:live": "shopify theme pull -l -n -o settings_data.json templates/*.json sections/*.json",
  "pull:dev": "shopify theme pull -d -n -o settings_data.json templates/*.json sections/*.json",
  "push:dev": "shopify theme push -d -o settings_data.json templates/*.json sections/*.json",
  "push:new": "shopify theme push -u -x .shopifyignore",
}

/*
1. These control theme pulling/pushing between local and Shopify store environments.
2. -l = live theme, -d = development theme, -n = no prompt, -o = output only specific files.
3. push:new: Uploads to a new unpublished theme, respecting .shopifyignore.
*/
```

## Linting & Formatting

```js
{
  "lint:all": "run-s -s prettier:fix eslint theme:check",
  "prettier": "prettier -c . --config .prettierrc.json --config-precedence file-override",
  "prettier:fix": "prettier -w . --config .prettierrc.json --config-precedence file-override",
  "eslint": "eslint assets/*.js --config ./.eslintrc.js",
  "theme:check": "shopify theme check"
}

/*
1. lint:all: Runs all the checks and fixers.
2. prettier: Checks formatting.
3. prettier:fix: Auto-fixes formatting issues.
4. eslint: Lints your JS files.
5. theme:check: Shopify's own theme linter (checks Liquid, templates, etc.).
*/
```
