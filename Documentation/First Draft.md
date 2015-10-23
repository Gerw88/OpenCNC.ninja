##Introduction

The goal is to design and build a multi-function CNC profiling system with a cutting area of 2.44m x 1.22m x 0.15m.  The intent is to design the entire system with a minimum cost, while providing a positional accuracy of +/- 0.05 mm (.002”), and high machining speeds of up to 15 m per minute. The basis of the design will be patterned after numerous CNC Router designs (namely but not limited to, Data-Cut CNC, ShopBot Alpha, JoesCNC Evolution & MechMate). The design should incorporate interchangeable profiling heads & beds to support the profiling of both metal (using a Plasma head with Torch Height Control (THC)) and wood/non-ferrous metal/ aluminium and plastics utilizing a 2.2 -3.0KW single phase motor.

The system must cater for the occasional break-down and reassembly for relocation purposes.

##Description
A CNC machine is a system that is able to accept numerical control inputs to machine a part specified by the exact positioning of the inputs. The machine is able to accept commands through a directly connected personal computer. The personal computer communicates to the main controller subsystem through (one of the following) Ethernet, USB, or parallel link. The main controller subsystem is able to interpret and directly control movement of the attachable tool head/s. The framework of the system is set up by the mechanical subsystem which will allow for movement in the x, y, and z axes and specify spatial limitations of any acceptable job. The main controller, and mechanical subsystems are able to interact through power provided by the motor driver subsystem. The overall block diagram of the machine is pictured below.

