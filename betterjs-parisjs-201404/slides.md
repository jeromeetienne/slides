title: Better.js From 10000 miles
author:
  name: "Jerome Etienne"
  twitter: "@jerome_etienne"
  url: "http://jetienne.com"
output: index.html
--

<base target='_blank'/>
<style>pre { background: lightgrey; font-size: 100%;}</style>

# Better.js

## For A Better Javascript In Javascript

## [Jerome Etienne](http://twitter.com/jerome_etienne)

--

## A Better Javascript In Javascript ?

--

## Like... javascript is not perfect ??

--

# Javascript WTF
## The Horrors

--

### negative zero equal but not equal

```
    0 === -0        //true
    1/0 === 1/-0    //false
```

[source](http://wtfjs.com/2011/12/16/negative-zero-equal-but-not-equal)

--

### Parseint Magic

```
parseInt(null, 24) === 23 // true
```

[source](http://wtfjs.com/2011/06/23/parseint-magic)

--

### Identity Crisis

```
var foo = [0];
console.log(foo == !foo); // => true
console.log(foo == foo);  // => true
```

Heard the rumor of ```maybe``` operator in ES6 ?

[source](http://wtfjs.com/2010/11/15/i-am-myself-but-also-not-myself)

--

### Concat Coerce

```
"3" + 1 // '31'
"3" - 1 // 2
```

[source](http://wtfjs.com/2010/02/19/concat-coerce)
--

## The list is endless

--

## OK... so javascript is far from perfect.

--

## Still...

# I Love Javascript!

--

## "This is the last thing you gonna see if you mess with javascript!" - [tweet](https://twitter.com/jerome_etienne/status/333203103472046080)

<img width='60%' src='images/last_thing_you_gonna_see.jpg'/>

--

## "Javascript fell from heaven!" - [tweet](https://twitter.com/jerome_etienne/status/333200144570929152")

<img width='80%' src='images/fell_from_even.jpg'/>

--

## "i love javascript THIIIIISSS much !" - [tweet](https://twitter.com/jerome_etienne/status/333195407620452352)

<img width='80%' src='images/love_js_this_much.jpg'/>

--

## I Wasn't Kidding You :)

--

# Why Do I Love Javascript

--

### Javascript is The King

* Javascript is open standard
* Javascript run everywhere
* You can't beat that.

--

### How to deal with Javascript Issues

* People are trying to fix them. Good
* What are they ? People dont agree
* How to fix them ? They really disagree

--

# Various Efforts

--

### Alternatives

* [typescript](http://www.typescriptlang.org/) by microsoft
* [dart](https://www.dartlang.org/) by google
* [react](http://facebook.github.io/react/) by facebook
* [asm.js](http://asmjs.org/) by mozilla

Just to name a few...

--

### Different Syntaxes

* new languages to learn
* require time for your team to train
* less docs and examples on the web

--

### Require compilation

* more complex build
* slower developement iterations
* harder to debug

--

### Vendor Tainted

* microsoft, google, mozilla, facebook...
* estimated time to converge... **infinity+1** :)

--

## Meanwhile **we, the webdevs,** are stuck with javascript...

--

# Plain Old Javascript

## Engaged Super Power

--

## How to improve Javascript In Javascript ?

--

### What Is Better.js

* 100% Plain Old Javascript
* unintrusive javascript library
* focused on helping you write better javascript

"Make writting JS safer, faster and easier"

--

# Braging Time

## Better.js Provides Features Unseen to Javascript

--

## Javascript got no **Private**!

# Think Again!

## with Better.js it does!


--

## Javascript got no **Strong Typing**!

# Think Again!

## with Better.js it does!

--

### Better.js is funky!

It is "Not your mother Javascript!"

* Provides Strong Typing to Javascript
* Provides Private Visibility to Javascript

**Features unseen in Javascript World!**

--

### 100% Plain Old Javascript

* No compilation Step
* No New Language to Learn


Better.js is 100% Plain Old Javascript

--

## What ?? How?

# Demo Time

--

## First...

# Strong Typing in Javascript

## An example

--

### Sample Function

```javascript
var cat = function(name, age){
  console.log('my name is', name, 'and im', age)
}
```

* Simple function to display a message
* receive a String ```name```
* receive a Number ```age```

--

### Play with Strong Typing In JS

* Define a function class
* Make a Better.js declaration for its arguments
  * works for function return types too
  * works for object property too
* See what happen


--

### Make a Better.js for it

```javascript
cat = BetterJS.Function(cat, {
    arguments : [String, Number],
})
```

* You overload ```Cat``` function
* Define the types for each arguments
* Better.js makes sure it is respected!

--

### Let's See What Happens

Calling the function with **valid types** - OK

```
cat('kitty', 5)
// display 'My name is kitty and im 5.'
```

--

### Let's See What Happens

Calling the function with **invalid types** - BAD

```
cat('kitty', 'ten')
// Exception thrown
// "Invalid arguments 1 - Should be Number"
```

**Error Immediatly detected and execution stopped**


--

### Strong Typing in Better.js

* Better.js provides strong typing to JS! **COOL! **
* Unauthorized access is immediatly detected


**Earlier bug detection, so helps you write better js**

--

## Second ...

# Private in Javascript

## An example

--

### Sample Class

```javascript
var Cat = function(name){
  this._name = name
  this.age   = 7
}
Cat.prototype.getName = function(){
  return this._name
}
```

* Let's define a nice kitty class.
* ```._name``` is a private property 
* ```.getName()``` is its getter

--

### Play with Private In Better.js

* Define a sample class
* Make a Better.js declaration for it
* See what happen

--

### Make a Better.js for it

```javascript
Cat = BetterJS.Class(Cat, {
  privatize : true
})
```

* You overload ```Cat``` constructor
* Now ```._name``` is private
* After that, you can access it only if you are the class

--

### Let's See What Happens

Create an instance for your class

```javascript
var cat = new Cat('kitty')
```

--

### Let's See What Happens (bis)

Accessing public property ```.age``` - OK

```
console.log('cat age is ', cat.age)
// Display "cat age is 7"
```

--

### Let's See What Happens (bis)

Now calling the getter ```.getName()``` - OK

```javascript
console.log('cat name is ', cat.getName())
// Display "cat kitty is kitty" - OK
```
--

### Let's See What Happens (bis)

Now accessing the private property ```._name``` - BAD

```javascript
console.log('cat name is ', cat._name)
// Exception thrown 
// "Denied access to private property _name"
```

**Error Immediatly detected and execution stopped**

--

### Private in Better.js

* Better.js provides private visibility to JS! **COOL!*
* Unauthorized access are immediatly detected


**Earlier bug detection, so helps you write better js**

--

## What now ?

# Packing it UP

--

### What better.js brings to the table ?

* better.js brings private visibility to JS
* better.js brings strong typing to JS

**Not Bad!**

--

### What better.js changes ?

* 2 Major features
* Both unseen in JS

### Result

* Helps you write Safer Javascript
* Helps you find bug Earlier

--

### Better.js Spirit

"Make writting JS safer, faster and easier"

* 100% plain javascript
* earlier bug detections
* monitor excutions

--

### What Better.js will be Doing

* object allocation tracking
* garbage collector monitoring
* function caller tracking
* global variable detector

#### Features not yet exposed, but coded

--

### Where to get Better.js

* Homepage - [http://betterjs.org](http://betterjs.org)
* Repo - [github](https://github.com/jeromeetienne/better.js/) 
* License - [MIT](http://jetienne.mit-license.org/)

--

# Questions ?



