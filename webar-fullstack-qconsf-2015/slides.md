title: Alternate Reality in the Web
output: index.html
--

<style>section.slide-content img { width: 100% }</style>
<style>pre { font-size: 100% }</style>

# Alternate Reality in the Web

## by [@jerome_etienne](https://twitter.com/jerome_etienne)

---

### Who Am I ?

- Best Known as the author of [Learning Three.js Blog](http://learningthreejs.com/)
- Wrote more than [45 game extensions for three.js](http://www.threejsgames.com/extensions/)
- Lead for
Three.js Team at [Daqri](http://daqri.com) in Dublin

Contact me anytime on twitter [@jerome_etienne](https://twitter.com/jerome_etienne)

---

### What is Alternate Reality ?

It is a mix!

- Virtual Reality
- Augmented Reality

---

# Devices Of Virtual Reality

---

### Everybody is Doing It

---

### Steam VR

<img src="images/devices/htc-vive.jpg">

---

### Steam VR

- Made by Steam/Valve

---

### Occulus

<img src="images/devices/occulus-picture-user.jpg">

---

### Occulus

- Started as [kickstarter](https://www.kickstarter.com/projects/1523379957/oculus-rift-step-into-the-game)
- Most well known devices
- acquired by [facebook for $2 billion](http://techcrunch.com/2014/07/21/facebooks-acquisition-of-oculus-closes-now-official/) 

---

### Hololens

<img src="images/devices/hololens-review-970-80.jpg">

---

### Hololens

- Made by microsoft
- No Wire!

---

### Google Glass

<img src="images/devices/google-glass.jpg">

---


### Google Glass

- Made by Google
- Got stopped in early 2015 

---

### Google Cardboard

<img src="images/devices/google-cardboard.jpg">

---

### Google Cardboard

- Made by Google
- Cheap, use your own phone
- "can build it from a pizza cardboard"

---

# What is the Difference ?
## Between VR and AR

---

### Virtual Reality

<img src="images/difference-ar-vr/VR example.jpg">

---

### Virtual Reality

- Nothing of the real world
- Total immersion in another world 

**You are teleported in another reality**

---

### Augmented Reality

<img src="images/difference-ar-vr/Augmented-Reality-retail.jpg">

---

### Augmented Reality

- Still see the real world around you
- Overlay additional content
- like special effect for the real world

**You Augment Your Reality**

---

# How To Code For Alternate Reality

---

# How to Code for VR ?

---

## Some Exotic ones, for the fun of it :)

---

### Anaglyph - Retro style

<img src="images/how-to-code/anaglyph-glass.jpg">

---

### Anaglyph - [wikipedia](https://en.wikipedia.org/wiki/Anaglyph_3D)

- Old fashion 
- Super low tech
- Available in three.js


---

### Anaglyph - [three.js examples](http://threejs.org/examples/webgl_effects_anaglyph.html)

<img src="images/how-to-code/anaglyph-demo-screenshot.png">

---

### Parallax Barrier

<img src="images/how-to-code/lenticularprinting-realworld-example.jpg">

---

### Parallax Barrier - [wikipedia](https://en.wikipedia.org/wiki/Parallax_barrier)

- Based on a device placed in front of an image source
- No need for the viewer to wear 3D glasses
- Similar to [lenticular printing](https://en.wikipedia.org/wiki/Lenticular_printing)
- Available in three.js

---

### Parallax Barrier - Theory

<img src="images/how-to-code/parallaxbarrier-glass.png" style='width:80%;'>

---

### Parallax Barrier - [three.js examples](http://threejs.org/examples/webgl_effects_parallaxbarrier.html)

<img src="images/how-to-code/parallaxbarrier-demo-screenshot.png">

---

## More concrete ones

---

### Stereo Effect

<img src="images/how-to-code/stereoeffect-glass.jpg">

---

### Stereo Effect

- Work on mobile devices!
- Made popular by [google cardboard](https://www.google.com/get/cardboard/)
- Cheap to buy (as low as $2)
- Available in three.js

---

### Stereo Effect - [three.js examples](http://threejs.org/examples/webgl_effects_stereo.html)

<img src="images/how-to-code/stereoeffect-demo-screenshot.png">

---

### WebVR

<img src="images/how-to-code/webvr-glass.jpg">

---

### WebVR

- It is standard! [link](http://mozvr.github.io/webvr-spec/webvr.html) 
- google and mozilla are working hard on it
- Available in three.js 

---

### WebVR - [three.js examples](https://va3c.github.io/three.js/examples/misc_controls_oculusrift.html)

<img src="images/how-to-code/webvr-demo-screenshot.png">

---

## Many possibilities...

---

### Which One To Pick ?

- Too many possibilities, can't code them all
- Should focus on the experience
- Not on coding support for each VR devices

---

### Which One To Pick ?

- Discard the exotic ones
- Focus on the popular ones
- i.e. occulus, cardboard, and plain phone

**All done in WebVR Boilerplate. GREAT!**

---

### What Is The WebVR Boilerplate ?

- Support all popular VR devices
- i.e. occulus, google cardboard, and plain phone
- [WebVR Boilerplate](https://github.com/borismus/webvr-boilerplate) code available on github
- Reuse it, so you can focus on your own stuff

---

### WebVR Boilerplate: a Safe Choice 

- Described as "Responsive WebVR, headset optional"
- Made by [Boris Smus](https://twitter.com/borismus) at google - [post](http://smus.com/responsive-vr/)
- Apply [Responsive Web](https://en.wikipedia.org/wiki/Responsive_web_design) principle

---

## You got what you need to start coding VR

---

## Now let's talk about AR

---

# How to Code For AR ?

---

### Coding AR is Not as simple as VR :(

- Most VR already in three.js
- WebVR is a standard in progress

**AR isn't there yet... Working hard tho**

---

## Lets review AR needs

---

### What is Needed For AR

1. Get a camera
1. Analyze it to localize AR Markers
1. Generate 3d on top
1. Finally display both, 3d and video, on the screen

---

### What is Missing ?

- Camera can be access via WebRTC/getUserMedia API - [spec](http://www.w3.org/TR/mediacapture-streams/) - [example](http://simpl.info/getusermedia/)
- Localisation of AR Markers
  - many small libraries
  - no clear winner
  - We decided to put ourselved to work

---

### AR Needs More Than VR

- AR needs a camera to capture reality
- AR needs to localize marker


---

## First handling the camera

---

### Camera Feed

- Simple color video like Webcam
- webrtc/getUserMedia - [spec](http://www.w3.org/TR/mediacapture-streams/) - [example](http://simpl.info/getusermedia/)
- Supported on Desktop and Android mobile
- Not IOS unfortunatly - [caniuse link](http://caniuse.com/#feat=stream)


---

### Open source is important at Daqri

- Feb 2015 - Daqri acquired AR Toolkit
- Before it has a free and a pro version

**We opened source it all!**

---

### More About Open Source at Daqri

- Will opensource four.js, our core library to do AR
- We keep improving ARToolkit
- We will opensource result
- e.g. more robust tracking algos, new features

---

### WebAR - Augmented Reality Solution for the Web

- Allow to easily do AR on top of three.js
- Our experiment to do AR in a Web page
- All open source, so you can use it.

[WebAR on github](https://github.com/jeromeetienne/threex.webar)

---

### WebAR - Results

- It works!
- It is usable today
- free as a chery on top :)
- It EVEN runs in mobile phones.

**Augmented reality in browsers is for real**

---

### WebAR - What about Phones ?

- WebAR is running on Phone (YES you read it well)
- People already got mobile phones
- So it can provide AR to your user today

---

### WebAR - More about Phones

- Not the perfect experience
- Not as good as Specific devices: e.g. hololens or daqri smart helmet 
- They provide high quality hand free experience
- But Phone available today, no need to wait 

**Availability is a powerful arguments**

---

## WebAR is cool, let's see what we can do

---

# WebAR's Examples

---

### WebAR's Examples

- Various AR applications built with WebAR
- Show possible usages and hopefully inspire more
- Good places to get starting

---

### Being Awesome - Basic Example

<img src="images/screenshots/being-awesome.jpg">

---

### Being Awesome - Description

- Display a trivial 3D on top of a marker
- Basic Example
- Written to be simple to understand

---

### Being Awesome - in Action

<iframe width="640" height="480" src="https://www.youtube.com/embed/fz9bmOfYvG0" frameborder="0" allowfullscreen></iframe>

---

### Being Awesome - Improvements ?

- May be the base for a FPS Game in AR
- People are identified by markers
- They shoot each other in AR
- You display special effect on top


---

## Now a more 'serious' one

---

### Data Visualisation - Serious applications

<img src="images/screenshots/data-visualization-histogram3d.png">

---

### Data Visualisation - Description

- Put a marker near a piece of equipment
- e.g. stoge, fridge, your car, up to you
- Display live information about it

**Provide useful info right when you need them**

---

### Data Visualisation - on Nexus 9

<iframe src="https://vine.co/v/ei1TDWLrYiX/embed/simple" width="480" height="480" frameborder="0"></iframe>

---

### Data Visualisation - Improvements ?

- You could put many makers in your office/house
- I added one near my microwave
- It shows me instructions in AR
- e.g. cooking timing, which button to push

**Actually useful in Real Life**

---

### Contact Sharing in AR

<img src="images/screenshots/contact-sharing.png">

---

### Contact Sharing - Description

- Everybody walk around in a conference with marker
- Each personn got a different marker, It identifies him
- Display Info From a Database on per-marker basis
- No more need to dictate your email and so on

**You can share contact fast and without error**

---

### Contact Sharing - in Action [link](https://github.com/jeromeetienne/arplayerforthreejs/blob/master/examples/contact-sharing-in-ar.html)

<iframe width="640" height="400" src="https://www.youtube.com/embed/wrMX_FH2hsc" frameborder="0" allowfullscreen></iframe>

---

## Last by not least, Hatsune Miku in AR! :)

---

### Hatsune Miku Dancing in AR

<img src="images/screenshots/hatsune-miku-dancing-in-ar.png">

---

### Hatsune Miku - Description

- Hatsune Miku is a mascotte in AR
- You have to do it :)
- model by [@superhoge](https://twitter.com/superhoge)

---

### Hatsune Miku - in Action

<iframe src="https://vine.co/v/eApD5rPtKxT/embed/simple" width="480" height="480" frameborder="0"></iframe>

---


## Now what if you want to use it yourself ?

---

### How we implemented it

- [three.js](http://threejs.org/) to ease webgl display
- [jsartoolkit](https://github.com/artoolkit5) to find AR markers within video streams

A Spoon of opensource

---

### Display WebGL with three.js

- Three.js javascript library from [mrdoob](https://twitter.com/mrdoob)
- Leading library to display Webgl
- MIT license, so easy to integrate
- Runs on desktop and mobile.

---

### JSARToolKit - AR Marker Recognition

- Javascript port of [artoolkit](artoolkit.org)
- Compiled with EMScripten (c++ to js compiler)
- Opensource it all obviously

---

# Code Overview

---

### WebAR - Extensions For Augmented Reality

- Follow the threex models for three.js Extensions
- wrote 50 of them already, proven to work
- Simple, standalone, accurate

---

### WebAR - Extensions For Augmented Reality

- [threex.jsartoolkitmarker.js](https://github.com/jeromeetienne/arplayerforthreejs/blob/master/src/threex.jsarucomarker.js) - marker recognition
- [threex.webcamgrabbing.js](https://github.com/jeromeetienne/arplayerforthreejs/blob/master/src/threex.webcamgrabbing.js) - video grabbing
- See [README.md](https://github.com/jeromeetienne/arplayerforthreejs/blob/master/README.md) for Details

**Simple, easy to access, dont hesitate to try**

---

# Questions ?
