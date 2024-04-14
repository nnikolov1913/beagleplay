# build the image
Prerequisites:

Install docker engine:
https://docs.docker.com/engine/install/

Install kas:
https://kas.readthedocs.io/en/latest/userguide.html

kas-container checkout beagleplay.yml

kas-container shell beagleplay.yml

bitbake core-image-minimal

