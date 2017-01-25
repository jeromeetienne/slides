title: Web based Augmented Reality
output: index.html
--

# WebAR with Artoolkit

## Web Based Augmented Reality

---

### Who Am I ?

- Best Known as the author of [Learning Three.js Blog](http://learningthreejs.com/)
- Wrote more than [50 game extensions for three.js](http://www.threejsgames.com/extensions/)
- Lead for Three.js Team at [Daqri](http://daqri.com) in Dublin

Contact me Anytime on twitter [@jerome_etienne](https://twitter.com/jerome_etienne)

---

### What we are gonna talk about ?

- Augmented Reality on the Web
- javascript version of artoolkit - [jsartoolkit](https://github.com/artoolkit/jsartoolkit5)

All that in javascript in your browser :)

--- 

### What is js-artoolkit ?

- javascript version of artoolkit
- [github repository](https://github.com/artoolkit/jsartoolkit5)
- license [LGPLv3](https://github.com/artoolkit/jsartoolkit5/blob/master/LICENSE.txt) : the same
as artoolkit

--- 

### jsartoolkit origin

- Written by [Ilmari Heikkinen](https://github.com/kig)
- Based on the C version of ARToolkit
- Compiled to javascript with [emscripten](https://github.com/kripken/emscripten) in asm.js

--- 

### A-Frame - 3d in your browser

- [aframe.io](http://aframe.io) - effort by mozila
- targeted to AR/VR since the begining
- aims to be easy to learn by webdevs

--- 

### A-Frame - an example

```html
<script src="https://aframe.io/releases/0.4.0/aframe.min.js"></script>
<body>
   <a-scene>
      <a-box color="#6173F4" opacity="0.8" depth="2"></a-box>
      <a-sphere radius="2" src="texture.png" position="1 1 0"></a-sphere>
      <a-sky color="#ECECEC"></a-sky>
   </a-scene>
</body>
```


<img src="images/basic-aframe-scene.png" width='40%'>

---

# Let's Get Started

---

### Step 1: Our basic scene

Here is a basic scene in A-Frame

```html
<!-- We define a scene -->
<a-scene>  
        <!-- add a box in the scene -->
        <a-box></a-box> 
        <!-- add a basic camera -->
        <a-entity camera></a-entity>
</a-scene>
```

Simple enougth :) 

---

### Step 2: Add Artoolkit to you scene

Now we add artoolkit in the scene and create a marker

```html
<!-- We define a scene -->
<a-scene artoolkit>  
        <!-- we put the content into a markers -->
        <a-marker>
                <a-box></a-box> 
        <a-marker>
        <!-- add a basic camera -->
        <a-entity camera></a-entity>
</a-scene>
```

That's it!

---

# Demo time 

## [link](https://jeromeetienne.github.io/aframe-artoolkit/examples/demo.html)


---

# Tune aframe-artoolkit

--- 

### Parameters for artoolkit detection

- **sourceType** : [image, video, webcam]
- **sourceUrl** : url for image/video
--- 

### Parameters for artoolkit detection

- **cameraParametersUrl**: to load the camera parameters for calibration
- **detectionMode**: color, color_matrix, mono, mono_matrix
- **matrixCodeType**: 3x3, 4x4, 3x3_HAMMING63 etc...

Directly extracted from artoolkit

--- 

### Artoolkit Parameters Example

```html
<!-- We define a scene -->
<a-scene artoolkit='detectionMode: mono_matrix; sourceType: webcam;'>  
        <!-- here, put the content of your scene -->
</a-scene>
```

Detect matrix markers from your webcam.


--- 

### Parameters for markers

- **type**: 'barcode' or 'pattern' 
- **size**: physical size of the marker in meters
--- 

### Parameters specific for patterns

- **url**: the url of the pattern to detect

Require to have matrix in the detection mode

--- 

### Examples of a hiro pattern

```html
<a-marker type='pattern' url='data/patt.hiro' >
        <!-- here put your content -->
</a-marker>
```

<img src="images/hiro.png" width='40%'>

--- 

### Parameters for specific barcode

- **value**: the value encoded in the barcode

Require to have matrix in the detection mode

--- 

### Examples of barcode 20

```html
<a-marker type='barcode' value='20' >
        <!-- here put your content -->
</a-marker>
```

<img src="images/matrix_3x3_20.png" width='40%'>

---

# Performances

---

### Current measures

- 30 fps on a desktop (macbook pro)
- 3 fps on a mobile (gasp :( )

Your mileage may vary

---

### Web Code vs Native Code

- Native code is faster to run
- Javascript is easier and faster to write
- web code => single version run everywhere

Up to you to choose according to your own needs :)

---

# Possible Improvements

## of js-artoolkit

---

### Use WebWorkers

- WebWorkers are threads for web pages
- Thus use multiple processors

**More power available for artoolkit to detect markers**

---

### Compile in WebAssembly

- jsartoolkit currently in asm.js
- asm.js is backward compatible with javascript

---

### Compile in WebAssembly

- WebAssembly will be faster
- how much ? unsure :(
- less time parsing
- WebAssembly is cleaner than asm.js so easier to optimize

---

### Futures of jsartoolkit

- Support of textures tracking
- try to improve performances
  - WebAssembly
  - WebWorker

---

### Links

- [aframe-artoolkit](https://github.com/jeromeetienne/aframe-artoolkit)
- [jsartoolkit repository](https://github.com/jeromeetienne/jsartoolkit5)
- [aframe](https://aframe.io)
- [three.js](https://threejs.org)

---

# Questions ?
