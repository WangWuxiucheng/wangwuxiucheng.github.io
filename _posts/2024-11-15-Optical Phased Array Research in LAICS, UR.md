---
layout: post
title:  "Optical Phased Array Research in LAICS, UR"
date:   2024-11-15 00:00:00 -0800
transition: convex
tags: [Research]
categories: Research
---
{:refdef: style="text-align: center;"}
![LAICS Logo](/images/LAICS_Logo_Vector.svg){: width="60" }
{: refdef}

Overview of the Optical Phased Array (OPA) research in Laboratory for Advanced Integrated Circuits and Systems (LAICS) at the University of Rochester developed from 2018 to present.

---
**Table of Contents**

[Research Objective](#obj)

[Challenges](#hard)

[Project Timeline ](#hist)

[Project Demo](#demo)

- [Photonics](#SiPh)

- [Electronics](#elec)

- [Testsetup Evolution](#setupEvo)

- [Beamsteering](#steer)

- [Multiplexing](#mux)

[Acknowledgments](#ackn)

---
>**What is an OPA in one sentence?**
> 
>*A solid-state electronic-controlled high-speed beamsteering photonic circuit*.

#### Research Objective {#obj}
The objective of my research is to design optical phased array (OPA) circuits and systems capable of rapid beamsteering and efficient information transmission. While the wave diffraction and interference nature of phased arrays enable light-speed beamsteering, the design, implementation, control, and analysis of OPAs remain significant engineering challenges. Once it succeeds, it will represents a fundamental advance in **LiDAR** and **free-space optical communication**. It would also improve our abillity to precisely manipulate light beams in a finer scale, enabling new applications for sensing, 3D-printing and light-matter interactions.

#### Challenges {#hard}
OPA beamsteering requires active control and is challenging to accomplish because it demands seamless coordination between the photonic chip (PIC) and its peripherial electronics, akin to a harmonic symphony. A control program acts as a symphony conductor, guiding the system to adhere to its calibration data and steering coefficients while minimizing crosstalk within the photonic chip. Calibrations serves as the symphony's rehearsal, ensuring optimal performance, and only through the analysis program can the best  calibration data be identified during these rehearsals.

#### Project Timeline {#hist}
`2016-2019` The OPA project was first initiated and executed by Dr.Francis Smith in 2016 for OPA concept verification. I joined the group in Fall 2017 as a M.S student, worked with Dr. Smith on OPA device, circuit level simulations, electronics, test setup construction and automation. By the end of 2018, we successfully achieved OPA beamsteering and attracted funding to continue the project.

`2019-2024` Dr.Smith graduated in 2019. In January 2019, I became a Ph.D student and continued the project. I came up new ideas and tapeouted new photonic chips through various foundries(IMEC, AMF and AIM). My research focused on improving OPA system performance, such as beamsteering speed, range, accuracy, and power efficiency. Meanwhile, I developed customized electronics to scale down the whole system size from bench-top to a more portable version as well as explored OPA-based free-space optical communication.

---

#### Project Demo {#demo}

An OPA system and its beamsteering and spatical multiplexing are demonstrated in the following sections.

##### Photonics {#SiPh}
We develop our integrated OPA circuits on silicon photonics platform. Below is a 4x4 OPA that implemented subarray configuration. 

{:refdef: style="text-align: center;"}
![OPA Chip](/images/OPA Research/OPA_Chip.png){: width="480" }
{: refdef}
*Fig: (a) OPA design illustration. (b) Micrograph of the prototype OPA chip. (c) OPA aperture region.*

##### Testsetup Evolution {#setupEvo}
The PIC needs active controls for beamsteering. Two generations of benchtop test setups and two generations of OPA driver/packages were developed to integrate and control OPA PICs. The following images show the evolution of our test setups.

{:refdef: style="text-align: center;"}
![Testsetup Evolution](/images/OPA Research/Testsetup Evolution.png){: width="500" }
{: refdef}
*Fig: (a) NI-DAQ based test setup in 2018. (b)(c) NI-PXI-DAQ based test setup in 2020. (d)(e) Test setup based on customized hardware in 2022.*

`2018` 32-channel analog outputs and automation to control OPA chip.

`2020` 64-channel analog input, outputs to control OPA chip. The analog inputs serve as electrical feedbacks to enable more precise control. The system update rate is 2ms per steering.

`2021-2022` Customized hardware (driver board, MCU board) and package with 64-channel analog inputs, outputs to control OPA chip. The package is temperature controlled by a TEC unit. The MCU board allows standalone contorl or PC-control. The system update rate is 350 microseconds per steering, which is 5X+ faster than the previous system.

##### Electronics {#elec}

We developed our customized hardware as shown in the following:
{:refdef: style="text-align: center;"}
![Testsetup Evolution](/images/OPA Research/Electronics.png){: width="500" }
{: refdef}
*Fig: (a) Gen1 driver board and package in 2021. (b) Gen2 driver board and package in 2022. (c) OPA region.*

The driver board provides all the analog inputs and outputs. Digital controls and power supplies are connected through a flex-cable to the MCU board.

##### Beamsteering {#steer}

With both the photonics and electronics, we finally can perform beamforming and beamsteering.


{:refdef: style="text-align: center;"}
![4x4 OPA Beamsteering in Azimuth Direction](/images/OPA Research/OPA_4X4_Rect_AzSteer.gif){: width="240" }
![4x4 OPA Beamsteering in Elevation Direction](/images/OPA Research/OPA_4X4_Rect_ElSteer.gif){: width="240" }
{: refdef}
*Fig: OPA beamsteering in azimuth and elevation directions under the microscope.*

{:refdef: style="text-align: center;"}
![OPA Beamsteering UR Logo Gif](/images/OPA Research/OPA_Beamsteering_UR_Logo.gif){: width="120" }
![OPA Beamsteering UR Logo](/images/OPA Research/UR_Logo.png){: width="360" }
{: refdef}
*Fig: real-time OPA beamsteering under the microscope. The IR camera frame rate is "sync" to the beamsteering speed, such that the 'U' and 'R' letters are displayed.*



##### Multiplexing {#mux}


---
##### Acknowledgments {#ackn}
This research is partially supported by NSF grants ECCS-1842691 and IIS-1722847. We also acknowledge funding support by L3Harris Space and Airborne Systems and CEIS. We would like to thank J.Daniel Newman, Andrew Sacco, and Daniel Sundberg for providing resources and support to our works; Dr. Wenhui Hou, Dr. Tara Peña, and Professor Stephen Wu for PIC wirebondings; Dr. Jingwei Ling and Professor Qiang Lin for equipment; Yujia Yan and Ge Zhu for enlightening discussions; IMEC for PIC fabrication.











