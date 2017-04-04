---
layout: post
title: "Notes on learning computer graphics"
date: 2017-02-26 9:37:00 -0500
---

A few months ago I began diving into computer graphics programming with the
platform of choice being WebGL. I knew libraries like Three.js existed, but when
learning a new domain, I like to see what the primitives are so that
I know what the limits of the platform are versus the limits of the tools and
abstractions I'm using. This is a content dump of various resources I've
discovered on my journey.

A good, fast-paced overview of what WebGL itself offers is Gregg Taveres'
 <a href="https://webglfundamentals.org/">WebGL Fundamentals</a>.
After going through these I was left with a new pile of topics to learn from
shaders and vector math, to 3D modeling and game physics.

## Game development

One of the main points of Gregg's tutorials is that WebGL is just a drawing API,
to get interesting results you have to perform the math and manipulation of
data that represents vertices and colors, among other things. I realized that these
problems are what game developers have been doing for decades. So, while you may
not be interested in creating games, it is worth while to learn enough about game
programming to know what techniques to steal.

One of the best resources for learning game development is Handmade Hero by
Casey Muratori.

<a href="https://hero.handmade.network/episodes" target="_blank">
  https://hero.handmade.network/episodes</a>

There is a _ton_ of material here, but you can pick and choose topics of interest.

My search for how to get real work done led me to the book WebGL Game Development
(linked below), this is a great place to start getting a feel for how to make things
happen with WebGL and a browser.

### Simulation loops

Along the way I happened upon <a target="_blank" href="http://gameprogrammingpatterns.com/contents.html">
Game programming patterns</a>; unfortunately it is steeped in object oriented
dogma. I still recommend reading it though, as it does contain some gems,
the most important being the game loop chapter:

<a href="http://gameprogrammingpatterns.com/game-loop.html" target="_blank">
http://gameprogrammingpatterns.com/game-loop.html
</a>

This is a fundamental topic when doing any animation and there isn't much out
there about it. Even the WebGL fundamentals chapter on animation gets it
<a href="https://webglfundamentals.org/webgl/lessons/webgl-animation.html" target="_blank">
wrong</a> (recommends using a variable time step).

The footnotes in the chapter includes references to other helpful articles on game loops:

<a href="http://gafferongames.com/game-physics/fix-your-timestep/">
http://gafferongames.com/game-physics/fix-your-timestep/</a>

<a href="http://www.koonsolo.com/news/dewitters-gameloop/" target="_blank">
http://www.koonsolo.com/news/dewitters-gameloop/</a>
<a href="" target="_blank"></a>

<a href="http://web.archive.org/web/20141116170950/http://www.richardfine.co.uk/2012/10/unity3d-monobehaviour-lifecycle/
" target="_blank">
Unity3D behaviour lifecylce</a>
and the updated version of that info:
<a href="https://docs.unity3d.com/Manual/ExecutionOrder.html" target="_blank">
https://docs.unity3d.com/Manual/ExecutionOrder.html</a>

The talk "We will all be game programmers" linked below also touches on this
important concept.

The big insight for me was that there are really two separate loops in all
simulations, a physics (AKA state management) loop and a rendering loop.

By separating how these two systems update you can control how your game performs
on a wide variety hardware with varying performance characteristics.

### Physics

One thing that was not obvious to me is that the physics you use in games is
not of the analytical kind like you find in high school and college classes,
but is numerical instead. Meaning, you're mostly using fairly simple algebraic
formulas in your code instead of manipulating abstract symbols.
The concepts may be similar but the applications are quite different.

I'm only beginning to dig into this subject but here are some resources I've
found useful:

<a href="http://buildnewgames.com/gamephysics/" target="_blank">http://buildnewgames.com/gamephysics/</a>

<a href="http://buildnewgames.com/physics-engines-comparison/" target="_blank">http://buildnewgames.com/physics-engines-comparison/</a>

<a href="http://gafferongames.com/game-physics/
" target="_blank">http://gafferongames.com/game-physics/
</a>

### Shaders

One quick point is that if you just want to render a "typical" 3D scene you
really only need one vertex and fragment shader that handles rendering in
3D perspective and uses Gouraud or Phong shading, once these are set you can
mostly use them without thinking about them.

Shaders is its own fascinating world which can be a dedicated area of study.

Some resources that focus just on fragment shaders:

<a href="http://thebookofshaders.com/" target="_blank">http://thebookofshaders.com/</a>

