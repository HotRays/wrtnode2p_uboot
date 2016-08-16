U-Boot
===
**Thanks to [Andy](https://github.com/andy-padavan)**

Install
---

1. Download this repository.
  ```bash
  $ git clone --depth 1 https://github.com/soonsebii/wrtnode2p_uboot.git
  ```

2. Copy wrtnode2p_uboot folder to wrtnode2p/openwrt/package/boot/uboot-mt7628.
  ```bash
  $ cp -rf wrtnode2p_uboot ~/wrtnode2p/openwrt/package/boot/uboot-mt7628
  ```

Build
---

1. Select uboot-mt7628 package under menuconfig in bootloader.
  ```bash
  $ make menuconfig
    Boot Loaders ---> [*] uboot-mt7628-sxx
  ```

2. building uboot with under commands
  ```bash
  $ make package/boot/uboot-mt7628/prereq V=s
  $ make package/boot/uboot-mt7628/compile V=s
  ```

3. uboot.bin will generated under wrtnode2p/openwrt/bin/ramips folder
