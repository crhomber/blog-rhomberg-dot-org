Olimex A20-OLinuXino-MICRO
############################
:date: 2014-03-20 14:00
:slug: olimex-a20
:tags: ARM, Olimex, Angelbird, Hardware

Aktuell spielen wir mit den Boards von Olimex [1]


Die Boards sind relativ guenstig, sehr gut erweiterbar und vor allem haben sie um einiges mehr "Power" als der Raspberry Pi.

Durch die hardwarebeschlaeunigte Grafik lassen sich dann wirklich tolle Sachen anstellen.

Auf den Bildern ist das A20 mit einer SSD von Angelbird [2] zu sehen.

.. image:: images/olimex5.jpg 
	:alt: Olimex

.. image:: images/olimex4.jpg 
	:alt: Olimex

.. image:: images/olimex3.jpg 
	:alt: Olimex

.. image:: images/olimex2.jpg 
	:alt: Olimex

.. image:: images/olimex.jpg 
	:alt: Olimex



Ausgabe von dmesg unter Debian GNU/Linux:

.. code-block:: bash

	olimex@a20-OLinuXino:~$ dmesg
	[    0.000000] Booting Linux on physical CPU 0
	[    0.000000] Initializing cgroup subsys cpuset
	[    0.000000] Initializing cgroup subsys cpu
	[    0.000000] Linux version 3.4.67+ (root@debian) (gcc version 4.7.1 (Debian 4.7.1-7) ) #6 SMP PREEMPT Fri Nov 1 17:32:40 EET 2013
	[    0.000000] CPU: ARMv7 Processor [410fc074] revision 4 (ARMv7), cr=10c5387d
	[    0.000000] CPU: PIPT / VIPT nonaliasing data cache, VIPT aliasing instruction cache
	[    0.000000] Machine: sun7i
	[    0.000000] Memory cut off:
	[    0.000000]  MALI : 0x5c000000 - 0x5fffffff  (  64 MB)
	[    0.000000] Ignoring unrecognised tag 0x00000000
	[    0.000000] Memory Reserved:
	[    0.000000]  SYS  : 0x43000000 - 0x4300ffff  (  64 kB)
	[    0.000000]  VE   : 0x44000000 - 0x48ffffff  (  80 MB)
	[    0.000000]  G2D  : 0x49000000 - 0x49ffffff  (  16 MB)
	[    0.000000]  LCD  : 0x5a000000 - 0x5bffffff  (  32 MB)
	[    0.000000] Memory policy: ECC disabled, Data cache writealloc
	[    0.000000] sunxi: Allwinner A20 (AW1651/sun7i) detected.
	[    0.000000] On node 0 totalpages: 245760
	[    0.000000] free_area_init_node: node 0, pgdat c08731c0, node_mem_map d0000000
	[    0.000000]   DMA zone: 512 pages used for memmap
	[    0.000000]   DMA zone: 0 pages reserved
	[    0.000000]   DMA zone: 65024 pages, LIFO batch:15
	[    0.000000]   Normal zone: 1008 pages used for memmap
	[    0.000000]   Normal zone: 111632 pages, LIFO batch:31
	[    0.000000]   HighMem zone: 528 pages used for memmap
	[    0.000000]   HighMem zone: 67056 pages, LIFO batch:15
	[    0.000000] PERCPU: Embedded 7 pages/cpu @d0808000 s7616 r8192 d12864 u32768
	[    0.000000] pcpu-alloc: s7616 r8192 d12864 u32768 alloc=8*4096
	[    0.000000] pcpu-alloc: [0] 0 [0] 1 
	[    0.000000] Built 1 zonelists in Zone order, mobility grouping on.  Total pages: 243712
	[    0.000000] Kernel command line: console=ttyS0,115200 root=/dev/mmcblk0p2 rootwait loglevel=8 panic=10
	[    0.000000] PID hash table entries: 4096 (order: 2, 16384 bytes)
	[    0.000000] Dentry cache hash table entries: 131072 (order: 7, 524288 bytes)
	[    0.000000] Inode-cache hash table entries: 65536 (order: 6, 262144 bytes)
	[    0.000000] allocated 2097152 bytes of page_cgroup
	[    0.000000] please try 'cgroup_disable=memory' option if you don't want memory cgroups
	[    0.000000] Memory: 448MB 512MB = 960MB total
	[    0.000000] Memory: 830740k/830740k available, 152300k reserved, 270336K highmem
	[    0.000000] Virtual kernel memory layout:
	[    0.000000]     vector  : 0xffff0000 - 0xffff1000   (   4 kB)
	[    0.000000]     fixmap  : 0xfff00000 - 0xfffe0000   ( 896 kB)
	[    0.000000]     vmalloc : 0xf0000000 - 0xff000000   ( 240 MB)
	[    0.000000]     lowmem  : 0xc0000000 - 0xef800000   ( 760 MB)
	[    0.000000]     pkmap   : 0xbfe00000 - 0xc0000000   (   2 MB)
	[    0.000000]     modules : 0xbf000000 - 0xbfe00000   (  14 MB)
	[    0.000000]       .text : 0xc0008000 - 0xc07da6dc   (8010 kB)
	[    0.000000]       .init : 0xc07db000 - 0xc080fdc0   ( 212 kB)
	[    0.000000]       .data : 0xc0810000 - 0xc087a0a0   ( 425 kB)
	[    0.000000]        .bss : 0xc087a0c4 - 0xc0a4b048   (1860 kB)
	[    0.000000] SLUB: Genslabs=11, HWalign=64, Order=0-3, MinObjects=0, CPUs=2, Nodes=1
	[    0.000000] Preemptible hierarchical RCU implementation.
	[    0.000000]  RCU dyntick-idle grace-period acceleration is enabled.
	[    0.000000]  Additional per-CPU info printed with stalls.
	[    0.000000] NR_IRQS:192
	[    0.000000] Architected local timer running at 24.00MHz.
	[    0.000000] sched_clock: 32 bits at 24MHz, resolution 41ns, wraps every 178956ms
	[    0.000000] start_kernel(): bug: interrupts were enabled early
	[    0.000000] Console: colour dummy device 80x30
	[    0.010896] Calibrating delay loop... 1915.28 BogoMIPS (lpj=9576448)
	[    0.076018] pid_max: default: 32768 minimum: 301
	[    0.079687] Mount-cache hash table entries: 512
	[    0.083957] Initializing cgroup subsys cpuacct
	[    0.087279] Initializing cgroup subsys memory
	[    0.090706] Initializing cgroup subsys devices
	[    0.094150] Initializing cgroup subsys freezer
	[    0.097375] Initializing cgroup subsys blkio
	[    0.101052] Initializing cgroup subsys perf_event
	[    0.104634] CPU: Testing write buffer coherency: ok
	[    0.109841] CPU0: thread -1, cpu 0, socket 0, mpidr 80000000
	[    0.116946] hw perfevents: enabled with ARMv7 Cortex-A7 PMU driver, 5 counters available
	[    0.122487] Setting up static identity map for 0x40571840 - 0x40571898
	[    0.238512] CPU1: Booted secondary processor
	[    0.297378] CPU1: thread -1, cpu 1, socket 0, mpidr 80000001
	[    0.299388] Brought up 2 CPUs
	[    0.304701] SMP: Total of 2 processors activated (3830.57 BogoMIPS).
	[    0.307901] devtmpfs: initialized
	[    0.313303] dummy: 
	[    0.316976] NET: Registered protocol family 16
	[    0.324726] hw-breakpoint: found 5 (+1 reserved) breakpoint and 4 watchpoint registers.
	[    0.329515] hw-breakpoint: maximum watchpoint size is 8 bytes.
	[    0.332692] [ccu-inf] aw clock manager init
	[    0.334963] [ccu-inf] aw_ccu_init
	[    0.338924] [ccu-inf] script config pll4 to 300MHz
	[    0.342675] [ccu-inf] script config pll6 to 600MHz
	[    0.346442] [ccu-inf] script config pll7 to 297MHz
	[    0.350188] [ccu-inf] script config pll8 to 336MHz
	[    0.352934] Init eGon pin module V2.0
	[    0.360981] bio: create slab <bio-0> at 0
	[    0.364409] sunxi_gpio driver init ver 1.3
	[    0.370645] gpiochip_add: registered GPIOs 1 to 75 on device: A1X_GPIO
	[    0.373776] SCSI subsystem initialized
	[    0.376621] libata version 3.00 loaded.
	[    0.381317] usbcore: registered new interface driver usbfs
	[    0.385653] usbcore: registered new interface driver hub
	[    0.389825] usbcore: registered new device driver usb
	[    0.392942] Linux media interface: v0.10
	[    0.396546] Linux video capture interface: v2.00
	[    0.402091] Advanced Linux Sound Architecture Driver Version 1.0.25.
	[    0.408268] cfg80211: Calling CRDA to update world regulatory domain
	[    0.412729] Switching to clocksource arch_sys_counter
	[    0.414856] FS-Cache: Loaded
	[    0.417032] CacheFiles: Loaded
	[    0.450583] sw_hcd_host0 sw_hcd_host0: sw_hcd host driver
	[    0.457297] sw_hcd_host0 sw_hcd_host0: new USB bus registered, assigned bus number 1
	[    0.460741] hub 1-0:1.0: USB hub found
	[    0.463637] hub 1-0:1.0: 1 port detected
	[    0.468209] NET: Registered protocol family 2
	[    0.474560] IP route cache hash table entries: 32768 (order: 5, 131072 bytes)
	[    0.481524] TCP established hash table entries: 131072 (order: 8, 1048576 bytes)
	[    0.488993] TCP bind hash table entries: 65536 (order: 7, 786432 bytes)
	[    0.495612] TCP: Hash tables configured (established 131072 bind 65536)
	[    0.497819] TCP: reno registered
	[    0.502696] UDP hash table entries: 512 (order: 2, 16384 bytes)
	[    0.508033] UDP-Lite hash table entries: 512 (order: 2, 16384 bytes)
	[    0.	511685] NET: Registered protocol family 1
	[    0.516987] RPC: Registered named UNIX socket transport module.
	[    0.520690] RPC: Registered udp transport module.
	[    0.524351] RPC: Registered tcp transport module.
	[    0.529752] RPC: Registered tcp NFSv4.1 backchannel transport module.
	[    0.535264] audit: initializing netlink socket (disabled)
	[    0.539023] type=2000 audit(0.520:1): initialized
	[    0.543371] highmem bounce pool size: 64 pages
	[    0.554780] VFS: Disk quotas dquot_6.5.2
	[    0.560358] Dquot-cache hash table entries: 1024 (order 0, 4096 bytes)
	[    0.567150] NFS: Registering the id_resolver key type
	[    0.571719] NTFS driver 2.1.30 [Flags: R/W].
	[    0.575040] fuse init (API version 7.18)
	[    0.578561] msgmni has been set to 1094
	[    0.589516] alg: comp: Compression test 1 failed for lzo-generic: output len = 57
	[    0.592750] alg: No test for stdrng (krng)
	[    0.599444] Block layer SCSI generic (bsg) driver version 0.4 loaded (major 252)
	[    0.602332] io scheduler noop registered
	[    0.605556] io scheduler deadline registered
	[    0.609274] io scheduler cfq registered (default)
	[    0.614094] sunxi disp driver loaded (/dev/disp api 1.0)
	[    0.619677] Serial: 8250/16550 driver, 8 ports, IRQ sharing disabled
	[    0.624155] [uart]: used uart info.: 0xc1
	[    0.628900] [uart]: serial probe 0 irq 33 mapbase 0x01c28000
	[    0.655129] sunxi-uart.0: ttyS0 at MMIO 0x1c28000 (irq = 33) is a U6_16550A
	[    1.386889] console [ttyS0] enabled
	[    1.395228] [uart]: serial probe 6 irq 51 mapbase 0x01c29800
	[    1.427079] sunxi-uart.6: ttyS1 at MMIO 0x1c29800 (irq = 51) is a U6_16550A
	[    1.438871] [uart]: serial probe 7 irq 52 mapbase 0x01c29c00
	[    1.470677] sunxi-uart.7: ttyS2 at MMIO 0x1c29c00 (irq = 52) is a U6_16550A
	[    1.480167] G2D: drv_g2d_init
	[    1.487859] G2D: g2dmem: g2d_start=49000000, g2d_size=1000000
	[    1.496828] G2D: head:c9000000,tail:ca000000
	[    1.504424] G2D: Module initialized.major:250
	[    1.511770] brd: module loaded
	[    1.520435] loop: module loaded
	[    1.529963] sw_ahci sw_ahci.0: controller can't do PMP, turning off CAP_PMP
	[    1.541217] sw_ahci sw_ahci.0: forcing PORTS_IMPL to 0x1
	[    1.553975] sw_ahci sw_ahci.0: AHCI 0001.0100 32 slots 1 ports 3 Gbps 0x1 impl platform mode
	[    1.568850] sw_ahci sw_ahci.0: flags: ncq sntf pm led clo only pio slum part ccc 
	[    1.579662] scsi0 : sw_ahci_platform
	[    1.590444] ata1: SATA max UDMA/133 mmio [mem 0x01c18000-0x01c18fff] port 0x100 irq 88
	[    1.601921] sunxi_emac Using mii phy on PortA
	[    1.621038] sunxi_emac Using MAC from SID: 02:8d:07:82:74:92
	[    1.631703] PPP generic driver version 2.4.2
	[    1.640067] PPP BSD Compression module registered
	[    1.648804] PPP Deflate Compression module registered
	[    1.658792] PPP MPPE Compression module registered
	[    1.667053] NET: Registered protocol family 24
	[    1.677444] ehci_hcd: USB 2.0 'Enhanced' Host Controller (EHCI) Driver
	[    1.689216] ohci_hcd: USB 1.1 'Open' Host Controller (OHCI) Driver
	[    1.697809] [sw-ehci1]: open clock
	[    1.723824] [sw-ehci1]: Set USB Power ON
	[    1.734205] sw-ehci sw-ehci.1: SW USB2.0 'Enhanced' Host Controller (EHCI) Driver
	[    1.747904] sw-ehci sw-ehci.1: new USB bus registered, assigned bus number 2
	[    1.759338] sw-ehci sw-ehci.1: irq 71, io mem 0x01c14000
	[    1.787196] sw-ehci sw-ehci.1: USB 2.0 started, EHCI 1.00
	[    1.795919] hub 2-0:1.0: USB hub found
	[    1.802567] hub 2-0:1.0: 1 port detected
	[    1.809073] [sw-ohci1]: open clock
	[    1.838563] sw-ohci sw-ohci.1: SW USB2.0 'Open' Host Controller (OHCI) Driver
	[    1.851916] sw-ohci sw-ohci.1: new USB bus registered, assigned bus number 3
	[    1.863277] sw-ohci sw-ohci.1: irq 96, io mem 0x01c14400
	[    1.930084] hub 3-0:1.0: USB hub found
	[    1.936750] hub 3-0:1.0: 1 port detected
	[    1.943246] [sw-ehci2]: open clock
	[    1.947601] ata1: SATA link down (SStatus 0 SControl 300)
	[    1.979076] [sw-ehci2]: Set USB Power ON
	[    1.989445] sw-ehci sw-ehci.2: SW USB2.0 'Enhanced' Host Controller (EHCI) Driver
	[    2.003171] sw-ehci sw-ehci.2: new USB bus registered, assigned bus number 4
	[    2.014591] sw-ehci sw-ehci.2: irq 72, io mem 0x01c1c000
	[    2.037237] sw-ehci sw-ehci.2: USB 2.0 started, EHCI 1.00
	[    2.045934] hub 4-0:1.0: USB hub found
	[    2.052565] hub 4-0:1.0: 1 port detected
	[    2.059139] [sw-ohci2]: open clock
	[    2.088628] sw-ohci sw-ohci.2: SW USB2.0 'Open' Host Controller (OHCI) Driver
	[    2.101975] sw-ohci sw-ohci.2: new USB bus registered, assigned bus number 5
	[    2.113329] sw-ohci sw-ohci.2: irq 97, io mem 0x01c1c400
	[    2.180133] hub 5-0:1.0: USB hub found
	[    2.186809] hub 5-0:1.0: 1 port detected
	[    2.195771] mousedev: PS/2 mouse device common for all mice
	[    2.206928] ===========================hv_keypad_init=====================
	[    2.217199] ========HV Inital ===================
	[    2.225811] tkey_fetch_sysconfig_para: tkey_unused. 
	[    2.237995] hv_keypad_init: after fetch_sysconfig_para:  normal_i2c: 0x0. normal_i2c[1]: 0x0 
	[    2.249876] sun4i-ts.c: sun4i_ts_init: start ...
	[    2.256031] rtp_used == 1. 
	[    2.262378] ata1: exception Emask 0x10 SAct 0x0 SErr 0x4050002 action 0xe frozen
	[    2.277467] ata1: irq_stat 0x00400040, connection status changed
	[    2.288576] ata1: SError: { RecovComm PHYRdyChg CommWake DevExch }
	[    2.297345] ata1: hard resetting link
	[    2.304386] sun4i-ts: tp_screen_size is 5 inch.
	[    2.311983] sun4i-ts: tp_regidity_level is 5.
	[    2.320088] sun4i-ts: tp_press_threshold_enable is 0.
	[    2.328449] sun4i-ts: rtp_sensitive_level is 15.
	[    2.336467] sun4i-ts: rtp_exchange_x_y_flag is 0.
	[    2.344641] sun4i-ts.c: sun4i_ts_probe: start...
	[    2.351803] begin get platform resourec
	[    2.361355] input: sun4i-ts as /devices/platform/sun4i-ts/input/input0
	[    2.368908] tp init
	[    2.373875] sun4i-ts.c: sun4i_ts_probe: end
	[    2.383030] sunxi-rtc sunxi-rtc: Warning: RTC time is wrong!
	[    2.393965] sunxi-rtc sunxi-rtc: rtc core: registered rtc as rtc0
	[    2.402571] i2c /dev entries driver
	[    2.409855] config i2c gpio with gpio_config api 
	[    2.420180] axp_mfd 0-0034: AXP (CHIP ID: 0x41) detected
	[    2.429898] i2c i2c-0: Invalid probe address 0x00
	[    2.437669] I2C: i2c-0: AW16XX I2C adapter
	[    2.445749] i2c i2c-1: Invalid probe address 0x00
	[    2.453520] I2C: i2c-1: AW16XX I2C adapter
	[    2.461580] i2c i2c-2: Invalid probe address 0x00
	[    2.469353] I2C: i2c-2: AW16XX I2C adapter
	[    2.475235] [ace_drv] start!!!
	[    2.480639] [ace_drv] init end!!!
	[    2.485632] [pa_drv] start!!!
	[    2.490803] [pa_drv] init end!!!
	[    2.496361] axp20_ldo1: 1300 mV 
	[    2.504783] axp20_ldo2: 1800 <--> 3300 mV at 3000 mV 
	[    2.514906] axp20_ldo3: 700 <--> 3500 mV at 2800 mV 
	[    2.525200] axp20_ldo4: 1250 <--> 3300 mV at 2800 mV 
	[    2.535388] axp20_buck2: 700 <--> 2275 mV at 1400 mV 
	[    2.545575] axp20_buck3: 700 <--> 3500 mV at 1250 mV 
	[    2.555503] axp20_ldoio0: 1800 <--> 3300 mV at 2800 mV 
	[    2.570287] input: axp20-supplyer as /devices/platform/sunxi-i2c.0/i2c-0/0-0034/axp20-supplyer.28/input/input1
	[    2.599407] axp20_ldo2: Failed to create debugfs directory
	[    2.609843] device-mapper: uevent: version 1.0.3
	[    2.622286] device-mapper: ioctl: 4.22.0-ioctl (2011-10-19) initialised: dm-devel@redhat.com
	[    2.635680] device-mapper: multipath: version 1.3.0 loaded
	[    2.646669] device-mapper: multipath round-robin: version 1.0.0 loaded
	[    2.658761] device-mapper: multipath queue-length: version 0.1.0 loaded
	[    2.670933] device-mapper: multipath service-time: version 0.2.0 loaded
	[    2.680957] cpuidle: using governor ladder
	[    2.687954] cpuidle: using governor menu
	[    2.694192] [mmc-msg] sw_mci_init
	[    2.703274] [mmc-msg] MMC host used card: 0x9, boot card: 0x0, io_card 8
	[    2.715251] [mmc-msg] sdc0 set round clock 400000, src 24000000
	[    2.729442] [mmc-msg] sdc0 set ios: clk 0Hz bm OD pm OFF vdd 3.3V width 1 timing LEGACY(SDR12) dt B
	[    2.746705] [mmc-msg] sdc0 Probe: base:0xf00e6000 irq:64 sg_cpu:ffdf7000(4fc00000) ret 0.
	[    2.759861] [mmc-msg] sdc3 set round clock 400000, src 24000000
	[    2.773944] [mmc-msg] sdc3 set ios: clk 0Hz bm OD pm OFF vdd 3.3V width 1 timing LEGACY(SDR12) dt B
	[    2.791170] [mmc-msg] sdc3 Probe: base:0xf00e8000 irq:67 sg_cpu:ffddf000(4fc01000) ret 0.
	[    2.803926] [mmc_pm]: failed to fetch sdio card configuration!
	[    2.814732] ledtrig-cpu: registered to indicate activity on CPUs
	[    2.825856] usbcore: registered new interface driver usbhid
	[    2.834219] usbhid: USB HID core driver
	[    2.840718] ashmem: initialized
	[    2.847508] logger: created 256K log 'log_main'
	[    2.855781] logger: created 256K log 'log_events'
	[    2.864171] logger: created 256K log 'log_radio'
	[    2.872552] logger: created 256K log 'log_system'
	[    2.882812] IPv4 over IPv4 tunneling driver
	[    2.889833] TCP: bic registered
	[    2.895280] TCP: cubic registered
	[    2.901113] TCP: westwood registered
	[    2.907304] TCP: highspeed registered
	[    2.913224] TCP: hybla registered
	[    2.918737] TCP: htcp registered
	[    2.924224] TCP: vegas registered
	[    2.929721] TCP: veno registered
	[    2.935479] TCP: scalable registered
	[    2.941052] TCP: lp registered
	[    2.946286] TCP: yeah registered
	[    2.952032] TCP: illinois registered
	[    2.958827] Initializing XFRM netlink socket
	[    2.967136] NET: Registered protocol family 10
	[    2.976123] NET: Registered protocol family 17
	[    2.984048] NET: Registered protocol family 15
	[    2.992208] Registering the dns_resolver key type
	[    2.998911] VFP support v0.3: implementor 41 architecture 2 part 30 variant 7 rev 4
	[    3.015130] Registering SWP/SWPB emulation handler
	[    3.024537] axp20_buck2: Failed to create debugfs directory
	[    3.029677] ata1: SATA link up 3.0 Gbps (SStatus 123 SControl 300)
	[    3.047589] [cpu_freq] INF:-------------------V-F Table-------------------
	[    3.059564] [cpu_freq] INF:  voltage = 1450mv        frequency = 1008MHz
	[    3.070703] [cpu_freq] INF:  voltage = 1400mv        frequency =  912MHz
	[    3.081836] [cpu_freq] INF:  voltage = 1300mv        frequency =  864MHz
	[    3.092969] [cpu_freq] INF:  voltage = 1250mv        frequency =  792MHz
	[    3.104101] [cpu_freq] INF:  voltage = 1200mv        frequency =  720MHz
	[    3.115234] [cpu_freq] INF:  voltage = 1150mv        frequency =  624MHz
	[    3.126366] [cpu_freq] INF:  voltage = 1100mv        frequency =  528MHz
	[    3.	137498] [cpu_freq] INF:  voltage = 1050mv        frequency =  312MHz
	[    3.148631] [cpu_freq] INF:  voltage = 1000mv        frequency =    0MHz
	[    3.160541] [cpu_freq] INF:-----------------------------------------------
	[    3.177056] [cpu_freq] INF:sunxi_cpufreq_initcall, get cpu frequency from sysconfig, max freq: 912MHz, min freq: 60MHz
	[    3.191550] registered taskstats version 1
	[    3.200770] axp20_buck3: incomplete constraints, leaving on
	[    3.211114] axp20_buck2: incomplete constraints, leaving on
	[    3.221362] axp20_ldo4: incomplete constraints, leaving on
	[    3.231524] axp20_ldo3: incomplete constraints, leaving on
	[    3.241685] axp20_ldo2: incomplete constraints, leaving on
	[    3.251847] axp20_ldo1: incomplete constraints, leaving on
	[    3.260270] console [netcon0] enabled
	[    3.267441] netconsole: network logging started
	[    3.279475] sunxi-rtc sunxi-rtc: setting system clock to 2010-01-01 00:00:00 UTC (1262304000)
	[    3.290013] ALSA device list:
	[    3.296041]   #0: sunxi-CODEC  Audio Codec
	[    3.304667] Waiting for root device /dev/mmcblk0p2...
	[    3.721723] [mmc-msg] mmc 0 detect change, present 1
	[    3.872110] ata1.00: ATA-8: Angelbird Crest SSD 60GB, 4.2, max UDMA/133
	[    3.884386] ata1.00: 117231408 sectors, multi 1: LBA48 NCQ (depth 31/32)
	[    3.929078] ata1.00: configured for UDMA/133
	[    3.935307] ata1: EH complete
	[    3.945853] scsi 0:0:0:0: Direct-Access     ATA      Angelbird Crest  4.2  PQ: 0 ANSI: 5
	[    3.961439] sd 0:0:0:0: [sda] 117231408 512-byte logical blocks: (60.0 GB/55.8 GiB)
	[    3.973633] sd 0:0:0:0: [sda] Write Protect is off
	[    3.982463] sd 0:0:0:0: [sda] Mode Sense: 00 3a 00 00
	[    3.995624] sd 0:0:0:0: [sda] Write cache: enabled, read cache: enabled, doesn't support DPO or FUA
	[    4.007514]  sda: sda1
	[    4.014637] sd 0:0:0:0: [sda] Attached SCSI disk
	[    4.230754] [mmc-msg] sdc0 set ios: clk 0Hz bm PP pm UP vdd 3.3V width 1 timing LEGACY(SDR12) dt B
	[    4.242160] [mmc-msg] sdc0 power on
	[    4.271164] [mmc-msg] sdc0 set ios: clk 400000Hz bm PP pm ON vdd 3.3V width 1 timing LEGACY(SDR12) dt B
	[    4.285457] [mmc-msg] sdc0 set round clock 400000, src 24000000
	[    4.373460] [mmc-err] smc 0 err, cmd 52,  RTO
	[    4.381950] [mmc-err] smc 0 err, cmd 52,  RTO
	[    4.394652] [mmc-msg] sdc0 set ios: clk 400000Hz bm PP pm ON vdd 3.3V width 1 timing LEGACY(SDR12) dt B
	[    4.414799] [mmc-msg] sdc0 set ios: clk 400000Hz bm PP pm ON vdd 3.3V width 1 timing LEGACY(SDR12) dt B
	[    4.429543] [mmc-err] smc 0 err, cmd 5,  RTO
	[    4.437850] [mmc-err] smc 0 err, cmd 5,  RTO
	[    4.446153] [mmc-err] smc 0 err, cmd 5,  RTO
	[    4.454458] [mmc-err] smc 0 err, cmd 5,  RTO
	[    4.467713] [mmc-msg] sdc0 set ios: clk 400000Hz bm PP pm ON vdd 3.3V width 1 timing LEGACY(SDR12) dt B
	[    4.485445] [mmc-msg] sdc0 set ios: clk 400000Hz bm PP pm ON vdd 3.3V width 1 timing LEGACY(SDR12) dt B
	[    4.505548] [mmc-msg] sdc0 set ios: clk 400000Hz bm PP pm ON vdd 3.3V width 1 timing LEGACY(SDR12) dt B
	[    4.554843] [mmc-msg] sdc0 set ios: clk 400000Hz bm PP pm ON vdd 3.3V width 1 timing SD-HS(SDR25) dt B
	[    4.572574] [mmc-msg] sdc0 set ios: clk 50000000Hz bm PP pm ON vdd 3.3V width 1 timing SD-HS(SDR25) dt B
	[    4.587196] [mmc-msg] sdc0 set round clock 42857143, src 600000000
	[    4.656872] [mmc-msg] sdc0 set ios: clk 50000000Hz bm PP pm ON vdd 3.3V width 4 timing SD-HS(SDR25) dt B
	[    4.675790] mmc0: new high speed SDHC card at address 0002
	[    4.685194] mmcblk0: mmc0:0002 00000 7.32 GiB 
	[    4.692696]  mmcblk0: p1 p2
	[    6.	047687] kjournald starting.  Commit interval 5 seconds
	[    6.051876] EXT3-fs (mmcblk0p2): using internal journal
	[    6.075556] EXT3-fs (mmcblk0p2): recovery complete
	[    6.086216] EXT3-fs (mmcblk0p2): mounted filesystem with ordered data mode
	[    6.098119] VFS: Mounted root (ext3 filesystem) on device 179:2.
	[    6.107689] devtmpfs: mounted
	[    6.113537] Freeing init memory: 208K
	[    7.009794] udevd[177]: starting version 175
	[    9.873180] EXT3-fs (mmcblk0p2): using internal journal
	[   10.331931] I2C: i2c-3: HDMI I2C adapter
	[   10.374625] disp clks: lcd 74250000 pre_scale 1 hdmi 74250000 pll 297000000 2x 0
	[   10.978649] Console: switching to colour frame buffer device 160x45
	[   11.071651] UMP<2>: Inserting UMP device driver. Compiled: Oct 29 2013, time: 10:19:59
	[   11.086682] UMP<2>: Using OS memory backend, allocation limit: 134217728
	[   11.099989] UMP: UMP device driver  loaded
	[   11.706857] usbcore: registered new interface driver rtl8192cu
	[   11.804430] [cedar dev]: install start!!!
	[   11.815745] [cedar dev]: install end!!!
	[   15.951491] sunxi_emac sunxi_emac.0: eth0: link up, 100Mbps, full-duplex, lpa 0xC5E1
	[   26.345601] eth0: no IPv6 routers present
	olimex@a20-OLinuXino:~$ 

[1] `Olimex <http://www.olimex.com/>`_

[2] `Angelbird <http://www.angelbird.com/>`_

