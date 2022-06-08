---
description: 80 watt CO2 Laser
---

# BFL Laser

![](<../.gitbook/assets/BFL Laser.jpg>)

## Useful Links

* [**User Manual**](https://drive.google.com/file/d/0BysG132m5sYncWg0Y1Z1M2hjTjA/view?usp=sharing)****
* ****[**Lightburn Documentation**](https://github.com/LightBurnSoftware/Documentation/blob/master/README.md)****
* ****[**Lightburn Forum**](https://forum.lightburnsoftware.com/)****
* ****[**Controller manual**](https://img.banggood.com/file/products/20170110002219AWC708CPLUS%20LCD%20Display%20Operation%20Manuals-1-25%20\(1\)-2-25%20\(2\).pdf)****

{% content-ref url="bfl.md" %}
[bfl.md](bfl.md)
{% endcontent-ref %}

****

## **Maintenance**

![](<../.gitbook/assets/image (100).png>)

* [Focus lens Oring 20mm diameter](https://www.amazon.com/dp/B07MY2YBKL/ref=cm\_sw\_r\_cp\_apa\_i\_u9HjEbS4N5DD2)

## Exhaust

We use a [Zoom W4L](https://zoomblowers.com/w4l-750-watt-zoom-blower.html) bouncy house fan for the exhaust. It boasts an insane amount of CFM (around 1300) in a small and relatively quiet package.

What makes this fan great is that just about every part on this fan is user serviceable with replacement [parts available from the manufacturer](https://zoomblowers.com/air-blowers/res-inflatable-blowers)

Before you question this decision over the obvious static pressure concerns, this decision was based off a [reddit thread](https://www.reddit.com/r/lasercutting/comments/5f0wmn/on\_extraction\_fans/) which said these fans are engineered to work under static pressure (kids bouncing in a bouncy house) and will actually burn out if they don't have that pressure. So far the random internet engineer seems to be correct in his findings!

![Off the shelf HVAC ducting was used to create an input and output adapter for the fan](<../.gitbook/assets/image (63).png>)

### Assembly

We used a [6" Ducting End Cap](https://www.lowes.com/pd/IMPERIAL-6-in-dia-Galvanized-Steel-Round-End-Cap/3711202) for the output. We removed the stock endcap of the fan, cut a similar diameter hold in the hvac endcap, then drilled 4 matching holes to mount the new cap in place of the original one.

![output adapter](<../.gitbook/assets/image (66).png>)

We used a [7.5" to 6" airtight adhesive duct take off ](https://www.lowes.com/pd/IMPERIAL-7-5-in-x-3-25-in-Galvanized-Steel-Airtight-Adhesive-Duct-Take-Off/1000228293) to attach the input side of the fan. We then used a standard 6" to 4" reducer to match our existing exhaust piping.

![input adapter](<../.gitbook/assets/image (65).png>)

Seal all mating surfaces with HVAC foil ducting tape to eliminate any air leaks

### Smoke Test

{% embed url="https://youtu.be/fq3A0CHQAbs" %}





## Specifications

* Power: 80 watt CO2
* Working area: 900mm x 1200mm (36" x 48")
* Speed: X: 900mm/s, Y: 500mm/s
* Based on: Light Objects XLE1200 X-Y Stage
* Custom built by: River City Labs

## **Operation**

1. Use a vector graphics program such as Adobe Illustrator or Inkscape to create the object that you want to cut. You may also use the Lightburn software on the RCL laser computer to create the object.
2. Turn on the System switch on the BFL. The laser will home in the upper right corner and then return to the last saved origin point. The control display will say “Continue to work after Powercut ?” Press ESC to dismiss.
3. Sign in to the RCL laser computer. Check the #laser-cutter slack channel description for the password.
4. Open the Lightburn application and import the file you created in step 1. You can also import picture objects. Lightburn supports the following file types: svg, ai, pdf, dxf, hpgl, lt, png, jpg, bmp.
5. Define layers and power, speed and type of cut for each layer using the Lightburn software. Make any adjustments needed to the file and save it as a .lbn file.
6. Set the Lightburn coordinate system to use “Current Position” and set the job origin to the lower right. **DO NOT** change the Device (machine) origin in Lightburn. This will always be the upper right for the BFL.
7. Click on the “Send” button to send your file to the BFL. Put in whatever name you want.
8. Go to the BFL. You will see the name and outline of the file you sent to the laser.
9. Place the material to be cut on the laser bed.
10. Use the arrow keys on the laser control to move the laser to the area on your material where you want to start the cut.
11. Press the Origin button.
12. Press the Box button. The laser will move to define the area of your cut.
13. If everything looks OK, close both of the lids. Turn on the Laser, Exhaust and Air switches.
14. Make sure the laser chiller is turned on.
15. Make sure the water valves to the laser are open.
16. Note the locations of the emergency stop button and fire extinguishers.
17. Press the Start button on the laser control to begin the cut.
18. STAY AT THE LASER until the cut is complete.
19. When the cut is complete, clear away any material from the laser bed.&#x20;
20. Turn the System, Laser, Exhaust and Air switches off. **DO NOT TURN OFF THE CHILLER.**
21. Clean the laser lens.
