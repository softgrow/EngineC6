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

An example is provided directed at the Country Fire Service through three files:

***cfs2.patch*** is provides custom transformation to include SA Ambulance Service sites as
fire stations with an "(Ambulance)" suffix, so that this feature can be easily found.

***Water.osm*** was edited in JOSM to make a series of "American Restaurants" which provide the private details of Water Points. These include the contact details of the local contact as in the Group Response Plan.

***get_data*** includes a bounding box for SA so that the entire state is included in the output map

## Requirements and Usage

A single script *get_data* is provided that will download
and run the whole tool chain. At the end a gmapsupp.![
file is produced in the *scratch* directory which Should
then be copied to the *Maps* directory (create if it doesn't already exist)
Then turn off

## Modify for other Uses

* Include

### Transforming Data

### Private Data
