# Shaktimaan Linux

> 'Rivers of power flowing everywhere. Fields of magnetism relating everything. This is your origin. This is your lineage.'
> - The Vijnana Bhairava Tantra

--- 

Based on another project generating RPI4 images with the `aarch64` kernel. 
## Build it

This Raspberry Pi OS is basically Alpine Linux with the `aarch64` kernel installed, this configuration is achieved using Docker containers, which provide reproducible environments
to build the images while isolating the build process from the system building them which mitigates potential harm caused by the build process or errors that were accidentally baked into it. 

The build process results in the creation of `Shaktimaan Linux` image files, which can then be flashed onto an SD card using your tool of choice (`dd` is great but `balena-etcher` is also an excellent option for fans of `GUI` environments).

To build Shaktimaan Linux, launch 

```bash

$ sudo docker-build-kernel && sudo docker-build-linux 


``` 

This runs the two wrapper scripts in the appropiate order, which each in turn run another script within the container. As mentioned above, this makes for a 

### Features

One advantage of using scripts to build `.img` files is that I was able t script out much of the initial set up of the pi on Alpine, meaning that I can get the OS into a state much closer to production before even burning it to the SD Card, saving me time after first boot!

Some of the things provisioned by the scripts are...

- default root 
- ethernet
- wifi
- bluetooth
- chronyd
- openssh server
- root partition 
- GPIO

### Coming Soon

When time permits me, I would like to add the following to the SD image itself 

- docker pre-installed
- variety of docker & docker-compose files in /opt
- simplified AwesomeWM GUI 


## Credit and Additional Reading

Based on the awesome work done on [Genepi](https://github.com/be-ys/Genepi). 

[Rapsberry Pi Kernel building](https://www.raspberrypi.org/documentation/linux/kernel/building.md).


[Alpine Linux](https://alpinelinux.org/).


