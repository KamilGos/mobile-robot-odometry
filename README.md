<h1 align="center"> mobile-robot-odometry </h1>
<h2 align="center"> Velocity and encoder-based odometry calculation for differentially driven mobile robot </h2>

<!-- https://shields.io/ -->
<p align="center">
  <img alt="Top language" src="https://img.shields.io/badge/Language-Python-yellow?style=for-the-badge&logo=python">
  <img alt="Status" src="https://img.shields.io/badge/Status-done-green?style=for-the-badge">
    <img alt="Repository size" src="https://img.shields.io/github/languages/code-size/KamilGos/mobile-robot-odometry?style=for-the-badge">
</p>

<!-- table of contents -->
<p align="center">
  <a href="#dart-about">About</a> &#xa0; | &#xa0;
  <a href="#package-content">Content</a> &#xa0; | &#xa0;
  <a href="#microscope-tests">Tests</a> &#xa0; | &#xa0;
  <a href="#checkered_flag-starting">Starting</a> &#xa0; | &#xa0;
  <a href="#eyes-implementation">Implementation</a> &#xa0; | &#xa0;
  <a href="#memo-license">License</a> &#xa0; | &#xa0;
  <a href="#technologist-author">Author</a> &#xa0; | &#xa0;
</p>

<br>

## :dart: About ##
Script for cacluclating odometry for mobile robot using data from encoders or velocity readings.

## :package: Content
 * [calculate_odometry.py](calculate_odometry.py) - main script
 * [data](data) - direcotry with example data:
   * forward.csv, backward.csv - motion length 1.15m 
   * left_full_turn.csv, right_full_turn.csv - full angle rotation
   * square_right.csv, square_left.csv - square side length = 1.15m and 
   return to initial pose

## :microscope: Tests ##
<h2 align="left">square right: </h2>
<div align="center" id="ex1"> 
  <img src=images/ex1.png width="500" />
  &#xa0;
</div>

---

<h2 align="left">full right turn: </h2>
<div align="center" id="ex1"> 
  <img src=images/ex2.png width="500" />
  &#xa0;
</div>

## :checkered_flag: Starting ##
```bash
# Clone this project
$ git clone https://github.com/KamilGos/mobile-robot-odometry

# Access
$ cd mobile-robot-odometry

# Run the project
$ sudo python3 calculate_odometry.py
```
## :eyes: Implementation ##
For caclulating pose with velocity readings, the following eqiations are used:
<div align="center" id="eq1"> 
  <img src=images/eq_vel.png width="150" />
  &#xa0;
</div>

and for calculating pose with encoder readings:
<div align="center" id="eq2"> 
  <img src=images/eq_enc.png width="300" />
  &#xa0;
</div>
, where:
<div align="left" id="eq3"> 
  <img src=images/eq_var.png width="300" />
  &#xa0;
</div>

For robot used in tests: L=330mm, d=195mm and T_PR=76600

## :memo: License ##

This project is under license from MIT.

## :technologist: Author ##

Made with :heart: by <a href="https://github.com/KamilGos" target="_blank">Kamil Goś</a>

&#xa0;

<a href="#top">Back to top</a>