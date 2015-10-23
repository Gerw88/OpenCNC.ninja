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

####Shopbot
The ShopBot design approach:
As we consider our table and bed design, we need to seriously evaluate the approach taken by ShopBot (as we can see from the machine here in the FABLAB).

Light but Stiff
From a machining point of view, it is always better to be heavier.  Weight provides substance, mass and rigidity. These factors lead to smoother cutting, but these factors also lead to higher costs, because all aspects of the motion system must be beefier. The drive system -- motors and their electronics -- are a particular challenge because their costs increase exponentially with the mass of the system they need to move.

In addition, there is a practical problem with heavy.  It makes the tool less portable, more limited in the locations in which it can be positioned or moved, and considerably less friendly for small shops.  These limitation do not fit well into the emphasis on flexibility and lean production techniques, which emphasize the importance of being able to readily reconfigure production flow and processes.  Lighter tools are more easily configured to the job at hand. They are more energy efficient, costing less to operate. Not to mention, making them and shipping them consumes fewer resources.

ShopBots are engineered of steel and aluminum as relatively light tools, but given that the design choice has been made for agility, they have frameworks that are as stiff and rigid as possible. ShopBots' stiff main beams and rigid support members provide good cutting, and - with careful selection of cutters, spindle speeds, feed rates and cutting strategies - they approach the cutting characteristics of much heavier and considerably more expensive machines.  Still, a ShopBot can be readily repositioned on the production floor or broken into modules for transport to another location.  In small shops, it can be set up in areas that have limited access to heavy equipment, in a basement or above the ground floor.
Table:  Bolt Together vs Single Piece Table
The table on which the gantry runs is a bolt-together assembly.  It is shipped unassembled to reduce shipping expenses and to allow convenient set-up anywhere in your shop.  It would be slightly stiffer if welded as a single component; however, it is more practical to have a tool that can be easily readjusted with standard tools if ever knocked out of alignment and whose parts can be readily replaced if ever damaged.

Table:  Enclosed Table Sides vs Exposed Worker
We settled on one that offered affordability and stiffness, and at the same time offered operators and observers an extra shield of protection from flying debris or material that might break loose during cutting and machining operations.  We call these our Safety Sides™.  It means that our tools are most conveniently front loaded and/or end loaded, but this system seems to work well for the work flow of most shops.  It also means that any debris from cutting or pieces of a broken bit - if not contained by the dust-collector/guard around the cutter - will be blocked by the table sides rather than flying into an open area.

Linear Motion: V-Wheels vs Re-circulating Bearing Systems
There are a number of schools of thought on which sort of wheels or bearings the axes of a CNC tool should ride.  We feel strongly that for full-size woodworking tools, the V-Wheel offers the most practical solution.

Rack & Pinion vs Ball Screw (or spring-loaded machine screw)
The debate over Rack & Pinion vs Ball Screw as the motion mechanism for CNC will continue forever. Both systems are pretty good.
In theory, ball screws offer the advantage of being virtually friction free and very smooth.  However, they are also more complex.  They require precision alignment.  They are very vulnerable to being disabled by debris, so they must be kept very clean.  As the length of an axis gets longer, an increasing stiffness in the ball screw is required to prevent the screw from wobbling, and this results in large, heavy and expensive screws (which, in turn, require larger motors to keep up to speed).

Rack & Pinion is a straightforward drive system.  Modern grinds of the gearing insure smooth action with limited friction.  The system does not require precision installation or alignment and is very impervious to dust and debris.  Its components can also be easily replaced if they become worn.  While we rarely see significant wear on the rack, pinions do wear, and you can expect to replace them every year or two during normal regular use.

Perhaps the best way to leave you on the Rack & Pinion vs Ball Screw question is to just encourage you to take a look at several $100,000 and up CNC tools.  These are tools where the drive mechanism is a small part of the costs so the decision is made with respect to perceived performance.  You'll note that these tools use both systems; indeed, it is frequently the case that ball screws are used for one axis and rack & pinion for another.  Both work well.

Motors for Motion: Open-Loop Steppers, Closed-Loop Steppers, and Servos
The motion of ShopBots is powered with stepper motors.  Steppers are an incredibly precise form of motor that have the unique feature of never producing incremental errors.  A stepper is just as accurate at 80" as it is at 8.  The motors are inherently digital and thus a perfect match to digital computers and digital cutting.

Conventional open-loop stepper motors are the most affordable solution to producing CNC motion.  They have the limitation that, if overpowered -- which usually occurs by attempting to cut too fast or by cutting with a dull bit -- they can lose synchronization with the computer controlling their motion. But, when used appropriately these tools will produce excellent cuts, day-in, day-out.

