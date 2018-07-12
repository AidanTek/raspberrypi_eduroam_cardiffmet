# raspberrypi_eduroam_cardiffmet
A script to quickly setup Eduroam WiFi access for Cardiff Metropolitan University

## Instructions for use

Python3 is required, but should be included even in the most basic version of stetch. Download this repository and transfer the file eduroam_setup.py to the Raspberry Pi (should work on any current model). 

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

by Aidan Taylor. 2018. Cardiff Metropolitan University.

This code is in the public domain.
