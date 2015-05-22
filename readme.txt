=== Google Maps VE ===
Contributors: Veebiekspert
Donate link: http://wordpress.veebiekspert.ee
Tags: google maps, maps, map, map markers, google, google map, easy map, store locator, map plugin, directions, map directions, google map plugin, polygons, polylines, streetview, location, marker, latitude, longitude, map widget, widget
Requires at least: 3.5
Tested up to: 4.2
Stable tag: trunk
License: GPLv2

Very powerful plugin for creating Google Maps. Easy to use and no programmer skills required. There is no limit for maps and markers count.

== Description ==

Very powerful plugin for creating Google Maps. Add maps with your customized settings to post and pages with shortcode or special editor tool. Show or hide elements with custom parameters. Get directions from any address to your destinations.

Plugin is built on wordpress core functionality. Maps, markers, polygons and polylines are based custom post type and categories are made with custom taxonomy. Images are associated with Wordpress media library.

Themes with widgets support are able to use plugin widgets: filter, elements list and directions.

Developers can use all features on their own source code and make extra functionality. Plugin is connectable with another plugins like Polylang, Taxonomy Terms Order, Advanced Custom Fields and so on.

In PRO version is also support for widgets and a lot of more features.

This is revolution in Google Maps in Wordpress.

See detailed overview about [Google Maps Ve PRO Version](http://wordpress.veebiekspert.ee)

https://www.youtube.com/watch?v=HfMk4M52P-4

= Free Version =
* Unlimited maps
* Unlimited markers, polyons and polylines
* Editable map height and width
* Get coordinates by address
* Responsive maps
* Easy to use
* UTF-8 support
* Support for localization
* Google maps types: roadmap, terrain, satellite and hybrid
* Animations
* Visitor based coordinates
* Polylang and another plugins support
* Wordpress core functionality
* Street view supported
* Maps are rendered by the latest Google maps API v3
* Autocomplete for address
* INSTALL AND INVESTIGATE more features

= Pro Version =
* Filter module
* Directions module
* Markers list module
* Carousel list
* Widgets for all modules
* Editor tool to generate shortcode into post or page
* Infowindows
* Links and images in infowindow
* Custom marker icon
* Custom marker parameters
* Insert addons above or below map
* Duplicate maps

== Changelog ==

= 1.0 =
* Added new plugin to create maps in seconds.

= 1.0.1 =
* Added autocomplete to address field.
* Fixed some small bugs

== Upgrade Notice ==

= 1.0.1 =
Fixed small bugs and added address autocomplete.

== Frequently Asked Questions ==

= How do I get PRO version? =

Visit http://wordpress.veebiekspert.ee - Free updates forever.

= How can I add multilanguage support? =

For example you can use Polylang module and enable custom post types in Polylang settings.

= How can I get maps by programmatical? =

`<?php 
// global variable for google maps object
global $google_maps_ve;

$maps = get_posts(array('post_type' => 'gmaps_map_ve'));

foreach ($maps as $map) {
	$map = $google_maps_ve->getApp()->getMap($map->ID); // see what you can do with map in next question
}
?>`

= How can I get markers, polygons and polylines by programmatical? =

`<?php 
// global variable for google maps object
global $google_maps_ve;

// get array with function get_posts()
$markers = get_posts(array('post_type' => 'gmaps_marker_ve'));
$polygons = get_posts(array('post_type' => 'gmaps_polygon_ve'));
$polylines = get_posts(array('post_type' => 'gmaps_polyline_ve'));

// get array with google maps object
$markers = $google_maps_ve->getApp()->getMapMarkers($map->ID);
$polygons = $google_maps_ve->getApp()->getMapPolygons($map->ID);
$polylines = $google_maps_ve->getApp()->getMapPolylines($map->ID);

// do something with markers
foreach ($markers as $marker) {
	$detailedMarker = $google_maps_ve->getApp()->getMapMarker($marker->ID);
}

// do something with polygons
foreach ($polygons as $polygon) {
	$detailedPolygon = $google_maps_ve->getApp()->getMapPolygon($polygon->ID);
}

// do something with polylines
foreach ($polylines as $polyline) {
	$detailedPolyline = $google_maps_ve->getApp()->getMapPolyline($polyline->ID);
}
?>`

= Where can I find custom map icons? =

You can find a lot of icons at url: http://mapicons.nicolasmollet.com/

== Screenshots ==

1. Mix of free and PRO versions.
2. Maps list in wp-admin.
3. Map basic settings.
4. Marker basic settings.
5. PRO version editor button.
6. Override map settings for post or page only.
