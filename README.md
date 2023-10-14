# piantor
My Piantor keyboard related stuff



# Specs

Model: Beekeep Piantor V2
Controller: WeAct RP2040 (Black - USB-C 2MB Flash Memory)
Number of Keys: 42 Keys
Key Switch: Choc Red Pro (Linear 35gf)
Keycap: MBK Blank Black
Plate / Case: Red PLA

Keyboard specs: https://docs.beekeeb.com/piantor-keyboard

# The Building Blocks: how does it all work?

## The firmware

On a highlevel things work like this: your keyboard has a firmware that is able to take in keyboard configuration files and make it work.

## Flashing firmware with UF2

In the context of keyboards, flashing means writing a new firmware to the keyboard's controller - the microcontroller that interprets key presses and communicates with the computer. This can allow you to customize the layout, functions, and behavior of the keys. UF2 stands for USB Flashing Format. The RP2040 is easy to program, thanks the UF2 bootloader. With the UF2 bootloader, the RP2040 shows up on your computer as a USB storage device without having to install drivers for Windows 10, Mac, and Linux! Flashing is simply copying the UF2 file to the device.

## QMK is the firmware

QMK is a powerful firmware that provides the foundation for keyboard customization. It allows you to redefine what each key on your keyboard does, create multi-key macros, layer configurations, and more. However, to configure QMK, you typically need to edit the firmware's code directly, which can be complicated and intimidating for users without programming experience.

## VIAL is the QMK bundler

VIAL, on the other hand, is a configuration tool that provides a user-friendly graphical interface for customizing your keyboard. It's designed to work with keyboards that use QMK firmware, and it simplifies the process of customizing your keyboard by allowing you to make changes through its interface rather than editing code. It allows you to make changes realtime without separate flashing step.

In other words, QMK is the firmware that runs on your keyboard and controls how it operates, and VIAL is a tool that makes it easy to customize that firmware. When a keyboard is said to be "VIAL compatible" or "VIAL enabled", it means that the QMK firmware on the keyboard has been modified to work with the VIAL configurator.

So, to use VIAL, you would flash your keyboard with a version of QMK firmware that has been modified to include VIAL functionality. This allows you to use the VIAL GUI for customization, while the QMK firmware is still what's actually running on your keyboard and controlling its operation.

# Starting from scratch

Download and flash the `beekeeb_piantor_weact_vial.uf2` from https://docs.beekeeb.com/piantor-keyboard (or from this REPO).

Firmware
it is running VIAL as firmware?
But VIAL is also a config GUI tool? https://get.vial.today/
