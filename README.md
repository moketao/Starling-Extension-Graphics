My porting to Starling 2.0 architecture (original extension https://github.com/StarlingGraphics/Starling-Extension-Graphics)

currently Fill and graphic class ported. 

example:

			var fill:Fill = new Fill();
			fill.texture = gaplessTexture;
			fill.textureRepeat = true;

			fill.addVertex(0, 0);
			fill.addVertex(300, 0);
			fill.addVertex(250, 300);			
			fill.addVertex(250, 500);
			fill.addVertex(200, 550);
			fill.addVertex(150, 400);
			fill.addVertex(0, 100);
			fill.addVertex(50, 50);
			fill.buildGeometry();
			
			fill.uvMatrix.a = 1 / text.width;
			fill.uvMatrix.d = 1 / text.height;
			fill.applyUVMatrix();
			
			addChild(fill);



-------------------------------------------------------------------------------


Starling-Extension-Graphics
===========================

This extension adds a suite of graphics primitives such as Planes, Fills and Strokes. These are starling display objects that are automatically triangulated for fast rendering on the GPU.

These primitives can be manipulated directly, or created on your behalf by using a familiar graphics API accessed via the Shape class.



Starling Framework: the GPU powered 2D Flash API
================================================

What is Starling?
-----------------

Starling is an ActionScript 3 library that mimics the conventional Flash display tree architecture. In contrast to conventional display objects, however, Starling "lives" entirely inside the Stage3D environment. That means that all objects are rendered directly by the GPU, which leads to a significant performance boost. 

Starling's API is not a direct 1:1 port of the Flash API. The classes were streamlined and optimized for working well with the GPU; common tasks in game development were simplified. Starling hides the Stage3D internals from developers, but makes it easy to access them for those who need to create custom display objects.

Just like its iOS sibling, the [Sparrow Framework][1], Starling aims to be as lightweight and easy to use as possible. As an Open Source project, much care was taken to make the source code easy to read, understand and extend.

Where do I find more information about Starling?
------------------------------------------------

Here are a few starting points:

* [Official Homepage](http://www.starling-framework.org)
* [API Reference](http://doc.starling-framework.org)
* [Support Forum](http://forum.starling-framework.org)
* [Starling Wiki](http://wiki.starling-framework.org)
  * [Showcase](http://wiki.starling-framework.org/games/start)
  * [Books, Courses, Tutorials](http://wiki.starling-framework.org/tutorials/start)
  * [Extensions](http://wiki.starling-framework.org/extensions/start)

[1]: http://www.sparrow-framework.org
