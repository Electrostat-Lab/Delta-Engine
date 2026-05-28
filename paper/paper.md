# Delta-Engine

## Abstract
Scientific abstractions are one of the very useful techniques to implement software to control embedded microcontrollers for heavy machinery operations. In this paper, we introduce a physics engine that provides a new software paradigm for IO control for embedded systems and robotics based on a mathematical-physical abstraction.

## Keywords
Embedded Systems - Embedded IO - C Programming Framework - Calculus-based Physics - Multivariate Calculus - Software programming paradigms

## Knowledge Gaps (Statement of Need)
There are a couple of theoretical and practical knowledge gaps that this software is going to address including, but not limited to:
- [ ] Precisional IO Embedded Control of heavy machines and robotics using Scientific Abstractions (e.g., Mathematical/Physical and Chemical Abstractions).
- [ ] Seamless hardware implementation of several physics simulation systems.
- [ ] Single abstraction for software and hardware systems.

## Introduction
Delta-Engine is a physics engine that provides a new software architectural paradigm for precisional IO switch and control over embedded systems and robotics without much knowledge in embedded systems, managing states and software engineering paradigms or if they fail to design the system (e.g., Object-oriented programming). It introduces the field of computational physics to the embedded world through providing a virtual machine and a runtime infrastructure based on the Newtonian physics spaces and supporting infrastructure IO libraries for several supported platforms.

## Methodologies
- Virtualization of physics objects and IO emulation using mathematical and physical abstractions.
- Newtonian physics spaces as Runtime Infrastructure (RTI).
- Implementation of several physics spaces modules (e.g., Kinematics Module - Fluid Mechanics Module).

## High-level Architecture
<img width="773" height="904" alt="architecture" src="https://github.com/user-attachments/assets/d5700f97-d21c-42fb-9279-818225b125d4" />

<img width="1662" height="1301" alt="ses-mb" src="https://github.com/user-attachments/assets/51447f44-0fc4-4b15-9e33-3a40257c5764" />

Two architectural models are being proposed here; a **hierarchial model** representing a hardware abstraction layer using a mathematical/physical abstraction, and a **System-Entity-Structure/Model-Base (SES/MB) model** to model the same system components into several subsytems; those subsystems display some components that may be formally linked with components from other subsystems (e.g., the formal linkage among Math Libraries, Mechanics Libraries, and the VMIO Libraries that enable a chained dispatch from Physics to IO).

### Subsystems:
* Atomic Newtonian RTI: a subsystem that groups the runtime infrastructure components; its instantiation reveals the base Newtonian physics of inertia, acceleration, and object interaction in space.
    * Molecular Component.
    * Inertial Ref. frame Component.
    * Acceleration Component.
    * Interaction Component.
* Physics Mechanics: a specialized subsystem of the Newtonian RTI; grouping the different types of objects in the universe that experience inertia, acceleration/deceleration, and interaction with other objects.
    * Mechanics Module.
    * Fluid Dynamics Module.
    * Thermodynamics Module.
    * Electromagnetism Module.
* Mathematical Libraries: a subsystem housing the base continous and discrete mathematical layer of the operations involved in the Physics Subsystems (both the Atomic/Newtonian RTI and the Physics Mechanics Subsystems).
    * Calculus Module.
    * VectorMath Module.
    * Matrix Algebra Module. 
* Virtualized IO (VMIO): a subsystem involving a platform-independent layer of driver modules to operate on the lower level platform-dependent IO infrastructure based on the output data from the Mathematical/Physical layers.
    * Analog Driver Module.
    * Digital Driver Module.
    * Comm Driver Module.
    * Memory Driver Module.
* IO Infrastructure: a subsystem involving a more platform specific dependent layer of the hardware IO; grouped together in a thin abstraction layer that encapsulates a procedural runtime for the hardware IO involved; links statically with **the Platform-dependent toolchain**.
    * GPIO Module.
    * PWM Module.
    * UART Module.
    * SPI Module.
    * I2C Module.
    * EEPROM Module. 
* Platform-dependent toolchain: a subsystem involving a platform-dependent layer of the hardware IO and the operating system operations that are encapsulated directly by the IO Infrastructure subsystem and indirectly by the Platform-agnostic VMIO subsystem.
    * Android Userspace Runtime.
    * AVR Runtime.
    * ARM Runtime.
    * x86 Userspace Runtime. 

## Implementation Phases and Milestones

## Integration Phases and Life Applications

## References
- [SES/MB Framework by Throsten Pawletta](https://dl.acm.org/doi/10.5555/3108244.3108245)
- [The Feynman Lectures Caltech University](https://www.feynmanlectures.caltech.edu/)
- [Fundamentals of Physics for Scientists and Engineers by Paul Tipler]()
- [Thomas' Calculus]()
