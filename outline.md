## Ember Addons

Turbocharge development with other people's code

How to tell which will:
- make us more productive
- be hard to integrate or maintain
- completely blow up our app

Example: Search google for angular2 bootstrap

Example: Search https://emberobserver.com/ for bootstrap

Ember Addons
- plugin system for ember-cli
- often a wrapper around 3rd party libraries
- automates installation and build = easy to use
- ember team tries to help authors make quality addons
 - `ember addon my-addon` includes dummy app
 - tests run in stable, beta, canary versions of ember
 - good docs https://ember-cli.com/extending/

Let's add some addons!

## Maps

Esri has 2 JS libraries:
- ArcGIS API for JavaScript: https://developers.arcgis.com/javascript/
 - SDK for the web (~feature parity w/ other SDKs)
- esri-leaflet: http://esri.github.io/esri-leaflet/
 - Lightweight plugin for popular Leaflet mapping library http://leafletjs.com/

Both work in ambitious app, depends on your needs
- use JSAPI if you need features like:
 - 3D
 - Smart mapping
 - web maps
- Leaflet is better for:
 - applications that target mobile users
 - integrating w/ other frameworks

Why is JSAPI hard to integrate w/ frameworks?
- better than ever, but
- loading modules is still a challenge (Dojo, AMD, blah, blah, blah)
- a few of us at Esri are dedicated to making this work
- start here: https://github.com/Esri/jsapi-resources/tree/master/frameworks
 - Ember: https://github.com/Esri/jsapi-resources/tree/master/frameworks/ember
 - https://github.com/Esri/ember-cli-amd

We're going to build:
- Map on items route that shows extents of paged search results
- Could use either lib, but this is _ambitious_ apps, so we're going to assume you'll need to later add other functionality, so will use JSAPI
- after we're done, I'll show a similar map built w/ esri-leaflet w/ link to source for reference

Let's make a map!
