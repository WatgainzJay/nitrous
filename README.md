# Nitrous

To compile the Linux version from source, do the following on Ubuntu 16.04.

# Create SWAP

sudo fallocate -l 2G /swapfile


sudo chmod 600 /swapfile

sudo mkswap /swapfile

sudo swapon /swapfile


# Install Prerequisites

sudo add-apt-repository ppa:bitcoin/bitcoin
sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils python3

sudo apt-get update

sudo apt-get upgrade

sudo apt-get install libboost-all-dev

sudo apt-get install software-properties-common

sudo apt-get update
sudo apt-get install libdb4.8-dev libdb4.8++-dev
sudo apt-get install libzmq3-dev
sudo apt-get install libminiupnpc-dev


# Compile

./autogen.sh

./configure

make

make install # optional


# Run

from nitrous/src directory:

./nitrousd

once running, to issue RPC commands use:

./nitrous-cli <command>