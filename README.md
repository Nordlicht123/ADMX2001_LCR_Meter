# ADMX2001_LCR_Meter
Qt6 Sources for controlling an Analog Devices ADM2001 LCR meter with a Raspberry Pi 5 (8 GB) OS Ubuntu 23.10.

See also https://wiki.analog.com/resources/eval/user-guides/admx/eval-admx2001ebz

Install usefull tools:
1.  sudo apt-get install mc
2.  sudo apt-get install git
3.  sudo apt-get install minicom
4.  sudo apt-get install wget

Setup UART:
/boot/config.txt:
  //Config settings specific to arm64
1.  arm_64bit=1
2.  dtoverlay=uart0
3.  enable_uart=1
4.  dtparam=uart0=on

Check presence of ADMX2001:
1. sudo minicom -s
2.  +-----------------------------------------------------------------------+   
    | A - Serieller Anschluss      : /dev/ttyAMA0                           |   
    | B - Pfad zur Lockdatei       : /var/lock                              |   
    | C - Programm zur Rufannahme  :                                        |   
    | D - Programm zum Wählen      :                                        |   
    | E - Bps/Par/Bits             : 115200 8N1                             |   
    | F - Hardware Flow Control    : Nein                                   |   
    | G - Software Flow Control    : Nein                                   |   
    | H -     RS485 Enable      : No                                        |   
    | I -   RS485 Rts On Send   : No                                        |   
    | J -  RS485 Rts After Send : No                                        |   
    | K -  RS485 Rx During Tx   : No                                        |   
    | L -  RS485 Terminate Bus  : No                                        |   
    | M - RS485 Delay Rts Before: 0                                         |   
    | N - RS485 Delay Rts After : 0                                         |   
    |                                                                       |   
    |    Welchen Parameter möchten Sie ändern?                              |   
    +-----------------------------------------------------------------------+
3.  Speichern als »dfl«
4.  Verlassen
5.  Press enter
6.  Willkommen zu minicom 2.8
                                                                                
    Optionen: I18n                                                                  
    Port /dev/ttyAMA0, 23:36:56                                                     
                                                                                
    Drücken Sie CTRL-A  Z für Hilfe zu speziellen Tasten                            
                                                                                
    ADMX2001>   <=== successful ADMX2001 response

Install latest Updates:
1.  sudo apt-get update && sudo apt-get upgrade

Setup Qt6:
1.  sudo apt install clang
2.  sudo apt install libclang-dev
3.  sudo apt install build-essential libgl1-mesa-dev cmake libfontconfig1-dev libfreetype6-dev libx11-dev libx11-xcb-dev libxext-dev libxfixes-dev libxi-dev libxrender-dev libxcb1-dev libxcb-cursor-dev libxcb-glx0-dev libxcb-keysyms1-dev libxcb-image0-dev libxcb-shm0-dev libxcb-icccm4-dev libxcb-sync-dev libxcb-xfixes0-dev libxcb-shape0-dev libxcb-randr0-dev libxcb-render-util0-dev libxcb-util-dev libxcb-xinerama0-dev libxcb-xkb-dev libxkbcommon-dev libxkbcommon-x11-dev clang

4.  wget https://download.qt.io/official_releases/qt/6.7/6.7.0/single/qt-everywhere-src-6.7.0.tar.xz
5.  tar xf qt-everywhere-src-6.6.1.tar.xz
6.  cd qt-everywhere-src-6.6.1
7.  ./configure
8.  cmake --build . --parallel
9.  sudo cmake --install .

10.  sudo apt-get install qtcreator
