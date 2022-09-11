---
title: "Junior Design Project - Bike Alert"
excerpt: "Uses computer vision to automatically alert pedestrians of cyclists<br/><a href='/projects/2bike-alert/'><img src='/images/bike-alert.png' width='980' height='692' alt='fully-assembled device mounted on bike handlebars'></a>"
collection: projects
---
This project was inspired by a love for cycling and a realization of the many distractions cyclists face. Cyclists are often distracted by advertisements and commotion on the road, and to pedestrians, a distracted cyclist can be a serious hazard. Thousands of pedestrians are injured by cyclists in major US cities every year. Our project aims to lower this figure.

Overview
-----
Bike Alert is a pedestrian alerting system that uses computer vision to automatically warn pedestrians of cyclists. This way, if cyclists are distracted, pedestrians will still be alerted of their presence. The device houses a camera and a distance sensor connected to a Raspberry Pi running a program that performs real-time human detection to sound a speaker whenever a person is detected within a few meters. The system is housed inside a custom 3D printed case that is mounted on a cyclist's handlebars.

Design process
-----
We spent the first week determining the major components of the project. During this time, we decided what to purchase and what the end product would look like. Each week thereafter, we came together to determine what would be best to work on next and split the workload according to team member preferences. I was most interested in learning about machine learning models, so I focused on researching possible development frameworks, while others focused on 3D modeling and circuit design. The system's block diagram and disassembly can be seen below.

<div class='row'>
  <div class='two-images'>
    <img src='/images/bike-alert-block-diagram.jpg' alt='diagram showing system interconnections' style='width:100%'>
  </div>
  <div class='two-images'>
    <img src='/images/bike-alert-disassembled.jpg' alt='gray open box with mess of wires and electronics inside' style='width:100%'>
  </div>
</div>
<br/>
Attached to the face of the device are the camera and the piezoelectric buzzer, and laying atop the Pi is the ultrasonic distance sensor. The battery sitting below serves as the system's power supply.

In my research, I found a promising open-source library called OpenCV. I even found examples of it being used to perform object detection. Unfortunately, the model was meant to run on more powerful machines, and the Raspberry Pi model 3B+ could not process the images at an adequate rate (one frame every few seconds). We were out of time and ended the course wanting more out of the project, but we were happy to learn so much about working as a team and learning independently.

Coming into the project, our group had little to no experience working with Raspberry Pi, Linux distributions, machine learning models, or 3D printing. There were a lot of hurdles to get over, and by meeting every week to determine the best course of action as a group, we learned a lot from the experience.

Teammates: <a href="https://www.linkedin.com/in/robert-tronnier-2ba4a5172/" target="_blank">Robert Tronnier</a>, <a href="https://www.linkedin.com/in/troy-odegaard-217698192/" target="_blank">Troy Odegaard</a>

Post-project
-----
After the course ended, I wanted to see the project through to a more useful state. I eventually came across a framework called TensorFlow Lite that was developed for embedded devices like the Raspberry Pi. As soon as I could, I purchased the most powerful new Raspberry Pi, the model 4B with 8 GB of RAM, and started coding. I based my code on an <a href="https://github.com/EdjeElectronics/TensorFlow-Lite-Object-Detection-on-Android-and-Raspberry-Pi/blob/master/Raspberry_Pi_Guide.md" target="_blank">example</a> that uses a Raspberry Pi to perform object detection at much faster speeds than before.

Connected to the Pi is Google's Coral USB Accelerator. The accelerator uses <a href="https://cloud.google.com/edge-tpu" target="_blank">Google's Edge TPU processor</a> which processes deep learning models <a href="https://cloud.google.com/blog/products/ai-machine-learning/what-makes-tpus-fine-tuned-for-deep-learning" target="_blank">much faster than a CPU or a GPU</a>. With it, we increase the number of frames the Pi can process from 5 to 30 frames per second. The human detection model used is <a href="https://www.tensorflow.org/lite/models/object_detection/overview" target="_blank">Google's sample TensorFlow Lite object detection model</a> that has been compiled to run on the Coral USB Accelerator.

See my GitHub repository <a href="https://github.com/noahcoleman42/BikeAlert" target="_blank">here</a>.

For more information
-----
* <a href="https://www.tensorflow.org/lite" target="_blank">See TensorFlow Lite documentation</a>
* <a href="https://github.com/tensorflow/examples/tree/master/lite/examples/image_classification/raspberry_pi" target="_blank">See official TensorFlow Lite on Raspberry Pi example</a>
