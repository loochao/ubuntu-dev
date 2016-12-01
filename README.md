# ubuntu-dev
Dockerfile for calibre development based on ubuntu

# how to run with Xquarz
install Xquartz (X-Windows on MacOSX), allow connection (choose in preference)
socat TCP-LISTEN:6000,reuseaddr,fork UNIX-CLIENT:\"$DISPLAY\"

docker run -u 0 -e DISPLAY=192.168.1.227:0 -i -t -v /Volumes/DATA/Code/Code_SRC2/Python01_Calibre/:/mnt loochao/ubuntu-dev:0.4 /bin/bash
-u 0 means login as root
-v mount host dir to docker dir

docker ps -a: listed all the container
docker commit: add changes (which are called containers) to images
docker commit -m "Calibre compiled and installed, GUI OK with OSX XQuartz" -a "loochao" 987a loochao/ubuntu-dev:0.4


