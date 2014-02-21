---
title: Technical
layout: submenu
---

## Technical overview

![diagram](https://raw2.github.com/mrzapp/opengui/master/Screenshots/diagram.jpg)

#### Rendering
OpenGUI utilises the low-level OpenGL library in Unity. Every [`OGWidget`](https://github.com/mrzapp/opengui/wiki/OGWidget) has its own drawing rectangle and texture coordinates depending on the assigned [`OGStyle`](https://github.com/mrzapp/opengui/wiki/OGStyle). [`OGRoot`](https://github.com/mrzapp/opengui/wiki/OGRoot) starts the draw loop by setting a pixel matrix according to the screen size, passes the atlas material from the [`OGSkin`](https://github.com/mrzapp/opengui/wiki/OGSkin) and then uses the drawing rectangles and texture coordinates to "move and crop the atlas" for every widget. The depth of a widget is solely dependent on the Z buffer, so there should be no confusion about what is on top of what.
   
#### Positioning and scaling
Screen-relative stretching and anchoring is calculated on the Transform component first. Then the position and scale of the drawing rectangle is derived from the Transform component and recalculated to fit the "flipped"" coordinates of OpenGL. 
