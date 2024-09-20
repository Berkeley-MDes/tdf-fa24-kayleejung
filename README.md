# Hello DES INV 202 Student!

# Outline
[week 1](README.md#week-1-report-1) <br>
[week 2](README.md#week-2-report-2) <br>
[week 3](README.md#week-3-report-3)


---
# Week 3: Report 3 - 09/16/2024 #
This week, the main focus was on the project deliverables, as the project is coming to completion. After last Thursday's class, I decided to pivot from the phone stand and create a 3D printed lamp. Moving to Berkeley from BC, I wasn't able to bring a lot of extra items and furniture aside from the things that fit in my suitcases. My apartment lacks a lot of lighting, so I thought this would be a perfect opportunity to create something that I will use everyday. <br>

<h3>Reflections</h3>

I started with some rough sketching on the potential form and structure of the lamp. This helped me envision how I would make it in a software like Fusion360 (which was both helpful and frustrating). Grasshopper has such a different workflow, it was difficult in the beginning to rework my thinking, and build shapes in alternative ways. <br> 

<img width =400 alt="Sketch1" src="assets/03lampsketch1.jpg">  <img width =400 alt="Sketch1" src="assets/03lampsketch2.jpg">

From the sketches, I moved on to Grasshopper, and making my dynamic model. The vase design from last week was particularly useful for implementing bezier curves, but it utilized a circular cross-section, and I wanted to make a more complex shape. I ended up utilizing the bezier curve, but also adding the element of a polar array, to pattern circles in the cross section. I also added a rotate element so the lamp design could have a twist element. After a series of lofts, merges and joins, I finally ended up with a closed brep set for baking! Special thank you to Cody for helping me troubleshoot :) <br>

<img height = 400 alt="Lamp" src="assets/03lampexperiment1.png">  <img height  =400 alt="Lamp" src="assets/03lampexperiment2.png">

<h3>My Final Lamp!</h3>
<img height = 400 alt="Lamp" src="assets/03lamplight.jpeg">


<h3>Speculations</h3>
The most fascinating part about designing this lamp was creating with parameters in mind, and creating relationships between the parameters and their respective geometries. To model my lamp system, I created a model for the lamp stand, lightbulb and lamp shade. While I only intended to print the lamp shade, having the whole system was very useful for visualizing parameters and relative size. I really like the aspect of being able to change parameters, and have the rest of the design be dependent on those changes. 

Another fascinating aspect about Grasshopper, while extremely challenging, is the use of data structures in CAD. In softwares like Fusion360 or Solidworks, if there is an error with carrying out an operation, it generally gives feedback that is slightly ambiguous. With Grasshopper, it provides more information on the data being passed to each component, which is often times the source of error, as data being passed is not always the same type or dimension. This was very tricky for me to troubleshoot as a new learner of Rhino and Grasshopper, but this was a good learning opportunity. I'm excited to continue learning and applying my foundational skills to another project, or maybe another lamp!

---
# Week 2: Report 2 - 09/09/2024 #
<h3> Rhino & Grasshopper Example Workflow Diagram</h3>
To understand the final product, I tried to dissect the grasshopper file and make sense of the parameters, and how they impact the final design. In doing so, I brainstormed design considerations and overarching specificiations pertaining to the phone stand requirements. While my final model will likely not resemble the examples shared in class, the importance of the design considerations/specifications will translate to various forms. 
<img width ="width" alt="Rhino & Grasshopper Example Workflow Diagram" src="assets/rhinograsshopper_exampleworkflow.png"> <br>  


<h3>Learning Grasshopper Terms</h3>
<strong>Brep</strong>: <strong>B</strong>oundary <strong>Rep</strong>resentation = polysurface (in rhino); geometry type that represents the surface of an object with a set of connected surfaces <br>
<br>
<strong>Baking</strong>: pushes new geometry to Rhino based on the current state of the Grasshopper parameters. Note: once the object is baked, it unresponsive to any further tweaks in Grasshopper.

<h3>Reflections</h3>
<h4>Experimenting with Example Model</h4>
<img width =600  src="assets/02bakedsphere.png"> <br>  
Using the example file, I played around with the parameters and baked a few forms. I was most interested in the offset from origin slider, and the diagram above shows an extreme case. While grasshopper counted this as a valid model, it is highly likely that this would not be able to balance the phone, given the far offset of the phone and the tilt angle. While it is difficult to quantify the balance and center of gravity, I am curious if a constraint can be put in place, with respect to the max offset of the phone, and how that could potentially mitigate balance issues. <br>

<h4>Experimenting with New Form</h4>
On Tuesday, I attended the grasshopper workshop, where we learned how to create a cube with a nested cylinder. It was challenging to follow along with the example since I was still unfamiliar with all the tools and commands. After class, I inputted the box model we made into the example file, and replaced the nested spheres. In doing so, the layout of the example file started to really make sense! <br><br>
<img width =600  src="assets/grasshopperbox.png"> <br>  
<img width =600  src="assets/02bakedphonestand.png"> <br>  

<h3>Speculations</h3>
<img width =600  src="assets/02vase.png"> <br>  
I followed a grasshopper tutorial on youtube on how to make a vase using bezier curves. While this was a bit outside of scope, it peaked my interest in how I could potentially utilize math and curves to make my phone stand. 
---

# Week 1: Report 1 – 09/05/2024 #


My focus of the week was to get reacquainted with CAD tools, and familiarize myself with Rhino which I have not used before. I followed a couple youtube tutorials outlining the Rhino interface, and practiced using the tools to model a watering can (not pictured because the app crashed before I saved - a good learning opportunity for future use). In my undergrad degree in engineering, I've used tools like Solidworks and Fusion360 for various academic and personal projects. My prior experience in CAD definitely helped in getting started with Rhino, since I am familiar with terms like 'extrude, sweep, revolve' etc, as well as visualizing how to model shapes from 2D sketches to 3D. However, there are noticeable differences in functionality/capability when comparing Rhino to more engineering-focused softwares. 

Differences I've noticed so far:
1. Solidworks is dimension-driven, and I heavily rely on the Smart Dimension tool when modeling. In Rhino, there is no tool to resize shapes after drawing. 
2. Rhino utilizes freeform surface modeling with NURBS (Non-Uniform Rational Basis Splines) Mathematical Model whereas Solidworks utilizes parametric modeling.
3. The freeform nature of Rhino is ideal for modeling organic shapes and curves. Solidworks is less compliant due to strict geometries. 

This week, I also got to try out the laser cutters at the Jacobs Makerspace! I have a 3D printer at home, but I've never been able to use a laser cutter before. I took a drawing I made of my dog, Cheeky, and redrew it in Adobe Illustrator. My initial cut with the laser cutter just etched the file instead of cutting through, but in my design I had specified an outer edge to be cut. The color and stroke of my lines were correct, but it appeared as black only on the laser cutting software. Through a bit of troubleshooting with file settings, particularly the way Adobe saves the file, I got a successful cut! The laser cutter is very efficient, as my keychain only took less than a minute to complete. I'm interested in ways I can incorporate this into future projects, both for MDes and art, especially with cutting acrylic sheets. 

<img width ="300" alt="Lasercut keychain of my dog Cheeky" src="assets/lasercut.png"> <br>  

[Wooj Design](https://wooj.design/?srsltid=AfmBOorDeVysMCg3r3KpSV4qGdLmuIJUsZzFeqlC6aK6UUAvHGMSMRW9) is a design company based in Brooklyn, NY, that produces 3D-printed home goods, and notably lighting fixtures. The most popular design is the [Wavy Lamp](https://wooj.design/collections/shop/products/lamp), which is entirely 3D-printed, and designed using Rhino and Grasshopper. This was how I initially discovered Rhino and Grasshopper, though I never fully explored the software. As a bit of a math nerd, I am excited to utilize these new functions in future projects!




---
