Please visit the BayLibre Product Page for more Informations about the ACME capes and probes : [http://baylibre.com/acme](http://baylibre.com/acme)

![ACME](https://avatars3.githubusercontent.com/u/19706065?v=3&s=300)

GitHub Project page : [https://github.com/baylibre-acme](https://github.com/baylibre-acme)

This project is to provide a reproductible, maintainable and functional Beaglebone Black images for the BayLibre ACME Cape using IIO as backend for Measurement transmission over network.

This image is targeted to be used using the following utilities : 
- PulseView or sigrok-cli using our specially crafted libsigrok with IIO support ([libsigrok](https://github.com/baylibre-acme/libsigrok))
- iio-capture to capture samples or min/max/avg on a sampling time ([iio-capture](https://github.com/BayLibre/iio-capture))
- Eventually any IIO enabled tools like "IIO Oscilloscope", see [wiki.analog.com/software/linux/docs/iio/iio](https://wiki.analog.com/software/linux/docs/iio/iio#pointers)
- acme-cli the new ACME control utility ([acme-cli](https://github.com/baylibre-acme/acme-cli))

**Warning:** This image is not compatible with the initial sigrok based release you can find at :
 * [acme wiki](http://wiki.baylibre.com/doku.php?id=acme:start)
The current *baylibre-acme* sigrok upstream driver will only work on this previous image release.

## Releases ##
**Warning** : This release is still in beta phase, some extended testing must be achieved
 * Initial Beta Release : [acme-beaglebone-black_b2](https://github.com/baylibre-acme/ACME/releases/tag/b2)

## Build Instruction ##

See [https://github.com/baylibre-acme/ACME](https://github.com/baylibre-acme/ACME)

**Warning** : Re-building is not the recommended way to use the ACME probes with the BeagleBone black, such instructions are given to give liberty to reports bugs or eventually personalize the system if needed

## Install Instruction ##

Simply copy the image file onto the microSD Card, under Linux run :
```
$ xzcat acme-beaglebone-black_b1-sdcard-image.xz | sudo dd of=/dev/mmcblk0 bs=1M
```

Insert the microSD Card into the BeagleBone Black slot, (optionally) connect an Ethernet cable to a DHCP backed LAN network and power it through USB.
When the LEDs blinks as an heartbeat, the system is up and running.

Using a system on the same local LAN network with Avahi or Bonjour installed, test the system connectivity by pinging the ACME board :
```
$ ping baylibre-acme.local
```

## Experimental Features ##
An USB Gadget interface with Network and Console links has been added along other personalization features.

Please refer at : [https://github.com/baylibre-acme/ACME#experimental-features](https://github.com/baylibre-acme/ACME#experimental-features)

## CLI Usage Instructions ##

The experimental Network CLI is available at [acme-cli](https://github.com/baylibre-acme/acme-cli)

The pyacmed server is provided in the latest ACME Yocto based images and works with this CLI software.

## Sigrok / PulseView Instructions

See [libsigrok](https://github.com/baylibre-acme/libsigrok) to install and use libsigrok with IIO on your system.

## iio-capture Instructions ##

See [iio-capture](https://github.com/BayLibre/iio-capture) to install and use the iio-caputure tool with the ACME probes.

## Bugs & Support ##

Please use the ACME project page to report any issues ([https://github.com/baylibre-acme/ACME/issues](https://github.com/baylibre-acme/ACME/issues))
