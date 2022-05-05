# Contributing Guide

### Developing and testing

Install dependencies, build the source files and crank up a server via:

```
git clone git@github.com:maplibre/maplibre-gl-draw.git
npm install
npm start & open "http://localhost:9967/debug/?access_token=<token>"
```

### Testing

```
npm run test
```

### Publishing

To GitHub and NPM:

```
npm version (major|minor|patch)
git push --tags
git push
npm publish
```

### Naming actions

We're trying to follow standards when naming things. Here is a collection of links where we look for inspiration.

- https://turfjs.org
- https://shapely.readthedocs.io/en/latest/manual.html
