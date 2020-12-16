# Shaktimaan Linux

> 'After the skatimaan is indistinguishable from the shakti'
> - The Vijnana Bhairava Tantra


Based on another project generating RPI4 images with the `aarch64` kernel. 
## Build it

This Raspberry Pi OS is basically Alpine Linux with the `aarch64` kernel installed, this configuration is achieved using the  

Generated Raspberry Pi 4 image is ready to burn to an SD card via [balenaEtcher](https://www.balena.io/etcher/)

### Features

The image automatically setup and configures:

* root user
* ethernet
* wifi
* bluetooth
* chronyd
* openssh server
* root partition auto-expand
* GPIO

To build Shaktimaan, launch 

``` 
sudo docker-build-kernel && sudo docker-build-linux 
``` 
## Informations

[Rapsberry Pi Kernel building](https://www.raspberrypi.org/documentation/linux/kernel/building.md).


Based on the awesome work done on [Genepi](https://github.com/be-ys/Genepi). 

[Alpine Linux](https://alpinelinux.org/).


