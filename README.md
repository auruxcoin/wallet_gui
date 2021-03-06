Auruxcoin GUI

Copyright (c) 2017-2018, The Auruxcoin Developers.
Portions Copyright (c) 2012-2017, The CryptoNote Developers, The Bytecoin Developers.

License
auruxcoin's GUI Wallet is licensed under the "MIT License" for more info, refer to the License file.

Download Releases
https://github.com/criptomineria/wallet-gui

How to build for Ubuntu Linux
sudo apt-get -y install build-essential libssl-dev libboost-all-dev

sudo apt-get -y install gcc-4.8 g++-4.8 git cmake

sudo apt-get install qt5-default qttools5-dev-tools

git clone https://github.com/auruxcoin/wallet-gui

cd wallet-gui

git submodule add -f https://github.com/auruxcoin/blockchain

cp CMakeLists_ubuntu.txt CMakeLists.txt

mkdir build ; cd build

cmake ..

make

./auruxcoinWallet

How to build for Mac OS
Install Homebrew from here: https://brew.sh/

mkdir homebrew && curl -L https://github.com/Homebrew/brew/tarball/master | tar xz --strip 1 -C homebrew

Open a Terminal and type:

brew install qt5

brew install cmake

Download a copy of the auruxcoin-gui source:

cd /opt

git clone https://github.com/auruxcoin/wallet-gui

Enter the auruxcoin-gui directory:

cd wallet-gui

Download the latest auruxcoincoin codebase:

git submodule add -f https://github.com/auruxcoin/blockchain

Use the correct CMake File

cp CMakeLists_Mac.txt CMakeLists.txt

Create a build directory and enter it:

mkdir build && cd build

Run the the cmake with your qt5 lib path:

/opt/homebrew/bin/cmake -DCMAKE_PREFIX_PATH:STRING='/opt/homebrew/opt/qt5/lib/cmake' ..

Run make to build the wallet:

make

Fix the Links

/opt/homebrew/opt/qt/bin/macdeployqt auruxcoinWallet.app/

When the build has finished, to copy the auruxcoin GUi app into your Application folder type:

cp -r auruxcoinWallet.app ~/Applications

You can now run the auruxcoin GUI from Finder. Make sure that auruxcoind is running in a terminal window else the GUI will crash on startup.
