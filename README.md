# Custom-Robotics-Control-Platform
Personal Project created as a cost-effective, robust, and user-friendly electronics controller to increase hobbyist access to high-quality robotics systems

<img width="331" height="311" alt="image" src="https://github.com/user-attachments/assets/d85fb4dd-17d9-4d74-bb8e-f28a4797a5a7" />

Picture of Board With Completed Reflow (Version 1)

# Hardware Summary
This is a custom PCB I am designing for a new advanced robotics project. The goal is to
create a cheaper version of cargo delivery robots for more static and predictable
environments, such as a college campus, a factory, or an office building. As of right now
it is not intended to make it road/street worthy, but if the effort is minimal to elevate it to
that level, it should be possible. The Board itself is 4 layers, and 100mm x 100mm has
multiple features including: Over current detection and hardware shutoff, multiple highly
filtered power domains (1.8V, 3.3V, 5V, A standby 5V, a Secondary 5V in case of
emergency, 12V, and 17V), two high Amperage motor drivers (17V at 10A max), an
integrated high pin count MPU with analog, PWM, I2C, and many other programmable
data transfer methods, an integrated AI Google Coral Edge TPU with 4 TOPS connected
through PCIe to a controller board, logic level shifts for GPIO to allow for 5V and 3.3V
digital inputs, a slot to plug in a standardized SBC with the form factor of a Raspberry Pi,
in my case it will be the Radxa Rock 5C, a block of N-Channel mosfet switches
connected to GPIO to turn off outside devices, and lastly a USB that connects to the
MPU to allow for connection between the SBC, or any other outside computer. The final
prototype cost board was ~$84, which to my knowledge, is a major success considering
the features and functionality.

# Firmware Summary
Firmware development has begun, and a few features have been added to ensure ease of
use. A function for PWM has been created to allow for customization, including
an easy modification of PWM frequency, pulse width, and pin activation. On top of this
I2C protocols have been implemented that automatically scans the address for connected
devices and inititiates communication protocols without the need for user definition.
Lastly, USB drivers and communication have been implemented allowing for debugging to
be completed without the need for a JTAG connector.
