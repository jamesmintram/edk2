   Boot Overview

   SD Card: EDK2 -> BOOTAA64.efi (sys/arch/stand/efiboot) -USB Stick-> Kernel (From OBSD miniroot)
   




EDK2 - Built on Aarch64 pi
Firefly SDK - built on Ubuntu 2018 VM
OBSD EFI Loader - built on OBSD pi
OBSD Kernel - built on OBSD pi

   
   
   Building EDK2 (Bootloader firmware)
   
    https://github.com/edk2-porting/edk2-rk3588/

   
   36  asdf
   37  asdf install
   38  asdf plugin-add python
   39  asdf install python 3.6.12
   40  python -V
   41  asdf use python 3.6.12
   42  asdf global python 3.6.12
   43  sudo apt-get install -y make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev python-openssl git
   44  sudo apt-get install -y make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev  git
   45  asdf install python 3.6.12
   46  asdf global python 3.6.12
   47  python -V
   48  repo init --no-clone-bundle --repo-url https://gitlab.com/firefly-linux/git-repo.git -u https://gitlab.com/firefly-linux/manifests.git -b master -m rk3588_linux_release.xml
   49  sudo lsblk -vvv
   50  sudo lspci -vvv
   51  sudo vi /boot/firmware/bootcode.bin 
   52  sudo vi /boot/firmware/config.txt 
   53  reboot
   54  sudo reboot
   55  ls /dev
   56  sudo apt update
   57  sudo apt install -y repo git python
   58  sudo apt install -y repo git python3
   59  mkdir rk3588_sdk
   60  cd rk3588_sdk/
   61  repo init --no-clone-bundle --repo-url https://gitlab.com/firefly-linux/git-repo.git -u https://gitlab.com/firefly-linux/manifests.git -b master -m rk3588_linux_release.xml
   62  python --version
   63  sudo apt search python
   64  git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.14.1
   65  vi ~/.bashrc 
   66  bash
   67  ls
   68  cd edk2-rk3588/
   69  ls
   70  exit
   71  sudo apt install git gcc g++ build-essential gcc-aarch64-linux-gnu iasl python3-pyelftools uuid-dev
   72  ls
   73  git clone --recurse-submodules https://github.com/edk2-porting/edk2-rk3588.git
   74  ls
   75  cd edk2-rk3588/
   76  sudo apt install git gcc g++ build-essential gcc-aarch64-linux-gnu iasl python3-pyelftools uuid-dev
   77  ./build.sh --device itx-3588j --release Debug
   78  aarch64-none-elf-gcc
   79  sudo apt search aarch64-none-elf-gcc
   80  sudo apt install gcc-13-aarch64-linux-gnu
   81  apt search gcc-
   82  apt search gcc-12-aarch64-linux-gnu
   83  apt search gcc-12-aarch64
   84  apt search aarch64
   85  sudo apt update
   86  apt search aarch64
   87  ./build.sh --device itx-3588j --release Debug
   88  find . -name toolchain.mk
   89  less arm-trusted-firmware/make_helpers/toolchain.mk
   90  which gcc
   91  export CROSS_COMPILE=/usr/bin/
   92  ./build.sh --device itx-3588j --release Debug
   93  pip3 install pyelftools
   94  ./build.sh --device itx-3588j --release Debug
   95  ls
   96  mv ./RK3588_NOR_FLASH.img ./RK3588_NOR_FLASH_ORIG.img 
   97  ls
   98  cd configs
   99  vim ./itx-3588j.conf 
  100  sudo apt install vim
  101  vim ./itx-3588j.conf 
  102  cd ..
  103  ls
  104  vim export CROSS_COMPILE=/usr/bin/
  105  vim config/it
  106  vim configs/itx-3588j.conf 
  107  cat configs/itx-3588j.conf 
  108  less edk2-rockchip/Platform/Firefly/ITX-3588J/ITX-3588J.dsc
  109  less edk2-rockchip/Platform/Firefly/ITX-3588J/ITX-3588J.dsc.inc 
  110  less edk2-rockchip/Platform/Firefly/ITX-3588J/ITX-3588J.Modules.fdf.inc 
  111  less edk2-rockchip/Platform/Firefly/ITX-3588J/ITX-3588J.dsc.inc 
  112  less edk2-rockchip/Silicon/Rockchip/RK3588/RK3588.dev
  113  less edk2-rockchip/Silicon/Rockchip/RK3588/RK3588.dec
  114  less edk2-rockchip/Silicon/Rockchip/RK3588/RK3588.dec 
  115  ls
  116  find . -name *.efi
  117  find . -name *.elf
  118  find . -name *.elf | Graph
  119  find . -name *.elf | grep Graph
  120  find . -name *.elf | grep Console
  121  find . -name *.elf | grep console
  122  find . | grep console
  123  find . | grep -i console
  124  find . | grep -i GraphicsOutput
  125  gdb ./workspace/Build/ITX-3588J/DEBUG_GCC/AARCH64/Silicon/Rockchip/Drivers/LcdGraphicsOutputDxe/LcdGraphicsOutputDxe/OUTPUT/LcdGraphicsOutputDxe.efi
  126  gdb ./workspace/Build/ITX-3588J/DEBUG_GCC/AARCH64/LcdGraphicsOutputDxe.efi
  127  gdb ./workspace/Build/ITX-3588J/DEBUG_GCC/AARCH64/LcdGraphicsOutputDxe.debug
  128  lspci -vvv
  129  sudo lspci -vvv
  130  ping 10.0.2.15
  131  ssh 
  132  ssh 192.168.0.25
  133  d:
  134  git clone https://github.com/openbsd/src.git obsd
  135  git clone --depth 1 https://github.com/openbsd/src.git obsd
  136  rm -rf ./obsd/.git/
  137  tar cfz obsd-src ./obsd/
  138  scop ./obsd-src james@192.168.10.119:~/
  139  scp ./obsd-src james@192.168.10.119:~/
  140  cd edk2-rk3588/
  141  ls
  142  find . -name GraphicsConsoleDxe
  143  file ./edk2/MdeModulePkg/Universal/Console/GraphicsConsoleDxe
  144  ls ./edk2/MdeModulePkg/Universal/Console/GraphicsConsoleDxe
  145  ls ./workspace/Build/ITX-3588J/DEBUG_GCC/AARCH64/MdeModulePkg/Universal/Console/GraphicsConsoleDxe
  146  ls ./workspace/Build/ITX-3588J/DEBUG_GCC/AARCH64/MdeModulePkg/Universal/Console/GraphicsConsoleDxe/GraphicsConsoleDxe/
  147  ls ./workspace/Build/ITX-3588J/DEBUG_GCC/AARCH64/MdeModulePkg/Universal/Console/GraphicsConsoleDxe/GraphicsConsoleDxe/DEBUG/
  148  gdb ./workspace/Build/ITX-3588J/DEBUG_GCC/AARCH64/MdeModulePkg/Universal/Console/GraphicsConsoleDxe/GraphicsConsoleDxe/DEBUG/GraphicsConsoleDxe.debug 
  149  ls
  150  gdb  RK3588_NOR_FLASH_ORIG.img
  151  gdb ./workspace/Build/ITX-3588J/DEBUG_GCC/AARCH64/MdeModulePkg/Universal/Console/GraphicsConsoleDxe/GraphicsConsoleDxe/DEBUG/GraphicsConsoleDxe.dll
  152  find . -name ConSplitterDxe.dll
  153  gdb ./workspace/Build/ITX-3588J/DEBUG_GCC/AARCH64/MdeModulePkg/Universal/Console/ConSplitterDxe/ConSplitterDxe/DEBUG/ConSplitterDxe.dll
  154  find . -name BdsDxe.dll
  155  gdb ./workspace/Build/ITX-3588J/DEBUG_GCC/AARCH64/MdeModulePkg/Universal/BdsDxe/BdsDxe/DEBUG/BdsDxe.dll
  156  ls
  157  ./build.sh --device itx-3588j --release Debug
  158  sudo apt-get install device-tree-compiler
  159  dtc
  160  ls
  161  find . -name *.dtb
  162  dtc -I dtb  -O dts -o itx.dts ./edk2-rockchip-non-osi/Platform/Rockchip/DeviceTree/itx-3588j.dtb
  163  ls
  164  less ./itx.dts 