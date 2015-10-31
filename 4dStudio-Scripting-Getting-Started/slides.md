title: 4D Studio Scripting - Getting Started
output: index.html
--

<style>section.slide-content img { width: 100% }</style>
<style>div.slide { background-image: url(images/daqri/daqri_ribbon.png); background-repeat: no-repeat; background-position: 0px 0px, top; }</style>

<style>pre { font-size: 80%; }</style>
<style>img { width: 100%; }</style>

![daqri_logo.png](images/daqri/daqri_logo.png)
# 4D Studio 3D Scripting 101

## By [@jerome_etienne](https://twitter.com/jerome_etienne)

---

### What are we gonna talk about ?
- Scripting 3D inside 4D Studio
- Recipes Style

---

### Who Am I ?

- Best Known as the author of [Learning Three.js Blog](http://learningthreejs.com/)
- Wrote more than [45 game extensions for three.js](http://www.threejsgames.com/extensions/)
- Lead for
Three.js Team at [Daqri](http://daqri.com) in Dublin

Contact me on twitter [@jerome_etienne](https://twitter.com/jerome_etienne)

---

### What is 4D Studio

- Authoring AR experience
- Edit once, play everywhere
- rich tools (models, animation, scripting)

---

### What we gonna learn ?

- How to script your 3d in 4D Studio
- Create interactive experience
- How to select object ?
- Change their appearance
- etc...

---

### Landing Page [link](http://test2.daqri.com/)


<img src='images/4dstudio-screenshot-landingpage.png'></img>

<!-- META: explain the page and the basic of 4d studio. just to a skitch -->

---

### Show Time

Let me show you - [demo here](http://test2.daqri.com/)

- How to create an object ?
- How to change its name ?
- How to add a script ?

---

### Where ? in js console

<img src='images/4dstudio-screenshot-htmltemplate.png'></img>

---

### How To Play Your Script

<img src='images/4dstudio-screenshot-playmode.png'></img>


---

### How To Reach the Scene Variable

```
// put that early in your script
var scene = this;
```

- scene is the root of your 3d tree (scene graph intro)

---

### How to Select a 3D Object

With its names

```
var object3d = scene.getObjectByName('superObject')
```

---

### Where to get the object3d names

<img src='images/4dstudio-objectname.png'></img>

---

### How to detect a click on an object

```
var scene = this;
// listen to click event
document.body.addEventListener('click', function(event){
  // find all objects under the mouse click
  var intersects = daqri.util.computeIntersects(event.x, event.y);
  // test if one object is found
  if(intersects.length>0){
    // get the selected object
    var selected = intersects[0].object;
    // here do what you like with it
    console.log('object selected', selected);
  }
})
```

---

### How to Change An Object Position

Move object to the right

```
// object3d is the variable containing the 3d javascript object
object3d.position.x += 50;
```

How to make the object twice bigger

```
// set x,y,z all in one
object3d.scale.set(2,2,2);
```

---

### How to Change the Opacity

```
// here we change the object material
// material is the way the object is reflecting lights
// you can change its color, and so on
// here we change the opacity
object3d.material.opacity = 0.1;
object3d.material.transparent = true
```

---

### How to Change the Visibility

Here we change the visibility of the 3d object

```
object3d.visible = true; // false
```

---

### How to Create a new Object

Let's create a sphere

```
var geometry = new THREE.SphereGeometry(1);
var material = new THREE.MeshPhongMaterial({
	color : 'red'
});
var object3d = new THREE.Mesh(geometry, material);
```

---

### How to add an object into the scene

To add an object to a scene

```
scene.add(object3d)
```

or with another parent

```
parent.add(object3d)
```

---

### How to remove from the scene

```
scene.remove(object3d);
```

---

# Questions ?

## Ping me anytime at [@jerome_etienne](http://twitter.com/jeromeetienne)