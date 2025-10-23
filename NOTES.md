# Notes

- `npm install --save-dev netlify-shortener`
- `npm run shorten <URL> <PATH>` (e.g., `npm run shorten https://github.com gh`)
- [Syntax for the `_redirects` file](https://docs.netlify.com/routing/redirects/#syntax-for-the-redirects-file)
- [@helloample/netlify-plugin-redirects](https://www.npmjs.com/package/@helloample/netlify-plugin-redirects) plugin
- https://github.com/keithamus/sort-package-json/releases/tag/v2.7.0
- https://github.com/netlify/build/tree/main/packages/redirect-parser
- https://vercel.com/docs/project-configuration
- https://github.com/joaopalmeiro/dataviz.link

## References

- [cass.run](https://github.com/cassidoo/cass.run) by Cassidy Williams
- [netlify-shortener](https://github.com/kentcdodds/netlify-shortener) by Kent C. Dodds
- [netlify-shortener-example](https://github.com/kentcdodds/netlify-shortener-example) by Kent C. Dodds

## Commands

```bash
npm install -D netlify-shortener sort-package-json
```

## Netlify version

### `_redirects`

```plain
/alt-blog   https://medium.com/feedzaitech/styling-altair-charts-with-the-feedzai-altair-theme-f3dcd27b3b68
/biy        https://research.feedzai.com/publication/benchmark-it-yourself-biy-preparing-a-dataset-and-benchmarking-ai-models-for-scatterplot-related-tasks/
/contribs   https://gitlab.com/joaommpalmeiro/os-contribs
/ds-paper   https://diglib.eg.org/handle/10.2312/evs20221097
/fi-blog    https://medium.com/feedzaitech/analyzing-data-drift-how-we-designed-visualizations-to-support-feature-investigation-e408d4de7e9f
/fig        https://www.figma.com/@joaopalmeiro
/lib-blog   https://medium.com/feedzaitech/plotting-the-first-point-of-the-feedzai-charting-library-50f21b4a5e01
/projs      https://github.com/joaopalmeiro
/thesis     http://hdl.handle.net/10362/119698

#fallback
/*          https://www.linkedin.com/in/joaopalmeiro/
```

### `package.json`

```json
{
  "name": "palmeiro.link",
  "version": "0.0.0",
  "private": true,
  "description": "My URL shortener.",
  "license": "MIT",
  "author": "João Palmeiro",
  "type": "module",
  "scripts": {
    "format": "sort-package-json",
    "lint": "sort-package-json --check",
    "shorten": "netlify-shortener"
  },
  "devDependencies": {
    "netlify-shortener": "2.4.0",
    "sort-package-json": "3.4.0"
  }
}
```

### `README.md`

````markdown
# palmeiro.link

[![Netlify Status](https://api.netlify.com/api/v1/badges/9b93e168-b2c8-4c65-a6fd-c58643077f19/deploy-status)](https://app.netlify.com/sites/elaborate-gecko-bcdf85/deploys)

My URL shortener.

## References

- [cass.run](https://github.com/cassidoo/cass.run) by Cassidy Williams
- [netlify-shortener](https://github.com/kentcdodds/netlify-shortener) by Kent C. Dodds
- [netlify-shortener-example](https://github.com/kentcdodds/netlify-shortener-example) by Kent C. Dodds

## Development

Install [fnm](https://github.com/Schniz/fnm) (if necessary).

```bash
fnm install && fnm use && node --version
```

```bash
npm install
```

```bash
npm run lint
```

```bash
npm run format
```

```bash
npm run shorten
```

The previous command will format/validate the `_redirects` file, commit, and try to push. Don't push through the CLI but from GitHub Desktop.
````
