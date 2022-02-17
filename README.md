# rtthread-pomegranate
Mutil-Operating System with RT-Thread

# Compile

## Install dependence package

    sudo apt install ninja-build pixman

    sudo apt-get install build-essential libcairo2-dev libpango1.0-dev libjpeg-dev libgif-dev librsvg2-dev

    apt-get install libmount-dev

    sudo apt install android-sdk-ext4-utils

    sudo apt install scons

    sudo apt install device-tree-compiler

## Clone and init submode

    git clone --recursive https://github.com/RT-Thread/rtthread-pomegranate

## Download u-boot、linux、qemu source

    ./dn.sh

## Download toolchains

    cd toolschains

    wget https://toolchains.bootlin.com/downloads/releases/toolchains/riscv64/tarballs/riscv64--glibc--bleeding-edge-2020.08-1.tar.bz2

    tar -xf riscv64--glibc--bleeding-edge-2020.08-1.tar.bz2

    wget https://static.dev.sifive.com/dev-tools/freedom-tools/v2020.12/riscv64-unknown-elf-toolchain-10.2.0-2020.12.8-x86_64-linux-ubuntu14.tar.gz

    tar -xf riscv64-unknown-elf-toolchain-10.2.0-2020.12.8-x86_64-linux-ubuntu14.tar.gz

    
## Compile qemu

    cd qemu
    ./build.sh

## Compile u-boot

    cd u-boot
    ./build.sh

    // test
    ./run.sh

## Compile rtt

    cd rtos

    git clone https://github.com/RT-Thread/rt-thread.git

    // checkout a last fork
    git checkout v4.1.0-beta

    ./build.sh

    // test
    ./run.sh
    
## Compile buildroot

    cd buildroot
    ./build.sh
