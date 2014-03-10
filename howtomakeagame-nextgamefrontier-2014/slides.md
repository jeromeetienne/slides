title: How To Make Games in THREE.js
author:
  name: "Jerome Etienne"
  twitter: "@jerome_etienne"
  url: "http://jetienne.com"
output: index.html

--

<style>pre { font-size: 90%; }</style>
<base target='_blank'>


# How To Make Games in THREE.js

## and having fun in the process :)

--

### META Intro

* present three.js
* who is doing it

--

## Three.js seems ok... but

# How to make a game with it

--

### Transition META

* First we need a hero
* in all game you need a hero
* a personna to embody you
* a virtual self for the player to interact with

* so lets do just that, lets create a hero

--

# New Part

--

# "A Hero is Born!"

--

### META Story Telling

* we gonna go for something simple
* very blocky 
* very lego like
* we go for minecraft character


* (hint: trick because i dunno how to use a modeler :) )

--

## So Let's Start with a cube

--

### How to create a cube ?

Here is the code

```
var geometry = new THREE.CubeGeometry(1,1,1)
var material = new THREE.MeshNormalMaterial()
var mesh     = new THREE.Mesh(geometry, material)
scene.add(mesh)
```

Let's details each part

--

### First the Geometry

* Geometry is ```the shape of the object```
* create a cube with dimension 1,1,1

```
var geometry = new THREE.CubeGeometry(1,1,1)
```

```
var material = new THREE.MeshNormalMaterial()
var mesh     = new THREE.Mesh(geometry, material)
scene.add(mesh)
```

--

### Other Predefined Geometry

* Meta TODO a select.html for geometry
* maybe some tweening for transition. make it bouncy, more games

--

## Well just a cube

# We Need a Hero

--

### we needs a hero!

* More Cubes
* Duplication same principle
* Cube for everything
* bouncy effect
* all in normalmaterial

--

### META tech demo needed

* select on geometry
* nice light setting
* autobuild of the player
  * based on minecraft with visibility of each part
  * change visibility until you arrive to full player
* then change materials
  * white lambert
  * flat shading/smooth shading
  * phong
  * texture is better for color
  * which skin
* with HOT or NOT at the bottom to go to next step

--

## Colors are strange

--

### Materials

"How the object reflect lights"

* Meta do a select with various lights and material
* boring lambert all white
* phong + random rainbow color for each box
* textures 
* various skin
* do something interactive ? 
  * like for each skin, display hot/not ?
  * with possible suggestion
  * you get close to the button suggested, do the yes animation, 
  * if close to the non recommended, do the no animation.
* stop on mine obviously :)

--

### Meta POST texture

* Do not forget parallel with JE/ pictures. 
* disclaimer about not being based on actual character
* I did that because I love the recursive jokes.

--

### Transition end

* Story telling: 
* After the animation the Minecraft (Mike) becomes alive. 
* He is Gollem. My Frankenstein. 
* Oh damn! Turing was right! 
* What have I done! 

--

### Transition end

* Now he is aware. 
* His name is Mike.
* He needs a purpose, a goal, a quest
* He is looking for love, fame and justice
* because that is what every video game hero is doing.

--

# New Part

--

# "Mike Goes Party"

--

### META

* demo: volumetric spotlight
* webaudiox
* change of spot color 
* multiple spot synchronized
* minecraft move ala saturday night fever
* like 10 minecraft players on the screen
* do a gowiththeflow.js with an animation of 2 guys discussing
  * "Hey guys, there are no girls here!"
  * "Where can I find a girl."
  * "Wait you are missing something too!"
  * camera move
  * even noticed how minecraft is lacking of female ?

--

### How to make the spot

* from where it comes from
* flexibility if you want your own effects and shader

-- 

### How to sync sound with color

* web audio api

--

# New Part

--

# "Mike Goes Home And Play Video Games"

--

### Demo

<a href='http://jetienne.com/games/'><img src='images/screenshot-videogames.png' width='100%'/></a>

--

### Meta

* goto portfolio games
  * use directly this demo
* do some story telling
* and then switch to the tech part

--

### Meta Story Telling

* here is a virtual game console
* you can play games inside a game
* you got a menu with all the games
* if you go close to the TV, the camera becomes centered on the tv and you can enjoy your play
* but still the actual games is going on around us
* see with the day night cycle

--

* ok so which game to play ?
* Lets see pong, this is classic
* or marble table, actual physics cannonjs, granular sound, play with camera
* or Let's play with a friend
  * launch mmo3d
  * multiplayer game 
  * demo it. run on nodejitsu. they got a "if it is opensource, we run it for free"
* or simply stellar7
  Another classic

--

### How to include webpage like that ?

* Meta html mixer [threex.htmlmixer](https://github.com/jeromeetienne/threex.htmlmixer)
  [demo](http://jeromeetienne.github.io/videobrowser4learningthreejs/)
  [post](http://learningthreejs.com/blog/2013/04/30/closing-the-gap-between-html-and-webgl/)
* Meta domEvenr repo [threex.domevents](https://github.com/jeromeetienne/threex.domevents)
  [post](http://learningthreejs.com/blog/2012/01/17/dom-events-in-3d-space/)
* take it from the blog
  * ["Mixing HTML Pages Inside Your WebGL"](http://learningthreejs.com/blog/2013/04/30/closing-the-gap-between-html-and-webgl/)

--

### Stellar7 and Post Processing

* [link](http://jeromeetienne.github.io/stellar7/)
* color adjust
* bad tv effect

--

### color adjust

* [repo](https://github.com/jeromeetienne/threex.coloradjust)
* [demo](http://jeromeetienne.github.io/threex.coloradjust/examples/demo.html)
* by [@greggman](http://greggman.com/)
  [original demo](http://webglsamples.googlecode.com/hg/color-adjust/color-adjust.html)
  explain in [this video](http://www.youtube.com/watch?v=rfQ8rKGTVlg#t=25m03s)

--

### bad tv effect

* from [@felixturner](https://twitter.com/felixturner)
  in [his demo](http://www.airtightinteractive.com/demos/js/badtvshader/)
* like one step further, from the demo to the reusable effect
* more scripted, some predefined usage linked with sound
* how to install it
* play with dat.gui to decompose the effect

--

# New Part

--

# "Mike Thinks about Wendy"

--

### META Storytelling: 

* After playing video games, 
* Mike gets tired and he starts to daydream
* "What would be the best video game for me?"
* I like games and i lack girls
* He wants to create a girl for him, 
* "I'm horny, sexually frustrated. My pet name for my dick is joystick" 
* Here is what is in mike head

* [demo](http://lo-th.github.io/olympe/index_diana.html)

--

### META tech

* Detailler chaque element technique de cette demo
* the guy who modeled that wasnt thinking about his grand mother
* then extend to the possibility of what could it be
* with leap motion, occulus drift
* multiplayer with webrtc
* [Simulated reality](http://en.wikipedia.org/wiki/Simulated_reality)
