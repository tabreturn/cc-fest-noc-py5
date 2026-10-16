---

marp: true
theme: TorrensUni
notes: ...

---

# ***The Nature of Code, but Python***
<!-- 
_backgroundColor: black
_backgroundImage: "url(title_bg.png)"
_backgroundSize: "cover"
_color: var(--color-background)
-->
<!--
- a session exploring how the nature of code (p5.js) translates into python using py5
-->

---

# Introduction
<!-- 
paginate: true
backgroundColor: darkslategrey
color: var(--color-background)
-->

---

<!--
_backgroundColor: white
_paginate: false
-->
![bg contain](intro--book.png)
> https://tisch.nyu.edu/itp/news/fall-2024/daniel-shiffman--itp-faculty-member--launches-new-book---the-nat
<!--
- note this is the 2nd edition (no starch press)
- show of hands: who has worked through any nature of code chapters?
- for anybody unfamiliar: the book builds up from simple random walks to vectors to physics to neural networks & neuroevolution, and everything between
- as audience likely knows, this book is (p5.)js-based ... [NEXT SLIDE]
-->

---

<!--
_backgroundColor: black
_class: lead
_color: var(--color-background)
_paginate: false
-->
***Think:**<br />Python wearing a Processing costume,   
and nobody at the Nature of Code party notices.*
<!--
- the next few slides give a quick sense of the final outcome (a sample from each chapter)
- as we flip through, notice three things:
- 1. the environment (thonny) looks nearly identical to the classic processing ide
- 2. look closer at the editor, though, and it's pure python
- 3. the code reads almost line-for-line like the p5.js originals, producing identical visual results
- ... [NEXT SLIDES]
-->

---

<!--
_backgroundColor: black
_paginate: false
-->
![bg 120%](sample--ch00.png)
> 00.06 (perlin_noise_walker.py)

---

<!--
_backgroundColor: black
_paginate: false
-->
![bg 120%](sample--ch01.png)
> 01.04 (vector_multiplication.py)

---

<!--
_backgroundColor: black
_paginate: false
-->
![bg 120%](sample--ch02.png)
> 02.07 (attraction_many_movers.py)

---

<!--
_backgroundColor: black
_paginate: false
-->
![bg 120%](sample--ch03.png)
> 03.09 (the_wave.py)

---

<!--
_backgroundColor: black
_paginate: false
-->
![bg 120%](sample--ch04.png)
> 04.09 (additive_smoke_system.py)

---

<!--
_backgroundColor: black
_paginate: false
-->
![bg 120%](sample--ch05.png)
> 05.12 (flocking_bin_lattice.py)

---

<!--
_backgroundColor: black
_paginate: false
-->
![bg 120%](sample--ch06.png)
> 06.12 (soft_swing_pendulum.py)

---

<!--
_backgroundColor: black
_paginate: false
-->
![bg 120%](sample--ch07.png)
> 07.03 (oop_game_of_life.py)

---

<!--
_backgroundColor: black
_paginate: false
-->
![bg 120%](sample--ch08.png)
> 08.06 (recursive_tree.py)

---

<!--
_backgroundColor: black
_paginate: false
-->
![bg 120%](sample--ch09.png)
> 09.04 (interactive_selection.py)

---

<!--
_backgroundColor: black
_paginate: false
-->
![bg 120%](sample--ch10.png)
> 10.02 (gesture_classifier.py)

---

<!--
_backgroundColor: black
_paginate: false
-->
![bg 120%](sample--ch11.png)
> 11.04 (neuroevolutionary_steering.py)

---

## Introduction  » Setup
*JS to Python, and IDE configuration ...*
<!--
- [NEXT SLIDE]
-->

---

<!--
_backgroundColor: #EEE
_paginate: false
-->
![bg 70%](intro--01-js-pythos.svg)
> https://py5coding.org
<!--
- really, both languages can do the same things, but it's libraries/frameworks that matter
- so, in order to port from javascript to python ... [NEXT SLIDE]
-->

---

