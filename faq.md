---
title: FAQ
layout: submenu
---

## FAQ

#### Is this open source? Where is the GitHub page?
Yes it is, and [here](http://github.com/mrzapp/opengui) it is.

#### Does OpenGUI work with C# even though it is written in UnityScript?
Yep, as long as the provided directory configuration is maintained and .cs files are in a subfolder, .e.g /Assets/Scripts. This is because of the Unity [compilation order] (http://docs.unity3d.com/412/Documentation/ScriptReference/index.Script_compilation_28Advanced29.html).

#### I have created widgets, but nothing is displaying. What might be wrong?
Make sure your [`OGPage`](https://github.com/mrzapp/opengui/wiki/OGPage) object is the current one, and make sure your OGRoot object has a Camera component

#### Where are the tutorials and documentation?
In the [wiki] (https://github.com/mrzapp/opengui/wiki)  

#### What about examples?
Check out the [example project] (https://github.com/mrzapp/opengui/releases/tag/example)

#### How can I align objects relatively to the screen?
The "anchor" and "pivot" properties of the [`OGWidget`](https://github.com/mrzapp/opengui/wiki/OGWidget) and subclasses take care of that.  

#### How do I deal with different aspect ratios?
Make sure to use "anchor" and "stretch" to position your content, if you want it to be flexible.
