# Procedural-Rig-built-in-MayaLT-using-Mel-script

Description:
------------
This is a Procedural rig (In development)
Scripted in Maya LT 2016 
Compatible with Maya 2016 and above and Unity 3D

The purpose of this was to explore the fundamentals of Mel scripting and build a dynamic rig with complex functionality yet easy to control and animate 
It’s also compatible with Unity 3D
 
How it works:
------------ 
By a click of a button you will spawn nodes which you will be able to move around in accordance to your characters body proportions. When happy with set positions you then press another button which will create specific joints and controllers relative to the positions of the nodes spawned previously.

Attributes:
-----------
IK FK Switching 
Custom UI
Select Controllers from UI
Reset Character Function
Stretchy IK System with ON OFF Switch  
Stretchy FK 
Inherit position form IK to FK and from FK to IK
Locally and World driven IK control switches 
Set key Form Custom UI   

List of Bugs:
-------------
Middle Finger moves to weird position When Switching from IK to FK. After controllers have been zeroed out. This only happens when FK Controllers has been rotated previous to the Resetting the Character (Fix in “Zero Character Script”)


When selecting controllers From UI "QWER" keyboard buttons does not seem to Work. My theory is that, Keyboard hotkeys like QWER relates only to the active window which is why you cannot switch from Move to rotate when selecting controllers from the UI Menu. It’s contained in its own window apart from your Maya scene.

IK to FK has a slight offset dew to IK handle swivel angle
When inheriting transforms from FK and giving them to IK the Middle joint of the arm and fingers will not line up dew to IK Swivel calculation. I have not yet figured out how to get this to line Up With the middle joint of the FK arms and Fingers 

IK System will always place your middle joint in line with your Start and End joint of the IK Chain. This can be bypassed with the use Vector maths.

When shut down and Closed UI Does not seem to respond to any controller objects. Run Start Script Again to counter this
When Closing Maya And reopening all procedure need to be reloaded Fist before UI Will function properly. (Fix this by Creating a separate script to load all procedure automatically when UI is gets rebooted)

UI buttons are not yet driven by UI node so it does not respond to the change of values in UI node this can become confusing when you scrub though you animation timeline. While values Change on the UI Node the UI Buttons remains in the same state. (Fix this by creating a backwards connection between the UI Node and the UI Window)


Things To Add and Improve:
-------------------------
IKFK Switches Should be added to the UI Node
Make UI part of channel box or its own separate Tab
Update UI According to UI Node
Change Key All to Key UI
Create Key Ctrl button 
Create a Select All button 
Create Key all button 
Make all procedure Attribute driven instead of Button Driven 
Relaunch all procedure with Launch of UI
Zero Transforms should zero out everything and set Character to its default position
