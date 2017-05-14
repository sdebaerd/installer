# installer
A Bash script to install everything related with [EV3Dev-lang-java](http://ev3dev-lang-java.github.io/)

## Motivation

[EV3Dev](http://www.ev3dev.org/) is a fantastic Complete Linux environment
to build software for robots. But as any technology, the installation
require some configuration to run in the right way.

This project tries to save time in this process.

The installer will install the following libraries & utilities:

+ Java JDK 8 (Only for BrickPi/PiStorms)
+ [BatteryMonitor](https://github.com/ev3dev-lang-java/batteryMonitor) (A Java utility to monitor the Battery)
+ OpenCV
+ RXTX (Library used on [RPLIDAR4J](https://github.com/ev3dev-lang-java/RPLidar4J))

## Getting Started

### Starting point:

The starting point to use this installer, is a Brick running
with EV3Dev and updated:

```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get dist-upgrade
sudo reboot
```

### EV3 Brick and Java

If you are using a EV3Brick, you will have to install Java JRE8 Manually.
Download the file: `ejdk-8-fcs-b132-linux-arm-sflt-03_mar_2014.tar.gz` from:
http://www.oracle.com/technetwork/java/embedded/downloads/javase/javaseemeddedev3-1982511.html
and copy the file the following route: `/home/robot/`

**Example:**

```
scp "/home/robot/ejdk-8-fcs-b132-linux-arm-sflt-03_mar_2014.tar.gz" "robot@192.168.1.85:/home/robot"
```

The Installer will manage later.

### Running the installer

```
cd /home/robot
mkdir installer
cd installer
wget -N https://raw.githubusercontent.com/ev3dev-lang-java/installer/develop/installer.sh
chmod +x installer.sh
sudo ./installer.sh
```


