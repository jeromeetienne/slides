notes about google devfest
==========================
### schedule
- 2 devfest
  * one 18th of october at valencienne
  * one 8th of november at nantes
  * maybe a workshop for the one in valencienne
- find the duration of each of your interventions
  * 45min for a talk
  * 1h25 for a 'workshop'
============================
### Meta
- prepare that to work offline
  - copy everything on your local computer
- prepare a schedule to write the slides
============================
- i have many threex extension at the moment
- threex extensions are easy to include thanks to yeoman
- they are good bricks if you want to make a game
=============================
Possible Plan for the presentation:
1. presentation three.js
  * find presentations from other people and copy
2. present the game angle using your threex extension as base
=============================
three.js for games:
- how threex can help you to build a game
- various inputs
  - threex.keyboardstate
  - mouse event
  - leap motion
  - virtualjoystick.js
- collisions
  - raycasting
  - octree
- multiple predefined models
  - threex.nyancat
  - threex.spaceships
  - threex.suzanne
  - threex.minecraft
  - md2 characters
  - threex.planets
  - threex.proceduralcity
- help to debug
  - rendererstats
  - debug from chrome dev tools, see posts
  - see work from benjavic
- various toy
  - laser beam
  - volumetric spotlight
  - threex.vertexanimations
  - threex.dynamictexture
  - threex.skymap
    - reflexion
    - refraction
    - skymap
  - realistic physic engine
    - with cannonjs
    - show domino demo
  - threex.basiclighting
  - threex.transparency
- various effects
  - godrays
  - glow 
    - glow key color
    - glow volumetric
  - depth of field
  - simple posteffect
  - lensflare
    - screenspace
    - geometric
  - threex.videotexture
    - various cases
    - plain video
    - webcam video
  - threex.coloradjust
    - show all effects
- how to mix your html content with webgl
  - threex.htmlmixer
  - how to do it
  - what does it do ?
    - mix webgl and css3d to merge web content with webgl display
  - see the blog posts
  - show videobrowser4learningthreejs
=============================
### Plan for the workshop
- one alternative would be to explain procedural city
  - the blog post already contains all the needed data
  - you just have to put them in form of slides
  - just put each stages and demo how to change the values live
- another alternative would be to do something similar with particles
- another alternative would be to do the farting nyancat
  - fun 
  - particle
  - sound
=============================
## Misc
- what to do of all the tQuery slides ?
  - they got some codes... not very usefull
  - what to do all the demo ? 
    - they are nice and shiny
=============================
## presentation of threex
- what is threex
  - policy: when you write extensions, thinks independant modules, not framework
- it started long ago
  - like 3 years ago
- how to install a threex extensions
- how to publish a threex extensions
- all available in MIT license
- threex playground
  - online editor
======================================
### Yeoman
- how to use it with yeoman
  - it is a tool from google
  - it is all open source
  - it aims to simplify the workflow when you are coding the web
  - it can do scaffolding with its 'generator'
    - we gonna come back on that later
  - it can handle package and their dependancies with bower
  - it can automatize repetitive tasks thanks to grunt
- it is possible to use yeoman to play with three.js and threex
  - but it isn't mandatory... it is just much easier
- do some demo of its usages
  - how to generate a boilerplate
  - how to install a threex extension
  - what is the list of currently published extensions
    - ```bower search threex.```
    - display current threex homepage - nice as it goes images on it
====================================================
###  THREE.js boilerplate
- META: more in the workshop
- details the code of the boilerplate
  - i did the first boilerplate 2 years ago
  - here is the version 2 :)
  - explain the code of it
- explain each part of the code
  - the base of html
  - definition of the renderer
  - definition of the scene and camera
  - how to make the object moves
  - concept of rendering loop
    - how to add function in the rendering loop
    - how to run the rendering loop
  - adding object to the scene
  - controls the camera movements


