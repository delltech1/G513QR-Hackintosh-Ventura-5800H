
# G513QR Hackintosh-Ventura-5800H
 Ventura for Asus Rog Strix G513QR with Ryzen 5800H

BIOS settings:

Enable Virtualization Support
Disable Secure-Boot

My config is:
5800H, 32gb of memory, RTX 3070, VEGA as iGPU
Wifi: AX200
2xNvME

There are 2 folders:

1st one called Pre-Install is for the OS installation, once everything is up and running use the EFI folder from the POST-Install folder and copy
it to your bootable USB
2nd EFI folder includes Kext for GPU acceleration (VEGA Support)

To build your ACPI files:

Follow Dortanias manual for ACPI, it was pretty simple. 
Basically all files in the ACPI folder can be generated with SSDTimemaster in Windows under couple minutes and just copy / overwrite your files
having the same name in the EFI/ACPI folder on your USB.

Follow Dortanias manual how to correctly format USB drive, i am using the Rufus method.
Dont forget to install Python 3 on your Windows Box.

Download the correct Recovery (ventura) - for this you have to download Open Core, macrecovery folder and use the python code from Dortanias website.
This will generate the mac recovery files and folder, which you will just copy / paste to the root of the USB Stick.
Afterwards just COPY EFI folder directly to ROOT of the USB, so you have just 2 folders - recovery + EFI folder in the root of the USB stick. 


Reboot F2 - F8 and boot from USB and select the DMG recovery and start installation. 
Should you see panics for NVME, you will have to use the DISABLE NVME method with SSDT - PRE Installer folder contains AML i used to disable my primary NVME for Windows.

What works:
OS, Wifi, Bluetooth (Probably) - not yet tested, didnt have time and GPU acceleration, still in early stage, but at least its something.

