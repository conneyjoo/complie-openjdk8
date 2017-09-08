# complie-openjdk8
complie openjdk8 step

### step 1 before complie perpare
OS: ubuntu 14.04</br>
complie support jdk: jdk1.7</br>
complie support lib: libx11-dev libxext-dev libxrender-dev libxtst-dev libxt-dev libcups2-dev libfreetype6-dev libasound2-dev</br></br>
* download and install jdk1.7
* install lib script
```Bash
sudo apt-get install libx11-dev libxext-dev libxrender-dev libxtst-dev libxt-dev libcups2-dev libfreetype6-dev libasound2-dev
```

### step 2 complie openjdk8
create file builld.sh and write complie script
```Bash
bash ./configure --with-target-bits=64 --with-boot-jdk=/usr/local/tools/jdk1.7.0_80/ --with-debug-level=slowdebug --enable-debug-symbols ZIP_DEBUGINFO_FILES=0
make all ZIP_DEBUGINFO_FILES=0 DISABLE_HOTSPOT_OS_VERSION_CHECK=OK #Bash
```
exec ./build.sh start compling... 
```Bash
./build.sh
```

### step 3 test openjdk8
new file hello.java
```Bash
cd build/linux-x86_64-normal-server-slowdebug/jdk/bin
./javac hello.java
./java hello
hello world
```

### step 4 gdb openjdk8
setting env
```Bash
export LD_LIBRARY_PATH=/root/workspace/openjdk/build/linux-x86_64-normal-server-slowdebug/hotspot/linux_amd64_compiler2/debug
```
gdb java
```Bash
cd build/linux-x86_64-normal-server-slowdebug/jdk/bin
gdb --args ./java hello
b thread.cpp:219
r
```
