# Build DeFi Node on Raspberry Pi 4B 4GB with Raspberry OS 64-Bit


## Documentation
- DefiCh/ain (https://github.com/DeFiCh/ain)
- Building from scratch (https://github.com/DeFiCh/ain/blob/master/doc/build-unix.md)


## Source Code
Download source code and extract them to your /home/user/ directory: 
- ain-1.8.1 (https://github.com/DeFiCh/ain/releases)


## Build ain-1.8.1

### Install all dependencies

`sudo apt-get install build-essential libtool autotools-dev automake pkg-config bsdmainutils python3 curl`

Now, you can either build from self-compiled depends or install the required dependencies:
```
sudo apt-get install libssl-dev libevent-dev libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-test-dev libboost-thread-dev
sudo apt-get install libminiupnpc-dev libzmq3-dev
```
Make sure you install the build requirements mentioned above. Then, install the toolchain:

`sudo apt-get install g++-aarch64-linux-gnu`

### Build Berkeley DB
It is recommended to use Berkeley DB 4.8. If you have to build it yourself, you can use installation script included in contrib:
```
cd /home/pi/ain-1.8.1/
./contrib/install_db4.sh /home/pi/ain-1.8.1/
```

### Build executables
```
cd /home/pi/ain-1.8.1/depends
make HOST=aarch64-linux-gnu NO_QT=1 
cd ..
./autogen.sh
```
```
export BDB_PREFIX='/home/pi/ain-1.8.1/db4' && ./configure BDB_LIBS="-L${BDB_PREFIX}/lib -ldb_cxx-4.8" BDB_CFLAGS="-I${BDB_PREFIX}/include" --prefix=$PWD/depends/aarch64-linux-gnu --enable-glibc-back-compat --enable-reduce-exports LDFLAGS=-static-libstdc++
```
And finally: 
`make`