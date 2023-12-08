The json files are maps we upload to the WLED microcontrollers. The numbers in the maps are the physical positions of the referenced LEDs. These maps "rearrange" the physical arrangement into a 2D arrangement of columns. Each line in a json represents a vertical column, with each column five LEDs high. 

The upshot of all this is that one or more playfields can be combined into a 2D space, so that 2D effects in WLED across several playfields will look marginally coherent.

The numbers in the images are physical LED positions and are used to create the maps.

These map jsons can be placed into "ledmap.json" or "ledmapX.json" using http://[wled]/edit --ledmaps are referenced in the segments interface.
