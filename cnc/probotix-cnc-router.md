---
description: Probotix Asteroid - GX3725
---

# Probotix CNC Router

![](../.gitbook/assets/IMG\_20190827\_191941.jpg)

<div align="left">

<img src="../.gitbook/assets/CNC_router_rotary_axis (1).jpg" alt="">

</div>

## Useful Links

[Product Page](https://www.probotix.com/CNC-ROUTERS/CNC-ROUTER-GX3725)

[Getting Started Guide](https://drive.google.com/open?id=1w\_1fAvfdo5E\_BJbUVDhZ0cz-6\_iwIFR7)

[Recommended Maintenance](https://www.probotix.com/wiki/index.php/Maintenance)

[RCL Router Training Videos on Youtube](https://www.youtube.com/playlist?list=PLcwu5-Mumv-a1A\_1BLDorSAILYLmQ7sUR)

## Recommended Materials

* Wood
* Aluminum
* Plastics
* Foam

## Recommended Bits

### Wood

* [**Surfacing Planing Tool**](https://www.amazon.com/gp/product/B07BF5ZHD1/ref=ppx\_yo\_dt\_b\_asin\_title\_o03\_s00?ie=UTF8\&psc=1)

### Aluminum

#### Square End

* [1/16" Dia x 1/4" LOC x 1-1/2" OAL Carbide 2 Fl Uncoated Single End 30° Hlx Finishing SQ EM](https://www.fastenal.com/products/details/0321346)
* [1/8" Dia x 1/2" LOC x 1-1/2" OAL Carbide 2 Fl Uncoated Single End 30° Hlx Finishing SQ EM](https://www.fastenal.com/products/details/0321350)
* [1/4" Dia x 3/4" LOC x 2-1/2" OAL Carbide 2 Fl Uncoated Single End 30° Hlx Finishing SQ EM](https://www.fastenal.com/products/details/0321358)

#### Ball End

* [1/4" Dia x 1-1/8" LOC x 3" OAL Carbide 2 Fl Bright Finish 30° Hlx Finishing BN EM](https://www.fastenal.com/products/details/0321512)
* [1/2" Dia x 1" LOC x 3" OAL Carbide 2 Fl Bright Finish 30° Hlx Finishing BN EM](https://www.fastenal.com/products/details/0321474)

## Technical Specifications

|                    |                                                                        |
| ------------------ | ---------------------------------------------------------------------- |
| **Work Envelope**  |                                                                        |
| X Travel           | 37+ Inches                                                             |
| Y Travel           | 25+ Inches                                                             |
| Z Travel           | 5+ Inches                                                              |
| **Performance**    |                                                                        |
| Maximum Speed      | 200 Inches Per Minute (per axis), 330 Inches Per Minute (combined)     |
| Resolution         | 0.00125 Inches                                                         |
| **Mechanical**     |                                                                        |
| Drive Mechanism    | 1/2" 5-Start ACME Screws w/ Anti-backlash Nuts                         |
| Linear Rails       | 16mm Fully Supported Rails on X & Y Axis, 16mm Open Rail on Z Axis     |
| Machine Frame      | 3060M Aluminum T-slot Extrusion                                        |
| **Electrical**     |                                                                        |
| Control System     | Unity CNC Controller (5x 4.2Amp Bi-polar Drivers), LinuxCNC Control PC |
| Power Requirements | 10A@110VAC for Control System, 20A@220VAC for optional VFD Spindle     |

## 1.5KW VFD, Variable Frequency Drive (KL-VFD15), 110VAC input

**Product Description**

Led Display

Input: 110VAC ±15%  1 or 3 phase (R,S or R, T or S,T)    50/60Hz

Output: 110VAC 3 Phase (U,V,W)  1.5KW

Frequency Range: 0.1-400Hz

0-10V Analog interface capability

Variable speed potentiometer

**VFD Parameter set:**

PD000=1 for Parameter unlock ( 1 ) for Parameter Lock

PD001=1 (1 For Remote Control)

PD002=1 ( 1 For 0-10v Terminal Control or Remote Trim Pot Control ) ( J1 Also Needs to be set for Terminal Control )

PD003=400

PD004=400

PD005=400

PD007=20

PD008=120 (Motor Rated Voltage, If you have 120v spindle then set to 120v )

PD009=15

PD010=8

PD011=120 ( 100 Minimum Setting with Quality VFD, 120 is Safe)

PD13= 08 is for Factory reset, Only use this to set VFD to Factory Default Settings

PD014 Acceleration=12 ( Adjust to suit)

PD015 Deceleration=12 (Adjust to suit) ( PD15 is ignored IF PD26=1 Then the Spindle will Coast to a Stop)

PD141=120 ( Motor Rated Voltage ) (120 for VFD Rated for 120v )

PD142= 7\
PD142=( 220vSet for your motor Amp Rating 2.2Kw Spindle 9 amp )\
PD142=( 220VSet for your motor Amp Rating 1.5Kw Spindle 7 amp )\
PD142=( 220v Set for your motor Amps Rating 800w Spindle 4 amps )\
PD142=( 120v Set for your motor Amp Rating 800w Spindle 7 amp )

PD143=2 ( Motor Number of Poles)

PD144=3000 (Max Motor RPM) =3,000= (24,000)

PD70=0 ( This may need to be set to 1 if Control Voltage is 0-5v )

PD72=400

PD73=120 ( 100 Minimum Setting )

**Manuals & Downloads**\
[VFD User Manual (1708 downloads)](http://www.automationtechnologiesinc.com/download/17521/)\
Thanks to our customer.

