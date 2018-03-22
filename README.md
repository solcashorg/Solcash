Solcash Org:

Download compiled solcash files in Solcash releases : https://github.com/solcashorg/solcash/releases

How To Compile

Linux
If you are using Arch Linux, there is an AUR precompiled package, solcash-bin, or a build from source version, solcash-git.

Prerequisites
You will need the following packages: boost (1.55 or higher), rocksdb, cmake, git, gcc (4.9 or higher), g++ (4.9 or higher), make, and python. Most of these should already be installed on your system.
For example on ubuntu: ''sudo apt-get install build-essential python-dev gcc g++ git cmake libboost-all-dev librocksdb-dev''

If you are using ubuntu and your version of ubuntu doesn't have librocksdb-dev, you can get it from a ppa instead:

sudo add-apt-repository ppa:ethcore/ethcore -y
sudo apt-get update
sudo apt-get install librocksdb-dev
Building
git clone https://github.com/solcashorg/solcash
cd solcash
mkdir build && cd $_
cmake ..
make


Apple

Prerequisites

Install cmake. See here if you are unable call cmake from the terminal after installing.
Install the boost libraries. Either compile boost manually or run brew install boost.
Install XCode and Developer Tools.
Building
git clone https://github.com/solcashorg/solcash
cd solcash
mkdir build && cd $_
cmake .. or cmake -DBOOST_ROOT=<path_to_boost_install> .. when building from a specific boost install
make
The binaries will be in ./src after compilation is complete.

Windows 10
Prerequisites
Install Visual Studio 2017 Community Edition
When installing Visual Studio, it is required that you install Desktop development with C++ and the VC++ v140 toolchain when selecting features. The option to install the v140 toolchain can be found by expanding the "Desktop development with C++" node on the right. You will need this for the project to build correctly.
Install Boost 1.59.0, ensuring you download the installer for MSVC 14.
Building
From the start menu, open 'x64 Native Tools Command Prompt for vs2017'.
cd <your_solcash_directory>
mkdir build
cd build
Set the PATH variable for cmake: ie. set PATH="C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\Common7\IDE\CommonExtensions\Microsoft\CMake\CMake\bin";%PATH%
cmake -G "Visual Studio 14 Win64" .. -DBOOST_ROOT=C:/local/boost_1_59_0 (Or your boost installed dir.)
MSBuild ByteCoin.sln /p:Configuration=Release /m
If all went well, it will complete successfully, and you will find all your binaries in the '..\build\src\Release' directory.
Additionally, a .sln file will have been created in the build directory. If you wish to open the project in Visual Studio with this, you can.
Thanks
Cryptonote Developers, Bytecoin Developers, Monero Developers, Forknote Project, SolCash Community
