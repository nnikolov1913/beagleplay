# build the image
Prerequisites:

Install docker engine:
https://docs.docker.com/engine/install/

Install kas:
https://kas.readthedocs.io/en/latest/userguide.html

How to build:

kas-container should be used as the YAML files are written for such a usage.
After cloning this repo, execute these commands:
```
cd beagleplay
kas-container checkout beagleplay.yml
kas-container shell beagleplay.yml
```
After the last comand docker container should be started and promt should be inside it already.
In the container build the image:
```
bitbake core-image-minimal
```
After some time(usually it takes 1-2 hours or more) image should be ready in deploy-ti/images/beagleplay.
Name is somethig like core-image-minimal-beagleplay-XXXXXXXXXXX.rootfs.wic.xz.
Flash the image into a SD card using balenaetcher for example. Start it in Beagleplay while pressing the boot button.

