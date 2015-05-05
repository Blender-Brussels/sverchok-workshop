Parametric modeling with Sverchok
=================================

Workshop of 29 April 2015 @ Arts2

https://github.com/Blender-Brussels/sverchok-workshop

Notes from the pad
------------------

http://piratepad.be/p/sverchok


To stay informed about the following workshops and activities, subscribe to our mailing-list
http://lurk.org/groups/blender-brussels/
We don't spam. You'll get just one or two emails a month. Max. Unless this list becomes really active for some reason :)


Installation
---------------

Domnload zip file from Github: https://github.com/nortikin/sverchok/archive/master.zip
Launch Blender and go into Users Preferences > Addons (and choose "import from file" and point to the .zip you just downloaded).

Usage
---------

Node list: http://wiki.blender.org/index.php/Extensions:2.6/Py/Scripts/Nodes/Sverchok


https://github.com/Blender-Brussels/sverchok-workshop/

Xuv's intermezzo :
https://github.com/Blender-Brussels/sverchok-workshop/blob/master/random-vertice-mask.blend

---

Little bugs found:
 - Group functions works to group them. But have not really found out how to ungroup.




---

Timeline - animate sverchok parameters
- hover over some parameter you want to animate
- use 'i' to add keyframes (interpolation works)
- the node-editor updates animated values when sliding through timeline
- BUT the 3D-view is not updated ...
    - ViewerDraw node doesn't update values automatically
    - BMeshViewer node neither.

this is a github issue concerning this topic :   https://github.com/nortikin/sverchok/issues/592
in the discussion there is a reference to checkout a specific branch, enabling the live-update of animated parameters
'git checkout origin/obj_in_liveupdate_mode' -- object_in nodes have a 'start/stop live update' button now
render works, animation render too
crashing blender when rendering animation (2.74 - sverchok commit 56ba7403220b4eb0f32fcefe4a765622c66c5c81)  was due to 'Current Frame' block in sverchok node tree -- i got rid of this in the uploaded example.

you can try 'live_update_animation.blend'  which contains two animated parameters (height & scale of an extruded cube), which is rendered to a blender BMesh (so a 'real' blender object, which is rendered a is)

---

frankie : try blender 'Drivers'  ??
