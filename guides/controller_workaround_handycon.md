## How to install Handycon - Controller Workaround w/ Steam/QAM

### Introduction
This guide will show you how to install handycon, the current and most stable workaround for steam controls and Steam/QAM Menu functionality.

### Step 1

Clone the github repository containing the current Legion Go changes/updates. This is currently awaiting a PR into the official repo but for now you can download and install the Legion Go fork instead...

```mkdir src```
```cd src```
```git clone https://github.com/aarron-lee/HandyGCCS.git```
```cd HandyGCCS```
```sudo pikaur -S python-setuptools python-build python-wheel python-installer```
```sudo ./build.sh```
```sudo systemctl daemon-reload```
```sudo systemctl restart handycon```

### Step 2

Reboot your device! 

```sudo systemctl reboot```

Once its booted back up you should have Handycon Controls with working Steam/QAM menus!

### Disclaimer

The buttons will not work on their own, but the Legion+X and Legion+A buttons should work just fine. By default, at the time of writing this, they control the On Screen Keyboard and Quick Access Menu, but if you want Legion+X to open the Steam Menu instead, as Legion+B is not currently working, perform the following steps...

```sudo nano /etc/handygccs/handygccs.conf```

Then change button 4 from its current value of "OSK" the following instead...

```
button4 = MODE
```

then simply ```sudo systemctl restart handycon``` and ```sudo systemctl reboot```