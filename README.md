# complie-openjdk8
complie openjdk8 step

<h1>step 1 before complie perpare</h1>
OS: ubuntu 14.04</br>
complie support jdk: jdk1.7</br>
complie support lib:</br>
sudo apt-get install libx11-dev libxext-dev libxrender-dev libxtst-dev libxt-dev libcups2-dev libfreetype6-dev libasound2-dev

<h1>step 2 complie openjdk8</h1>
create file builld.sh and write complie script
bash ./configure --with-target-bits=64 --with-boot-jdk=/usr/local/tools/jdk1.7.0_80/ --with-debug-level=slowdebug --enable-debug-symbols ZIP_DEBUGI    NFO_FILES=0
make all ZIP_DEBUGINFO_FILES=0 DISABLE_HOTSPOT_OS_VERSION_CHECK=OK #Bash





