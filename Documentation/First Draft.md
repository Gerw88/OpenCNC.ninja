##Introduction

The goal is to design and build a multi-function CNC profiling system with a cutting area of 2.44m x 1.22m x 0.15m.  The intent is to design the entire system with a minimum cost, while providing a positional accuracy of +/- 0.05 mm (.002”), and high machining speeds of up to 15 m per minute. The basis of the design will be patterned after numerous CNC Router designs (namely but not limited to, Data-Cut CNC, ShopBot Alpha, JoesCNC Evolution & MechMate). The design should incorporate interchangeable profiling heads & beds to support the profiling of both metal (using a Plasma head with Torch Height Control (THC)) and wood/non-ferrous metal/ aluminium and plastics utilizing a 2.2 -3.0KW single phase motor.

The system must cater for the occasional break-down and reassembly for relocation purposes.

##Description
A CNC machine is a system that is able to accept numerical control inputs to machine a part specified by the exact positioning of the inputs. The machine is able to accept commands through a directly connected personal computer. The personal computer communicates to the main controller subsystem through (one of the following) Ethernet, USB, or parallel link. The main controller subsystem is able to interpret and directly control movement of the attachable tool head/s. The framework of the system is set up by the mechanical subsystem which will allow for movement in the x, y, and z axes and specify spatial limitations of any acceptable job. The main controller, and mechanical subsystems are able to interact through power provided by the motor driver subsystem. The overall block diagram of the machine is pictured below.

~~image link here~~

##Subsystems


##Machine Tolerance
One of the most important considerations when designing and building the CNC router is the accuracy and precision of the machine. Don’t get accuracy and precision confused. Take a look at the illustration below.

~~image link here~~

 We want to design and build our machine to hold a certain accuracy and precision. For example, our machine may be able to cut a piece that is within 0.00254mm but the repeatability may be 0.254mm.
 
We could design and build our CNC router and live with the results, or keep adjusting to get the results we want. However, there are ways to design machine to hold a certain tolerance. For example, if we know we only need a tolerance of 0.254mm and we know that’s all we will ever need, we can save a lot of money by designing for that requirement.

On the other hand, if we want our machine to hold a tolerance of 0.00254mm repeatable, then there are some design requirements that must be met to get the required performance.

Typical self-built CNC routers hold a tolerance of 0.0254mm to 0.00254mm. However, this is up to us. At this point all we need to do is have an idea as to what kind of tolerance we require. Keep in mind the larger the machine, the more costly it is to hold tight tolerances.

##Design information review

###Introduction
The goal is to design and build a high quality CNC which can perform multiple job functions by attaching different head styles.  At the same time, the unit will have a minimum cost price point compared with other machines of similar functionality.  The areas of technology that will be covered in this review are:

- Comparison with current designs
- Mechanical Systems Review
- Drive Electronic Techniques
- Communication/Linking
- Software
- System Control

###Comparison with Current Designs

#### Data-Cut CNC Router System
####JoesCNC Evolution
####MechMate
####Solsylva

Rack and leadscrew machine with aluminum gantry and carriage. This solid machine is straightforward to build for a low cost. 
- Uses a full sized router
- Leadscrew, or rack and pinion X and Y axes
- Leadscrew Z axis
- Uses a variety of leadscrews
- Aluminum or wood for gantry and carriage
- 2x4 and 2x6 lumber for the table chassis
- Belt and pulley stepper couplings
- Printable 8.5" x 11" templates

#####Construction
These plans have hundreds of drawings and dimensioned images with detailed step by step directions for the components and their assembly. The machine can be built in a modest shop with basic tools. Though not mandatory, a table saw and drill press are helpful. The 24 x 48 inch cutting area machines have a footprint of 37 x 60 inches, and use stock sized materials efficiently. The table frame is made of standard 2x4 and 2x6 framing lumber. The gantry can be a 2x6 board or an aluminum channel. The gantry ends and Z carriage are made of stock sized aluminum flat bar or plywood. The gantry uses standard sized leadscrews or racks to give a cutting width of 24 inches. The table bed axis uses 48 inch racks and 60 inch pipe rails. These stock sizes give a cutting length of 48 inches. Directions are included for using 6 foot leadscrews. The rails’ bearings are 608 or 1603 bearings, which are inexpensive and easily found. 
#####Options
This machine is designed to allow options in materials and drive components. The gantry and carriage can be made of aluminum or wood. The X and Y axes can be driven by leadscrews or racks and pinions. The stepper to leadscrews coupling on the table bed axis can be one long belt with 1 stepper, 2 short belts with 1 stepper, or 2 slaved steppers. 
The pulleys for the leadscrew to stepper connections are common sizes, which simplifies upgrades. The machine can initially be built with inexpensive leadscrews and later be upgraded as need and budget warrant.
#####Building Cost
The price of the table will vary according to the components used. $600 is a fair expectation for the basic wooden table with All Thread leadscrews. This does not include the spindle-router, steppers, drives and power supply. 
The aluminum gantry and carriage version adds ~$190 and gives a more solid machine, which is capable of more aggressive cuts. Racks and pinions are ~$125 for the table bed axis and ~$55 for the gantry axis. The prices of the leadscrews and leadnuts can range from a few dollars for All Thread to hundreds for Acme with anti-backlash leadnuts. Stepper, drive and power supply packages start at $270. Routers start at $100.
#####Steppers and Speeds
NEMA 23 steppers move each axis. This is a standard size that is available in many stepper and drive packages. The prototype machines used the Xylotex and HobbyCNC steppers and drives with torque ranges from 269 to 425 oz.in. 
Other systems can be used. However, steppers below 269 oz.in. Are not recommended. These steppers are pushed to their upper limits on this larger and heavier machine. The XL belts used in the machine are also pushed to their limits at ~425 oz.in. The aluminum gantry and carriage can carry a full sized router. However, the steppers will not be able to push the router to its potential. They usually stall before the router does. The speeds range from 30 inches per minute with hardware store threaded rod, to 200+ ipm with multi-start Acme leadscrews or racks and pinions.
#####Scaling
Lengthening the rack table bed version of this machine is straightforward because racks, unlike leadscrews, can be abutted. The plans address using 6 foot leadscrews on the long axis. Widening the machine more than a few inches will increase the weight of the gantry, which will require more power from the steppers. The machine as designed already pushes 300 oz.in. Steppers to their upper limits. Significantly increasing the stepper sizes will load the XL belts, which will cause the belts to stretch sooner. Up-sizing the belts and pulleys will require reworking some of the machine's dimensions, which is not covered in the plans.
