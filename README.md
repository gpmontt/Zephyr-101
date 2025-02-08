# Zephyr-101
workbook to record my progres with ZephyRTOS

# Working with application
First we need on Zephyr a structure folder to work in a proper  way. 

A Zephyr application directory has the following components: 

- CMakeLists.txt: your build settings configuration file – this tells west (really a cmake build system under the hood) where to find what it needs to create your firmware. For more advanced projects, it’s also used for debug settings, emulation, and other features.
- prj.conf: the Kernel configuration file. For most projects, it tells Zephyr whether to include specific features for use in your application code – if you use GPIO, PWM, or a serial monitor, you’ll need to enable them in this file first. 
- src/main.c: your custom application code – where the magic happens! It’s advisable to put all of your custom source code in a 
src/ directory like this so it doesn’t get mixed up with your configuration files.

- Optional boards/ or soc/ overlay directories: in some cases, the board or even the specific MCU chip you want to use might not be supported yet in Zephyr. If this is the case, you can create your own definitions in your custom projects. It’s out of the scope of this starting tutorial, but it’s a good option to know about. 

# how to build and run Zephyr OS
go to your zeohyr_base folder and run the following command: 
```bash 
cd ~/zephyrproject
west --version
mkdir applications
cd applications
cp ~/zephyrproject/zephyr/samples/basic/blinky/{CMakeLists, src/main.c, prj.conf} .
cd ~/zephyrproject/applications/
west build -p auto -b samr21_xpro -s .
```

