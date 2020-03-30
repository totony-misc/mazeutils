# mazeutils
maze map making utils for warcraft 3

## TerrainKill.jass

This script is used to detect the tile at coordinates and provides a trigger that kills
units that touch a terrain type.

### install

In World editor, create a trigger named "Terrain kill".
Then, in the menu, do "Edit -> Convert to custom text" and copy paste the script.

Create variables that are needed (see the file header).

## vloc.jass

This script adds a glitched version of locust to all units in the map.
It makes every unit unclickable (but selectable).

Note that units are still vulnerable (whereas locust makes units invulnerable, unclickable
and unselectable).

### install

#### Protected/external map

Edit the war3map.j of any map, and copy paste this in the file.

Add `call vlocInit()` in the map initialization function.

#### Your own map

Create a new trigger, add an event "Map Initialization" do "Edit -> Convert to custom text"
and replace the second argument to `call TriggerAddAction(...)` of the converted trigger to
`call TriggerAddAction(..., function vlocInit)`
