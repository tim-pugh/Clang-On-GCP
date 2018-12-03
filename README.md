# Clang-On-GCP

This repo are instructions for building Clang on a Google Cloud Platform VM instance (GCP) running Ubuntu 18.04 LTS. This will work on 18.04 LTS most anywhere too, I just needed it on GCP.

Required Packages followed by pulling in the code and then building:

sudo apt install build-essential

sudo apt install python

sudo apt-get install zlib1g-dev

sudo apt install unzip

sudo apt install zip

sudo apt-get install subversion

sudo apt install cmake

sudo apt-get update

sudo apt-get dist-upgrade

svn co http://llvm.org/svn/llvm-project/llvm/trunk llvm

cd llvm/tools

svn co http://llvm.org/svn/llvm-project/cfe/trunk clang

cd ../..

mkdir build

cd build

cmake -G "Unix Makefiles" ../llvm

make