<!--
_backgroundColor: #EEE
_paginate: false
-->
![bg 70%](intro--02-p5js-py5.svg)
> https://py5coding.org
<!--
- i opted to use py5 as a python processing framework
- of course, there are other solutions (processing.py, p5py, pyp5js, a few others), each with its pros/cons
-->

---

<!--
_backgroundColor: #EEE
_paginate: false
-->
![bg 70%](intro--py5.png)
> https://py5coding.org
<!--
- for those who are unfamiliar with py5, find out more at py5coding.org
-->

---

## Introduction  » py5 Features
* <highlight>Modern Python:</highlight> full Python 3 support, including C-extension libraries,  
  including native integration with NumPy, Pillow, Shapely, etc.
* <highlight>Processing engine:</highlight> Java Processing graphics backend via JPype,  
  and can load and use many existing Java Processing libraries
* <highlight>Any editor:</highlight> works in Jupyter Notebooks, VS Code, etc.  
  with flexible modes: static & imported (beginner), module, or class
* <highlight>Fun features to explore:</highlight> pixel manipulation using NumPy arrays,  
  live coding, Matplotlib, Shapely geometries, Pandas/Polars etc.

---

## Introduction » Run py5
* <highlight>Standard python script:</highlight> VS Code, PyCharm, terminal, etc.
* <highlight>Jupyter notebook:</highlight> via standard ipykernel, or py5 kernel
* <highlight>Thonny-py5mode:</highlight> Thonny IDE + py5 plugin <span style="color:orange;font-weight:bold">🠄</span>
<!--
- discuss pros/cons of each:
- standard -- any editor; requires manual environment/pip setup
- jupyter -- notebook format mixing different cells (good for teaching?); perhaps not your style
- thonny -- familiar to legacy processing users; feels 'dedicated'; perhaps not your style
-->

---

<!--
_backgroundColor: #EEE
_paginate: false
-->
![bg 70%](setup--01-thonny.org.png)
> https://thonny.org
<!--
- find out more at thonny.org 
- features include ... [NEXT SLIDE]
-->

---

## Introduction » Thonny Features
* <highlight>Beginner-focused:</highlight> minimal, uncluttered interface designed for learning
* <highlight>Bundled Python:</highlight> includes a built-in Python 3 runtime
* <highlight>Cross-platform:</highlight> runs on Linux, macOS, Windows
* <highlight>Fully portable:</highlight> runs directly from a USB drive without admin rights
* <highlight>Several neat panels:</highlight> interactive shell, plotter, outline, and more
<!--
- but thonny won't handle py5 natively ...
- so this is where the thonny-py5mode plugin enters the picture ... [NEXT SLIDE]
-->

---

## Introduction » Thonny-py5mode Installation
*A plugin that turns the Thonny IDE into a Python 3 ~~shameless ripoff~~ replacement for the original Processing IDE.*
<br /><hr style="color:rgba(255,255,255,0.3)" />
<highlight>Process</highlight><br />

1. Download and run Thonny
2. Add plugin
<!--
- it's easy ... [NEXT SLIDE]
-->

---

<!--
_backgroundColor: black
_paginate: false
-->
![bg 50%](setup--02-thonny-install.png)
<!--
- this appears upon downloading thonny and running the first time
-->

---

<!--
_backgroundColor: black
_paginate: false
-->
![bg 50%](setup--03-thonny-1st-launch.png)
<!--
- note the simple application layout
-->

---

<!--
_backgroundColor: black
_paginate: false
-->
![bg 50%](setup--04-thonny-plugin-step-1.png)

---

<!--
_backgroundColor: black
_paginate: false
-->
![bg 50%](setup--05-thonny-plugin-step-2.png)

---

<!--
_backgroundColor: black
_paginate: false
-->
![bg 50%](setup--06-thonny-plugin-step-3.png)

---

<!--
_backgroundColor: black
_paginate: false
-->
![bg 50%](setup--07-thonny-plugin-restart.png)

---

<!--
_backgroundColor: black
_paginate: false
_class: lead
-->
*... restarting ...*

