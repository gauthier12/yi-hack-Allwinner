<p align="center">
	<img height="200" src="https://i.imgur.com/5oxxpmD.png">
</p>

yi-hack-Allwinner is a modification of the firmware for the Allwinner-based Yi Camera platform.

## Table of Contents
- [Table of Contents](#table-of-contents)
- [Installation](#installation)
  - [Update Procedure](#update-procedure)
- [Contributing](#contributing)
- [Features](#features)
- [Performance](#performance)
- [Supported cameras](#supported-cameras)
- [License](#license)
- [Disclaimer](#disclaimer)
- [Donation](#donation)


## Installation

### Update Procedure
1. Format an SD Card as FAT32. It's recommended to format the card in the camera using the camera's native format function.
2. Download the latest release from [the Releases page](https://github.com/roleoroleo/yi-hack-Allwinner/releases)
3. Extract the contents of the archive to the root of your SD card.
4. Insert the SD Card and reboot the camera
5. Wait for the camera to update. It will reboot a couple of times as the camera is rooted and the new firmware is applied. It will take a few minutes to update. Once the light is solid blue for at least a minute it is complete.


## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

---

## Features
This custom firmware contains features replicated from the [yi-hack-MStar]() project and similar to the [yi-hack-v4](https://github.com/TheCrypt0/yi-hack-v4) project.

- FEATURES
  - RTSP server - allows a RTSP stream of the video (high and/or low resolution) but without audio.
    - rtsp://IP-CAM/ch0_0.h264        (high res)
    - rtsp://IP-CAM:8554/ch0_1.h264   (low res)
  - ONVIF server (with support for h264 stream, snapshot, ptz and presets - standardized interfaces for IP cameras.
  - Snapshot service - allows to get a jpg with a web request.
    - http://IP-CAM:8080/cgi-bin/snapshot.sh?res=low&watermark=yes        (select resolution: low or high, and watermark: yes or no)
    - http://IP-CAM:8080/cgi-bin/snapshot.sh        (default high without watermark)
  - MQTT - Motion detection through mqtt protocol.
  - Web server - web configutation interface (port 8080).
  - SSH server - dropbear.
  - Telnet server - busybox.
  - FTP server.
  - Authentication for HTTP, RTSP and ONVIF server.
  - Proxychains-ng - Disabled by default. Useful if the camera is region locked.
  - The possibility to change some camera settings (copied from official app):
    - camera on/off
    - video saving mode
    - detection sensitivity
    - status led
    - ir led
    - rotate
  - Management of motion detect events and videos through a web page.
  - PTZ support through a web page (if the cam supports it).
  - The possibility to disable all the cloud features.
  - Online firmware upgrade

## Performance

The performance of the cam is not so good (CPU, RAM, etc...). Low ram is the bigger problem.
If you enable all the services you may have some problems.
For example, enabling both rtsp streams is not recommended.

## Supported cameras

Currently this project supports only the following cameras:

| Camera | Firmware | File prefix | Remarks |
| --- | --- | --- | --- |
| **Yi 1080p Home 9FUS** | 8.2.0* | y20gam | - |
| **Yi 1080p Home BFUS** | 8.2.0* | y20gam | - |

USE AT YOUR OWN RISK.

**Do not try to use a fw on an unlisted model**

**Do not try to force the fw loading renaming the files**

----

## License
[MIT](https://choosealicense.com/licenses/mit/)

## DISCLAIMER
**NOBODY BUT YOU IS RESPONSIBLE FOR ANY USE OR DAMAGE THIS SOFTWARE MAY CAUSE. THIS IS INTENDED FOR EDUCATIONAL PURPOSES ONLY. USE AT YOUR OWN RISK.**

## Donation
If you like this project, you can buy Roleo a beer :) 
[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=JBYXDMR24FW7U&currency_code=EUR&source=url)
