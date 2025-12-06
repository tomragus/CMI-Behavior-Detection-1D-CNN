# CMI-Behavior-Detection-1D-CNN
This is a neural network that classifies and distinguishes behaviors using sensor data collected from a worn wrist device. Created for the Child Mind Institute "Detect Behaviors with Sensor Data" Kaggle competition, [which is linked here](https://www.kaggle.com/competitions/cmi-detect-behavior-with-sensor-data)

Submission notebook on Kaggle:

**✎  Overview:**

Have you ever wondered what makes someone tick? How about, what *is* a tick? This interesting problem from the Child Mind Institute asks us to investigate Body-Focused Repetitive Behaviors (BFRBs) such as nail-biting, hair-pulling and skin-picking, in an effort to better understand how they relate to Obsessive Compulsive Disorder (OCD). 

In a month-long research study conducted by the institute, 81 subjects (children and adults) were given a wrist device (developed by CMI, called "Helios") to wear for an extended period of time. While wearing the device, they were instructed to perform 18 different gestures from 1-4 sitting positions including sitting, sitting while leaning forward with their non-dominant arm resting on their leg, lying on their back, and lying on their side. [Gesture example video](https://youtu.be/WJVFUSJm4As?si=2XfSJGNk4j3Lja4D)

**✎  Data and Task:**

Among these gestures, there were 8 gestures classified as "BRFB-like", and 10 gestures classified as "non-BFRB-like", where BFRB-like gestures being linked to OCD.

In this competition, the Child Mind Institute has tasked the Kaggleverse with building a predictive machine learning model that correctly classifies sequences as one of these 18 gestures. The data is made up of over 1,000 sequences, recorded using the Helios device, with 15-700 observations each being recorded at 10 Hz.

The Helios device recorded 3D acceleration data (in x/y/z directions), orientation data (with w/x/y/z quaternions), temperature (through 5 different sensors), as well as 5 sets of "time-of-flight" data. The acceleration and orientation components are a cateogry of feature commonly referred to as Inertial Measurement Units (IMU), and I will refer to them this way throughout this notebook. If you'd like to read more about the specific sensors used in this study, you can do so below.

- [Accelerometer](https://fcon_1000.projects.nitrc.org/indi/cmi_healthy_brain_network/Competitions/Helios2025/IMU_Sensor.pdf)
- [Temperature](https://fcon_1000.projects.nitrc.org/indi/cmi_healthy_brain_network/Competitions/Helios2025/Thermopile_Sensor.pdf)
- [Time-of-Flight](https://fcon_1000.projects.nitrc.org/indi/cmi_healthy_brain_network/Competitions/Helios2025/Time_of_Flight_Sensor.pdf)

**✎  Gestures:**

*BFRB:*
Above ear - Pull hair, Forehead - Pull hairline, Forehead - Scratch, Eyebrow - Pull hair, Eyelash - Pull hair, Neck - Pinch skin, Neck - Scratch, Cheek - Pinch skin

*non-BFRB:*
Drink from bottle/cup, Glasses on/off, Pull air toward your face, Pinch knee/leg skin, Scratch knee/leg skin, Write name on leg, Text on phone, Feel around in tray and pull out an object, Write name in air, Wave hello

**✎  Credit:**

I would like to thank Ted Kyi and Ryan Chesler from the [San Diego Machine Learning](https://www.meetup.com/san-diego-machine-learning/) group for their help and guidance in tackling this problem, and more generally for the service they are doing for the San Diego community by teaching this useful skill to the public free of charge.

*Most of this project was built on another repo, but on account of the version control becoming a total unworkable disaster (still in the learning phase of Git) I came to the unfortunate conclusion that the only path forward was to nuke the repo and import all of my work to a new one.*