---

<!--
_backgroundColor: black
_paginate: false
-->
![bg 50%](setup--08-thonny-activate.png)
<!--
- you don't *have to use* imported mode, but this means:
- no import line(s) required
- no py5. prefix for every method
- more beginner-friendly
- so, largely matches traditional processing and p5.js syntax
- easier porting (to py5)
- (so, basically, it's more like processing!)
-->

---

<!--
_backgroundColor: black
_paginate: false
-->
![bg 50%](setup--09-thonny-activate-jdk.png)
<!--
- (recall that py5 is running on java processing)
- if java is not detected, it'll download and install a local version
-->

---

<!--
_backgroundColor: black
_paginate: false
-->
![bg 50%](setup--10-thonny-apply-settings.png)
<!--
- optional step to apply processing colour scheme and few other settings
-->

---

<!--
_backgroundColor: black
_paginate: false
-->
![bg 50%](setup--11-thonny-applied-settings.png)

---

<!--
_backgroundColor: black
_paginate: false
-->
![bg 50%](setup--12-thonny-run.png)
<!--
- just like processing, it has a static mode (not available in p5.js?)
- (of course, there are setup and draw functions for animated sketches)
-->

---

<!--
_backgroundColor: black
_paginate: false
-->
![bg 50%](setup--13-change-mode.png)
<!--
- (unchecking imported mode in the graphic)
- as i mentioned earlier, there is also a module mode
-->

---

<!--
_backgroundColor: black
_paginate: false
-->
![bg 50%](setup--14-thonny-run-module.png)
<!--
- note: import line, py5 prefixes, run_sketch method
-->

---

# py5
<!-- 
paginate: true
backgroundColor: maroon
color: var(--color-background)
-->
<!--
- to understand the porting process and requirements, a short py5 intro is necessary
-->

---

## py5 » Porting Approach
<b style="font-family:monospace;font-weight:bold">1</b>
<highlight>Translate Directly</highlight>  
<smaller>Vectors, forces, particles: *near* line-for-line</smaller>

---

## py5 » Porting Approach
<b style="font-family:monospace;font-weight:bold">1</b>
<highlight>Translate Directly</highlight>  
<smaller>Vectors, forces, particles: *near* line-for-line</smaller>

<b style="font-family:monospace;font-weight:bold">2</b>
<highlight>Rethink Logic</highlight>
<smaller>Language differences and library substitutions</smaller>

---

## py5 » Porting Approach
<b style="font-family:monospace;font-weight:bold">1</b>
<highlight>Translate Directly</highlight>  
<smaller>Vectors, forces, particles: *near* line-for-line</smaller>

<b style="font-family:monospace;font-weight:bold">2</b>
<highlight>Rethink Logic</highlight>
<smaller>Language differences and library substitutions</smaller>

<b style="font-family:monospace;font-weight:bold">3</b>
<highlight>Simplify Code</highlight>
<smaller>Python idioms to potentially simplify JS</smaller>

---

# 1. Translate Directly
<!-- 
backgroundColor: indigo
color: var(--color-background)
-->

---

## 1. Translate Directly » py5 Naming
```javascript
// p5.js
function setup() {
  createCanvas(640, 240);
}
function draw() {
  circle(mouseX, mouseY, 48);
}
```

<hr style="color:rgba(255,255,255,0.3)" />

```python
# py5
def setup():
    size(640, 240)
def draw():
    circle(mouse_x, mouse_y, 48)
```

---

## 1. Translate Directly » Key Renames to Know

<table style="width:100%;border:none;font-size:0.9em">
  <tr style="background-color:rgba(0,0,0,0.3)">
    <td style="border-color:rgba(0,0,0,0.3)">p5.js</td>
    <td style="border-color:rgba(0,0,0,0.3)">py5</td>
    <td style="border-color:rgba(0,0,0,0.3)">Why</td>
  </tr>
  <tr style="background:none">
    <td style="border-color:rgba(0,0,0,0.3);background:transparent"><code>createCanvas()</code></td>
    <td style="border-color:rgba(0,0,0,0.3);background:transparent"><code>size()</code></td>
    <td style="border-color:rgba(0,0,0,0.3);background:transparent">Processing Java</td>
  </tr>
  <tr style="background:none">
    <td style="border-color:rgba(0,0,0,0.3);background:transparent"><code>mouseX</code>, <code>strokeWeight()</code></td>
    <td style="border-color:rgba(0,0,0,0.3);background:transparent"><code>mouse_x</code>, <code>stroke_weight()</code></td>
    <td style="border-color:rgba(0,0,0,0.3);background:transparent">snake_case</td>
  </tr>
  <tr>
    <td style="border-color:rgba(0,0,0,0.3);background:transparent"><code>map()</code></td>
    <td style="border-color:rgba(0,0,0,0.3);background:transparent"><code>remap()</code></td>
    <td style="border-color:rgba(0,0,0,0.3);background:transparent">Python built-in</td>
  </tr>
  <tr style="background:none">
    <td style="border-color:rgba(0,0,0,0.3);background:transparent">NOC <code>next</code>, <code>len</code> variables</td>
    <td style="border-color:rgba(0,0,0,0.3);background:transparent"><code>next_</code>, <code>len_</code></td>
    <td style="border-color:rgba(0,0,0,0.3);background:transparent">Python built-in</td>
  </tr>
  <tr style="background:none">
    <td style="border-color:rgba(0,0,0,0.3);background:transparent"><code>createVector</code></td>
    <td style="border-color:rgba(0,0,0,0.3);background:transparent"><code>Py5Vector2D</code>, <code>Py5Vector3D</code></td>
    <td style="border-color:rgba(0,0,0,0.3);background:transparent">real class</td>
  </tr>
  <tr style="background:none">
    <td style="border-color:rgba(0,0,0,0.3);background:transparent"><code>random()</code></td>
    <td style="border-color:rgba(0,0,0,0.3);background:transparent">also <code>random()</code></td>
    <td style="border-color:rgba(0,0,0,0.3);background:transparent">py5 built-in</td>
  </tr>
  <tr style="background:none">
    <td colspan="3" style="border-color:rgba(0,0,0,0.3);background:transparent"><i>More on slides to come ...</i></td>
  </tr>
</table>
<!--
- mostly everything is a mechanical camelCase-to-snake_case conversion
- renaming cuts the other way too: noc names like next and len shadow python builtins -- the port uses next_, len_
- (js uses array.length; its next method is not a global function)
-->

---

## 1. Translate Directly » Randomness & Noise

```javascript
// p5.js
let x = random(width);
let g = randomGaussian(0, 1);
let n = noise(xoff);
let coinflip = floor(random(2));  // 0 or 1
```

<hr style="color:rgba(255,255,255,0.3)" />

```python
# py5
x = random(width)                 # py5's own, not the random module
g = random_gaussian(0, 1)
n = noise(xoff)
coinflip = random_int(1)          # inclusive: returns 0 or 1
```
<!--
- chapter 0 ports near line-for-line: random(), random_gaussian(), noise() all exist in py5
- noise() is processing's perlin implementation, not p5.js's -- same effect, different exact values
- py5 also offers os_noise() (opensimplex) as an alternative
-->

---

## 1. Translate Directly » Vector Operations

```javascript
// p5.js
position = createVector(100, 100);
velocity = createVector(2.5, 2);
position.add(velocity);
print(position.mag());
position.setMag(10);
```

<hr style="color:rgba(255,255,255,0.3)" />

```python
# py5 
position = Py5Vector2D(100, 100)
velocity = Py5Vector2D(2.5, 2)
position += velocity
print(position.mag)
position.mag = 10
```
<!--
- (i really like what jim schmitz with vectors, because noc uses a lot of vectors!)
- createVector() needs setup() (unless using new p5.Vector); Py5Vector is a standalone class usable anywhere
- p5.Vector mutates via method calls: add(), sub(), mult() ...
- Py5Vector overloads the arithmetic operators (+, +=, *=) -- more on this in the simplify section
- p5.js uses getter/setter methods (mag(), setMag()); py5 uses python properties (position.mag = 10)
- Py5Vector is explicitly sized (Py5Vector2D, Py5Vector3D) and backed by numpy under the hood
-->

---

## 1. Translate Directly » Multi-File Caveat

<highlight><em>sketch.py</em></highlight>
```python
from mover import Mover
...

def setup():
    ...
    mover = Mover()
    ...

def draw():
    ...
    mover.show()
```
<!--
- consider a sketch that imports a class from another file (in this case, Mover)
- imported mode magic only applies to the main sketch.py file -- not the files it imports
- so how does mover.py access py5 functions and variables? [NEXT SLIDE]
-->

---

## 1. Translate Directly » Multi-File Solution #1

<highlight><em>mover.py</em></highlight>
```python
from py5 import *

class Mover:
    def __init__(self, width, height):  # must pass in width & height
        self.width = width
        self.height = height
        self.position = Py5Vector2D(self.width / 2, self.height / 2)

    def show(self):
        fill(127)
        circle(self.position.x, self.position.y, 48)
```
<!--
- without an import in mover.py: NameError on Py5Vector2D, fill, circle, etc.
- from py5 import * imports functions/classes, but dynamic variables (width, height, mouse_x) fail
- forces workarounds like passing width/height or ... [NEXT SLIDE]
-->

---

## 1. Translate Directly » Multi-File Solution #2

<highlight><em>mover.py</em></highlight>
```python
from py5 import *

class Mover:
    def __init__(self):
        s = get_current_sketch()
        self.position = Py5Vector2D(s.width / 2, s.height / 2)

    def show(self):
        fill(127)
        circle(self.position.x, self.position.y, 48)
```
<!--
- use get_current_sketch() to grab a reference to the running sketch, then --
- read dynamic variables as attributes on that sketch instance (s.width, s.height)
- keeps class parameter-free, but there's another way ... [NEXT SLIDE]
-->

---

## 1. Translate Directly » Multi-File Solution #3

<highlight><em>mover.py</em></highlight>
```python
# PY5 IMPORTED MODE CODE

class Mover:
    def __init__(self):
        self.position = Py5Vector2D(width / 2, height / 2)

    def show(self):
        fill(127)
        circle(self.position.x, self.position.y, 48)
```
<!--
- use the # PY5 IMPORTED MODE CODE marker at the top (case-insensitive)
- no constructor workarounds needed -- keeps multi-file sketches line-for-line with the book
- signals py5's import hook to transform this module just like the main sketch
- injects the full py5 api: classes, drawing functions, and live dynamic variables (width, height, mouse_x)
- and if you forget the marker ... [NEXT SLIDE]
-->

---

<!--
_backgroundColor: black
_class: lead
_color: var(--color-background)
_paginate: false
-->
<i style="font-family:monospace;font-size:0.9em">
NameError: The name "Py5Vector2D" is not defined. Your Sketch is also running in Imported Mode. If the code throwing this exception was imported into your main py5 Sketch code, please ensure the py5 Imported Mode marker "# PY5 IMPORTED MODE CODE" has been properly added to the module.
</i>
<!--
- this is how i actually discovered this solution -- how useful!
-->

---

# 2. Rethink Logic
<!-- 
backgroundColor: midnightblue
color: var(--color-background)
-->
<!--
- (exclusive p5.js libraries that require substitutes)
-->

---

## 2. Rethink Logic » Scope Is Different

```javascript
// p5.js -- outer variables just work
let position;

function draw() { 
    position.add(velocity);
}
```

<hr style="color:rgba(255,255,255,0.3)" />

```python
# py5 -- assignment needs an explicit declaration
def draw():
    global position
    position += velocity
```
<!--
- javascript closures reassign outer variables freely
- python requires global for reassignment in setup() / draw()
-->

---

## 2. Rethink Logic » No preload()

```javascript
// p5.js -- assets load asynchronously before setup()
let img;

function preload() {
  img = loadImage('texture.png');
}
```

<hr style="color:rgba(255,255,255,0.3)" />

```python
# py5 -- loading is synchronous: just do it in setup()
def setup():
    global img
    size(640, 240)
    img = load_image('texture.png')
```
<!--
- the browser can't pause and wait for files, so p5.js needs preload() / callbacks for assets
- py5 is happily: load_image() returns the finished image, preload() disappears
-->

---

## 2. Rethink Logic » Matter.js to Pymunk

```python
from pymunk import Body, moment_for_box, Poly, Space

engine = Space()                           # world/engine = Space
engine.gravity = (0, 1.0 * SCALE_GRAVITY)  # calibration constant

# Pymunk separates Body (physics) from Shape (collision skin)
box_body = Body(mass, moment_for_box(mass, (w, h)))
box_body.position = (100, 100)
box_shape = Poly.create_box(box_body, (w, h))
box_shape.friction = 0.01 * SCALE_FRICTION
box_shape.elasticity = 0.75
engine.add(box_body, box_shape)
...
```
<!--
- matter.js is javascript-only -- pymunk is a chipmunk2d wrapper
- pymunk separates body (physics) from shape (collision skin); multiple shapes can attach to one body
- no render module: matter.js bundles a renderer; this is only for a sketch or two, so i added a few extra lines to get py5 rendering
-->

---

## 2. Rethink Logic » Matter.js Calibration
<highlight><em>pymunk_constants.py</em></highlight>
```python
"""
Since the Matter.js and Pymunk engines use different units and solvers,
these values provide an *approximate* conversion for matching visual behavior.
"""

SCALE_GRAVITY = 900.0
FPS = 60.0
DT = 1.0 / FPS
SCALE_TIME = FPS
SCALE_VELOCITY = SCALE_TIME
SCALE_ANG_VELOCITY = SCALE_TIME
SCALE_FRICTION = SCALE_TIME
```
<!--
- i just imported this file as required
-->

---

## 2. Rethink Logic » Toxiclibs (jars)
Simply skip the JS Toxiclibs port and use the Java original.
<br /><hr style="color:rgba(255,255,255,0.3)" />
```python
"""
NOTE:
Examples 6.11 through 6.15 (end of chapter) use the Toxiclibs Java libraries.
For details on py5's integration with Processing (Java) libraries, see:
https://py5coding.org/how_tos/use_processing_libraries.html
"""

from toxi.geom import Vec2D, Rect
from toxi.physics2d import VerletPhysics2D, VerletParticle2D, VerletSpring2D
from toxi.physics2d.behaviors import GravityBehavior2D
```
<!--
- toxiclibs.js is a port of a java library -- py5 runs on the jvm
- so python can use the original java toxiclibs directly
- just drop a jars directory alongside the sketch
-->

---

## 2. Rethink Logic » Wrapping Toxiclibs Objects

<smaller>

```javascript
// p5.js -- subclass the Java particle directly
class Particle extends VerletParticle2D {
  constructor(x, y, r) {
    super(x, y); this.r = r; 
  }
  show() {
    circle(this.x, this.y, this.r * 2);
  }
}
physics.addParticle(particle);  // pass the object itself
```

<hr style="color:rgba(255,255,255,0.3)" />

```python
# py5 -- wrap the Java particle via composition
class Particle:
    def __init__(self, x, y, r):
        self.p = VerletParticle2D(x, y)  # underlying Java object
    def show(self):
        circle(self.p.x(), self.p.y(), self.r * 2)

physics.addParticle(particle.p)  # pass the Java object via .p
```

</smaller>
<!--
- in py5 composition is cleaner than subclassing java classes
- gotcha: the world needs the underlying java object, not the wrapper
-->

---

## 2. Rethink Logic » Machine Learning: ml5.js » scikit-learn

```python
from sklearn.neural_network import MLPClassifier

classifier = MLPClassifier(hidden_layer_sizes=(16,), max_iter=2500)
classifier.fit(inputs, outputs)   # trains before setup() runs
```
<!--
- ml5.js trains asynchronously with callbacks (whenTrained, ...)
- scikit-learn trains synchronously, before the window opens
- callbacks disappear entirely; the shell replaces ml5's visor
- async is the deepest rethink: the browser cannot block, python happily can
- ch10's perceptron is hand-rolled in both languages -- that one is a direct port
-->

---

## 2. Rethink Logic » Neuroevolution: a Bespoke NumPy Brain

```python
class Brain:
    """Vectorized NumPy brain with GA helpers."""

    def __init__(self, inputs, outputs, hidden=8):
        self.w_ih = _rng.uniform(-1.0, 1.0, (hidden, inputs))
        self.b_h  = _rng.uniform(-1.0, 1.0, (hidden,))
        # ... w_ho, b_o ...

    def forward(self, inputs):
        h = np.tanh(self.w_ih @ inputs + self.b_h)
        return (self.w_ho @ h + self.b_o).tolist()
```
<!--
- ml5's neuroEvolution has no drop-in substitute -- write one (~50 lines)
- forward pass is two matrix multiplications -- numpy's @ operator
- ga helpers (crossover, mutate) operate directly on the weight arrays
- sometimes "rethinking" means realising the library was hiding very little
-->

---

# 3. Simplify Code
<!-- 
backgroundColor: darkslategray
color: var(--color-background)
-->

---

## 3. Simplify Code » Operator Overloading

```javascript
// p5.js -- verbose static/method calls
let force = p5.Vector.sub(attractor, mover);
force.normalize();
force.mult(strength);
mover.acceleration.add(force);
```

<hr style="color:rgba(255,255,255,0.3)" />

```python
# py5 -- reads like the maths
force = (attractor - mover).norm * strength
mover.acceleration += force
```
<!--
- the vector algebra chapters are where python shines brightest
- normalize as .norm property, magnitude as .mag -- expressions compose naturally
-->

---

## 3. Simplify Code » Comprehensions

```javascript
// p5.js
let training = [];
for (let i = 0; i < 2000; i++) {
  training.push([random(-width/2, width/2), random(-height/2, height/2), 1]);
}
```

<hr style="color:rgba(255,255,255,0.3)" />

```python
# py5
training = [
  [random(-width / 2, width / 2), random(-height / 2, height / 2), 1]
  for _ in range(2000)
]
```
<!--
- training-data setup and particle spawning collapse into single expressions
-->

---

## 3. Simplify Code » Backward Filter

```javascript
// p5.js -- loop backward to splice safely
for (let i = particles.length - 1; i >= 0; i--) {
  particles[i].run();
  if (particles[i].isDead()) particles.splice(i, 1);
}
```

<hr style="color:rgba(255,255,255,0.3)" />

```python
# py5 -- same backward-loop technique works ...
for i in range(len(particles) - 1, -1, -1):
    particles[i].run()
    if particles[i].dead: del particles[i]
```
<!--
- the particle systems chapter's central trick carries over directly
- but python has a nicer answer ... [NEXT SLIDE]
-->

---

## 3. Simplify Code » Backward Filter Simpler

```javascript
// p5.js -- backward loop + splice
for (let i = particles.length - 1; i >= 0; i--) {
  if (particles[i].isDead()) particles.splice(i, 1);
}
```

<hr style="color:rgba(255,255,255,0.3)" />

```python
# py5 -- rebuild the list declaratively
self.particles = [p for p in self.particles if not p.dead]
...
# computed property -- accessed as particle.dead (no parentheses).
    @property
    def dead(self) -> bool:
```
<!--
- the chapter 4 index-juggling disappears entirely
- callback to the rethinking section: the backward loop works, but this is the pythonic answer
- isDead() method becomes a dead property -- same attribute-over-method pattern as .mag
-->

---

## 3. Simplify Code » Slices: Cellular Automata

```javascript
// p5.js
let nextgen = cells.slice();
```

<hr style="color:rgba(255,255,255,0.3)" />

```python
# py5
next_gen = cells[:]                # copy a generation
cells = [0] * (width // W)         # build a row of dead cells
left, me, right = cells[i - 1], cells[i], cells[i + 1]
```
<!--
- list building, copying, and unpacking shrink the wolfram ca code
- tuple unpacking makes the neighborhood read like the book's prose
- integer division // avoids the js-style floor() call for grid math
-->

---

## 3. Simplify Code » Small Quality-of-Life Wins

- `position += velocity` -- augmented assignment on vectors
- `Particle(*self.origin)` -- vectors unpack as iterables
- `10_000` -- readable numeric literals
- Type hints: `def step(self) -> None:` documents intent
- No `let` / `const` / semicolons / braces
- Synchronous ML training -- no callback pyramids
<!--
- none of these are transformative alone; together the ports are consistently shorter
- type hints are optional but the py5 port uses them throughout
-->

---

# Materials
<!-- 
backgroundColor: saddlebrown
color: var(--color-background)
-->

---

<!--
_backgroundColor: #EEE
_paginate: false
-->
![bg 70%](materials--01-noc-book-lin.png)
> https://natureofcode.com
<!--
- the book is free to read online; the additional resources page lists ports to other languages
- the py5 port lives alongside pygame, openframeworks, and go ports
-->

---

<!--
_backgroundColor: #EEE
_paginate: false
-->
![bg 70%](materials--02-repo-1.png)
> https://github.com/tabreturn/py5-nature-of-code
<!--
- the complete py5 port: all chapters, built with thonny-py5mode
-->

---

<!--
_backgroundColor: #EEE
_paginate: false
-->
![bg 70%](materials--03-repo-2.png)
> https://github.com/tabreturn/py5-nature-of-code

---

<!--
_backgroundColor: #EEE
_paginate: false
-->
![bg 70%](materials--04-repo-3.png)
> https://github.com/tabreturn/py5-nature-of-code
<!--
- the readme links every py5 sketch to its original p5.js editor sketch
-->

---

<!--
_backgroundColor: #EEE
_paginate: false
-->
![bg 70%](materials--05-jupyter-holly.png)
> https://github.com/hollygrimm/py5-noc-book-2
<!--
- if notebooks are your style: all 12 chapters as runnable jupyter notebooks, full book text plus code
-->

---

<!--
_backgroundColor: #EEE
_paginate: false
-->
![bg 70%](materials--06-jupyter-chapter.png)
> https://github.com/hollygrimm/py5-noc-book-2
<!--
- book prose, figures, and editable py5 cells interleaved per chapter
-->

---

# Takeaways
<!-- 
backgroundColor: darkolivegreen
color: var(--color-background)
-->

---

## Takeaways

- **Most of the book translates directly** -- randomness, vectors, forces, oscillation, particles, steering, CA, fractals, and GA are near line-for-line
- **Renames to remember**: `map()` » `remap()`, camelCase » snake_case, `.mag()` » `.mag`
- **The `global` keyword** is the most common porting stumble
- **Library substitution**: Pymunk for Matter.js, original Java Toxiclibs via the JVM, scikit-learn / NumPy for ml5.js
- **Python often simplifies**: operator overloading, comprehensions, slices
- **AI drafts, you verify**: great at renaming passes, weak on library judgement and visual correctness
<!--
- the ecosystem swap is the interesting part: sometimes a wrapper (pymunk), sometimes the original library (toxiclibs), sometimes diy (numpy brain)
-->

---

## Try It Yourself

- Install **Thonny-py5mode**, activate *py5 » Imported mode*
- Port a chapter 1 or 2 sketch by hand -- it's mostly renaming
- Compare against the complete **py5-nature-of-code** port
- Read the book free online: natureofcode.com
<!--
- suggested exercise: port example 2.6 (attraction) and then simplify it with operator overloading
- the py5 port's readme links every sketch to its p5.js editor original
-->

---

## *End*
<!-- 
paginate: false 
backgroundColor: black
color: var(--color-background)
-->

