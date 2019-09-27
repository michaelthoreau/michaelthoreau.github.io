---
layout: page
title: Projects
---

## 2019

**Self-Supervised feature learning in video - In Progress** <br />
One of my major projects of 2019; I'm working with some great people at CSIRO including the project's supervisor [Peyman Moghadam](https://scholar.google.com/citations?user=QAVcuWUAAAAJ&hl=en), on self-supervised learning. Our aim is to adapt tasks such as object detection to new domains by learning correspondence from unlabelled videos. We are building on the works of [Wang et al.](https://arxiv.org/pdf/1903.07593.pdf)

![Learning Correspondence via Cycle-Consistency](../img/timecycle.jpg)


---
<br />
<br />

**Removing the burden of controlling for time in espresso coffee extraction** <br />
Making the perfect shot of espresso coffee is a semi-scientific persuit that combines well through numerous iterations with the other persuits of engineers. Below are the major variables in my opinion, with their most significant influences alongside. The aim is to control these variables to achieve a consistent 30-50ml shot of coffee extracted evenly over 25-35 seconds (approximate numbers).

* Beans - Roasting Quality and timing of consumption is everything, origin may have some effect too.
* Grind - Major variable affecting flow rate.
* Pressure - Most machines have a maximum output pressure, typically **9 PSI**.
* [Tamping force](https://www.youtube.com/watch?v=AvKqcgweUSk) - along with grind, affects flow rate and flow distribution.
* Extraction Time - Ideally 25-35 seconds, is there a better way than counting?

![Coffee Timer](../img/coffee_timer.jpg){: width="300px"}

To control for this last variable, I designed and built an automatic timer, it processes accelerometer signals in the fourier domain to robustly estimate the start and end of the extraction. The vibrations sensed vary with each machine, so the detection is tailored to look for any salient high-frequency signal. It has, approximately, a two year batttery life with a user-replaceable 2032 coin cell battery. To reduce device thickness the battery positive terminal is connected to the stainless steel case, with the negative terminal as a spring-loaded contact on the PCB. The device attaches magnetically to the front of the machine and is approximately the thickness of a modern iPhone.

![Construction Secrets](../img/timer_construction.jpg){: width="500px"}

---
<br />
<br />





**Simple 2D traversibility map from Lidar Point Clouds** <br />
To enable route planning over pre-mapped environments, I developed a simple obstacle detection process to work on LiDAR point clouds, like in the example below. 

![Point Cloud](../img/point_cloud.jpg){: height="250px"}

I used am assumption world was sensed from above e.g. from a [ground vehicle](https://scholar.google.com/citations?user=QAVcuWUAAAAJ&hl=en) in this case. With this simplification, I used a spatial filter on a height map generated from the highest points in each pixel. With a few heuristics and a hand tuned gradient threshold, a map is generated for navigation:

![Point Cloud](../img/obstacles.jpg){: height="250px"}

---
<br />
<br />


**Learning to Fly - and relating this hobby to robotics** <br />
Learning to fly light aircraft has given me a huge appreciation for simple and robustly engineered solutions. Just like in aircraft operations, having a deeper understanding of the systems inside the black boxes we work with may be valuable for safer robotics. An upcoming trend in deep learning is encorporating bayesian processes within neural networks, with [bayesian deep learning](https://medium.com/neuralspace/bayesian-neural-network-series-post-1-need-for-bayesian-networks-e209e66b70b2), posterior uncertainty can give us a peek inside the box for a given example.

![Me in a borrowed 172](../img/zoom.jpg){: width="300px"}

* Complete:
   - First Solo
   - Recreational Pilots License (RPL) Theory Exam
* Next:
   - RPL Practical Exam
   - PPL Exams
   - Instrument rating

---
<br />
<br />


## 2018

**The Most Accurate Pedestrian Counter in the World\*** <br />
My first major project as a freshly graduated engineer was to count pedestrians entering and exiting a hazardous industrial area. Current solutions were found to be unsuitable, so I developed a system to detect, track, and count pedestrians using a top-down camera.

![Top down pedestrian tracking and counting](../img/count.jpg)

I designed a 'fully convolutional' neural network to detect pedestrians, in the presence of significant industrial equipment movements. The network predicts points as a opposed to more typical bounding boxes, allowing for a far smaller and faster detector, running at over **60FPS**. I worked closely with the very talented [Lachlan Tyschen-Smith](https://scholar.google.com.au/citations?user=Lcv38FAAAAAJ&hl=en) at CSIRO in Canberra, Australia, on incremental hard-example mining. With incremental learning, the detector's weaknesses  were corrected with minimal labelled examples. With the addition of a kalman filter and a [Siamese Re-Identification Network](https://arxiv.org/pdf/1806.07592.pdf), we were able to reach a counting accuracy of **99.7%** over the period of a month. I learned a valuable lesson on the behaviours of people in this project, we saw that people, given time, will generate any edge case that hasn't been considered or learnt.

![Umbrella Detector](../img/umbrella.jpg){: width="300px"}

**\*Be careful with accuracy claims, all claims are data dependant and machine learning systems generally do not adapt well to new situations**

---
<br />
<br />


## 2017


**Bruxism Monitoring - More Data means More Solutions?** <br />
Surely the reason medical monitoring equipment is so expensive is the high sensor costs? This is almost certainly not the case, medical devices are very expensive, but likely due to high both R&D costs and exorbitant certification requirements.

![My data gathering device](../img/bruxism.jpg){: width="500px"}

Lighter weight and lower power sensors however, can mean less obtrusive monitoring devices capable of longer-term data recording. These are very desirable requirements for long term high-resolution sleep monitoring.

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

The complex interfacing between the FPGA fabric, the front-end ADC and the linux kernel taught me a huge amount about computer architecture and memory, however I would avoid this work for a research project if given a second go. [Here](https://link.springer.com/content/pdf/10.1007%2Fs42401-019-00026-w.pdf) is an example of a modern  machine learning method for source localisation, a brilliant high resolution Angle of Arrival (AoA) estimation method worth knowing about is the [MUSIC](https://en.wikipedia.org/wiki/MUSIC_(algorithm)) algorithm. This research has grown significantly recently, along with the rise of circular speakers with inbuilt assistants.





