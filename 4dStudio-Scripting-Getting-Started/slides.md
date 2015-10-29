title: 4D Studio Scripting - Getting Started
output: index.html
--

<style>pre { font-size: 100%; }</style>
<style>img { width: 100%; }</style>

# 4D Studio Scripting
## Getting Started

## By [@jerome_etienne](https://twitter.com/jerome_etienne)

---

### Recipes
- 4D Studio Scripting
- Getting Started
- Recipes Style

---

### What is 4D Studio

- authoring AR experience
- edit once, play everywhere

---

### Landing Page [link](http://test2.daqri.com/)

<img src='images/4dstudio-screenshot-origin.png'></img>

---

### Where ? in js console

<img src='images/4dstudio-screenshot-htmltemplate.png'></img>

---

### How To Play Your Script

<img src='images/4dstudio-screenshot-playmode.png'></img>

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

### How To Reach the Scene Variable

```
// put that early in your script
var scene = this;
```

---

### How to Change An Object Position

Move object to the right

```
object3d.rotation.x += 50;
```

How to make the object twice bigger

```
object3d.scale.set(2,2,2);
```

---

### How to Change the Opacity

```
object3d.material.opacity = 0.1;
object3d.material.transparent = true
```

---

### How to Change the Visibility

```
object3d.visible = true | false;
```

---

### How to Create a new Object

Let's create a sphere

```
var geometry = new THREE.SphereGeometry(1);
var material = new THREE.MeshNormalMaterial();
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