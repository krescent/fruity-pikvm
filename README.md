# Fruity PiKVM

This is an experimental script in an attempt to port PiKVM installation to other SBCs such as OrangePi, BananaPi, MangoPi etc..
it is based on the original raspberry pikvm software which can be found [HERE](https://pikvm.org/)


This script was tested on OrangePi Zero 2, a working OS image for OrangePi Zero 2 can be downloaded [HERE](https://github.com/jacobbar/fruity-pikvm/releases/download/os-images/Orangepizero2_2.2.2_ubuntu_jammy_server_linux5.13.0.zip)

At the moment this script supports architecture arm64/aarch64 and armhf/armv7l, and should work with any debian based distribution such as Ubuntu, Debian, Armbian etc...

## Installation
Install git, clone and run the script with the following code

```bash
sudo apt install -y git
git clone http://github.com/jacobbar/fruity-pikvm
cd fruity-pikvm
sudo ./install.sh
```
## MSD KVMD Patch
Befor applying the patch, you would need to resize your SD card and create a new partition, finally you need to add the new partition to /etc/fstab

Applying the MSD KVMD patch
```
sudo ./msd-patch.sh
```
to enable msd after applying the patch you would need to comment out the msd override configuration in file /etc/kvmd/override.yaml
