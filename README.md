# UEFI High Definition (HD) Audio Research

### Abstract
This repository contains a collection of researching tools and information relevent to developing High Definition (HD) Audio drivers for a UEFI environment. The goal of this research is to prototype needed components to interact with HD audio devices and identify best practices for driver implementation.

### Motivation
The primary incentive for HD Audio in UEFI is accessibility concerns. Individuals that rely on sound based design, such as those hard of sight, will be left completely in the dark when interacting with firmware infrastructure. Moreover, when firmware fails to initialize existing accessible software, the user will be completely unaware as to the reason.

Beyond accessibility, there are other utilities to audio in a UEFI environment involving debugging and system management. Audio hints can be given when various hardware fails, providing diagnostic feedback when a systems display is hindered. Hindered displays are common in headless environments such as severs or when a display is faulty or nonfunctional.

### Research Objectives
1. **Device Identification:** Prototyping reliable methods to correctly identify a HD Audio controller on the PCI bus.
2. **Controller Initialization:** Implementing a standard initialization sequence for an HD Audio controller.
3. **Link Control:** Establish a data link between the HD Audio controller and codecs for command traffic.
4. **DMA Management:** Allocating and managing buffers for communication between an HD Audio driver and device.
5. **Codec Enumeration:** Methods of identifying and enumerating various audio codecs.
6. **Sound Playback:** Generate simple sound queues stored in application memory or external files.