<a href="https://www.shadertoy.com/" target="_blank">https://www.shadertoy.com/</a>

# Books

<a href="http://shop.oreilly.com/product/9781849699792.do" target="_blank">
WebGL Game Development
</a>

For showing actual examples and containing runnable code, this book stands alone.
It shows how to perform practical tasks like exporting models from Blender and
rendering them via WebGL. A lot of the code samples are from parts of Three.js,
but instead of just using that API like a magic black box, the author guides you
through how the code works, providing much needed insights into how to actually
get stuff done and understand what is happening.

<a href="https://www.amazon.com/WebGL-Programming-Guide-Interactive-Graphics/dp/0321902920/"
target="_blank">
WebGL Programming Guide: Interactive 3D Graphics Programming with WebGL
</a>
This book provides a low level view of the WebGL API, but isn't very practical
as far as getting work done goes.

<a href="https://www.amazon.com/Interactive-Computer-Graphics-Top-Down-Approach/dp/0133574849" target="_blank">
Interactive Computer Graphics: A Top-Down Approach with WebGL (7th Edition)
</a>

This is a book about computer graphics intended for use as an undergraduate class
textbook. I found the book via a talk the authors gave at SIGGRAPH

<a href="https://www.youtube.com/watch?v=tgVLb6fOVVc" target="_blank">
https://www.youtube.com/watch?v=tgVLb6fOVVc</a>

# Talks

Some of the more insightful talks I've found along the way.

<a href="https://www.youtube.com/watch?v=avwDj3KRuLc" target="_blank">
We will all be game programmers</a>

A talk by Steven Wittens (http://acko.net)

<a href="https://www.youtube.com/watch?v=GNO_CYUjMK8" target="_blank">Making WebGL Dance</a>

Mikola Lysenko giving an overview of ReGL:
<a href="https://www.youtube.com/watch?v=rFjszW5L2aw" target="_blank">
https://www.youtube.com/watch?v=rFjszW5L2aw</a>

Here is a talk Gregg gave in 2011 which provides a nice overview of WebGL techniques.
<a href="https://www.youtube.com/watch?v=rfQ8rKGTVlg" target="_blank">
https://www.youtube.com/watch?v=rfQ8rKGTVlg</a>.

Edward Angel and Dave Shreiner present an overview of the benefits of using
WebGL to teach computer graphics.

<a href="https://www.youtube.com/watch?v=tgVLb6fOVVc" target="_blank">
https://www.youtube.com/watch?v=tgVLb6fOVVc</a>

# Online classes

UC Davis Computer Graphics class, covers core graphics concepts.
<a href="https://www.youtube.com/watch?v=01YSK5gIEYQ&list=PL_w_qWAQZtAZhtzPI5pkAtcUVgmzdAP8g" target="_blank">
https://www.youtube.com/watch?v=01YSK5gIEYQ&list=PL_w_qWAQZtAZhtzPI5pkAtcUVgmzdAP8g</a>

UC San Diego class on edX

<a href="https://courses.edx.org/courses/course-v1:UCSDx+CSE167x+2T2016/information/" target="_blank">
https://courses.edx.org/courses/course-v1:UCSDx+CSE167x+2T2016/information/</a>

A code editor in WebGL

<a href="https://www.youtube.com/watch?v=hM1oLr9G3-Q" target="_blank">
https://www.youtube.com/watch?v=hM1oLr9G3-Q</a>

Tony Parisi at HTML5 Dev Conf

<a href="https://www.youtube.com/watch?v=c3_Q3T6Gzxk" target="_blank">https://www.youtube.com/watch?v=c3_Q3T6Gzxk
</a>

# Libraries

## WeGL Utils
<a href="https://github.com/greggman/webgl-fundamentals/blob/master/webgl/resources/webgl-utils.js"
 target="_blank">
 https://github.com/greggman/webgl-fundamentals/blob/master/webgl/resources/webgl-utils.js
</a>

These functions can be found in a proper library:

<a href="http://twgljs.org/docs/" target="_blank">
http://twgljs.org/docs/</a>

## MathBox
<a href="https://github.com/unconed/mathbox" target="_blank">https://github.com/unconed/mathbox</a>

## regl
<a href="http://regl.party/" target="_blank">http://regl.party/</a>

# Examples

<a href="http://webglsamples.org/" target="_blank">http://webglsamples.org/</a>
<a href="" target="_blank"></a>
