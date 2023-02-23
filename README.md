# Ender Klipper adventures

https://github.com/makerbase-mks/MKS-PI

After assembling the thingMKS-PI, connect it via ethernet.
Find the device via nmap:

    nmap -p 22 192.168.2.0/24

Log in via:

    ssh root@ipaddresss

The password is makerbase.

To setup WiFi do the following:

    apt install network-manager
    nmtui

Configure your wifi via `Activate a connection`.
Add these lines to `/etc/rc.local` to fix WiFi connection after reboot: 

    usb_modeswitch -v 0x0bda -p 0x8179 --reset-usb
    modprobe r8188eu rtw_power_mgnt=0

