# Coordinate-Generator 

The purpose of this module is to generate random coordinates within a specified area. For this 
project the coordinates are supposed to be part of the greater Gothenburg area. Changing the 
code to generate coordinates in other areas should be possible without much additional work 
however.

## Approaches
- Epicentrum: Select a centrum for the generation of coordinates and generate generate 
coordinates in randomly selected circular distance.
Pros: simple, balanced distribution
Cons: Unaware of environment (creating coordinates in sea, forests, lakes)
- Polygon: Select a polygon and randomly generate coordinates within.
Pros: can be very precise (excluding sea, forests, lakes, river)
Cons: very complex model, difficult to define good polygon
- Point-Cloud: Randomly select coordinates form a list of locations.
Pros: Simple implementation, can deal with non-urban areas
Cons: discrete set of locations

## Implementations

Some of the suggested approaches have been implemented and tested:

### Point-Cloud

This approach was tested by using a list of points as basis for the random point generation. The 
list of points is extracted from a .geojson-file which is created using the overpass-API of 
open-street-maps. The image gothenburg_busstop_map.png shows the distribution of the extracted 
bus stops through the area of Gothenburg.

An approach to solving the problem of discreteness introduced by using this set of bus-stops 
could be the superimposition of a blurring filter. E.g. placing the final location in a radius 
of 200 meter around the selected bus stop location.
