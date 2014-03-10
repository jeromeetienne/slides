title: How To Make Games in THREE.js
author:
  name: "Jerome Etienne"
  twitter: "@jerome_etienne"
  url: "http://jetienne.com"
output: index.html

--

# How To Make Games in THREE.js

## Easier than Ever

--

# Package Management

--

### What is it ?

* why package extensions
* not mandatory
* convention to use [bower](http://bower.io/)
  * but not required
  * can use other if you wish (META: list some)
* how to package extensions
* how to handle dependancies

--

# Physics

--

### alternatives

* [oimo.js](http://lo-th.github.io/Oimo.js/)
* [cannon.js](http://cannonjs.org/)
* [ammo.js](https://github.com/kripken/ammo.js/)

--

### meta

* present each of them
* explain why it isnt in the library itself
* basic about performance

--

### interfacing with them and three.js

* [threex.cannonjs.js](https://github.com/jeromeetienne/threex.cannonjs)
  * [demo](http://jeromeetienne.github.io/threex.cannonjs/examples/domino.html)
* [threex.oimo.js](https://github.com/jeromeetienne/threex.oimo)
  * [demo](http://jeromeetienne.github.io/threex.oimo/examples/demo.html)

--

# Post Processing

--

### meta

* list presentation

--

# Inputs

--

### Available list

* [threex.keyboardstate](https://github.com/jeromeetienne/threex.keyboardstate)
  * ["Let's Make a 3D Game: Keyboard"](http://learningthreejs.com/blog/2011/09/12/lets-Make-a-3D-game-keyboard/)
* [leapjs](https://github.com/leapmotion/leapjs)
  * post ["Discovering Leap Device"](http://learningthreejs.com/blog/2013/06/11/discovering-leap-device/)
* touch screen and virtualjoystick.js

--

# Performances Monitoring

--

### Inside Three.js

* [threex.rendererstats](https://github.com/jeromeetienne/threex.rendererstats)

--

### In Chrome

* ["Debugging With Chrome's Canvas Inspection"](http://learningthreejs.com/blog/2013/04/05/debugging-with-chromes-canvas-inspection/)

--

### in Internet Explorer

* meta there is a post on mdn, find it

--

# Importing 3d models

--

### meta

* get 3 slides on this

--

# Loading 3d models

--

### meta

* get 3 slides on this

--

# Animating 3d models

--

### meta

* get 3 slides on this

--

# Particles

--

### meta

* threex.particles work
* not yet organized
  * todo... how ? post ?
* is this cleanup too much work for now ?

--

# On Screen Display

## or 2d User Interface

--

### Using The DOM

--

# Mobile

--

### Cloud Gaming

* [threex.cloudgaming](https://github.com/jeromeetienne/threex.cloudgaming)
--

### TouchScreen Input

* meta: present [virtualjoystick.js](https://github.com/jeromeetienne/virtualjoystick.js)
  * all the flexibility of it

--

### Meta

* what is the current availability of webgl on mobile
* how to handle non webgl device ?

--

# Sounds

--

### Alternative Tech

* html5 audio element
  * standard
* flash
  * sound manager
* webaudio api
  * more accurate
  * more flexible

--

### WebAudiox

* similar architechture than threex
* *meta* presents the library. take data from [the post](http://blog.jetienne.com/blog/2014/02/18/webaudiox-a-dry-library-for-webaudio-api/)
* explain marvel of web audio api
  * from your [web audio api slides](http://jeromeetienne.github.io/slides/webaudioapi/#1)
* explain how to do it with this library
* explain [webaudiox.gamesounds.js](https://github.com/jeromeetienne/webaudiox#webaudioxgamesoundsjs)
