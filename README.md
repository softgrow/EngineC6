# EngineC6
Tools for modifying and styling OpenStreetMap on Garmin for specialist uses.

## Introduction

If you use OSM on Garmin it might not suit your particular use if the default map style isn't exactly what you want. By providing generic
styling tools the utility is increased greatly as a task based map can be produced. The usual workflow is:

* Extract an area from OpenStreetMap
* Process with mkgmap using a simple style
* Load to Garmin

This projects outlines techniques to transform the OpenStreetMap data by:

* Transform the presentation of information
* Add in separate (possibly private) data

## Example provided

An example is provided directed at the Country Fire Service by providing a "Map Book" on Garmin through three files:

***cfs2.patch*** is provides custom transformation to include SA Ambulance Service sites as
fire stations with an "(Ambulance)" suffix, so that this feature can be easily found in the *Everyday Life*->*Community Services*->*Fire Stations* Category

***Water.osm*** was edited in JOSM to make a series of "American Restaurants" which provide the private details of Water Points. These include the contact details of the local contact as in the Group Response Plan. These can be easily found in the *Restaurants*->*Cuisine*->*American* Category. This category was chosen as it is relatively unused in South Australia (and you never know you might want some ribs as well).

***get_data*** includes a bounding box for SA so that the entire state is included in the output map.

## Requirements and Usage

* Written to run under *OS X* but can easily be changed for Linux or Windows
* Java JRE 7 or later for mkgmap
* Access to the internet to download prequesites


A single script *get_data* is provided that will download
and run the whole tool chain. At the end a *gmapsupp.img*
file is produced in the *scratch* directory which Should
then be copied to the *Maps* directory (create if it doesn't already exist)

Turn on the GPS then de-select other maps and restart the GPS and you are ready

## Modify for other Uses

### Transforming Data

Produce a patch file to modify the default style (a patch allows easier incorporation of new features from the mkgmap default tree). A feature that currently does not appear on the GPS can be included by mapping to an existing category and probably modifying the name as shown in the example.

### Private Data
Edit this as a separate layer in JOSM including any details you want and save the resultant XML to a *.osm* file. Include each of these as a "input-file" term in the invocation of *mkgmap*
