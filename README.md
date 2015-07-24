#DRAPER
####Main file
+ Initialize the windows (design window & simulation window)
  + Window size, position
  + Clear color
  + Set the perspective projection...
  + Draw text for information (ShowTextDesign, ShowTextSimulation)
+ Initialize the parameters for program:
  + camera (left & right)
  + mouse event tool mode (drag, drag cut, edit curve, dart, slider)
  + gui_listner (CDesigner2D_Cloth): load cloth models, set texture, move, change camera position...)
  + pAnalysis (CAnalysis2D_Cloth_Static*): The implementation of cloth models, mapping the 2D to 3D 
+ Register handler for menu (myGlutMenu_Des, myGlutMenu_Sim)
+ Register mouse events (myGlutMotion)
+ Register keyboard events (special keys - myGlutSpecial, function keys - myGlutKeyboard)
+ Register handler when idle, resize (myGlutIdle, myGlutResize)
+ Change the problem (SetNewProblem): Call the gui_listener and pAnalysis to change the new problem (cloth models, texture, body model, ...)

####analysis2d_cloth_static.cpp
+ SetModelProblem_Cloth: Define and switch the cloth models, map the edges, load the body model, call the cloth_handler instance to create the 3D model from 2D cad models and mesh2D

##The Design Window
####Tools
-----
To change the tool, press right button and select tool from pop-up menu.
+ Drag : you can drag vertex/edge/loop of a pattern.
+ Dart Cutter : you can draw dart on a pattern. 
+ Edit Curve : you can grab the curve by click and dragging a polyline edge.
+ ChangeToLine : you can change a polyline edge to line.
+ ChangeToPolyline : you can change a line edge to a polyline edge.
+ SmoothPolyline : you can smooth a polyline edge by moving mouse with left button pressed near the polyline edge.

####Keyboard
------
+ ' '  : change 3D model
+ 'b'  : Initialize the simulation 

####View Change
-----------
This design window should be activated so as to change the view of the design window.
+ Pan : Shift+Left drag
+ Zoom : Page Up / Down


##The Simulation Window
####Texture
-------
you can change texture of cloth from pop up menu. select [texture] and chose one from submenu.

####View Change
------
This design window should be activated so as to change the view of the simulation window.
+ Pan : Shift+Left drag
+ Rotataion : Ctrl+Left drag
