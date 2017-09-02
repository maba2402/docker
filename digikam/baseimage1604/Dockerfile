FROM ubuntu:16.04
RUN apt-get update
RUN apt-get install -y software-properties-common 
RUN apt-get install -y python-software-properties
RUN add-apt-repository ppa:orangain/opencv

RUN apt-get update
RUN apt-get install -y firefox
RUN apt-get install -y git
RUN apt-get install -y g++
RUN apt-get install -y cmake
RUN apt-get install -y extra-cmake-modules 
RUN apt-get install -y qt5-default 
RUN apt-get install -y libfontconfig1
RUN apt-get install -y mesa-common-dev
RUN apt-get install -y gperf
RUN apt-get install -y sqlite3
RUN apt-get install -y libicu-dev
RUN apt-get install -y libkf5xmlgui-dev
RUN apt-get install -y libkf5i18n-dev
RUN apt-get install -y libkf5solid-dev
RUN apt-get install -y libkf5windowsystem-dev 
RUN apt-get install -y libkf5service-dev 
RUN apt-get install -y libkf5config-dev 
RUN apt-get install -y libkf5coreaddons-dev 
RUN apt-get install -y libqt5webkit5-dev 
RUN apt-get install -y docker.io 
RUN apt-get install -y xserver-xephyr
RUN apt-get install -y libqt5webkit5-dev
RUN apt-get install -y libqt5webkit5-dev 
RUN apt-get install -y libjpeg-dev 
RUN apt-get install -y libpng-dev
RUN apt-get install -y libtiff-dev 
RUN apt-get install -y libkf5wallet-dev
RUN apt-get install -y libkf5kiocore5 
RUN apt-get install -y kio-dev 
RUN apt-get install -y libkf5webkit-dev 
RUN apt-get install -y libkf5archive-dev 
RUN apt-get install -y libxml2-dev 
RUN apt-get install -y libxslt1-dev 
RUN apt-get install -y libthreadweaver4 
RUN apt-get install -y libmarble-dev 
RUN apt-get install -y libopencv-dev 
RUN apt-get install -y libopencv-objdetect-dev
RUN apt-get install -y libopencv-highgui-dev
RUN apt-get install -y libgtk2.0-dev
RUN apt-get install -y libgdk-pixbuf2.0-dev
RUN apt-get install -y libpng12-dev
RUN apt-get install -y libgdk-pixbuf2.0-dev
RUN apt-get install -y libgtk2.0-dev
RUN apt-get install -y libmarble-dev 
RUN apt-get install -y libopencv-dev 
RUN apt-get install -y liblcms2-dev 
RUN apt-get install -y libboost-graph-dev 
RUN apt-get install -y liblensfun-dev   
RUN apt-get install -y libsane-dev
RUN apt-get install -y zlibc
RUN apt-get install -y libssl-dev
RUN apt-get install -y libltdl-dev 
RUN apt-get install -y wget
RUN apt-get install -y make
RUN apt-get install -y sed
RUN apt-get install -y libkf5filemetadata-dev
RUN apt-get install -y libkf5threadweaver-dev
RUN apt-get install -y libkf5notifyconfig-dev
RUN apt-get install -y libkf5notifications-dev
RUN apt-get install -y libkf5akonadicontact-dev
RUN apt-get install -y libkf5calendarcore-dev
RUN apt-get install -y appstream



RUN groupadd --gid 1000 dockeruser && \
        useradd --uid 1000 --gid 1000 --create-home dockeruser
RUN mkdir /home/dockeruser/digikam

RUN cd /home/dockeruser/digikam && git clone git://anongit.kde.org/digikam-software-compilation dk && cd dk && export GITSLAVE=.gitslave.devel && ./download-repos

RUN mkdir -p /home/dockeruser/digikam/sqlite && \
    cd /home/dockeruser/digikam/sqlite && \
    wget https://www.sqlite.org/2017/sqlite-autoconf-3200000.tar.gz && \
    tar -xf sqlite-autoconf-3200000.tar.gz 

#Install latest version of ECM package
RUN mkdir -p /home/dockeruser/digikam/ecm &&\
    cd /home/dockeruser/digikam/ecm &&\
    git clone https://github.com/KDE/extra-cmake-modules.git &&\
    cd extra-cmake-modules &&\
    mkdir build &&\
    cd build &&\
    cmake .. &&\
    make &&\
    make install 