![](https://cloud.githubusercontent.com/assets/8729407/10703947/572c744a-79cb-11e5-8920-7bb6153bd51d.png)

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

###Guide Rail Design
The linear motion system (LM) plays a vital role in any linear CNC machine, and CNC routers are no exception. Without these systems coupled with a drive system, a CNC router would be of little use.

The LM is responsible for three primary tasks. 
1. Support Machine Components
2. Guide the machine in a precise linear motion with minimal friction
3. Support secondary loads (Torque, Lateral Loads, etc.) 

A complete LM is a combination of a drive system and linear bearing system. However in this section, this term is referring to the linear bearing assemblies and the associated parts.

A LM is composed of some type of linear bearing and the linear bearing guides. There are a number of types of bearings and guides, each with advantages and disadvantages. Because of the importance of this system, it is vital to be knowledgeable about the linear motion LM components. 

###Supporting Machine Components
The LM system must be able to handle the weight of the components while transporting it along a linear distance and maintaining linearity. For example, the gantry on a CNC router is supported on a LM system and is able to move along the X-axis. The LM system must support the weight of the gantry and still provide a low friction motion.

###Providing Precise Linear Motion
While supporting a load, the LM system must also provide a precise linear motion with minimal friction. This is the primary task of a LM system. The type of LM system directly relates to the accuracy or a CNC router. A “sloppy” linear motion system leads to a “sloppy” CNC machine. That is why it is important to have the correct LM system installed on each axis.

###Supporting Secondary Loads
Aside from supporting the weight of the machine, LM systems must also be able to support secondary loads such as torque or lateral loads, depending on the setup. Some applications of LM systems require only one dimensional load ratings, such as supporting a vertical load like weight. Other applications require multi-dimensional load ratings. For example, the LM system of the Y-axis on a CNC router is required to support the vertical loads caused by the weight of the Z-axis assemble, and also support torsion forces cause by the cutting action.

Every LM system is rated for certain loads and certain applications. Choosing or identifying the right system for our CNC profiler is vital.

###Categories of LM Systems
We can categorize linear motion systems into 2 categories: 
- Fully Supported Systems
- Partially/End Supported Systems

Fully supported LM systems are supported throughout the entire length of the system. This type of system can usually support more load without sacrificing linear precision due to deflection. Our goal is to have fully supported LM systems on the X and Y-axis while using end supported systems on the Z-axis. As the length of an axis increases the more vital it is to have a fully supported system. Examples of these systems include linear rails and guide blocks as well as track rollers. 

Partially or end supported LM systems are just what they seem. These systems are supported on their ends. These systems are prone to flex and deformation because of the machine weight or the forces applied. However, these systems are more suitable in some applications. The most common type of end supported LM system is the linear rod and bushing setup.

Of course each category contains many different types of linear motion systems. 

###Profile Rail Guides
Rails and guide blocks, also often referred to as simply linear guides, are high end linear motion systems. Profile guide block systems are another form of linear bearing system used to move a load along a straight path with as little resistance to the direction of motion as possible.

These systems offer numerous advantages over other linear motion systems. Profile guide blocks and rail systems are, as the name suggests, composed of two primary components. The profile rail, which guides the guide blocks and provides a smooth and durable surface for linear motion, and the Guide Block which rides on the rail and supports the load that is to be moved. Think of it as a roller coaster, with the rail being the track and the block being the cars.

There are several advantages to profile guide systems. They are very robust and accurate due to their construction. Most all guide block systems use ball bearings to roll the load along the rail, which means high efficiency. This high efficiency means less work must be done by the drive system to move the load. 

This is the strongest and best performing rail design. These systems offer push, pull, and rotational/moment load resistance in many directions.

###Round Shaft Railing
 A precision machined steel rod is combined with a rectangular, aluminum bearing block that houses the recirculating bearing insert. There are a variety of mounting arrangements for this type of rail-and-bearing system (Fully supported shown left and end supported shown below). The single biggest problem with this design is that the bearings contact the rail on a single point. Over time the bearings will wear a groove in the rail along that point, which can start to develop lash and reduce performance. Also, as grooves wear into the rail, more debris gets past the seals and bigger problems can develop.
 
###V-Rails
This is one of the least expensive and weakest rail designs. In its simplest form, a piece of steel plate with a V profile is positioned with the V-point up, creating the riding surfaces. One, two or more V-bearing wheels with the matching V-profile are attached to the moving structure and ride on the V-rail. The weight of the moving structure is the only force maintaining the bearing wheel to rail connection. The stronger design includes V-profiles on the top and bottom edges of the V-rail. V-bearing wheels on the top and bottom secure the moving structure to the V-rail providing added strength and rigidity. Cutting and rapid feed rates will be slower and depth- per-pass will be smaller.

The rails must be fastened with multiple fasteners to the supporting structure. The standard holes are spaced at 2 inch (51mm), 3 inch (76mm), or 4 inch (102mm) intervals depending on the rail size. 
The accuracy of the system is dependent on the flatness, straightness and parallelism of the supporting structure. Most v‐roller applications do not require high accuracy. It is adequate in many applications to attach the rails directly to cold finished or extruded material. Rails are supplied with shoulders to mount against the square edges of plates or bars.

For designs requiring accuracy levels of ±.13mm/300mm and better, the mounting surfaces must be prepared appropriately flat, straight, and parallel Reference edge assemblies should also be used. Greater accuracy can be obtained by fastening the rails to a plate or bar that has been prepared by milling or grinding the mounting surfaces flat and parallel.

###Drive Designs
The drive components are the mechanical components that "drive" the CNC machine along its axis. The most common components associated with a drive system are the motors, and either lead screws or rack and pinions. The whole idea of a drive system is to convert controlled rotary motion to controlled linear motion with the help of a CNC Controller.

The drive system has a direct correlation to the machines capabilities. By understanding the CNC drive system, you have a much better understanding of a CNC machine. Just by changing a few components you can control the machines cutting speed, cutting force, precisions, and accuracy.

We will be looking at 3 main type of drive systems, however there are some characteristics which need to be understood irrespective of the drive system used.

###Essentials
There are a few criteria for selecting a drive system (Leadscrew) that should never be overlooked. Choosing the correct, diameter and lead are the most basic and crucial but there are other factors to consider as well.

Weights
We must know or be ready to estimate the weights of the individual moving assemblies. This is important. We will use these values to calculate the loads that the drive system must withstand.
Velocity and Acceleration
We must know the desired velocity at which we want your assembly to move. This is usually in Millimeters per minute (mm/min). We must also know the desired acceleration in meter per second squared (m/s2), or the time at which you want to reach your goal velocity. It is much easier to estimate the time to reach velocity. E.g., we would like the machine to reach 5080 mm/min in .4 seconds.
Length/Span
You must know the total length or span of each Leadscrew. It would also be helpful to know the maximum distance that the nut could be from the bearing support on each axis.
Bearing Supports and End mounting
At this point of the design we may have some idea as to how we will secure the lead screw to the machine. Actually, it is best to fully understand how the different end mounting types will affect the outcome of your machine before choosing.

There are four primary types of bearing supports. Reference the image below, which represents the four bearing end mounting types. Shown least to greatest rigidity, from the top down.


Bearing Support Types
Critical Speed
Critical speed refers to the RPM at which the natural frequency of a rotating shaft begins. This vibration, also called resonance, will occur regardless to the orientation of the leadscrew. The critical speed also applies to rotating nuts about a lead screw.
Column Strength
Column strength refers to the maximum load a lead screw can withstand in compression before failing. Compression loads that exceed the column strength will cause the lead screw to buckle, or bend. Even the slightest bend can ruin a leadscrew.
Back Lash and Back Driving
Back lash and back driving are both concerns that need to be understood and addressed:
Back-Lash
The technical definition of backlash (lash) is the amount of free movement between the nut and the lead screw without rotation of the nut. In short terms, it is the ‘play’ between the nut and lead screw. If you take a nut and thread it on a bolt or threaded rod, you should be able to pull and push on the nut along the bolts length and feel slight movement. The lash is a factor that may reduce repeatability and accuracy in a machine.
The lash is usually referred to as back lash because of when the lash affects the machine. If the CNC machine only moved in one direction, the gap between the nut and lead screw threads would always be compressed and would not affect the machine. Reference the image to the left.

In normal operation without an anti-back lash nut, the lash allows the lead screw to rotate slightly without engaging the nut. This means that the desired position is lost.

The lash between a nut and lead screw will increase as they wear. This is why most acme nuts used on CNC routers are wear compensation anti-backlash nuts. 

There is also radial or transverse back lash. This can be noticed by trying to rotate the nut perpendicular to the lead screw axis. Again, this may be minimized by anti-back lash nuts. Also, increasing the length of the nut will help.
Back Driving (Creep)
Just as lead screws can convert rotary motion into linear motion they can also convert linear motion into rotational motion. This conversion from a linear force into rotational force is what is known as back driving or creep in the CNC industry. ACME screws are often considered to be self-locking, meaning back driving is not an issue. However if the efficiency of the lead screw is sufficient, then back driving may still occur. Generally, any linear motion system with efficiency greater than 50% may back drive or creep.
Furthermore, vibration may assist the system to back drive. Systems that typically would not creep may if vibration occurs. For us, this primarily affects the z-axis system. The combination most attributing to back drive is a z-axis servo driven system with a ball screws or rack and pinion. Because gravity affects the z-axis system, counterbalance or springs are usually used to deal with back driving issues. A very efficient system will drive itself into the bed or piece if power is lost and there is no braking or counterweight system.
Also, back driving may occur on a smaller scale only causing enough position loss to ruin the project. It is vital to keep this in mind when doing our design. Even if using acme screws, leave some room in the design for an anti-back driving system (springs etc.). The simplest approach is to use a low lead acme system for the z axes.
Threaded rod and drive nut systems (Leadscrews)
Since CNC machines require linear movement in multiple axes, multiple screw systems are most often used to accomplish this goal. These systems offer a simple and compact means of transmitting power and motion with excellent reliability. For these machines motors generating linear motion and thrust on the nut turn the screws. There are two main types of screws, and both power screws and ball screws operate in this way. However, the differences arise in the efficiency with which this motion is transmitted, the friction loss, the allowable rotational speed, and the required linear speeds. Before these differences are discussed it is necessary to explain the specifics of each type of screw.
Power Screw (ACME) versus Ball Screw:
Power screw is a general term for screws that transmit motion to threaded nuts using a variety of thread shapes. The threads used include ACME, show in Figure 2-1, and metric trapezoidal (Ball screws) among others. The trapezoid or squared thread shape allows for smoother rotation without the clapping force that is present in fastener threads. Most power screws are made from steel and nuts are made from bronze and plastics to reduce friction.  
As seen in Figure 22, ball screws use ball bearings between the threads of the nut and screw. These ball bearings travel a continuous path through the nut providing rolling contact and reducing friction. Some ball screws offer multiple ball circuits distributing the load and improving reliability. 

 ACME Power Screw			 Ball Screw

Both types of screws are available in various leads and with multiple starts. The lead of a screw gives the linear travel of the nut for every revolution of the screw.  The speed of the linear advance is determined by dividing the rpm by the lead.  When a lead is increased and the helical threads are lengthened, gaps would be left between individual threads. This is when multiple start geometry is utilized. 

A screw with multiple starts indicates that there is more than one thread running down the length of the screw filling the gaps between threads that would otherwise be present in high lead screws. The linear speed requirement of the system is used to determine both the rpm and the lead. A screw with a high lead can be rotated more slowly to produce a given linear speed while a screw with a lower lead must be rotated faster to create the same linear velocities.  However, each type of screw has limits on the rpm they are capable of operating at and the leads that they are manufactured in. In this case, other factors must be analyzed, and together, the system requirements specify the best type screw for the machine. 

The type of contact between the nut and screw determines most of the screw characteristics. A power screw such as ACME uses a screw to nut contact resulting in sliding friction.  While the coefficient of friction depends on the part materials, it is generally higher than that of ball screws, which have rolling contact provided by the ball bearings. This friction results in a loss of torque transmitted and lower output efficiency for ACME lead screws. 
ACME lead screws have efficiencies that range from 20-30%, while ball screws transmit motion with over 90% efficiency.  This friction significantly impacts the system, but most important is the increase in the required drive motor torque. If the system requires high speeds, then motors must be much larger, increasing cost and adding weight. Also, the low efficiency of ACME screws converts a majority of that torque into heat. For these reasons, ACME screws are limited to speeds below 300 rpm with most applications below 100 rpm. 
 
However, with improved nut materials, these negatives can be reduced making power screws more attractive. The sliding contact of ACME threaded screws that reduces its allowable speeds also creates its many advantages. Most importantly, the larger friction force allows the screw to self-lock and keep any thrust load from being converted to torque and back driving the motor. Ball screws will experience free linear motion of the nut, known as backlash, unless a preloaded nut or double nut or some type of brake is used.  This can create complexity in the design and increase cost of the system, making ACME screws desirable when this is a significant problem. These screws are available with many different leads.  Higher leads provide for quick linear translation, but require greater rotational torque to move loads.  Smaller leads provide for precise positioning and require less rotational torque.  Due to the greater complexity of the ball nut, ACME screws generally have the advantage for low lead, high precision applications as they can be manufactured in leads as low as 0.5mm/rev. 

Another consideration includes screw life and reliability. For this, the advantage belongs to the ball screws. Due to the extensive testing done with balls for roller bearings there are less unknowns than for ACME screws in which load, speed, lubrication, heat, and other factors must be taken into account.  The life of power screws depend greatly on the system variables where life for ball screws can be reasonably estimated from wear life calculations.

In the process of selecting the best screw for a particular application, all of the system variables must be examined to determine what requirements must be met and which compromises can be allowed. If higher rotational speeds are needed, with the lower friction, less heat generation, and more efficient conversion of drive torques will require the use of ball screws. However, if simplicity, lower costs, self-locking, or high precision leads are the more desirable attributes, then power screws such as ACME are the more likely choice. 

CNC machines currently on the market use both power screws and ball screws. Most of the lower end machines use power screws such as ACME threads for cost savings and design simplicity. However, as speeds increase and higher reliability requirements are desired, ball screws become more common. We are the ultimate judge on system practicality, and besides speed and accuracy requirements, the only concern in regards to the drive system is that it works now and continues to work for a reasonable length of time. 

For many in this market, an ACME screw will provide excellent function and life that their usage will require. The small businesses and more active users will most likely desire ball screw drives and will be willing and capable of paying for its advantages. As with all purchases and design comparisons, all of the options must be weighed with the advantages, disadvantages, and costs of each in order to determine best drive mechanism for the system.   
Rack & Pinion
Rack and pinion is a design where teeth of a steel pinion gear are meshed into the teeth of a steel rack. The connection is metal on metal with grease applied, and sometimes the pinion will be a little softer so it will wear, since it is the easier component to change.

Rack and pinion.
Recent developments in preloading have revolutionized the overall performance and energy efficiency of rack-and-pinion drives. These advantages include long-term, backlash-free operation and unlimited travel length. Helical gearing is also an option which allows teeth to engage smoothly and quietly.

Backlash between the rack and pinion can be a problem, and the pinion can ratchet out of the rack, so a tensioning system is needed to keep the pinion in the rack. The use of a split pinion also reduces the backlash.


Split Pinion.
There is major difference between the US/imperial specification and metric specifications on racks. Module is a metric pitch, inversely related to diametral pitch, e.g. Module = 25.4 / Diametral Pitch.

Helical versus Straight.
There are two styles of gear racks – Straight tooth, where the teeth are perpendicular to rack length, and helical tooth, where the teeth are at an angle to the rack length.  The helical style provides several key benefits over the straight style, including:
Helical rack & pinions runs quieter than the straight, especially at high speeds
Helical rack & pinions has a higher contact ratio (the number of effective teeth engaged) than straight, which increases the load carrying capacity
Straight racks lengths are always a multiple of pi. E.g. 502.65 mm and 1005.31 mm.
In most cases, helical rack & pinions cost the same as the straight rack & pinions!
The only real disadvantage to using helical rack & pinions is it requires more time to set up and align properly.
Accuracy:
When talking about rack & pinion accuracy, it can be broken down into three components:  Backlash, Pitch Deviation and Tooth Quality.

#####Backlash
is the amount of clearance between the rack & pinion tooth flanks, and will depend on the type of rack selected and alignment accuracy between the rack and pinion.  The backlash can be eliminated completely by using a preloaded split-pinion or dual pinion drive system.

#####Pitch Deviation
is the difference between the theoretical rack length and its actual length.  This varies depending on the rack quality selected and is shown as GTf per 300 mm length. Zero cumulative pitch deviation for long travels is available.

#####Tooth Quality
is the accuracy that the tooth flanks are manufactured to, which affects the running precision and smoothness of the axis drive.  
- Soft rack & pinions have a quality level of ~AGMA 9 (DIN 9).  
- Induction-hardened rack & pinions have a quality level of ~AGMA 8 (DIN 10), due to deformation from the heat treatment process.  
- Quenched & Tempered rack & pinions have a quality level of ~AGMA 10 (DIN 8).  
- Hardened & Ground rack & pinions have a quality level of ~AGMA 12 (DIN 6), since the teeth are precision ground.  For high accuracy applications, a precision rack, such as the Hardened & Ground, should be used.

#####Lubrication:
With open gearing such as rack & pinions, lubrication is critical!  A thin film of grease or oil should always be on the contacting tooth flanks to ensure there is no metal-to-metal contact, which can damage the teeth.

###The Frame and Base
The base and frame of a CNC router is the main structural element of the machine. The base and frame is what holds everything together. This is what will determine our motor placement and linear motion component placement along with everything else.

The frame and base design will be determined partially by the materials and supplies that are available, the number of linear motion components and motors the budget allow etc. However, we need to become familiar with different designs so that you may buy parts that fit our design.

When we look at other CNC router designs, you may notice that almost every unit is different. Although this is true, you can break down these designs into categories.
####The X-Axis Base and Frame 
The X-axis frame should also act as the base for the machine as the X-axis should be the axis closest to the ground. This portion of the machine will perform 3 primary tasks.
- Act as the base for the machine 
- Support the X axis linear motion system
- Support the cutting table

##Common designs for the base.

###Fully Supported Frame 
The fully supported base is one of the best designs and is the design used on most industrial or professional routers.

This shows only the base and does not show the gantry
The fully supported design means that both the Y and X axis may rest on the floor or some other structure. There is nothing connecting the gantry across the Y-axis. This allows for a very sturdy design and is not susceptible to the cutting table or the structure itself flexing under its own or external weight.

In order for this system to flex or deform, the material itself would need to compress.

We are not talking about massive amounts of flex. This all ties back to our machine tolerance decision, hence we should already have some idea as to the desired precisions and accuracy we want our machine to hold. A deformation of 0.0254mm is acceptable if we only expect a 0.254mm accuracy from our machine.

There are drawbacks with this design, the cost. We will need multiple LM components & motors (2 x linear guides, 2 x LM drive mechanisms and 2 x motors). We could employ a fully supported frame design with one motor using a pulley and belt system, but we would need to make sure the motor is up to the task. With this design we can get away with a lighter material as it will be supported against the ground or some other structure. 


###Fully Supported Bearing Rods/Rails 
When we say “fully supported” in this section, we mean there is no obstruction sweeping across that axis during operation.

It is possible to have a fully supported linear bearing system and not have a fully supported frame. You can see this in the Solsylva design below.


~~Image Link Here. Partially Supported X-axis Fully Supported Y-axis Frame~~

A common design is the partially supported X or Y-axis.

~~Image Link Here. ~~

The gantry would have an undercarriage that would connect the gantry to the lead screw. With this setup you could have a ‘fully supported’ linear rails or rods setup. However, the rods or rails would still be able to flex with the frame itself.

The frame will only be supported on the ends since there must be clearance between the ground and the frame to allow the gantry undercarriage to move along the X-axis. In the image above, the Y-axis would be considered supported since you could have a frame that would not interfere with the gantry movement.

The frame across the Y-axis would prevent flexing for that axis. This would mean the cutting bed would be very rigid in the Y-axis but could flex or deform along the X-axis.

With the design above, even if the frame were made of solid aluminum (38mm x 110mm) and the X-axis span were 1524mm, the frame would ‘sag’  0.2540mm in the center, just under its own weight. That does not include the weight of the gantry or anything else.

We see this would be an issue if we’re trying to design a machine to hold a tolerance of 0.0254mm in the Z-axis. It is true that the machine would flex as a whole and could be compensated. However, the machine could vibrate and bounce when cutting, creating lines in the work. If our machine has a relatively small X-axis span, this design works well and is probably the easiest to setup. There are other solutions.


###Partially Supported Y- axis Fully Supported X-axis 
Assume we have only one motor and lead screw for the X-axis and still wish to maintain a high tolerance on the machine. We could move the Y-axis gantry assembly inside the frame which would allow us to fully support the X-axis because the gantry would not cut under the X-axis frame. However in that situation, the Y-axis frame would not be fully supported.


We see in this design, the longer X-axis is fully supported (on the ground), however the gantry would cut through any frame in the Y-axis inside the cutting area.
This means that no matter how much weight we put on the gantry or cutting table (not pictured), the X-axis frame would only deform if the material itself deformed.

With this design, the cutting bed would need to have its own frame and could ‘sag’ in the center. However, the machine itself would be constant and once the cutting bed is installed, you could true the cutting table surface by planing the surface with the machine.

The cutting bed would then be true to the machine.

When we design or build the CNC router, we need to decide which is more important. Have the machine remain constant or have the cutting bed and the machine flex together. 

###Alternatives 
There are other alternatives when we build or design a CNC router. One way to obtain a fully supported router is to do away with the gantry undercarriage and have the lead screw connect at the top of the gantry, or have 2 lead screws high on each side. We can see this application in the Solsylva designs. 

However, with a single lead screw up high above the gantry, it makes access to the cutting bed somewhat difficult. This design works well for smaller machines that are mobile. For instance, a CNC router designed to carve shapes on wood flooring.

The Mobile bed design would not be suitable in our case as the footprint of the machine would be too large.

###Other Considerations 
When we design and build the CNC router, the material we use to construct the frame will play a big role in the design of the frame.

Different materials will deform differently. Keep the material consideration in mind as we choose a frame design. Most popular materials are:
- MDF
- Plywood
- Aluminum Stock
- Structural aluminum profiles.
- Steel

###The Gantry (Y-Axis) Design Considerations
The gantry design is the most popular design in the CNC router community. It is popular for a reason: it works. 

The gantry design is a proven design for CNC routers. However, there are still many things that we should be aware of.

From a design standpoint, we want our gantry to be stable and balanced. Design the CNC gantry to meet the forces that it will encounter. This will prevent excess stress and strain on you bearings, lead screw, motor, etc.

In order for you to be able to design and build your gantry to meet the required forces, you first need to identify and understand the forces involved.

Let’s take a look at the forces evolved with a do it yourself CNC router gantry

~~Image Link Here. Side view of a typical CNC router gantry.~~

We will briefly cover the following (A full technical explanation of CNC Router Forces will be covered in a separate document). 
- Center of gravity/mass
- Forces 
- Moment

Let’s identify the labels above: 
- D1 = the distance between the cutting tool (the router bit) and the center between the two Y-axis linear bearing rods/rails (D3). 
- D2 = distance between lead screw/ linear bearings and the bottom Y-axis linear bearing rail/rod. 
- D3 = distance between the lower and upper Y-axis linear bearing rods/rails. 
- D4= distance between the 2 linear bearings that sit on the X-axis linear bearing rods/rails. 

Now we will look at the forces evolved. This is the short answer (summary, the full technical explanation of CNC Router Forces will be covered in a separate document) 

###When we design or build the CNC router, keep the following in mind:

- Try and keep the distance between the X-axis lead screw and linear bearings, as close as possible to the bottom Y-axis linear bearing rods/rails. Or as close to the center distance between the top and bottom Y-axis linear rods/rails. (Minimize D2).
- Keep the spindle plunge arm on the Z-axis assembly as short as possible and make that arm out of rigid material to prevent flexing. A normal Z-axis arm travel is anywhere from 75 to 150mm. (Minimize D1).
- Calculate or estimate where the center of gravity of the gantry will be located, including the spindle. Design the gantry side arms to compensate and place the center of gravity (CG) between the front and back X-axis linear bearings per arm. (CG should be located at ½ D4 and as close to X-axis lead screw as possible).
- Maximize the distance between the upper and lower Y-axis linear bearing rods/rails but still allow for clearance under the bottom rod/rail for your max Z travel. (Maximize D3).

###Other considerations 
A good gantry design is one of the most crucial factors for a quality CNC router. As with all CNC routers, budget is a concern which means material are also a concern. Try and visualize and estimate the forces involved and make our CNC router design work with the materials we decide to use.

Topics such as lead screw placement, motor placement, linear bearing attachments, etc. will be discussed further into this document, as they are all important consideration with CNC router project.

###The Z-axis assembly
Below you can see two examples of Z-axis assemblies with the Y-Axis CNC Router Gantry in the background.

It is important to consider the forces that are involved. That way, we can adjust our design and verify that it will meet our design requirements. However, in order to design and build our machine to meet our requirements, you first need to understand the forces involved.

~~Image Link Here~~

Forces on the Z- Axis Assembly.

Let’s interpret the above image. 

The following explains the dimensions: 
- D1 = the vertical distance between the upper and lower Y-axis linear bearing rods/rails. 
- D2 = the vertical distance between the upper and lower sets of Z-axis linear bearings. 
- D3 = the length of the spindle attachment plunge arm. 
- D4 = the width of the Z-axis assembly.
- D5 = the horizontal distance between the Z-axis linear bearing rods/rails. 
- D6 = the thickness of the plunge arm
- D7 = the distance between the cutting force (approx., tip of the cutting tool) and 1/2 D2. 

Now that we understand what the dimensions are, let’s analyze the forces and moments.
Forces and Moments on the Z-Axis Assembly 
Building a CNC router can be easy or hard. Some people over analyze and some people just build it and see if it works. I think the best approach is a mix of the two methods. So let’s first try and understand what is happening.

The above image illustrates an example of a Z-axis assembly shown in a front view and a side view. Look at the front view and notice that the Z-axis assembly is moving to the right while it rides on the Y-axis linear bearing rails/rods.

The plunge arm is at max Z travel and is cutting into a material as it moves from left to right. This cutting action produces a cutting force that opposes the movement of the Z-axis assembly.

The cutting force is a variable of spindle RPMs, the number of flutes on the cutting tool, the feed rate, and the material that is being cut.

For now, just understand that there is a force in the opposite direction than the Z-axis assembly is moving. Now let’s see what happens because of this cutting force.

The cutting force creates a moment, which is illustrated in the image above as Moment A. (A moment is just a force that is applied at a distance).
 
````Moment A = D6 x Cutting Force.````

 Moment A torques the plunge arm in the opposing direction of the cutting force, which torques the whole Z-axis assembly.
 
This moment results in resultant forces that are applied to the Z-axis linear bearing rails/rods and the Z-axis linear bearings themselves. (Yellow arrows)

As D5 and D2 increase in length, the resulting forces decrease. You can see that when we are designing or building a CNC router, it is important to maximize the horizontal distance between the Z-axis linear rails (D5), and the vertical distance between the Z- axis linear bearing blocks.

###The Plunge Arm 
D2 also has an effect while cutting along the X-axis. Take a look at the image to the left.

The cutting force causes another moment; Moment B.

````Moment B is the result of the cutting force being multiplied by the distance between the cutting force and ½ D2.````

This moment will apply resulting forces on the Z-axis bearings. As the distance between these bearings (D2) increase, these forces will decrease. That is why it is best to maximize D2.

As a rule of thumb when building a CNC router, D2 should never be any less than half the length of the plunge arm. Also, we want the thickness if the plunge arm (D6) to be thick enough to not flex under our maximum cutting force.

The flex will depend on the maximum cutting force we are designing our machine around, the thickness of the material (D6), plunge arm length (D3), and the material it is made of.

###Summary 
Keep the following in mind when you design or build a CNC router: 

- Maximize D1, reduces the forces due to torque caused by the cutting force in the X-axis.
- Maximize D2 reduces the forces due to torque caused by the cutting force in the X-axis. 
- Minimize D3, but still allow for your desired Z-axis travel. 
- Maximize D4, reduces the forces due to torque caused by the cutting force in the Y-axis. 

###Other Considerations 
Other features such as lead screws, motor placement, linear bearings etc. all have an input here.


###The Router Table Top
The CNC router table top is where the cutting magic happens. The table top, also called the cutting bed, can make the life of a CNC router operator enjoyable or a nightmare.

For example, if we are in the prototyping business, we will probably be working with all kinds of materials and shapes. This would probably push you towards a T-slot style, which offers numerous clamping options. On the other hand, you might produce the same type of product on a daily basis which would push you towards a different style. On some CNC router tables we may find a combination of different types of cutting table tops. 

###The T-Slot table top
The T-slot table is often seen on traditional CNC milling machines. However, these are usually made of tooling steel and are extremely heavy. The T-slot tables found on CNC routers are usually made of extruded aluminum. There are many advantages to the T-slot type table. 

###The Vacuum table top
The vacuum style CNC router table top is often found on higher end models. They can be very useful for many applications. However, there are drawbacks. For example the...

###The Perforated table top
Similar to the vacuum table in appearance, the perforated table top is simple yet affective. Much cheaper than a T-slot style bed, yet offers similar performance. The perforated table offers a lot as far as...

###The "Disposable" table top
The "The "Disposable" table top is actually one of my favorites. Especially if you are new to operating a CNC router. This table style, usually composed of one or two sheets of high density MDF board, are very useful even if you have some other table top installed. I can't tell you how awful it makes you feel when you cut into your brand new t-slot or vacuum table. Yes I know there are limit switches, touch off pad and sensors to prevent that type of mistake. However, you would be surprised at how often we "bypass" those features. The disposable bed can also... 

###Building your own CNC router table top
The CNC router table top on a homemade machine is a very important considerations. The budget usually pushes towards the MDF style cutaway table top, which I actually think is best because of its versatility. However, design of the table support and structure should *NOT* be overlooked.
