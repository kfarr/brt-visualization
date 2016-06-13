# brt-webvr
WebVR model of the SFMTA Van Ness BRT Project

Select intersections:
- Geary and Van Ness
- Market and Van Ness

## How to run?
* No online demo yet. Instead, follow these instructions to download and install the app locally.

## How to install and run?
* git clone this repo
* npm install
* npm start
* your browser should open a new tab
* the console should show the local IP address and port for testing in browser
* navigate to /vn-geary.html or /vn-market.html

# Random dev notes below

## OSM2World for source map data
This project uses osm2world for exporting Open Street Maps data into 3D vertices in obj format. The object can be modified using Blender, handy for reducing extraneous layers from Open Street Map that can distract the visualizations.

See http://osm2world.org/

## How export 3D data from OSM2World?
* Open OSM2World (Java download required)
* Click "File > Download OSM data"
* Use Google Maps to find maximum / minimums of longitudes and latitudes or use example values below

MARKET AND VAN NESS:
LAT			LON
	37.777087 MAX, -122.421386 MIN
	37.771736 MIN, -122.416901 MAX

GEARY AND VAN NESS: (inclusive of O'Farrell)
	Upper-Left: 37.786415, -122.423218 (Post and Franklin)
	Lower-Right: 37.784058, -122.419356 (Ellis and Polk)

	LAT			LON
	37.786415 MAX, -122.41935 MAX
	37.784058 MIN, -122.423218 MIN

## Sample A-Frame code for importing obj files as assets
<a-scene>
  <a-assets>
    <a-asset-item id="tree-obj" src="/path/to/tree.obj"></a-asset-item>
  </a-assets>
</a-scene>

More docs here:
https://aframe.io/docs/0.2.0/components/obj-model.html

## Other projects that could be integrated
* https://github.com/IdeaSpaceVR/aframe-particle-system-component
* https://github.com/richardanaya/aframe-webvr-controller
