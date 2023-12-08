The json files are "maps" we upload to the WLED microcontrollers. The numbers in the maps are the physical positions of the referenced LEDs. These maps "rearrange" the physical arrangement into a 2D arrangement of columns. Each line in a json represents a vertical column, with each column five LEDs high. 

The upshot of all this is that one or more playfields can be combined into a 2D space, so that 2D effects in WLED across several playfields will look marginally coherent.

The numbers in the images are physical LED positions and are used to create the maps. Numbers in parentheses represent physical LEDs that are behind the playfield, invisible to the viewer (because a wire in the string might not have been long enough).

These map jsons can be placed into "ledmap.json" or "ledmapX.json" using http://[wled]/edit --ledmaps are referenced in the segments interface.

But that's not the clever bit. The clever bit comes when we place as many as 5 playfields next to each other on the wall, using WLED's ability to control a string of LEDs by IP address. But for a big 2D virtual string we need a giant composite ledmap, comprised of all the ledmaps of each of the constituent playfields. But! We can't use them without modification. When adding the map from the second playfield to the first, we have to take into account the starting number. So let's say Flash is the first playfield, on the left. It has (say) 73 LEDs total. So if we put Phoenix next to Flash, then we need to add 73 to each of the values in the Phoenix json. GPT can help with this, or you can code it up in python or whatever. An example of this can be found in the "Metamaps" folder.
