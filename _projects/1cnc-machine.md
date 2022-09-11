---
title: "Senior Design Project - CNC Milling Machine"
excerpt: "Computer Numerically Controlled machine built using 3D printed parts that can carve wood and aluminum<br/><a href='/projects/1cnc-machine/'><img src='/images/cnc-1.jpg' alt='cnc machine' width='980' height='735'></a>"
collection: projects
---

What is a CNC machine?
------
A CNC machine is a machine that follows computer instructions to automate a tool's movements. 3D printing heads, laser cutters, and plasma cutters can all be computer numerically controlled (CNC), but generally, the term refers to machining tools like mills or lathes.

Why we built it
------
Since CNC machines are controlled by computers, they can reach levels of precision that only masters of a craft could obtain. As engineers, my teammates and I are far better at modeling objects on the computer than carving them with hand tools. Unfortunately, industrial CNC machines can cost thousands of dollars, which to hobbyist college students is completely unjustifiable. I have a saying for situations like this: if you can't afford it, you've gotta build it.

How it works
------
The machine uses stepper motors to control the movement of a high-speed spindle in all 3-axes (X, Y, Z). A computer speaks to the motor drivers (which "drive" the motors) in a language called G-code. G-code instructions tell the motor drivers how to move the motors, controlling their direction and speed. A computer-aided manufacturing (CAM) program (like the one built into Fusion 360) uses designer specified toolpaths to compile a list of instructions into a .gcode file. This file is read by a program called CNCjs which sends the G-code instructions to an Arduino running a firmware called GRBL, which outputs signals via the Arduino pins to control the motors.

CNCjs allows users to manually control the movement of the machine to match the starting location of your design's toolpath with the real world. The program also helpfully displays a real-time animation of the path via a graphical interface.

How we built it
------
We spent the first week determining the major components of the project. During this time, we drew sketches and decided what the end product would look like, which parts we would design to be 3D printed, and which would be purchased. Each week, we came together as a team to determine what would be best to work on next and split the workload according to team member preferences. I wanted to learn how to make 3D models, so I modeled most of the parts. We based the models off of our sketches and used Fusion 360 to turn the pen and paper designs into 3D models. The models were printed on Prusa machines with infill percentages between 20 and 30 percent depending on the part. 

Unfortunately, just after printing the final part, the school shut down due to COVID-19, and our group had to finish assembling the machine outside of the lab. We no longer had a good place to work on the project as a group, so I took the machine to my hometown to finish assembling it. After testing movement control of the spindle carrier, the final step before attaching a 500 Watt tree carcass shaper to it was adding safety protection. This was assembled using plexiglass sheets epoxied together to create a shield between users and the cutting tool. The images below show the progress made to the machine.

<img src='/images/base-complete.jpg' alt='machine base complete' width='769' height='577'>

Here you can see the beginnings of our project. The bent rod you see on the right is unfortunately not a fisheye distortion. The lead screw is really bent, and it really hurt our schedule waiting for a new one to arrive.

<div class='row'>
  <div class='two-images'>
    <img src='/images/side-printed.jpg' alt='3D printed part laying on print bed' style='width:100%'>
  </div>
  <div class='two-images'>
    <img src='/images/spindle-holder-printed.jpg' alt='3D printed part laying on print bed' style='width:100%'>
  </div>
</div>
<br/>
Here are a few parts I 3D modeled and printed. The small rectangular holes are for sliding in nuts to secure machine screws.

<img src='/images/carrier-complete.jpg' alt='mostly finished machine' width='769' height='577'>

This is as far as we got before campus was locked down.

<div class='row'>
  <div class='two-images'>
    <img src='/images/t-nuts.jpg' alt='plywood machine base with holes for attaching parts and wasteboard' style='width:100%'>
  </div>
  <div class='two-images'>
    <img src='/images/wasteboard.jpg' alt='Wasteboard attached to machine plywood base' style='width:100%'>
  </div>
</div>
<br/>
Here I'm building the machine's base using plywood and t-nuts to secure wasteboard and parts in the future.

<img src='/images/cnc-drawing-test1.jpg' alt='machine fails to draw spirals and decides to draw lines instead' width='769' height='577'>

Nothing ever works on the first try.

<img src='/images/cnc-drawing-test2.jpg' alt='machine writes the letters s e n in progress of writting senior design flaw' width='769' height='577'>

After adjusting some settings, the machine was calibrated.

<img src='/images/protective-shield.jpg' alt='plexiglass box missing top and bottom standing on a side to let epoxy dry' width='769' height='577'>

Safety precautions were made.

<img src='/images/cnc-done.jpg' alt='fully-assembled machine' width='769' height='690'>

The final product.

Results
------
Owning a CNC machine gives you a lot of artistic freedom. You can carve just about anything into a piece of wood with a comparatively low amount of talent. I wanted to make something unique, and a show called <i>Solar Opposites</i> gave me an idea. In the show, the main characters are aliens and there is an episode where they first learn about man caves. Being aliens, they aren't quite fluent in the english language and mishear "man caves" as "manc aves". As a bit of fun, I made a wooden manc ave sign.

<img src='/images/manc-ave1.jpg' alt='sign with wood burrs around letters' width='769' height='577'>

This is what the sign looked like after being carved by the machine.

<img src='/images/manc-ave2.jpg' alt='manc ave sign with letters painted black' width='769' height='577'>

It started to look good after some sanding and a few coats of paint.

<img src='/images/manc-ave3.jpg' alt='wooden sign with charred edges around letters' width='769' height='577'>

Finally, I burnt the edges to give the sign a bit more character.

This machine presents a number of oppurtunities to hobbyist makers. From prototyping parts to making art, after learning basic CAD and CAM, their ability is only limited by their imagination. We are proud to have designed and built our own CNC machine.

Teammates: <a href="https://www.linkedin.com/in/robert-tronnier-2ba4a5172/" target="_blank">Robert Tronnier</a>, <a href="https://www.linkedin.com/in/devin-kohnke-048b6b159/" target="_blank">Devin Kohnke</a>
