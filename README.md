# ADMX2001_LCR_Meter
Qt6 Sources for controlling an Analog Devices ADM2001 LCR meter with a Raspberry Pi 5 (8 GB) under Ubuntu 23.10.

Latest Updates:
sudo apt-get update && sudo apt-get upgrade

Usefull tools:
sudo apt-get install mc
sudo apt-get install git
sudo apt-get install minicom
sudo apt-get install wget

Setup Qt6:
sudo apt install clang
sudo apt install libclang-dev
sudo apt install build-essential libgl1-mesa-dev cmake libfontconfig1-dev libfreetype6-dev libx11-dev libx11-xcb-dev libxext-dev libxfixes-dev libxi-dev libxrender-dev libxcb1-dev libxcb-cursor-dev libxcb-glx0-dev libxcb-keysyms1-dev libxcb-image0-dev libxcb-shm0-dev libxcb-icccm4-dev libxcb-sync-dev libxcb-xfixes0-dev libxcb-shape0-dev libxcb-randr0-dev libxcb-render-util0-dev libxcb-util-dev libxcb-xinerama0-dev libxcb-xkb-dev libxkbcommon-dev libxkbcommon-x11-dev clang

wget https://download.qt.io/official_releases/qt/6.7/6.7.0/single/qt-everywhere-src-6.7.0.tar.xz
tar xf qt-everywhere-src-6.6.1.tar.xz
cd qt-everywhere-src-6.6.1
./configure
cmake --build . --parallel
cmake --install .

sudo apt-get install qtcreator
