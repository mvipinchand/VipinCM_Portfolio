---
title: "Left Ventricular Assist Device (LVAD)"
description: "Levitation, Drive Electronics & Monitoring of a Left Ventricular Assist Device (LVAD) in collaboration with Inertial Systems Unit of Indian Space Research Organisation"
dateString: June 2021
draft: false
tags: ["AWS", "RegEx", "MkDocs", "GitHub Action", "Docker", "Bash", "TypeScript", "Node.JS"]
weight: 201
cover:
    image: "/projects/LVAD/Results.jpeg"
---

## Intro
In my video about [**How we designed and developed our 3rd gen LVAD**](https://www.youtube.com/watch?v=Lj_ukoOZl54), 
Left Ventricular Assist Device (LVAD) is a surgically implantable mechanical pump for Heart failure (HF) which is a frequent cause of inpatient admissions, for patients who have reached end-stage systolic heart failure. It augments blood flow to the body and shares the workload of the Left Ventricle. Apart from the apparent advantage of not having to wait for a suitable donor, there are several advantages to using an LVAD. For instance, unlike cadaver transplants that require the intake of immuno-suppressants, to facilitate organ acceptance, patients with the implanted device need to take only one simple blood-thinning medicine to ensure the free flow of blood.

![my notes](/projects/LVAD/lvad.jpg)


## Motivation
The number of people diagnosed with heart failure is increasing and projected to rise by 46 percent by 2030, resulting in more than 8 million people with heart failure, according to the American Heart Association’s 2017 Heart Disease and Stroke Statistics. Cardiovascular diseases including coronary artery disease, high blood pressure and stroke collectively remain the leading cause of death in the world. One way to get the heart back into a healthy rhythm, and help one get back to a normal routine, is with an implanted LVAD. However, the main drawback of the LVADs currently available in the market is their cost. Hospitals pay a range of prices around $80,000 for a HeartWare device, while the HeartMate III runs closer to $95,000. The average total cost to implant an LVAD was $175,000 (more than double the cost of a heart transplant), which is not a ordable for the common man. This was our motivation to accept the opportunity to work as a part of the project by ISRO Inertial Systems Unit (IISU) for developing cheaper and more effcient third-generation LVADs.

## Working
The magnetic and hydrodynamic levitation of the impeller without any contact bearings with the pump is the major advancement of the third-generation pumps. Earnshaw’s theorem states the condition for instability in magneto static inverse square fields. Its practical consequence as applied to paramagnetic material is that external stabilizing means must be provided in at least one coordinate direction. A completely passive and contactless magneto static bearing, stable in all 6 degrees of freedom (DOF), cannot be realised under normal conditions. In practice, at least one axis has to be controlled actively by means of electromagnets. Preference was given to the 2 DOF options where the wheel is actively controlled along two orthogonal radial directions where axial movements and all other degrees of rotor freedom are passively controlled by means of permanent magnets, except for the rotor spin. The next step is to create a neural network that will learn to model how the magnet changes position. Two-layer NARX (nonlinear autoregressive with external input) neural networks can fit any dynamical input-output relationship given enough neurons in the hidden layer.

![published notes](/projects/LVAD/levitation.jpg)

Drive Electronics of the LVAD system was implemented by designing a PCB consisting of the DRV10983-Q1 motor driver and MSP430G2553 MCU intefaced together, to drive either a brushless DC electric motor (BLDC motor) or a permanent magnet synchronous motor (PMSM) which has ability to provide Torque (BEMF constant) > 30 mN, in the speed range of 1800-4000 rpm with an accuracy of +- 2 rpm. Only such a motor will be able to overcome both the Cogging Torque and friction due to blood flow. The design also provides access to proprietary sensorless control (unlike the normal ones using Hall sensors for position tracking) and the ability to tune motor parameters for optimizing performance according to the end-application needs.

![published notes](/projects/LVAD/lvad1.jpg)

We intend to have a miniature monitoring system to monitor the important health parameters of the LVAD, such as battery percentage indication, speed (rpm), power and levitation status. It also includes necessary alarm signals using a buzzer in case it overrides the specified limit set on the levitation alignment. OLED Graphic Display interfacing with MSP-EXP430G2 TI Launchpad is used under this section as it involves least power consumption, which is one of the major constraint in our application.


## Future Scope
Minimally invasive LVAD surgery will be made possible by newer surgical techniques focusing on two main areas: less-invasive cardiac access and off-pump technique. A totally implantable LVAD system represents the next logical advancement in LVAD design wherein Thermal energy transfer system (TETS) technology or Coplanar Energy Transfer (CET) system will be been incorporated into numerous mechanical support designs. Incorporating a Distant Monitoring and Control Station (DMCS) set up would increase its acceptance not just in its native country but be viable to people across the globe. As our understanding of heart failure continues to grow, there is little doubt that LVADs will continue to play a pivotal role as a therapeutic option for those suffering from end-stage heart failure.

## Resources
- [My Youtube Glimpse](https://www.youtube.com/watch?v=Lj_ukoOZl54)
- [LVAD - GitHub](https://github.com/mvipinchand/UG-Final-Year-Project-Report)