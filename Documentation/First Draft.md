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
