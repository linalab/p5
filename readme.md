# P5.js

## **Intro to P5: [https://p5js.org/](https://p5js.org/)**
p5.js is a JavaScript library  based on  [Processing](https://processing.org/) for **creating creative designs**, interaction and more things that can be added on a web.

Using the original metaphor of **a software sketchbook**, p5.js has a full set of **drawing** functionality. However, you're not limited to your drawing canvas, you can think of your whole browser page as your sketch!

For this, p5.js has [addon libraries](http://p5js.org/libraries/) that make it easy to interact with other **HTML5 objects, including text, input, video, webcam, and sound.** This libraries are created and maintained by the community.

<aside>
ℹ️ Some cool examples from the P5 showcase ([https://showcase.p5js.org/#/2022-All](https://showcase.p5js.org/#/2022-All))

</aside>
<br>
<aside>
🔹 **Cave - *Sikai Li***

Cave is an audio-visual experience, the images are created by the artiste in advance  and are transformed in realtime, reacting to the frequencies of the music.

[https://skyl.fr/play/cave?id=Amarrage](https://skyl.fr/play/cave?id=Amarrage) 

</aside>

<aside>
🔹 **Visual Synonyms - *Shawn Peters***

Takes a user input word and generates levels of synonyms from that word. 

[https://skyl.fr/play/cave?id=Amarrage](https://editor.p5js.org/shawnpeters/full/F7KwxeMGt) 

</aside>

<aside>
🔹 W O V E - *patternseeing*

Words created by using mathematical formulas and animating back and 
forth. So! cool to see. I'll eventually add more in this project.

[https://wove.pages.dev/](https://wove.pages.dev/)

</aside>

<aside>
🔹 Flock - *Amy Goodchild*
 is a multiplayer online experience where you can create clouds of 
bubbles and interact with them. Simultaneous visitors are paired up to 
play together in real time

[https://in.bimble.space/flock](https://in.bimble.space/flock)

</aside>

---

## **Hello world**

<aside>
ℹ️  From: 
[https://github.com/processing/p5.js/wiki/p5.js-overview](https://github.com/processing/p5.js/wiki/p5.js-overview)
[https://p5js.org/learn/coordinate-system-and-shapes.html](https://p5js.org/learn/coordinate-system-and-shapes.html)
[https://nycdoe-cs4all.github.io/](https://nycdoe-cs4all.github.io/units/1/lessons/lesson_1.1)
[https://processing.org/tutorials/coordinatesystemandshapes](https://processing.org/tutorials/coordinatesystemandshapes)

</aside>

2.1 **Coordinate System and Shapes:** 
Open: ****[https://p5js.org/learn/coordinate-system-and-shapes.html](https://p5js.org/learn/coordinate-system-and-shapes.html) 

In p5, we use code to **draw graphics on a “canvas”.** The canvas displays the output of your code and we use coordinates to know where the pixels are and what do we want to do with them. 


Let’s start by using the [https://editor.p5js.org/](https://editor.p5js.org/)  great tool to test the code instantly: 

There are two main functions you will use in your program. The `setup()` block **runs once**, and is typically used for initialization, or for creating a program that does not need a loop running code repeatedly. The `draw()` block **runs repeatedly**, and is used for animation.

Point: 

```jsx
function setup(){
  createCanvas(100, 100);
}
function draw(){
  point(40, 50); // point(x, y)
}
```

Line:

```jsx
function setup() {
  createCanvas(400, 400);
}

function draw() {
  line(0,400,400, 0); //line(x1, y1, x2, y2)}
```

Rectangle:

```jsx
function setup() {
  createCanvas(400, 400);
}

function draw() {
rect(100, 100, 300, 200)// x, y, width, height
}
```

A second way to draw a rectangle involves specifying the **centerpoint**, along with width and height. If we prefer this method, we first indicate that we want to use the [CENTER](https://p5js.org/reference/#/p5/CENTER) mode before the instruction for the rectangle itself. Note that p5 is case-sensitive. the first method is called [CORNERS](https://p5js.org/reference/#/p5/CORNERS) 

```jsx
function setup(){
  createCanvas(400, 400);
  rectMode(CENTER);
}
function draw(){
  rect(200, 200, 300, 200); //  x, y, width, height
}
```

At this point an important think here is the [**REFERENCE**](https://p5js.org/reference/)

Same thing with ellipse: CENTER and CORNER

```jsx
function setup(){
  createCanvas(400, 400);
  ellipseMode(CENTER);
}
function draw(){
  ellipse(200, 200, 30, 30); //  x, y, width, height
}
```

## **3. Variables**

1. **Built-in variables:**

Now we can use the mouse to variate the position: 

`(mouseX, mouseY, 30, 30);` 

And if we want to erase the canvas when pressed: 

```jsx
function setup() {
  createCanvas(400, 400);
}

function draw() {
  if (mouseIsPressed) {
    background(255);}
  ellipse(mouseX, mouseY, 30, 30);
}
```

1. **Our own variables** 

<aside>
ℹ️  From: [https://youtu.be/Bn_B3T_Vbxs?feature=shared](https://youtu.be/Bn_B3T_Vbxs?feature=shared)

</aside>

1. Declare a variable:  
    
    `var name` declare
    
2. Initialize (initial value) `= 200 ;`
3. use it

```jsx
var circleX = 200;

function setup() {
  createCanvas(400, 400);
}

function draw() {
  if (mouseIsPressed) {
    background(255);}
  ellipse(circleX, mouseY, 30, 30);
}
```

Change the number of the variable (+1)

```jsx
var circleX = 0;

function setup() {
  createCanvas(400, 400);
}

function draw() {
  if (mouseIsPressed) {
    background(255);
}
  ellipse(circleX, mouseY, 30, 30);

circleX = circleX +1;
}
```

or: 

`circleX += 1;`

`circleX ++;`

**Random**

```jsx
var circleX = 0;
var circleY = 0;

function setup() {
  createCanvas(400, 400);
}

function draw() {
  if (mouseIsPressed) {
    background(255);    
}
  	circleX = random(0, 400);
	circleY = random(0, 400);
  fill(random(0, 255), 0, 0 );
  ellipse(circleX, circleY, 30, 30);

circleX = circleX +5;
  circleY = circleY +5;
}
```

`width/2`

---

## **Setting up p5.js**

1. **Download the files**: complete [https://p5js.org/download/](https://p5js.org/download/)  
    
    Include the code inside the script.js inside the example 
    
2. **Set up a local server**: Some functionality (loading external files, for example) works as expected when the files are placed online via FTP or SSH. However, if you try to view them locally, you see some kind of "cross-origin" errors in console. The solution to this is to view them using what's called a local web server. 

<aside>
ℹ️ [https://github.com/processing/p5.js/wiki/Local-server](https://github.com/processing/p5.js/wiki/Local-server)

</aside>

Server with node: 

- [Download and Install node.js](https://nodejs.org/en/download/)
- Open a terminal or command prompt (on Windows you might need to open the command prompt as admin)
- In the terminal type:
    
    `npm install -g http-server`
    
    From then on just `cd` to the folder that has the files you want to serve and type 
    `http-server`
    
    Then point your browser at `http://localhost:8080/`
