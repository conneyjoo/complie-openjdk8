# complie-openjdk8
complie openjdk8 step

### step 1 before complie perpare
OS: ubuntu 14.04</br>
complie support jdk: jdk1.7</br>
complie support lib: libx11-dev libxext-dev libxrender-dev libxtst-dev libxt-dev libcups2-dev libfreetype6-dev libasound2-dev</br>
install lib
```Bash
sudo apt-get install libx11-dev libxext-dev libxrender-dev libxtst-dev libxt-dev libcups2-dev libfreetype6-dev libasound2-dev

### step 2 complie openjdk8
create file builld.sh and write complie script
```Bash
bash ./configure --with-target-bits=64 --with-boot-jdk=/usr/local/tools/jdk1.7.0_80/ --with-debug-level=slowdebug --enable-debug-     symbols ZIP_DEBUGI    NFO_FILES=0
make all ZIP_DEBUGINFO_FILES=0 DISABLE_HOTSPOT_OS_VERSION_CHECK=OK #Bash


