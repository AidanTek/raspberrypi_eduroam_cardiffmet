# raspberrypi_eduroam_cardiffmet
A script to quickly setup Eduroam WiFi access for Cardiff Metropolitan University

## Instructions for use

Python3 is required, but should be included even in the most basic version of stretch. Download this repository and transfer the file eduroam_setup.py to the Raspberry Pi (should work on any current model). 

You can transfer with a USB stick, or if you can initially connect with an ethernet cable then you can clone this repo directly to the Raspberry Pi with the CLI command:

```
git clone https://github.com/AidanTek/raspberrypi_eduroam_cardiffmet.git
```

Then all you need to do is open your CLI and point it to the directory with eduroam_setup.py. Run the script with the command:

```
sudo python3 eduroam_setup.py
```

Follow the instructions in the script - you will need your Eduroam login credentials. Once you have entered them, the Pi will reset automatically.

Please be aware/assured that your password is hashed securely by the script!

---

*If you are based at a different University, check to see if your IT department offer a solution for Raspberry Pi access. This code will not work for you because the included Eduroam Certificate is unique to this institution - however, it is not too difficult to modify the script to include the certificate provided to your institution, please consult with your IT department first!* 

**by Aidan Taylor. 2018. Cardiff Metropolitan University.**

This code is in the public domain. You alone are responsible for your use of this script and your use of the Raspberry Pi on the network. 
