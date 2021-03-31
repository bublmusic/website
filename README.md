# Airleventy

Build static websites with 11ty, Sass for CSS, and modern JavaScript.

Comes with a Netlify deploy config, but can be hosted anywhere.

## Increase your power levels

5. [Add favicons/device icons](https://www.favicon-generator.org/)
6. [Add a sitemap](https://developers.google.com/search/docs/advanced/sitemaps/build-sitemap)
7. [Configure eleventy](https://www.11ty.dev/docs/watch-serve/)

## Setup

```shell
$ npm i
```

## Commands

### Develop

```sh
$ npm run watch
```

### Build

```sh
$ npm run build
```

There are also a slew of individual commands to run individual build processes such as styles, scripts, etc.

## Netlify

First, enable your Eleventy Skeleton repo on Netlify's interface.

When prompted, clear the `build` and `publish` fields (that's what your `netlify.toml` is for). Then set your deploy branch (e.g., `main`).

Now each time you push to your deploy branch you'll also deploy your most recent changes. 🎉

## Writing JavaScript

Writing JS is pretty straightforward, but has prescriptions on file structure & naming:

-   All scripts are processed through rollup with a basic Babel configuration using `preset-env`. Configure this as you please.
-   Any file with a preceding underscore is treated as a module, and not copied as a direct file output.
-   Any file without an underscore is conversely treated as an asset file and copied over.
-   All file paths are preserved. Meaning if you create `assets/js/hello/world/script.js`, the output becomes `assets/dist/js/hello/world/script.js`.