For heavy duty production work, we recommend closed-loop tools.  These tools use closed-loop stepper motors and drivers.  They are called closed loop because they have sensors that continuously monitor their performance.  When the forces on these motors become greater or if they are pushed slightly off line, the motors instantly increase force and recover to the correct position.  This is similar to the behavior of servo motors, which are also closed loop.  Servo motors are a good solution for CNC tools because of their closed-loop control; however, servos can be more complex because they are continuously seeking their targeted location and modifying their location.  This means that servos are typically more expensive than steppers and is the second reason why heavy industrial CNC tools are expensive.  Be careful of the small servos sometimes offered on less expensive CNC tools as these motors may not provide the speed, power or acceleration you expect.  In a closed-loop system, look for something comparable to a PRSalpha, a CNC router than can travel at about 1800ipm and have 150-250 pounds of cutting force.

The stepper motors in all of ShopBot's PRS tools are made by the Japanese manufacturer Oriental Motor (OM).  OM has been building high-quality motors for more than a hundred years.  Their industry-leading technology has been much copied, and it is easy to find budget motors made to look exactly like OM products.  However, the copies often fail to live up to the OM performance, which depends on extremely high-grade bearings, precisely cut armatures, dense magnets and carefully wound coils.  

The OM alphaStep stepper motor/driver is the system we use in our PRSalpha tools.  The alphaStep combines the best of stepper and servo capabilities in a robust and technologically sophisticated system that has been virtually failure-free in the four years that we have been shipping them in our alpha tools. 

###Materials Review for Frame
A variety of materials have been used in the building of CNC machines. In comparing the materials there are a number of selection factors that need to be reviewed. 
- CNC frame materials need to have some strength in order to support the weight of the gantry and the cutting head as well as withstand forces resulting from the milling process. 
- Stiffness is also required to prevent any deflections due to both static forces and dynamic forces resulting from the acceleration of the tool head. 
- Weight is also important because the mass of the frame contributes to both the static and acceleration forces. 

The best frame material would accomplish all three and offer excellent machinability and be available at a low cost.

Several materials including some metals, steel and aluminum, and a range of plastics that include high density polyethylene (HDPE), ultra high molecular weight polyethylene (UHMW PE), polypropylene, polycarbonate, nylon, and Delrin (acetal) have been researched. Their properties are tabulated (see Materials Comparisons) in order to compare their characteristics and assess their applicability as a CNC frame material. The properties that were gathered include the modulus of elasticity, yield strength, and density. The ratio of the modulus of elasticity to density was calculated to give an indication of stiffness and the ratio of yield strength to density was found to give a strength value relative to weight. For steel and aluminum the thickness is indicated in the table while the width and length remained the same.

Comparing metals and plastics is not easy as metals have a much higher strength and modulus of elasticity, but also have a greater weight and are more difficult to machine. It’s interesting to note that both steel and aluminum have similar stiffness to weight properties indicated by the ratio E/ρ, while the high grade aluminum has a significant advantage in strength to weight. 

The advantage of building with plastics is the reduction in weight. From the data (Materials Comparison) the polyethylene, both HDPE and UHMW PE, and polypropylene plastics were the lightest with densities of 0.90-0.96g/cm3. Another benefit of plastics is easier machining as drilling and cutting processes do not significantly wear on the blades and bits. Good strength and stiffness properties are available in plastics as well. When nylon is reinforced, it has some excellent properties, as does the acetal, Delrin. However, comparing the costs, HDPE and polypropylene are the most economical choices and due to their low densities they have strength to weight ratios very near to that of steel.

| Material | E (10^6psi) | Sy (ksi) | ρ (g/cm^3) | E/ρ | Sy/ρ | Hardness | Cost of 1/2"x24"x48" sheet |
|:---------|:------------|:---------|:-----------|:----|:-----|:---------|:---------------------------|
| Steel A36 (18) | 29 | 36 | 7.85 | 3.69 | 4.6 | | 3/16” 64.32 (19) |
| Aluminum 6061-T6 | 10 | 37 | 2.71 | 3.69 | 13.7 | | ¼” 167.98 |
| HDPE (20) | 0.12 | 4.3 | 0.96 | 0.13 | 4.5 | D60-70 | 61.19 |
| UHMW PE | 0.06 | 3 | 0.94 | 0.06 | 3.2 | D60-70 | 150.38 |
| Polypropylene | 0.16 | 5 | 0.9 | 0.18 | 5.6 | R80-110 | 45.09 |
| Polycarbonate | 0.32 | 9 | 1.2 | 0.27 | 7.5 | M70-82 | 151.60 |
| Nylon 6/6 (30% glass reinforced)  | 1.3 | 25 | 1.25 | 1.04 | 20.0 | R101-119 | 272.78 |
| Delrin (acetal)  | 0.46 | 9.5 | 1.42 | 0.32 | 6.7 | M80-90 | 372.50 |

###Mechanical Systems
The Mechanical Subsystem of a CNC provides the means needed to cut and machine various materials for a given job.  The choice of materials has a direct impact on performance, precision, repeatability, longevity, of the complete system.

The mechanical subsystem is comprised of the guide system, the drive system, and the frame housing structure.  Each of these systems has a direct impact on the aforementioned qualities of a CNC.
