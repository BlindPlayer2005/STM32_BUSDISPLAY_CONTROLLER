# STM32_BUSDISPLAY_CONTROLLER

## Why an STM32-Based Controller for Bus Displays?

---

### 1. Introduction
The VDL LED bus displays we are experimenting with were originally designed to operate together with the **AMELI FY7000 controller** and other proprietary hardware.  
While these systems are reliable, they are also **closed-source, outdated, and difficult to repurpose** for custom applications.  

To reuse these displays in modern projects, we require a **new controller platform** that is:
- Flexible
- Easy to program
- Compatible with existing hardware interfaces  
The **STM32 microcontroller family** is an excellent candidate.

---

### 2. Why Not Use the Original Controller?
- **Proprietary protocols**: The AMELI FY7000 speaks IBIS/RS485 in a format that is not well documented.
- **Locked ecosystem**: Original hardware and software are designed only for bus applications.
- **Limited expandability**: Adding features (USB, WiFi, custom UI) is not possible.
- **Age & availability**: Spare parts are rare and not future-proof.

---

### 3. Why STM32?
STM32 microcontrollers combine performance, flexibility, and ecosystem support:

#### ✅ Technical Advantages
- **RS485 support**: Native UARTs with configurable parity and stop bits for communication with the displays.
- **Low-power ARM cores**: Efficient and reliable, perfect for 24/7 operation.
- **Multiple interfaces**: USB, SPI, I²C, CAN bus, Ethernet — enabling easy integration with PCs, networks, or additional sensors.
- **24V tolerant design (with regulators)**: Easy to integrate into existing bus power systems.

#### ✅ Development Advantages
- **Open ecosystem**: Full access to datasheets, libraries, and community resources.
- **Scalable**: Wide range of STM32 chips (from small F0 series to powerful H7).
- **Supported in many IDEs**: STM32CubeIDE, PlatformIO, Arduino framework, etc.
- **Cost-effective**: Cheap to source, with plenty of development boards available.

---

### 4. Project Goals with STM32
With the STM32 controller, we want to achieve:

1. **Decode and send RS485/IBIS commands** to the displays.  
2. **Provide a user interface** (buttons, small display, or USB connection to PC).  
3. **Add flexibility**: ability to select text, line numbers, and control display behavior.  
4. **Future expansion**:  
   - WiFi/Ethernet for remote control  
   - SD card for custom message storage  
   - Touchscreen or web-based configuration  

---

### 5. Long-Term Vision
The STM32-based controller should become a **universal replacement** for the original bus system:
- Easy to build with off-the-shelf components  
- Well-documented, open, and customizable  
- Reusable in hobby, maker, or even professional transport projects  

This ensures that the LED displays can **live a second life**, far beyond their original bus applications.

---

### 6. Conclusion
The decision to design a new STM32-based controller is driven by the desire for **freedom, flexibility, and future-proofing**.  
Instead of being locked into outdated proprietary hardware, we can build a **modern, open platform** that makes these bus displays useful again — for prototyping, education, or creative projects.
