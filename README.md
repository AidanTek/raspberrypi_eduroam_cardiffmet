# raspberrypi_eduroam_cardiffmet
A script to quickly setup Eduroam WiFi access for Cardiff Metropolitan University

## Instructions for use

Python3 is required, but should be included even in the most basic version of Raspbian OS. Download this repository and transfer the file eduroam_setup.py to the Raspberry Pi (should work on any current model). 

You can download the files in this repository and transfer them to your Raspberry Pi with a USB stick, or you can initially connect your Raspberry Pi with an ethernet cable, then you can clone this repo directly with the CLI command:

```
git clone https://github.com/AidanTek/raspberrypi_eduroam_cardiffmet.git
```

All you need to do is open your CLI (e.g. Terminal) and change (cd) or point to the repository directory so that you can access eduroam_setup.py. Run the script with the command:

```
sudo python3 eduroam_setup.py
```

Follow the instructions in the script - you will need your Eduroam login credentials. Once you have entered them, the Pi will reset automatically.

Please be aware/assured that your password will not appear on screen and is hashed securely by the script!

The following files will be created or modified by this script:
* /etc/wpa_supplicant/wpa_supplicant.conf
* /lib/dhcpcd/dhcpcd-hooks/10-wpa_supplicant *(optional)*
* /etc/ca_certificates/ca.pem

---

*There was initially a change in Raspbian Buster that broke this script, it took me some time too find it, but now there is an option to fix the offending file which is found in /lib/dhcpcd/dhcpcd-hooks/10-wpa_supplicant - however I am not sure if this fix is still needed. You might also want to fix it manually if you know how, find the line that says
```
wpa_supplicant_driver="${wpa_supplicant_driver:-wext,nl80211}"
```

and swap the last two words so it ends with nl80211,wext
* 

*If you are based at a different University, check to see if your IT department offer a solution for Raspberry Pi access. This code will not work for you because the included Eduroam Certificate is unique to this institution - however, it is not too difficult to modify the script to include the certificate provided to your institution, please consult with your IT department first!* 

**by Aidan Taylor. 2018 (updated 2021). Cardiff Metropolitan University.**

This code is in the public domain. You alone are responsible for your use of this script and your use of the Raspberry Pi on the network. 
