This project is a port of OpenXcom for Android.

OpenXcom: http://openxcom.ninex.info

The port uses a port of SDL for android: http://www.anddev.org/code-snippets-for-android-f33/sdl-port-for-android-sdk-ndk-1-6-t9218.html

Development for this port is being done on Linux, but you could get this working on Windows assuming you had a Unix environment setup like cygwin.  

Setup Instructions:
------------------
1. Download and install android SDK
2. Download and install CrystaX android NDK: http://smartctl.net/android/ndk-r4.php
3. Clone the repository.
4. Run git submodule init.
5. Run git submodule update.  You will need to run this again in the future when the submodules update.
6. Go to the sdl_android/project directory and run android update project -p .
7. Uncomment the line in sdl_android/build.sh for adding the CrystaX NDK to your path.  Make sure this line is pointing to your install of the Crystax NDK.

Build Instructions:
------------------
1. Make sure you have an emulator or device running.
2. Run sdl_android/build.sh.  When this completes, the apk will be installed to your device.

Run Instructions:
------------------
1. When you run the application the first time, you will be prompted with some SDL configuration options.  The MIDI support and game language data
   need to be installed to the sd card.  This is done with the default options.
2. You will need to add your Xcom game data to the sd card.  After running the game for the first time, you will have a /sdcard/app-data/com.sirnacnud.openxcom/DATA/
   folder, put your Xcom game data in this folder.

Notes:
------------------
* Game currently runs at 320x240, but will be scaled to fit your screen, aspect ratio isn't maintained.
