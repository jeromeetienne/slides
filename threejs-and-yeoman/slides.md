title: WebGL Workshop 
author:
  name: "Jerome Etienne"
  twitter: "@jerome_etienne"
  url: "http://jetienne.com"
output: index.html

--

# Three.js+Yeoman
## three.js easier than ever

--

### What Is Yeoman ?

* Modern Workflow for WebApps
* [homepage](http://yeoman.io/)

--

### Why Using Yeoman ?

* Optional
* Much Faster with it tho
* Time is limited!
* **YES**

--

### What to use in Yeoman ?

* [generator](http://yeoman.io/generators.html) for initiate bootstrap
* [bower](http://yeoman.io/packagemanager.html) for threex modules

--

### Installing yeoman

```
sudo npm install -g yo
```

### Installing three.js Generator

usefull to install three.js boilerplate

```
sudo npm install -g generator-threejs-boilerplate
```

--

### Project Directory

#### create it

```
mkdir mythreejsproject
```

#### go in

```
cd mythreejsproject
```

--

### Generate Three.js Boilerplate

```
yo threejs-boilerplate
```

<img src="images/yeoman-threejs-boilerplate.png" style="width: 80%;"/>

--

### Try Three.js Boilerplate

```make server``` then goto [http://127.0.0.1:8000/](http://127.0.0.1:8000/)

<iframe src='http://127.0.0.1:8000/' width='100%' height='400px'></iframe>

