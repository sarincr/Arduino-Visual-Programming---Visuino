# Arduino-Visual-Programming---Visuino
Arduino Visual Programming using Visuino




HOW TO BUILD
============

The project needs Qt5 and qmake to build properly. It supports Linux,
Windows and Mac platforms.


Qt Creator
----------

The easiest way to build the project is using Qt Creator. Install a
recent version with Qt5 support. Then open the project file src.pro
and build.

Command line
------------

```
$ qmake
$ make
```


Debian-based system
-------------------

The project comes with debian build rules, in debian/ folder. To build it,
install the required dependencies.

```
$ sudo apt-get install qtbase5-dev qt5-qmake libqt5webkit5-dev \
    libqt5serialport5-dev qttools5-dev-tools libudev-dev \
    build-essential debhelper
$ dpkg-buildpackage
```

Fedora-based system
-------------------

Install the required dependencies in Fedora

```
$ sudo dnf install qt-devel qt5-qtserialport-devel qt5-linguist qt5-qtwebkit-devel
```

Then open the ts.pro archive and change all "lupdate" by "lupdate-qt5"
and all "lrelease" by "lrelease-qt5". Save changes
In the console type:

```
$ make
$ make install 
```

If no errors appear then write 

```
$ sudo mkdir /usr/share/visualino/ && cp -r roboblocks/html/ /usr/share/visualino/
```
from the Visualino directory.
