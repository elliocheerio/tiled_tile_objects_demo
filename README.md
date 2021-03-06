# haxeflixel-tiled-tile-objects-demo

This is a demo for Adding Support for Tiled Collision Editor to HaxeFlixel.

HaxeFlixel/Flixel-addons issue: [316](https://github.com/HaxeFlixel/flixel-addons/issues/316)

### Use Case

This feature will add objects to tiles which were created in the Tile Collision Editor in Tiled. The objects can be used for collisions, or anything else a developer wants.

![Tiled Editor Demo](assets/html_images/tiled_five.png)  
*Objects added to tiles, drawn in HaxeFlixel debugger*

### In Code

Objects are saved as `TiledObject`s and can be accessed from `TiledTilePropertySet`
``` 
var propertySet = new TiledTilePropertySet(tileID);
for (i in 0...propertySet.tileObjects.length)
{
    trace('loaded a tile object of type ' + properySet.tileObjects[i].objectType);
}
```

### In Tiled Editor

To add objects to tiles in Tiled Editor:

1. Select **Edit Tileset**  
![Tiled Editor Edit Tileset](assets/html_images/tiled_one.png)

2. Select a Tile to edit
3. Select an object type from **Tile Collision Editor**  
![Tiled Editor Insert Rectangle](assets/html_images/tiled_two.png)

4. Draw objects on the tile  
![Tiled Editor Draw Objects](assets/html_images/tiled_three.png)

5. Optionally alter or set the object properties from **Properties**  
![Tiled Editor Optional](assets/html_images/tiled_four.png)

### Targets Tested

The following have been manually tested and succesfully compiled and ran

- windows  
- mac  
- html5 - *on mac and windows*  
- flash - *on mac*  
- neko - *on mac and windows*  