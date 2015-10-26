###Get SD card image for Tuxono S/L
Download complete image (as a compressed zip file) from Google Drive: https://drive.google.com/open?id=0B3fAL9wNxT7XNzJGeWduME5MYjQ

###Extract and copy to SD card
Extract the zip file with your favorite tool.

####Copy to SD card on Windows
Copy image to SD card with the 'Win32DiskImager' (http://sourceforge.net/projects/win32diskimager/) tool.

####Copy to SD card on Linux
Copy file to SD card with the following command:
>```
$ sudo dd bs=4M if=tuxono-ArchLinuxARM-17-Sep-2015.img of=/path/to/sdcard
```


###Bootlog
Below you can see the debug log output of the booting system:

```text
U-Boot 2014.10-00002-g0127499 (Sep 18 2015 - 11:52:40)

CPU:   Freescale i.MX28 rev1.2 at 454 MHz
BOOT:  SSP SD/MMC #0, 3V3
DRAM:  128 MiB
MMC:   MXS MMC: 0
In:    serial
Out:   serial
Err:   serial
Net:   Phy not found
FEC0, FEC1
Hit any key to stop autoboot:  0
2496256 bytes read in 791 ms (3 MiB/s)
17045 bytes read in 61 ms (272.5 KiB/s)
## Booting kernel from Legacy Image at 42000000 ...
   Image Name:   Linux-3.10.79-00002-gc5ac6b2
   Image Type:   ARM Linux Kernel Image (uncompressed)
   Data Size:    2496192 Bytes = 2.4 MiB
   Load Address: 40008000
   Entry Point:  40008000
   Verifying Checksum ... OK
## Flattened Device Tree blob at 41000000
   Booting using the fdt blob at 0x41000000
   Loading Kernel Image ... OK
   Loading Device Tree to 47b5e000, end 47b65294 ... OK

Starting kernel ...

Uncompressing Linux... done, booting the kernel.
[    0.000000] Booting Linux on physical CPU 0x0
[    0.000000] Initializing cgroup subsys cpuset
[    0.000000] Initializing cgroup subsys cpu
[    0.000000] Initializing cgroup subsys cpuacct
[    0.000000] Linux version 3.10.79-00002-gc5ac6b2 (sebastian@ubuntu) (gcc version 4.8.2 (GCC) ) #2 PREEMPT Fri Sep 11 15:48:01 CEST 2015
[    0.000000] CPU: ARM926EJ-S [41069265] revision 5 (ARMv5TEJ), cr=00053177
[    0.000000] CPU: VIVT data cache, VIVT instruction cache
[    0.000000] Machine: Freescale MXS (Device Tree), model: SchulerControl GmbH, SC SPS 1
[    0.000000] Memory policy: ECC disabled, Data cache writeback
[    0.000000] Built 1 zonelists in Zone order, mobility grouping on.  Total pages: 32512
[    0.000000] Kernel command line: root=/dev/mmcblk0p3 rw rootwait rootflags=barrier=1,data=journal,commit=1 panic=1 init=/usr/lib/systemd/systemd console=ttyAMA0,115200
[    0.000000] PID hash table entries: 512 (order: -1, 2048 bytes)
[    0.000000] Dentry cache hash table entries: 16384 (order: 4, 65536 bytes)
[    0.000000] Inode-cache hash table entries: 8192 (order: 3, 32768 bytes)
[    0.000000] Memory: 128MB = 128MB total
[    0.000000] Memory: 123152k/123152k available, 7920k reserved, 0K highmem
[    0.000000] Virtual kernel memory layout:
[    0.000000]     vector  : 0xffff0000 - 0xffff1000   (   4 kB)
[    0.000000]     fixmap  : 0xfff00000 - 0xfffe0000   ( 896 kB)
[    0.000000]     vmalloc : 0x88800000 - 0xff000000   (1896 MB)
[    0.000000]     lowmem  : 0x80000000 - 0x88000000   ( 128 MB)
[    0.000000]     modules : 0x7f000000 - 0x80000000   (  16 MB)
[    0.000000]       .text : 0x80008000 - 0x80604710   (6130 kB)
[    0.000000]       .init : 0x80605000 - 0x80625758   ( 130 kB)
[    0.000000]       .data : 0x80626000 - 0x80656e20   ( 196 kB)
[    0.000000]        .bss : 0x80656e20 - 0x8068b618   ( 210 kB)
[    0.000000] SLUB: HWalign=32, Order=0-3, MinObjects=0, CPUs=1, Nodes=1
[    0.000000] NR_IRQS:16 nr_irqs:16 16
[    0.000000] of_irq_init: children remain, but no parents
[    0.000000] sched_clock: 32 bits at 24MHz, resolution 41ns, wraps every 178956ms
[    0.000000] Console: colour dummy device 80x30
[    0.000548] Calibrating delay loop... 226.09 BogoMIPS (lpj=1130496)
[    0.080262] pid_max: default: 32768 minimum: 301
[    0.080563] Mount-cache hash table entries: 512
[    0.091700] Initializing cgroup subsys devices
[    0.091758] Initializing cgroup subsys freezer
[    0.091787] Initializing cgroup subsys blkio
[    0.091922] CPU: Testing write buffer coherency: ok
[    0.092791] Setting up static identity map for 0x804668e0 - 0x8046691c
[    0.096052] devtmpfs: initialized
[    0.098006] pinctrl core: initialized pinctrl subsystem
[    0.098690] regulator-dummy: no parameters
[    0.099258] NET: Registered protocol family 16
[    0.100779] DMA: preallocated 256 KiB pool for atomic coherent allocations
[    0.123387] Serial: AMBA PL011 UART driver
[    0.123918] 80074000.serial: ttyAMA0 at MMIO 0x80074000 (irq = 215) is a PL011 rev2
[    0.391403] console [ttyAMA0] enabled
[    0.406450] bio: create slab <bio-0> at 0
[    0.415314] mxs-dma 80004000.dma-apbh: initialized
[    0.423579] mxs-dma 80024000.dma-apbx: initialized
[    0.429234] usb0_vbus: 5000 mV
[    0.433869] SCSI subsystem initialized
[    0.438276] usbcore: registered new interface driver usbfs
[    0.444098] usbcore: registered new interface driver hub
[    0.449893] usbcore: registered new device driver usb
[    0.460090] pps_core: LinuxPPS API ver. 1 registered
[    0.465324] pps_core: Software ver. 5.3.6 - Copyright 2005-2007 Rodolfo Giometti <giometti@linux.it>
[    0.474576] PTP clock support registered
[    0.483564] Switching to clocksource mxs_timer
[    0.488942] cfg80211: Calling CRDA to update world regulatory domain
[    0.523484] NET: Registered protocol family 2
[    0.530139] TCP established hash table entries: 1024 (order: 1, 8192 bytes)
[    0.537190] TCP bind hash table entries: 1024 (order: 0, 4096 bytes)
[    0.543698] TCP: Hash tables configured (established 1024 bind 1024)
[    0.550303] TCP: reno registered
[    0.553590] UDP hash table entries: 256 (order: 0, 4096 bytes)
[    0.559563] UDP-Lite hash table entries: 256 (order: 0, 4096 bytes)
[    0.566447] NET: Registered protocol family 1
[    0.571453] NetWinder Floating Point Emulator V0.97 (double precision)
[    0.603685] msgmni has been set to 240
[    0.614151] Block layer SCSI generic (bsg) driver version 0.4 loaded (major 250)
[    0.621993] io scheduler noop registered (default)
[    0.809417] of_dma_request_slave_channel: dma-names property missing or empty
[    0.816604] uart-pl011 80074000.serial: no DMA platform data
[    0.823058] 8006a000.serial: ttyAPP0 at MMIO 0x8006a000 (irq = 212) is a 8006a000.serial
[    0.831913] mxs-auart 8006a000.serial: Found APPUART 3.1.0
[    0.837877] 8006c000.serial: ttyAPP1 at MMIO 0x8006c000 (irq = 213) is a 8006c000.serial
[    0.846778] mxs-auart 8006c000.serial: Found APPUART 3.1.0
[    0.852907] 8006e000.serial: ttyAPP2 at MMIO 0x8006e000 (irq = 214) is a 8006e000.serial
[    0.861763] mxs-auart 8006e000.serial: Found APPUART 3.1.0
[    0.884657] brd: module loaded
[    0.897112] loop: module loaded
[    0.900608] at24 0-0052: 8192 byte 24c64 EEPROM, writable, 32 bytes/write
[    0.930110] m25p80 spi32766.0: mr25h256 (32 Kbytes)
[    0.942840] libphy: Fixed MDIO Bus: probed
[    0.949085] CAN device driver interface
[    1.064749] libphy: fec_enet_mii_bus: probed
[    1.072686] usbcore: registered new interface driver ath9k_htc
[    1.078804] ehci_hcd: USB 2.0 'Enhanced' Host Controller (EHCI) Driver
[    1.085653] usbcore: registered new interface driver usb-storage
[    1.095701] ci_hdrc ci_hdrc.0: EHCI Host Controller
[    1.100888] ci_hdrc ci_hdrc.0: new USB bus registered, assigned bus number 1
[    1.128206] ci_hdrc ci_hdrc.0: USB 2.0 started, EHCI 1.00
[    1.135232] hub 1-0:1.0: USB hub found
[    1.139190] hub 1-0:1.0: 1 port detected
[    1.144057] imx_usb 80090000.usb: pinctrl get/select failed, err=-19
[    1.153671] ci_hdrc ci_hdrc.1: EHCI Host Controller
[    1.158867] ci_hdrc ci_hdrc.1: new USB bus registered, assigned bus number 2
[    1.178193] ci_hdrc ci_hdrc.1: USB 2.0 started, EHCI 1.00
[    1.185250] hub 2-0:1.0: USB hub found
[    1.189207] hub 2-0:1.0: 1 port detected
[    1.194911] mousedev: PS/2 mouse device common for all mice
[    1.201029] rtc-pcf8563 0-0051: chip found, driver version 0.4.3
[    1.209215] rtc-pcf8563 0-0051: rtc core: registered rtc-pcf8563 as rtc0
[    1.219976] stmp3xxx-rtc 80056000.rtc: rtc core: registered 80056000.rtc as rtc1
[    1.227675] i2c /dev entries driver
[    1.268180] mxs-mmc 80010000.ssp: initialized
[    1.273409] leds-gpio leds.7: pins are not configured from the driver
[    1.284729] ledtrig-cpu: registered to indicate activity on CPUs
[    1.291364] hidraw: raw HID events driver (C) Jiri Kosina
[    1.298639] usbcore: registered new interface driver usbhid
[    1.304352] usbhid: USB HID core driver
[    1.312808] TCP: cubic registered
[    1.316159] Initializing XFRM netlink socket
[    1.323251] NET: Registered protocol family 10
[    1.331042] sit: IPv6 over IPv4 tunneling driver
[    1.339081] ip6_gre: GRE over IPv6 tunneling driver
[    1.345642] NET: Registered protocol family 17
[    1.350344] NET: Registered protocol family 15
[    1.355006] can: controller area network core (rev 20120528 abi 9)
[    1.361650] NET: Registered protocol family 29
[    1.366266] can: raw protocol (rev 20120528)
[    1.370777] can: broadcast manager protocol (rev 20120528 t)
[    1.376616] Key type dns_resolver registered
[    1.384233] regulator-dummy: disabling
[    1.391568] rtc-pcf8563 0-0051: setting system clock to 2015-09-28 08:00:07 UTC (1443427207)
[    1.405865] mmc0: host does not support reading read-only switch. assuming write-enable.
[    1.416397] Waiting for root device /dev/mmcblk0p3...
[    1.425628] mmc0: new high speed SDHC card at address e624
[    1.432091] mmcblk0: mmc0:e624 SU04G 3.69 GiB
[    1.439216]  mmcblk0: p1 p2 p3 p4
[    1.531043] EXT4-fs: Warning: mounting with data=journal disables delayed allocation and O_DIRECT support!
[    2.192158] EXT4-fs (mmcblk0p3): recovery complete
[    2.199379] EXT4-fs (mmcblk0p3): mounted filesystem with journalled data mode. Opts: barrier=1,data=journal,commit=1
[    2.210124] VFS: Mounted root (ext4 filesystem) on device 179:3.
[    2.216825] Freeing unused kernel memory: 128K (80605000 - 80625000)
[    2.818776] systemd[1]: systemd 225 running in system mode. (+PAM -AUDIT -SELINUX -IMA -APPARMOR +SMACK -SYSVINIT +UTMP +LIBCRYPTSETUP +GCRYPT +GNUTLS +ACL +XZ +LZ4 +SECCOMP +BLKID -ELFUTILS +KMOD +IDN)
[    2.838542] systemd[1]: Detected architecture arm.

Welcome to Arch Linux ARM!

[    2.870657] systemd[1]: Set hostname to <tuxono-1539414>.
[    2.901072] systemd[1]: Initializing machine ID from random generator.
[    4.241685] systemd[1]: display-manager.service: Cannot add dependency job, ignoring: Unit display-manager.service failed to load: No such file or directory.
[    4.279579] systemd[1]: Started Dispatch Password Requests to Console Directory Watch.
[  OK  ] Started Dispatch Password Requests to Console Directory Watch.
[    4.309061] systemd[1]: Reached target Encrypted Volumes.
[  OK  ] Reached target Encrypted Volumes.
[    4.339997] systemd[1]: Started Forward Password Requests to Wall Directory Watch.
[  OK  ] Started Forward Password Requests to Wall Directory Watch.
[    4.369043] systemd[1]: Reached target Remote File Systems.
[  OK  ] Reached target Remote File Systems.
[    4.401247] systemd[1]: Created slice Root Slice.
[  OK  ] Created slice Root Slice.
[    4.431279] systemd[1]: Listening on udev Kernel Socket.
[  OK  ] Listening on udev Kernel Socket.
[    4.459702] systemd[1]: Listening on udev Control Socket.
[  OK  ] Listening on udev Control Socket.
[    4.489768] systemd[1]: Listening on Journal Socket (/dev/log).
[  OK  ] Listening on Journal Socket (/dev/log).
[    4.521636] systemd[1]: Created slice User and Session Slice.
[  OK  ] Created slice User and Session Slice.
[    4.551636] systemd[1]: Created slice System Slice.
[  OK  ] Created slice System Slice.
[    4.582401] systemd[1]: Created slice system-serial\x2dgetty.slice.
[  OK  ] Created slice system-serial\x2dgetty.slice.
[    4.612089] systemd[1]: Created slice system-promiscuous.slice.
[  OK  ] Created slice system-promiscuous.slice.
[    4.639008] systemd[1]: Reached target Slices.
[  OK  ] Reached target Slices.
[    4.659881] systemd[1]: Listening on Journal Socket.
[  OK  ] Listening on Journal Socket.
[    4.691237] systemd[1]: Starting Setup Virtual Console...
         Starting Setup Virtual Console...
[    4.756163] systemd[1]: Mounting POSIX Message Queue File System...
         Mounting POSIX Message Queue File System...
[    4.852965] systemd[1]: Mounting Configuration File System...
         Mounting Configuration File System...
[    4.973687] systemd[1]: Mounting Debug File System...
         Mounting Debug File System...
[    5.089590] systemd[1]: Starting Apply Kernel Variables...
         Starting Apply Kernel Variables...
[    5.156808] systemd[1]: Starting Remount Root and Kernel File Systems...
         Starting Remount Root and Kernel File Systems...
[    5.327952] systemd[1]: Mounting Temporary Directory...
         Mounting Temporary Directory...
[    5.453434] systemd[1]: Starting Journal Service...
         Starting Journal Service...
[    5.491367] systemd[1]: Reached target Paths.
[  OK  ] Reached target Paths.
[    5.524820] systemd[1]: Listening on /dev/initctl Compatibility Named Pipe.
[  OK  ] Listening on /dev/initctl Compatibility Named Pipe.
[    5.543473] systemd[1]: Reached target Swap.
[  OK  ] Reached target Swap.
[    5.618888] systemd[1]: Mounted POSIX Message Queue File System.
[  OK  ] Mounted POSIX Message Queue File System.
[    5.631271] EXT4-fs (mmcblk0p3): re-mounted. Opts: barrier=1,data=journal,commit=1
[    5.649406] systemd[1]: Mounted Debug File System.
[  OK  ] Mounted Debug File System.
[    5.669260] systemd[1]: Mounted Configuration File System.
[  OK  ] Mounted Configuration File System.
[    5.719418] systemd[1]: Mounted Temporary Directory.
[  OK  ] Mounted Temporary Directory.
[    5.814975] systemd[1]: Started Apply Kernel Variables.
[  OK  ] Started Apply Kernel Variables.
[    5.854401] systemd[1]: Started Remount Root and Kernel File Systems.
[  OK  ] Started Remount Root and Kernel File Systems.
[    6.641097] systemd[1]: Started Setup Virtual Console.
[  OK  ] Started Setup Virtual Console.
[    8.032558] systemd[1]: Starting Rebuild Dynamic Linker Cache...
         Starting Rebuild Dynamic Linker Cache...
[    8.090508] systemd[1]: Starting Load/Save Random Seed...
         Starting Load/Save Random Seed...
[    8.159263] systemd[1]: Starting Create System Users...
         Starting Create System Users...
[    8.334758] systemd[1]: Starting Rebuild Hardware Database...
         Starting Rebuild Hardware Database...
[    8.477787] systemd[1]: Started Load/Save Random Seed.
[  OK  ] Started Load/Save Random Seed.
[    8.524558] systemd[1]: Started Create System Users.
[  OK  ] Started Create System Users.
[    9.401558] systemd[1]: Starting Create Static Device Nodes in /dev...
         Starting Create Static Device Nodes in /dev...
[   10.009144] systemd[1]: Started Create Static Device Nodes in /dev.
[  OK  ] Started Create Static Device Nodes in /dev.
[   10.110303] systemd[1]: Starting udev Kernel Device Manager...
         Starting udev Kernel Device Manager...
[   10.158933] systemd[1]: Reached target Local File Systems (Pre).
[  OK  ] Reached target Local File Systems (Pre).
[   10.860550] systemd[1]: Started Journal Service.
[  OK  ] Started Journal Service.
         Starting Flush Journal to Persistent Storage...
[  OK  ] Started udev Kernel Device Manager.
[   11.460449] systemd-journald[79]: Received request to flush runtime journal from PID 1
[  OK  ] Started Rebuild Dynamic Linker Cache.
[  OK  ] Started Flush Journal to Persistent Storage.
[  OK  ] Started Rebuild Hardware Database.
         Starting udev Coldplug all Devices...
[  OK  ] Started udev Coldplug all Devices.
[  OK  ] Found device /dev/ttyAMA0.
[  OK  ] Found device /dev/mmcblk0p2.
[  OK  ] Found device /dev/mmcblk0p4.
         Mounting /data...
         Mounting /boot...
[   52.656144] EXT4-fs (mmcblk0p4): recovery complete
[   52.693513] EXT4-fs (mmcblk0p4): mounted filesystem with journalled data mode. Opts: barrier=1,data=journal,commit=1
[  OK  ] Mounted /data.
[   52.858834] EXT4-fs (mmcblk0p2): recovery complete
[   52.892191] EXT4-fs (mmcblk0p2): mounted filesystem with journalled data mode. Opts: barrier=1,data=journal,commit=1
[  OK  ] Mounted /boot.
[  OK  ] Reached target Local File Systems.
         Starting Create Volatile Files and Directories...
         Starting Rebuild Journal Catalog...
[  OK  ] Started Create Volatile Files and Directories.
         Starting Update UTMP about System Boot/Shutdown...
         Starting Network Time Synchronization...
[  OK  ] Started Rebuild Journal Catalog.
[  OK  ] Started Network Time Synchronization.
[  OK  ] Started Update UTMP about System Boot/Shutdown.
[  OK  ] Reached target System Time Synchronized.
         Starting Update is Completed...
[  OK  ] Started Update is Completed.
[  OK  ] Reached target System Initialization.
[  OK  ] Started Daily rotation of log files.
[  OK  ] Listening on D-Bus System Message Bus Socket.
[  OK  ] Reached target Sockets.
[  OK  ] Reached target Basic System.
         Starting Permit User Sessions...
         Starting SSH Key Generation...
         Starting Login Service...
[  OK  ] Started D-Bus System Message Bus.
         Starting Network Service...
[  OK  ] Started Daily Cleanup of Temporary Directories.
[  OK  ] Started Daily verification of password and group files.
[  OK  ] Reached target Timers.
[  OK  ] Started Permit User Sessions.
[  OK  ] Started Network Service.
[  OK  ] Started Login Service.
[   59.695056] device eth1 entered promiscuous mode
[  OK  ] Reached target Network.
[   59.781918] device eth0 entered promiscuous mode
         Starting Set br0 interface in promiscuous mode...
[   59.870568] fec 800f4000.ethernet eth1: Freescale FEC PHY driver [SMSC LAN8710/LAN8720] (mii_bus:phy_addr=800f0000.etherne:01, irq=-1)
[   59.940137] IPv6: ADDRCONF(NETDEV_UP): eth1: link is not ready
[   59.950156] device br0 entered promiscuous mode
         Starting Network Name Resolution...
[   60.078327] fec 800f0000.ethernet eth0: Freescale FEC PHY driver [SMSC LAN8710/LAN8720] (mii_bus:phy_addr=800f0000.etherne:00, irq=-1)
[  OK  ] Started Serial Getty on ttyAMA0.
[  OK  ] Reached target L[   60.157361] IPv6: ADDRCONF(NETDEV_UP): eth0: link is not ready
ogin Prompts.
[  OK  ] Started Set br0 interface in promiscuous mode.
[  OK  ] Started Network Name Resolution.
[   61.868884] libphy: 800f0000.etherne:01 - Link is Up - 100/Full
[   61.874896] IPv6: ADDRCONF(NETDEV_CHANGE): eth1: link becomes ready

Arch Linux 3.10.79-00002-gc5ac6b2 (ttyAMA0)

tuxono-1539414 login: [   86.343216] br0: port 1(eth1) entered forwarding state
[   86.348656] br0: port 1(eth1) entered forwarding state
[  101.368114] br0: port 1(eth1) entered forwarding state
alarm
Password:
[alarm@tuxono-1539414 ~]$
```
