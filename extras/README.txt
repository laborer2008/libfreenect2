This directory holds some extras for compiling with the NVIDIA Jetson TK1.

90-kinect2.rules is for the udev permissions
usbfs.patch patches MAX_ISO_BUFFER_LENGTH to be 49152. The default does not work on the Jetson with a Renasis USB mini PCIE card.
turbojpeg.h is the header file for libjpegturbo. It is included in opencv-dev, but not in the libopencv4tegra-dev. libjpegturbo is installed in the normal libfreenect2, so it needs a header to compile against.


