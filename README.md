# WSL-OpenCV
WSL-OpenCV

############################## Enable UVC Camera Support in WSL Kernel ################################

#https://www.youtube.com/watch?v=t_YnACEPmrM&ab_channel=AgileDevArt

#https://zenn.dev/pinto0309/articles/e1432253d29e30

#https://github.com/PINTO0309/wsl2_linux_kernel_usbcam_enable_conf

#https://olof-astrand.medium.com/compiling-your-own-wsl2-kernel-4428d5258578

#https://gist.github.com/tatumroaquin/b51d16be877d66de9bd3c1bac94faec9

#https://github.com/dorssel/usbipd-win/wiki/WSL-support

#https://zenn.dev/pinto0309/articles/e1432253d29e30



########################## Compile OpenCV from Source on WSL Ubuntu24.04.1 ############################

#https://github.com/Eemilp/install-opencv-on-wsl

#https://docs.opencv.org/4.10.0/d7/d9f/tutorial_linux_install.html

#https://stackoverflow.com/questions/37188623/ubuntu-how-to-install-opencv-for-python3

#https://phoenixnap.com/kb/installing-opencv-on-ubuntu#ftoc-heading-2


sudo apt-get update
sudo apt-get install build-essential
sudo apt-get install cmake
sudo apt-get install git

sudo apt-get install pkg-config libgtk-3-dev
sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev libxvidcore-dev libx264-dev
sudo apt-get install libjpeg-dev libpng-dev libtiff-dev gfortran openexr libatlas-base-dev
sudo apt-get install python3-dev python3-numpy libtbb2 libtbb-dev libdc1394-22-dev

sudo apt-get install libjpeg8-dev libtiff5-dev libpng-dev libavcodec-dev libavformat-dev libswscale-dev libv4l-dev

sudo apt-get update && sudo apt-get install -y cmake g++ wget unzip

cd /usr/src/

#sudo git clone https://github.com/opencv/opencv.git

#sudo git clone https://github.com/opencv/opencv_contrib.git

sudo wget -O opencv.zip https://github.com/opencv/opencv/archive/4.x.zip

sudo wget -O opencv_contrib.zip https://github.com/opencv/opencv_contrib/archive/4.x.zip

sudo unzip opencv.zip

sudo unzip opencv_contrib.zip

#cd ./opencv

#sudo git checkout 4.10.0

#cd ../opencv_contrib

#sudo git checkout 4.10.0

#cd ..

sudo mkdir -p build

cd build

sudo cmake -D CMAKE_BUILD_TYPE=Release -D OPENCV_GENERATE_PKGCONFIG=ON -D OPENCV_ENABLE_NONFREE=ON -D INSTALL_C_EXAMPLES=ON -D INSTALL_PYTHON_EXAMPLES=ON -D BUILD_EXAMPLES=ON -D OPENCV_EXTRA_MODULES_PATH=../opencv_contrib-4.x/modules -D BUILD_opencv_legacy=OFF  -D OPENCV_EXTRA_MODULES_PATH=../opencv_contrib-4.x/modules ../opencv-4.x

#sudo cmake -D CMAKE_BUILD_TYPE=Release -D OPENCV_GENERATE_PKGCONFIG=ON -D OPENCV_ENABLE_NONFREE=ON -D INSTALL_C_EXAMPLES=ON -D INSTALL_PYTHON_EXAMPLES=ON -D BUILD_EXAMPLES=ON -D OPENCV_EXTRA_MODULES_PATH=../opencv_contrib-4.x/modules -D BUILD_opencv_legacy=OFF  -D OPENCV_EXTRA_MODULES_PATH=../opencv_contrib/modules ../opencv

#sudo cmake --build ./

sudo make -j5

sudo make install -j5

pkg-config --modversion opencv4

nano ~/.bashrc

# put this at the bottom of .bashrc file

#OpenCV include path for gcc
CPLUS_INCLUDE_PATH=/usr/local/include/opencv4
export CPLUS_INCLUDE_PATH


#########################################################################################

%userprofile%\AppData\Local\Packages\

WSL-Kernel : https://github.com/microsoft/WSL2-Linux-Kernel

enable wsl kernel driver .config patch : https://github.com/PINTO0309/wsl2_linux_kernel_usbcam_enable_conf

Windows Side usbipd driver : https://github.com/dorssel/usbipd-win

kernel compile instructions :

https://github.com/PINTO0309/wsl2_linux_kernel_usbcam_enable_conf

https://olof-astrand.medium.com/compiling-your-own-wsl2-kernel-4428d5258578

https://github.com/Eemilp/install-opencv-on-wsl

https://github.com/dorssel/usbipd-win/wiki/WSL-support

https://zenn.dev/pinto0309/articles/e1432253d29e30

https://learn.microsoft.com/en-us/community/content/wsl-user-msft-kernel-v6

https://gist.github.com/tatumroaquin/b51d16be877d66de9bd3c1bac94faec9

https://medium.com/@dufresne.danny/usb-webcam-wls2-setup-gvcuview-cheese-opencv-c-b4b5bc43df29

https://devblogs.microsoft.com/commandline/connecting-usb-devices-to-wsl/


https://superuser.com/questions/1714345/change-of-wsl-installation-location

https://learn.microsoft.com/en-us/windows/wsl/wsl-config

https://dev.to/naruaika/using-opencv-on-windows-subsystem-for-linux-1ako


https://developer.ridgerun.com/wiki/index.php/Compiling_OpenCV_from_Source

https://docs.opencv.org/4.10.0/d7/d9f/tutorial_linux_install.html

https://docs.opencv.org/4.x/d7/d9f/tutorial_linux_install.html

https://phoenixnap.com/kb/installing-opencv-on-ubuntu

https://www.geeksforgeeks.org/how-to-install-opencv-in-ubuntu/


https://github.com/opencv/opencv

install using pip : https://data-flair.training/blogs/install-opencv-on-ubuntu/

https://zenn.dev/pinto0309/articles/e1432253d29e30

https://askubuntu.com/questions/1384456/usbipd-not-found-for-kernel-when-using-usb-ip-with-wsl

https://stackoverflow.com/questions/72255353/wsl-webcam-usb-can-not-open-camera-by-index

https://stackoverflow.com/questions/65939167/problem-using-opencv-in-wsl-when-opening-windows

https://www.youtube.com/watch?v=k3PcVruvZCs&ab_channel=ProgrammingHero

https://www.youtube.com/watch?v=vJWzH_2F64g&ab_channel=ProgrammingHero

#################################################

sudo apt-get purge libopencv-dev libopencv-python libopencv-samples libopencv*

sudo apt-get install build-essential cmake git libgtk-3-* pkg-config libavcodec-dev libavformat-dev libswscale-dev python-dev-is-python3

sudo apt-get install gstreamer1.0*
sudo apt-get install ubuntu-restricted-extras
sudo apt-get install libgstreamer1.0-dev libgstreamer-plugins-base1.0-dev

sudo apt-get install libgl1-mesa-glx
sudo apt-get install xdg-utils



