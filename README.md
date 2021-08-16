# Defi Node for Raspberry Pi

The official DeFiChain client release of the Defi Node for Linux will not work for the Raspberrys. So I have made for myself a compiled version of the Defi Node for my Raspberry Pi 4B 4GB with official Raspberry Pi OS (32-Bit). This so called `armv7l` version is different to other Linux distributions. 

The compiled Raspberry Pi client bases on the [DeFiChain](https://github.com/DeFiCh/ain) original source code. No code was modyfied and was 100% taken from the DeFiChain repository.


## Howto Start

You can [download here the client](https://github.com/Martin8617/Defi-Node-for-Raspberry-Pi/releases) for your Raspberry Pi,

or

You can check for official DeFiChain [releases](https://github.com/DeFiCh/ain/releases) for latest downloadable installers for Windows, Mac and Linux.

Setting up nodes are exactly similar to how to run a node from the command-line for Bitcoin. Please follow any bitcoin instructions, substituting the binaries name of bitcoin for defi, that's available under the /bin dir.
The default data directory is `~/.defi`, with the default conf read from `~/.defi/defi.conf` if found.
After download the client, save the file where you want (e.g. `/home/user/defichain`), change to the `/bin` directory and run the Node with `./defid` - that's all...


## Quick Start refers to Defich/ain
- [Running a node](https://github.com/DeFiCh/ain/blob/master/doc/setup-nodes.md)
- [Running a node with docker](https://github.com/DeFiCh/ain/blob/master/doc/setup-nodes-docker.md)
- [Running a masternode](https://github.com/DeFiCh/ain/blob/master/doc/setup-masternodes.md)


# Licenses

By using `Defi-Wallet for Raspberry Pi` (this repo), you (the user) agree to be bound by [the terms of this license](LICENSE).

Last updated August 14, 2021
