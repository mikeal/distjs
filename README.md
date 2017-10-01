# distjs - Distribute standalone WebComponents w/ npm

Usage:

```
> npm install distjs
> distjs install
```

Or, you can manually enable in your package.json.

```
{
  ...
  "scripts": {
    "prepublishOnly": "distjs",
    ...
  }
}
```

Before each npm publish `distjs` will build standealone scripts in a `dist/`
directory. These scripts dynamically load a WebComponents polyfill before
requiring your package.

The dist files will be named `${pkgname}.js` and `${pkgname}.min.js`.

This means that people can use your new elements with a simple script include
from one of the many npm content CDN's.

Example:

```html
  <script src="https://cdn.jsdelivr.net/npm/pkgnamt@latest/dist/pkgname.min.js"></script>
```