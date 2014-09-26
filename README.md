How to cross compile driver

For simplicity let's assume that you work in folder called GIT

Downloading source (pick different git branches if you are not compiling for current master)

0. create enter GIT folder 

1. Clone this repository.

git clone --depth=1 https://github.com/daber/rtl8188eu.git

2. Clone raspbery pi kernel source

git clone --depth=1 https://github.com/raspberrypi/linux.git

3. Clone build tools

git clone --depth=1 https://github.com/raspberrypi/tools.git

4. Clone build firmware

git clone --depth=1 https://github.com/raspberrypi/firmware.git


After steps 0-4 you should have following structure:
GIT
|-/linux
|-/rtl8188eu
|-/tools
|-/firmware
   
5. go to GIT/rtl8188eu folder. Then into that folder copy /proc/config.gz file from your raspberry PI (use ethernet and SCP or copy proc/config.gz to sdcard and use card reader to copy)

6. in rtl8188eu folder run "make" command

7. Copy out dir back to RPi

8. On RPI enter out folder then sudo ./install.sh. -after that donle should start blinking.
