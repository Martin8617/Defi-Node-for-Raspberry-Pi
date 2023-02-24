# Build DeFi Node on Raspberry Pi 4B with Raspberry OS 32-Bit


## Documentation
- DefiCh/ain (https://github.com/DeFiCh/ain)
- Building from scratch (https://github.com/DeFiCh/ain/blob/master/doc/build-unix.md)


## Source Code
Download the latest source code from DefiCh/ain and extract them to your `/home/user/` directory (eg. /home/pi/):
- [Source code (tar.gz)](https://github.com/DeFiCh/ain/releases)


## Build ain-3.2.5

### Install all dependencies

```
sudo apt-get install build-essential libtool autotools-dev automake pkg-config bsdmainutils python3 curl
```

Now, you can either build from self-compiled depends or install the required dependencies:
```
sudo apt-get install libssl-dev libevent-dev libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-test-dev libboost-thread-dev
sudo apt-get install libminiupnpc-dev libzmq3-dev
```
Make sure you install the build requirements mentioned above. Then, install the toolchain:

```
sudo apt-get install g++-arm-linux-gnueabihf
```

### Build Berkeley DB
It is recommended to use Berkeley DB 4.8. If you have to build it yourself, you can use installation script included in contrib:
```
cd /home/pi/ain-3.2.5/
./contrib/install_db4.sh /home/pi/ain-3.2.5/
```

### Build executables
```
cd /home/pi/ain-3.2.5/depends
make HOST=arm-linux-gnueabihf NO_QT=1 
cd ..
./autogen.sh
```
```
export BDB_PREFIX='/home/pi/ain-3.2.5/db4'
./configure BDB_LIBS="-L${BDB_PREFIX}/lib -ldb_cxx-4.8" BDB_CFLAGS="-I${BDB_PREFIX}/include" --prefix=$PWD/depends/arm-linux-gnueabihf --enable-glibc-back-compat --enable-reduce-exports LDFLAGS=-static-libstdc++
```
And finally: 
```
make HOST=arm-linux-gnueabihf -j4
```
...and if you want you can create a package (e.g. /home/pi/ain-3.2.0/depends/arm-linux-gnueabihf/) which contains the files as you get them from DeFiChain for the other platforms: 
```
make install
```
