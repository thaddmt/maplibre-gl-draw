# @maplibre/maplibre-gl-draw

[![Build Status](https://travis-ci.org/mapbox/mapbox-gl-draw.svg?branch=main)](https://travis-ci.org/mapbox/mapbox-gl-draw)

Adds support for drawing and editing features on [mapbox-gl.js](https://www.mapbox.com/mapbox-gl-js/) maps. [See a live example here](https://www.mapbox.com/mapbox-gl-js/example/mapbox-gl-draw/)

**Requires [mapbox-gl-js](https://github.com/mapbox/mapbox-gl-js).**

### Installing

```
npm install @mapbox/mapbox-gl-draw
```

Draw ships with CSS, make sure you include it in your build.

### Usage in your application

#### JavaScript

**When using modules**

```js
import mapboxgl from 'mapbox-gl';
import MapboxDraw from "@mapbox/mapbox-gl-draw";
```

**When using a CDN**

```html
<script src='https://api.mapbox.com/mapbox-gl-js/plugins/mapbox-gl-draw/v1.3.0/mapbox-gl-draw.js'></script>
```

#### CSS

**When using modules**
 ```js
import '@mapbox/mapbox-gl-draw/dist/mapbox-gl-draw.css'
 ```

**When using CDN**
```html
<link rel='stylesheet' href='https://api.mapbox.com/mapbox-gl-js/plugins/mapbox-gl-draw/v1.3.0/mapbox-gl-draw.css' type='text/css' />
```

### Typescript

Typescript definition files are available as part of the [DefinitelyTyped](https://github.com/DefinitelyTyped/DefinitelyTyped/tree/master/types/mapbox__mapbox-gl-draw) package.

```
npm install @types/mapbox__mapbox-gl-draw
```

### Example usage

```js
mapboxgl.accessToken = 'YOUR_ACCESS_TOKEN';

var map = new mapboxgl.Map({
  container: 'map',
  style: 'mapbox://styles/mapbox/streets-v11',
  center: [40, -74.50],
  zoom: 9
});

var Draw = new MapboxDraw();

// Map#addControl takes an optional second argument to set the position of the control.
// If no position is specified the control defaults to `top-right`. See the docs
// for more details: https://docs.mapbox.com/mapbox-gl-js/api/#map#addcontrol

map.addControl(Draw, 'top-left');

map.on('load', function() {
  // ALL YOUR APPLICATION CODE
});
```

https://www.mapbox.com/mapbox-gl-js/example/mapbox-gl-draw/

### See [API.md](https://github.com/mapbox/mapbox-gl-draw/blob/main/docs/API.md) for complete reference.

### Enhancements and New Interactions

For additional functionality [check out our list of custom modes](https://github.com/mapbox/mapbox-gl-draw/blob/main/docs/MODES.md#available-custom-modes).

Mapbox Draw accepts functionality changes after the functionality has been proven out via a [custom mode](https://github.com/mapbox/mapbox-gl-draw/blob/main/docs/MODES.md#creating-modes-for-mapbox-draw). This lets users experiment and validate their mode before entering a review process, hopefully promoting innovation. When you write a custom mode, please open a PR adding it to our [list of custom modes](https://github.com/mapbox/mapbox-gl-draw/blob/main/docs/MODES.md#available-custom-modes).
