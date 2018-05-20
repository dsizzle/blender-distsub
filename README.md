# blender-distsub
Add-on by Dale Cieslak

www.artifisizzler.com

sizzler@artifisizzler.com

The Distance-based Subdivision add-on is a simple script to prevent wasted polygons and slow render times!  In a nutshell, it sets the Subdivision level of objects in your scene based on the distance from the camera.  

The way the script works is that you set a "Near Distance" and a "Far Distance."  Anything closer to the camera than the Near Distance will get the highest subdivision level, and anything farther away than the Far Distance will get the lowest subdivision level.  Between the Near and Far Distance, the level will decrease from the highest to lowest subdivisions depending on how far away the object is.  

The default Near Distance is 0, and the Far Distance is 10000 Blender Units.  You can set those manually, or use the convenient buttons for some simple presets.  The options for Near Distance are:

1. Nearest Object - clicking this button will try to find the closest object to the camera, and set the Near Distance based on the origin of that object.

2. Nearest Selected - clicking this button will find the nearest object to the camera based on the objects you currently have selected, and set the Near Distance based on the origin of that object.

3. Camera Clip Start - clicking this button will set the Near Distance based on the Camera's near clipping distance.

Likewise, the options for Far Distance are:

1. Farthest Object - clicking this button will try to find the farthest object from the camera, and set the Far Distance based on the origin of that object.

2. Farthest Selected - clicking this button will find the farthest object from the camera based on the objects you currently have selected, and set the Far Distance based on the origin of that object.

3. Camera Clip End - clicking this button will set the Far Distance based on the Camera's far clipping distance.

The Max. Subd Level is the subdivision level that will be set for objects closest to the camera.  The Min. Subd Level is the subdivision level that will be set for objects farthest from the camera. 

The "All Objects" checkbox will allow you to affect the entire scene, or just the selected items.

By default, only the Render Level of objects will be set, so you won't see any difference in the viewport.  If you want to set the View Level so that you can see a visible representation of the subdivision levels, check the "Visible Levels" checkbox.  Just a warning, if you set the Max Subdivision level too high, it can affect your viewport performance.  

An important note is that this is based purely on the origin of objects.  If you have a large object or an object that has an origin far from the actual geometry, you might not see the results you expect. 

Also, this might be obvious, but ONLY objects with Subsurf modifiers will be affected!  