---
layout: post
title:  "Installing klee with LLVM and Clang 2.9"
date:   2015-10-07 23:04:00
categories: guide llvm clang klee
---

**The website is under construction and will receive a big update soon. Meanwhile, you can have a look at my [cv here](/cv/).**



<!-- sudo apt-get update
sudo apt-get install -y build-essential curl python-minimal git bison flex bc libcap-dev git cmake libboost-all-dev valgrind libm4ri-dev libmysqlclient-dev libsqlite3-dev libtbb-dev libncurses5-dev libc6-dev-i386
echo export C_INCLUDE_PATH=/usr/include/x86_64-linux-gnu >> ~/.bashrc
echo export CPLUS_INCLUDE_PATH=/usr/include/x86_64-linux-gnu >> ~/.bashrc
sudo ln -sf /usr/lib/x86_64-linux-gnu /usr/lib64
cd /opt
sudo mkdir llvm
sudo chmod 777 llvm
sudo wget 'http://llvm.org/releases/2.9/llvm-gcc4.2-2.9-x86_64-linux.tar.bz2'

sudo tar -xjf llvm-gcc4.2-2.9-x86_64-linux.tar.bz2 
 sudo rm llvm-gcc4.2-2.9-x86_64-linux.tar.bz2 
sudo mv llvm-gcc4.2-2.9-x86_64-linux/ llvm-gcc
echo 'export PATH=$PATH:/opt/llvm-gcc/bin' >> ~/.bashrc
source ~/.bashrc

sudo wget -O - "http://llvm.org/releases/2.9/llvm-2.9.tgz" | sudo tar xzf -
sudo mv llvm-2.9/ llvm
sudo chmod -R 777 llvm

cd llvm
wget 'http://www.mail-archive.com/klee-dev@imperial.ac.uk/msg01302/unistd-llvm-2.9-jit.patch'
patch "lib/ExecutionEngine/JIT/Intercept.cpp" "unistd-llvm-2.9-jit.patch" 

cd tools
wget -O - "http://llvm.org/releases/2.9/clang-2.9.tgz" | tar xzf -
mv clang-2.9/ clang

wget "https://raw.githubusercontent.com/antiagainst/klee-build-scripts/master/ubuntu/2.9-stable/patches/clang-2.9-gcc.patch"
patch "clang/lib/Driver/ToolChains.cpp" clang-2.9-gcc.patch
rm clang-2.9-gcc.patch
cd ../

./configure --enable-optimized --enable-assertions
make
echo 'export PATH=$PATH:/opt/llvm/Release+Asserts/bin' >> ~/.bashrc
cd ..

sudo mkdir minisat
sudo chmod 777 minisat/
git clone https://github.com/stp/minisat.git minisat
cd minisat
mkdir build
cd build
cmake ..  
make
sudo make install
cd ../..
sudo mkdir stp
sudo chmod 777 stp/
git clone 'https://github.com/stp/stp.git' stp
cd stp
mkdir build
cd build
cmake -DBUILD_SHARED_LIBS:BOOL=OFF -DENABLE_PYTHON_INTERFACE:BOOL=OFF ..
make OPTIMIZE=-O2 CFLAGS_M32=
sudo make install
ulimit -s unlimited


cd ../..
sudo mkdir klee-uclibc
sudo chmod 777 klee-uclibc/
git clone --depth 1 --branch klee_0_9_29 'https://github.com/klee/klee-uclibc.git' klee-uclibc/
cd klee-uclibc/
./configure --with-llvm-config=/opt/llvm/Release+Asserts/bin/llvm-config --with-cc=/opt/llvm-gcc/bin/llvm-gcc --make-llvm-lib
make -j


cd ..
sudo mkdir klee
sudo chmod 777 klee
git clone 'https://github.com/klee/klee.git' klee

cd klee
./configure --with-llvm="/opt/llvm" --with-stp="/opt/stp/build" --with-uclibc="/opt/klee-uclibc" --enable-posix-runtime
make ENABLE_OPTIMIZED=1
echo 'export PATH=$PATH:/opt/klee/Release+Asserts/bin' >> ~/.bashrc
source ~/.bashrc
make check
make unittests


if fails 
echo 'export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/lib' >> ~/.bashrc
 -->