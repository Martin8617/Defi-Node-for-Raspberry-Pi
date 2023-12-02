# ![image](https://user-images.githubusercontent.com/79512509/135573091-5b12a44c-3654-459e-964b-0429d772763a.png) Defi Node for Raspberry Pi

The official DeFiChain client release of the Defi Node is available for the Raspberrys since version 4.0.0. 
So my work to create a version myself is done. 
I recommend to use the latest 64-bit Raspberry OS. Download the file for `aarch64-linux`.


## Documentation

- [DeFiChain.com](https://defichain.com/)
- [DeFiCh/ain](https://github.com/DeFiCh/ain/README.md)
- [Build from Scratch (32-Bit)](https://github.com/Martin8617/Defi-Node-for-Raspberry-Pi/blob/main/build-ain-armv7l.md)
- [Build from Scratch (64-Bit)](https://github.com/Martin8617/Defi-Node-for-Raspberry-Pi/blob/main/build-ain-arm64.md)


## Howto Start

You can check for official DeFiChain [releases](https://github.com/DeFiCh/ain/releases) for latest downloadable installers for Raspberry Pi, Windows, Mac and Linux.

Setting up nodes are exactly similar to how to run a node from the command-line for Bitcoin. Please follow any bitcoin instructions, substituting the binaries name of bitcoin for defi, that's available under the /bin dir.
The default data directory is `~/.defi`, with the default conf read from `~/.defi/defi.conf` if found.
After download the client, save the file where you want (e.g. `/home/user/defichain`), change to the `/bin` directory and run the Node with `./defid` - that's all...


## Quick Start refers to DeFiCh/ain

- [Running a node](https://github.com/DeFiCh/ain/blob/master/doc/setup-nodes.md)
- [Running a node with docker](https://github.com/DeFiCh/ain/blob/master/doc/setup-nodes-docker.md)
- [Running a masternode](https://github.com/DeFiCh/ain/blob/master/doc/setup-masternodes.md)


## Howto Continue

### Buy Hardware and setup a Raspberry Pi

On [DefiNode](https://github.com/DefiNode/DeFiNode) you find a shopping list for the hardware of a Raspberry Pi node as well as a 3D printer case program with DeFiChain logo. A good installation guide of the setup of a Raspberry Pi you can find there as well, however don't mix up this Defi Wallet with the docker installation at DefiNode.

Watch out [DeFiNode Druckservice](https://www.gabrielkunzer.com/definode), there you can order your own DEFI case.


### Run your own Masternode

The [DefiChain-Wiki](https://defichain-wiki.com/wiki/Masternode_installation_extended) tells you the steps to setup a masternode and the guys from [mydeficha.in](https://mydeficha.in) will serves you with operating your own masternode. 


## Licenses

By using `Defi-Wallet for Raspberry Pi` (this repo), you (the user) agree to be bound by [the terms of this license](LICENSE).

Last updated August 14, 2021
