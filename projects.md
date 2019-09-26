---
layout: page
title: Projects
---

## 2019

**Self-Supervised feature learning in video - In Progress** <br />
This is one of my major projects for 2019, however it cant be published yet.

**Less Variables, Better Coffee?** <br />
In Espresso coffee extraction, there are the following variables and their drivers:

* Beans - freshness,cost
* Grind - varies with bean
* Pressure - Fixed limit with machine
* Tamping force - 25lbs ideally, varies with arm
* Extraction Time - hmm?
* Volume fo Extraction - Varies with all other variables

![Coffee Timer](../img/coffee_timer.jpg){: width="300px"}

I made an espresso timer, it processes accelerometer signals in the fourier domain to estimate salient signals that are consistent across time. It has approximately a two year batttery life, with a user-replaceable 2032 coin cell, notice that the battery current is through the case. The device attaches magnetically to the front of the machine and is the thickness of a modern iPhone.

![Construction Secrets](../img/timer_construction.jpg){: width="500px"}

<br />
<br />

---


**Flying - How hard can it be?** <br />
Learning to fly has given me a huge appreciation for simple and robustly engineered solutions. It has also taught me the importance of understanding the systems we use i.e. what is inside the black box. An upcoming trend in deep learning is encorporating bayesian processes, with [bayesian deep learning](https://medium.com/neuralspace/bayesian-neural-network-series-post-1-need-for-bayesian-networks-e209e66b70b2), posterior uncertainty can give us a peek inside the box for a given example.

![Me in a borrowed 172](../img/zoom.jpg){: width="300px"}

Engineering and flying make great parallel persuits, with engineering giving a head start on topics such as radio comms, aerodynamics and procedural efficency coming from the practicalities of flight safety.

* Complete:
   - First Solo
   - Recreational Pilots License (RPL) Theory Exam
* Next:
   - RPL Practical Exam
   - RPL Navigation Endorsment
   - Controlled Airspace Endorsment
   - PPL Exams
* After:
   - Instrument rating (ASAP)

<br />
<br />

---

**Simple 2D traversibility map from Lidar Point Clouds** <br />


![Point Cloud](../img/point_cloud.png){: height="250px"}

Explaination coming soon.

![Point Cloud](../img/obstacles.jpg){: height="250px"}
<br />
<br />

---


## 2018

**The Most Accurate Pedestrian Counting System in the World\*** <br />
My first major project as a freshly graduated engineer was to accurately count pedestrians entering and exiting a hazardous industrial area. Current solutions were not suitable to the situation, so I developed a system to detect and count pedestrians using a top-down camera.

![Top down pedestrian tracking and counting](../img/count.png)

I designed a 'fully convolutional' neural network to detect pedestrians. The network predicted points as an output rather than bounding boxes, this allowed for a far smaller and faster detector, running at over **60FPS**. I worked closely with the very talented [Lachlan Tyschen-Smith](https://scholar.google.com.au/citations?user=Lcv38FAAAAAJ&hl=en) to do incremental hard-example mining, with all hand labelled images, meaning the detector improved over time, with minimal labelling effort. With the addition of a kalman filter and a Siamese Re-Identification Network, we were able to reach a counting accuracy of **99.7%** over the period of a month. However I learned a valuable lesson on the behaviours of people, we saw that people are the ultimate edge case generators.

![Umbrella Detector](../img/umbrella.png){: width="300px"}

**\*All Accuracy Claims are Data Dependant, other systems probably used harder data**

<br />
<br />

---


## 2017


**Bruxism Monitoring - More Data means More Solutions?** <br />
Surely the reason medical monitoring equipment is so expensive is the high sensor costs? This is almost certtainly not the case, medical devices are expensive, likely due to high both R&D costs and certification requirements.

![My data gathering device](../img/bruxism.jpg){: width="500px"}

Lightweight and low power sensors however, can lead to unobtrusive monitoring devices capable of long-term data recording. The motivation for this project was to study whether it is possible to use ML on an embedded device to capture [bruxism](https://en.wikipedia.org/wiki/Bruxism) events while a patient sleeps. Using [EMG](https://en.wikipedia.org/wiki/Electromyography) as a ground truth, it may be possible to learn a classifier that works on accelerometer data only. Pictured below is a device I designed as a research platform. It has sufficient onboard flash memory to capture Accelerometer and EMG data for several nights, to be transferred over USB upon the return of the device from the patient.    

<br />
<br />

---


## 2016


**European Student Earth Orbiter - Ground Station Antenna Control** <br />
On an exchange visit to the Technical University of Munich, I had the privilege to work in the Institute for Communications and Navigation with a Masters student, Marcus Buttke. 

![My data gathering device](../img/ESEO.png){: width="500px"}

Together we designed and implemented a vertical axis control system for a 4m s-band antenna reflector. This antenna is now used for the main high speed downlink for the [European Student Earth Orbiter](https://www.esa.int/Education/ESEO/ESEO_student_satellite_successfully_launched_to_space). A 50kg Micro-Satellite which launched successfully in Dec 2018 aboard a SpaceX Falcon 9.

<br />
<br />

---


**Microphone Array Hardware for Robotics - Thesis Project and Internship** <br />
For my undergraduate thesis I designed a new high-performance microphone array, linked directly in to a hybrid [Xilinx Zynq FPGA](https://www.aldec.com/en/company/blog/144--introduction-to-zynq-architecture) for real-time processing onboard a **robot**.

![Microphone Array](../img/Microphone_Array.jpg){: width="500px"}

The complex interfacing between the FPGA fabric, the front-end ADC and the linux kernel taught me a huge amount about computer architecture and memory, however I would avoid this work for a research project if given a second go. [Here](https://link.springer.com/content/pdf/10.1007%2Fs42401-019-00026-w.pdf) is an example of a machine learning method for source localisation. This research has grown significantly recently, along with the rise of circular speakers with inbuilt assistants. Does the Amazon Echo Dot hardeware below look familiar?

![Amazon Echo Dot PCB](../img/echo_dot.jpg){: width="500px"}



