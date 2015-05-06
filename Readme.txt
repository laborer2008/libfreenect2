2-26-15

Here is a list of modifications to this repository for installation on the NVIDIA Jetson TK1.

1. In the original instructions, the user is instructed to install opencv-dev. On the Jetson, this removes the accelerated opencv4tegra libraries. Therefore, opencv-dev is not installed.

2. Not installing opencv-dev means that 'turbojpeg.h' is not installed. This file is included in the 'extras' folder and placed into the nv_headers folder during installation.

3. The folder 'nv_headers' is placed into the depends folder. nv_headers contains the header for gstjpeg library. 

4. libusb has issues when the default MAX_ISO_BUFFER_LENGTH size in usb_src usbfs.h. The 'extras' folder has a patch that changes the default size.

5. The 'udev' rules adds 90-kinect2.rules to give permission for the Kinect V2 to run

6. The demo Protonect is changed slightly to add a color mapped depth image. These colormap map be changed by hitting a number key while the demo is running.

7. A copy of 'installLibfreenect2.sh' is included in the 'extras' directory
