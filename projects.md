---
layout: page
title: Projects
---
---

<!-- ## 2020
**NYU Rogue Aerospace apogee control drag system**


![Drag System](../img/drag_system.png)

<br />
<br /> -->

## 2019

**Self-Supervised from video** <br />
One of my major projects of 2019; working with some great people at CSIRO on the topic of self-supervised learning. Our aim was to adapt tasks such as object detection and action recognition to new domains by learning from from unlabelled videos. We built on top of works such as that of [Wang et al.](https://arxiv.org/pdf/1903.07593.pdf). Our team was successful in building a model to learn temporally coherent representations from unlabelled videos. Preliminary results are documented [here](https://arxiv.org/pdf/2004.02753.pdf).

![Learning Correspondence via Cycle-Consistency](../img/timecycle.jpg)


---
<br />
<br />

**Removing the burden of controlling for time in espresso coffee extraction** <br />
Making the perfect shot of espresso coffee is a semi-scientific persuit that combines well through numerous iterations with the other persuits of engineers. Below are, in my opinion, the major variables affecting the quality of an espresso coffee shot, with the most significant influences for each variable alongside. The aim is to control these variables to achieve a consistent 30-50ml shot of coffee extracted evenly over 25-35 seconds (approximate numbers).

* Beans - Roasting Quality and timing of consumption is everything, origin may have some effect too.
* Grind - Has the largest affect on flow rate.
* Pressure - Most machines have a maximum output pressure, typically **9 PSI**.
* [Tamping force](https://www.youtube.com/watch?v=AvKqcgweUSk) - along with grind, affects flow rate and flow distribution.
* Extraction Time - Ideally 25-35 seconds, is there a better way than counting in your head?

![Coffee Timer](../img/coffee_timer.jpg){: width="300px"}

To control for this last variable, I designed and built an automatic timer. The device processes accelerometer signals in the fourier domain to robustly estimate the start and end of the extraction. Vibration signals vary with each machine, so detection is tailored to look for **any** salient high-frequency signal. The battery life is approximately two years, with a user-replaceable 2032 coin cell battery. To reduce the thickness of the device, the battery positive terminal is connected to the stainless steel case, with the negative terminal as a spring-loaded contact on the PCB. The device attaches magnetically to the front of the machine and is approximately the thickness of a modern iPhone.

![Construction Secrets](../img/timer_construction.jpg){: width="500px"}

---
<br />
<br />





**Generating 2D traversibility maps from Lidar Point Clouds** <br />
To enable route planning over pre-mapped environments, I developed a simple obstacle detection and traversability method for processing LiDAR point clouds, like in the example below. 

![Point Cloud](../img/point_cloud.jpg){: height="250px"}

I used a simplifying assumption that the world was sensed from above, in this case from an autonomous [ground vehicle](https://scholar.google.com/citations?user=QAVcuWUAAAAJ&hl=en). With this simplification, I designed a spatial filter to work on a height map generated from the highest points in each pixel in an x,y grid. With a few heuristics and a hand tuned gradient threshold, a robust map is generated for navigation:

![Point Cloud](../img/obstacles.jpg){: height="250px"}

---
<br />
<br />


**Learning to Fly - and relating this hobby to robotics** <br />
Learning to fly light aircraft has given me a huge appreciation for simple and robustly engineered solutions. Just like in aircraft operations, having a deeper understanding of the systems inside the black boxes we work with may be valuable for safer robotics. An upcoming trend in deep learning is encorporating bayesian processes within neural networks, with [bayesian deep learning](https://medium.com/neuralspace/bayesian-neural-network-series-post-1-need-for-bayesian-networks-e209e66b70b2) posterior uncertainty can give us a peek inside the big black box that is deep learning.

![Me in a borrowed 172](../img/zoom.jpg){: width="300px"}

* Complete:
   - Recreational Pilots License
* Next:
   - PPL Exams
   - Instrument rating

---
<br />
<br />


## 2018

**The Most Accurate Pedestrian Counter in the World\*** <br />
My first major project as a freshly graduated engineer was to count pedestrians entering and exiting a hazardous industrial area. Current solutions were found to be unsuitable, so I developed a system to detect, track, and count pedestrians using a top-down camera.

![Top down pedestrian tracking and counting](../img/count.jpg)

I designed a 'fully convolutional' neural network to detect pedestrians in the presence of complex industrial equipment. The network predicts points as a opposed to more typical bounding boxes, allowing for a far smaller and faster detector, running at over **60FPS**. I worked closely with the very talented [Lachlan Tyschen-Smith](https://scholar.google.com.au/citations?user=Lcv38FAAAAAJ&hl=en) at CSIRO in Canberra, Australia. Incremental learning and hard example mining meant the detector's weaknesses were corrected over time with minimal extra labelling of examples as the system adapted to the environment. With the addition of a kalman filter and a [Siamese Re-Identification Network](https://arxiv.org/pdf/1806.07592.pdf), we were able to reach a counting accuracy of **99.7%** over the period of one month. I learned a valuable lesson on the behaviours of people in this project. We saw that people will generate almost any edge case imaginable, such as continuing to use an umbrella indoors as seen below.

![Umbrella Detector](../img/umbrella.jpg){: width="300px"}

**\*Be careful with accuracy claims, all claims are data dependant and machine learning systems generally do not adapt well to new situations.**

---
<br />
<br />


## 2017


**Bruxism Monitoring - More Data means More Solutions?** <br />
Surely the reason medical monitoring equipment is so expensive is the high sensor costs? This is almost certainly not the case, medical devices are very expensive, but likely due to high both R&D costs and exorbitant certification requirements.

![My data gathering device](../img/bruxism.jpg){: width="500px"}

Lighter weight and lower power sensors however, can mean less obtrusive monitoring devices, capable of longer-term data recording. These are very desirable features for long-term high-resolution sleep monitoring.

The motivation for this project was to study whether it is possible to use machine learning on an embedded device to capture [bruxism](https://en.wikipedia.org/wiki/Bruxism) events while a patient sleeps. Using [EMG](https://en.wikipedia.org/wiki/Electromyography) as a ground truth, it may be possible to learn a classifier that works on accelerometer data only, hence reducing power consumption during monitoring. Pictured above is a device I designed as a research platform. It has sufficient onboard flash memory (512 mb) to capture Accelerometer and EMG data for several nights, to be transferred over USB upon the return of the device from the patient.    

---
<br />
<br />


## 2016


**European Student Earth Orbiter - Ground Station Antenna Control** <br />
On an exchange visit to the Technical University of Munich, I had the privilege to work in the Institute for Communications and Navigation in conjunction with [DLR](https://www.dlr.de/EN/Home/home_node.html) along side a german Masters student and good friend, Marcus Buttke. 

![My data gathering device](../img/ESEO.jpg){: width="500px"}

Together we designed and implemented a vertical axis control system for the above 4 meter s-band antenna reflector. This antenna is now used for the main high speed downlink for the [European Student Earth Orbiter](https://www.esa.int/Education/ESEO/ESEO_student_satellite_successfully_launched_to_space). A 50kg Micro-Satellite which launched successfully in Dec 2018 aboard a SpaceX Falcon 9.

![System Dynamics](../img/combined.png){: width="650px"}


---
<br />
<br />


**Microphone Array Hardware for Robotics - Thesis Project and Internship** <br />
For my undergraduate thesis I designed a new high-performance microphone array, linked directly to a hybrid [Xilinx Zynq FPGA](https://www.aldec.com/en/company/blog/144--introduction-to-zynq-architecture) for real-time processing onboard a **robot**.

![Microphone Array](../img/comparison.jpg){: width="700px"}

The complex interfacing between the FPGA fabric, the front-end ADC and the linux kernel taught me a huge amount about computer architecture and memory, however I would avoid this work for a research project if given a second go. [Here](https://link.springer.com/content/pdf/10.1007%2Fs42401-019-00026-w.pdf) is an example of a modern  machine learning method for source localisation. A brilliant high resolution Angle of Arrival (AoA) estimation method worth knowing about is the [MUSIC](https://en.wikipedia.org/wiki/MUSIC_(algorithm)) algorithm. This research has grown significantly recently with the rise of circular voice assistant speakers, such as the Amazon Echo Dot seen alongside my hardware above.





