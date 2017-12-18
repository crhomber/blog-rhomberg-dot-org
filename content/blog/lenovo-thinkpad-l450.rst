Lenovo Thinkpad L450
######################
:date: 2015-09-05 13:00
:slug: lenovo-thinkpad-l450
:tags: Lenovo, Laptop, Thinkpad, L450, Linux, Hardware

Da mein Thinkpad E130 auf dem CCCamp 2015 endgueltig gestorben ist, habe ich einige Zeit nach einem Ersatz gesucht.

Eigentlich wollte ich kein Lenovo mehr kaufen, jedoch habe ich keine passende Alternative gefunden.

Meine Anforderungen waren ein passables Display, kein optisches Laufwerk, gute Tastatur und unbedingt einen Trackpoint mit eigenen Tasten (das T440 hat das nicht, erst das T450!)

Somit ist es ein Thinkpad L450 geworden, da mir das T450 doch zu teuer war.

Unter Linux laueft das Teil einwandfrei, hier dennoch die Ausgaben von lspci, lsusb und dmesg.

.. code-block:: bash

        [crhomber@192-168-001-109 ~]$ lspci
        00:00.0 Host bridge: Intel Corporation Broadwell-U Host Bridge -OPI (rev 09)
        00:02.0 VGA compatible controller: Intel Corporation Broadwell-U Integrated Graphics (rev 09)
        00:03.0 Audio device: Intel Corporation Broadwell-U Audio Controller (rev 09)
        00:14.0 USB controller: Intel Corporation Wildcat Point-LP USB xHCI Controller (rev 03)
        00:16.0 Communication controller: Intel Corporation Wildcat Point-LP MEI Controller #1 (rev 03)
        00:19.0 Ethernet controller: Intel Corporation Ethernet Connection (3) I218-V (rev 03)
        00:1b.0 Audio device: Intel Corporation Wildcat Point-LP High Definition Audio Controller (rev 03)
        00:1c.0 PCI bridge: Intel Corporation Wildcat Point-LP PCI Express Root Port #1 (rev e3)
        00:1c.2 PCI bridge: Intel Corporation Wildcat Point-LP PCI Express Root Port #3 (rev e3)
        00:1c.5 PCI bridge: Intel Corporation Wildcat Point-LP PCI Express Root Port #6 (rev e3)
        00:1d.0 USB controller: Intel Corporation Wildcat Point-LP USB EHCI Controller (rev 03)
        00:1f.0 ISA bridge: Intel Corporation Wildcat Point-LP LPC Controller (rev 03)
        00:1f.2 SATA controller: Intel Corporation Wildcat Point-LP SATA Controller [AHCI Mode] (rev 03)
        00:1f.3 SMBus: Intel Corporation Wildcat Point-LP SMBus Controller (rev 03)
        00:1f.6 Signal processing controller: Intel Corporation Wildcat Point-LP Thermal Management Controller (rev 03)
        04:00.0 Network controller: Intel Corporation Wireless 7265 (rev 59)
        05:00.0 Unassigned class [ff00]: Realtek Semiconductor Co., Ltd. RTS5227 PCI Express Card Reader (rev 01)
        [crhomber@192-168-001-109 ~]$ 



.. code-block:: bash

        Bus 003 Device 002: ID 8087:8001 Intel Corp. 
        Bus 003 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
        Bus 002 Device 001: ID 1d6b:0003 Linux Foundation 3.0 root hub
        Bus 001 Device 005: ID 04f2:b444 Chicony Electronics Co., Ltd 
        Bus 001 Device 004: ID 138a:0011 Validity Sensors, Inc. VFS5011 Fingerprint Reader
        Bus 001 Device 002: ID 05e3:0608 Genesys Logic, Inc. Hub
        Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub


.. code-block:: bash

        [crhomber@192-168-001-109 ~]$ dmesg
        [    0.000000] Initializing cgroup subsys cpuset
        [    0.000000] Initializing cgroup subsys cpu
        [    0.000000] Initializing cgroup subsys cpuacct
        [    0.000000] Linux version 4.1.6-200.fc22.x86_64 (mockbuild@bkernel02.phx2.fedoraproject.org) (gcc version 5.1.1 20150618 (Red Hat 5.1.1-4) (GCC) ) #1 SMP Mon Aug 17 19:54:31 UTC 2015
        [    0.000000] Command line: BOOT_IMAGE=/vmlinuz-4.1.6-200.fc22.x86_64 root=/dev/mapper/fedora_192--168--001--109-root ro rd.luks.uuid=luks-f395d3d9-b322-4fe3-94b8-8a74105213f4 rd.lvm.lv=fedora_192-168-001-109/root rd.lvm.lv=fedora_192-168-001-109/swap rhgb quiet LANG=en_US.UTF-8
        [    0.000000] e820: BIOS-provided physical RAM map:
        [    0.000000] BIOS-e820: [mem 0x0000000000000000-0x000000000009cfff] usable
        [    0.000000] BIOS-e820: [mem 0x000000000009d000-0x000000000009ffff] reserved
        [    0.000000] BIOS-e820: [mem 0x00000000000e0000-0x00000000000fffff] reserved
        [    0.000000] BIOS-e820: [mem 0x0000000000100000-0x000000000fffffff] usable
        [    0.000000] BIOS-e820: [mem 0x0000000010000000-0x000000001000afff] reserved
        [    0.000000] BIOS-e820: [mem 0x000000001000b000-0x00000000beccffff] usable
        [    0.000000] BIOS-e820: [mem 0x00000000becd0000-0x00000000ccdfefff] reserved
        [    0.000000] BIOS-e820: [mem 0x00000000ccdff000-0x00000000ccf7efff] ACPI NVS
        [    0.000000] BIOS-e820: [mem 0x00000000ccf7f000-0x00000000ccffefff] ACPI data
        [    0.000000] BIOS-e820: [mem 0x00000000ccfff000-0x00000000cfffffff] reserved
        [    0.000000] BIOS-e820: [mem 0x00000000f8000000-0x00000000fbffffff] reserved
        [    0.000000] BIOS-e820: [mem 0x00000000fec00000-0x00000000fec00fff] reserved
        [    0.000000] BIOS-e820: [mem 0x00000000fed08000-0x00000000fed08fff] reserved
        [    0.000000] BIOS-e820: [mem 0x00000000fed10000-0x00000000fed19fff] reserved
        [    0.000000] BIOS-e820: [mem 0x00000000fed1c000-0x00000000fed1ffff] reserved
        [    0.000000] BIOS-e820: [mem 0x00000000fee00000-0x00000000fee00fff] reserved
        [    0.000000] BIOS-e820: [mem 0x00000000ff000000-0x00000000ff000fff] reserved
        [    0.000000] BIOS-e820: [mem 0x00000000ffa00000-0x00000000ffffffff] reserved
        [    0.000000] BIOS-e820: [mem 0x0000000100000000-0x000000012effffff] usable
        [    0.000000] NX (Execute Disable) protection: active
        [    0.000000] SMBIOS 2.7 present.
        [    0.000000] DMI: LENOVO 20DT0003GE/Intel powered classmate PC, BIOS JDET50WW (1.12 ) 03/25/2015
        [    0.000000] e820: update [mem 0x00000000-0x00000fff] usable ==> reserved
        [    0.000000] e820: remove [mem 0x000a0000-0x000fffff] usable
        [    0.000000] e820: last_pfn = 0x12f000 max_arch_pfn = 0x400000000
        [    0.000000] MTRR default type: write-back
        [    0.000000] MTRR fixed ranges enabled:
        [    0.000000]   00000-9FFFF write-back
        [    0.000000]   A0000-BFFFF uncachable
        [    0.000000]   C0000-FFFFF write-protect
        [    0.000000] MTRR variable ranges enabled:
        [    0.000000]   0 base 00E0000000 mask 7FF0000000 uncachable
        [    0.000000]   1 base 00D0000000 mask 7FF0000000 uncachable
        [    0.000000]   2 base 00CE000000 mask 7FFE000000 uncachable
        [    0.000000]   3 base 00CD000000 mask 7FFF000000 uncachable
        [    0.000000]   4 base 00F0000000 mask 7FF0000000 uncachable
        [    0.000000]   5 disabled
        [    0.000000]   6 disabled
        [    0.000000]   7 disabled
        [    0.000000]   8 disabled
        [    0.000000]   9 disabled
        [    0.000000] PAT configuration [0-7]: WB  WC  UC- UC  WB  WC  UC- UC  
        [    0.000000] e820: last_pfn = 0xbecd0 max_arch_pfn = 0x400000000
        [    0.000000] found SMP MP-table at [mem 0x000f0100-0x000f010f] mapped at [ffff8800000f0100]
        [    0.000000] Base memory trampoline at [ffff880000097000] 97000 size 24576
        [    0.000000] Using GB pages for direct mapping
        [    0.000000] init_memory_mapping: [mem 0x00000000-0x000fffff]
        [    0.000000]  [mem 0x00000000-0x000fffff] page 4k
        [    0.000000] BRK [0x02039000, 0x02039fff] PGTABLE
        [    0.000000] BRK [0x0203a000, 0x0203afff] PGTABLE
        [    0.000000] BRK [0x0203b000, 0x0203bfff] PGTABLE
        [    0.000000] init_memory_mapping: [mem 0x12ee00000-0x12effffff]
        [    0.000000]  [mem 0x12ee00000-0x12effffff] page 2M
        [    0.000000] BRK [0x0203c000, 0x0203cfff] PGTABLE
        [    0.000000] init_memory_mapping: [mem 0x120000000-0x12edfffff]
        [    0.000000]  [mem 0x120000000-0x12edfffff] page 2M
        [    0.000000] init_memory_mapping: [mem 0x100000000-0x11fffffff]
        [    0.000000]  [mem 0x100000000-0x11fffffff] page 2M
        [    0.000000] init_memory_mapping: [mem 0x00100000-0x0fffffff]
        [    0.000000]  [mem 0x00100000-0x001fffff] page 4k
        [    0.000000]  [mem 0x00200000-0x0fffffff] page 2M
        [    0.000000] init_memory_mapping: [mem 0x1000b000-0xbeccffff]
        [    0.000000]  [mem 0x1000b000-0x101fffff] page 4k
        [    0.000000]  [mem 0x10200000-0x3fffffff] page 2M
        [    0.000000]  [mem 0x40000000-0x7fffffff] page 1G
        [    0.000000]  [mem 0x80000000-0xbebfffff] page 2M
        [    0.000000]  [mem 0xbec00000-0xbeccffff] page 4k
        [    0.000000] BRK [0x0203d000, 0x0203dfff] PGTABLE
        [    0.000000] BRK [0x0203e000, 0x0203efff] PGTABLE
        [    0.000000] RAMDISK: [mem 0x359e7000-0x36cebfff]
        [    0.000000] ACPI: Early table checksum verification disabled
        [    0.000000] ACPI: RSDP 0x00000000000F0120 000024 (v02 LENOVO)
        [    0.000000] ACPI: XSDT 0x00000000CCFFE1C0 0000E4 (v01 LENOVO TP-JD    00001120 PTEC 00000002)
        [    0.000000] ACPI: FACP 0x00000000CCFF8000 00010C (v05 LENOVO TP-JD    00001120 PTEC 00000002)
        [    0.000000] ACPI: DSDT 0x00000000CCFE3000 010FC1 (v01 LENOVO TP-JD    00001120 INTL 20120711)
        [    0.000000] ACPI: FACS 0x00000000CCF68000 000040
        [    0.000000] ACPI: SLIC 0x00000000CCFFD000 000176 (v01 LENOVO TP-JD    00001120 PTEC 00000001)
        [    0.000000] ACPI: ASF! 0x00000000CCFFC000 0000A5 (v32 LENOVO TP-JD    00001120 PTEC 00000002)
        [    0.000000] ACPI: HPET 0x00000000CCFFB000 000038 (v01 LENOVO TP-JD    00001120 PTEC 00000002)
        [    0.000000] ACPI: ECDT 0x00000000CCFFA000 000052 (v01 LENOVO TP-JD    00001120 PTEC 00000002)
        [    0.000000] ACPI: APIC 0x00000000CCFF7000 000098 (v01 LENOVO TP-JD    00001120 PTEC 00000002)
        [    0.000000] ACPI: MCFG 0x00000000CCFF6000 00003C (v01 LENOVO TP-JD    00001120 PTEC 00000002)
        [    0.000000] ACPI: SSDT 0x00000000CCFF5000 000033 (v01 LENOVO TP-SSDT1 00000100 INTL 20120711)
        [    0.000000] ACPI: SSDT 0x00000000CCFF4000 000486 (v01 LENOVO TP-SSDT2 00000200 INTL 20120711)
        [    0.000000] ACPI: SSDT 0x00000000CCFE2000 0009CB (v01 LENOVO SataAhci 00001000 INTL 20120711)
        [    0.000000] ACPI: SSDT 0x00000000CCFE1000 00062A (v01 LENOVO Cpu0Ist  00003000 INTL 20120711)
        [    0.000000] ACPI: SSDT 0x00000000CCFE0000 000B74 (v02 LENOVO CpuSsdt  00003000 INTL 20120711)
        [    0.000000] ACPI: SSDT 0x00000000CCFDF000 000369 (v02 LENOVO CtdpB    00001000 INTL 20120711)
        [    0.000000] ACPI: SSDT 0x00000000CCFDD000 001477 (v01 LENOVO SaSsdt   00003000 INTL 20120711)
        [    0.000000] ACPI: SSDT 0x00000000CCFDC000 000394 (v02 LENOVO CppcTabl 00001000 INTL 20120711)
        [    0.000000] ACPI: PCCT 0x00000000CCFDB000 00006E (v05 LENOVO TP-JD    00001120 PTEC 00000002)
        [    0.000000] ACPI: SSDT 0x00000000CCFDA000 000AC4 (v02 LENOVO Cpc_Tabl 00001000 INTL 20120711)
        [    0.000000] ACPI: TCPA 0x00000000CCFD9000 000032 (v02 PTL    LENOVO   06040000 LNVO 00000001)
        [    0.000000] ACPI: SSDT 0x00000000CCFD8000 0006A5 (v01 Intel_ TpmTable 00001000 INTL 20120711)
        [    0.000000] ACPI: UEFI 0x00000000CCFD7000 000042 (v01 LENOVO TP-JD    00001120 PTEC 00000002)
        [    0.000000] ACPI: MSDM 0x00000000CCEB1000 000055 (v03 LENOVO TP-JD    00001120 PTEC 00000002)
        [    0.000000] ACPI: BATB 0x00000000CCFD6000 000046 (v01 LENOVO TP-JD    00001120 PTEC 00000002)
        [    0.000000] ACPI: FPDT 0x00000000CCFD5000 000064 (v01 LENOVO TP-JD    00001120 PTEC 00000002)
        [    0.000000] ACPI: UEFI 0x00000000CCFD4000 0002F6 (v01 LENOVO TP-JD    00001120 PTEC 00000002)
        [    0.000000] ACPI: Local APIC address 0xfee00000
        [    0.000000] No NUMA configuration found
        [    0.000000] Faking a node at [mem 0x0000000000000000-0x000000012effffff]
        [    0.000000] NODE_DATA(0) allocated [mem 0x12efeb000-0x12effefff]
        [    0.000000]  [ffffea0000000000-ffffea0004bfffff] PMD -> [ffff88012aa00000-ffff88012e5fffff] on node 0
        [    0.000000] Zone ranges:
        [    0.000000]   DMA      [mem 0x0000000000001000-0x0000000000ffffff]
        [    0.000000]   DMA32    [mem 0x0000000001000000-0x00000000ffffffff]
        [    0.000000]   Normal   [mem 0x0000000100000000-0x000000012effffff]
        [    0.000000] Movable zone start for each node
        [    0.000000] Early memory node ranges
        [    0.000000]   node   0: [mem 0x0000000000001000-0x000000000009cfff]
        [    0.000000]   node   0: [mem 0x0000000000100000-0x000000000fffffff]
        [    0.000000]   node   0: [mem 0x000000001000b000-0x00000000beccffff]
        [    0.000000]   node   0: [mem 0x0000000100000000-0x000000012effffff]
        [    0.000000] Initmem setup node 0 [mem 0x0000000000001000-0x000000012effffff]
        [    0.000000] On node 0 totalpages: 973921
        [    0.000000]   DMA zone: 64 pages used for memmap
        [    0.000000]   DMA zone: 21 pages reserved
        [    0.000000]   DMA zone: 3996 pages, LIFO batch:0
        [    0.000000]   DMA32 zone: 12148 pages used for memmap
        [    0.000000]   DMA32 zone: 777413 pages, LIFO batch:31
        [    0.000000]   Normal zone: 3008 pages used for memmap
        [    0.000000]   Normal zone: 192512 pages, LIFO batch:31
        [    0.000000] Reserving Intel graphics stolen memory at 0xce000000-0xcfffffff
        [    0.000000] ACPI: PM-Timer IO Port: 0x1808
        [    0.000000] ACPI: Local APIC address 0xfee00000
        [    0.000000] ACPI: LAPIC_NMI (acpi_id[0x00] high edge lint[0x1])
        [    0.000000] ACPI: LAPIC_NMI (acpi_id[0x01] high edge lint[0x1])
        [    0.000000] IOAPIC[0]: apic_id 2, version 32, address 0xfec00000, GSI 0-39
        [    0.000000] ACPI: INT_SRC_OVR (bus 0 bus_irq 0 global_irq 2 dfl dfl)
        [    0.000000] ACPI: INT_SRC_OVR (bus 0 bus_irq 9 global_irq 9 high level)
        [    0.000000] ACPI: IRQ0 used by override.
        [    0.000000] ACPI: IRQ9 used by override.
        [    0.000000] Using ACPI (MADT) for SMP configuration information
        [    0.000000] ACPI: HPET id: 0x8086a301 base: 0xfed00000
        [    0.000000] smpboot: Allowing 8 CPUs, 4 hotplug CPUs
        [    0.000000] PM: Registered nosave memory: [mem 0x00000000-0x00000fff]
        [    0.000000] PM: Registered nosave memory: [mem 0x0009d000-0x0009ffff]
        [    0.000000] PM: Registered nosave memory: [mem 0x000a0000-0x000dffff]
        [    0.000000] PM: Registered nosave memory: [mem 0x000e0000-0x000fffff]
        [    0.000000] PM: Registered nosave memory: [mem 0x10000000-0x1000afff]
        [    0.000000] PM: Registered nosave memory: [mem 0xbecd0000-0xccdfefff]
        [    0.000000] PM: Registered nosave memory: [mem 0xccdff000-0xccf7efff]
        [    0.000000] PM: Registered nosave memory: [mem 0xccf7f000-0xccffefff]
        [    0.000000] PM: Registered nosave memory: [mem 0xccfff000-0xcfffffff]
        [    0.000000] PM: Registered nosave memory: [mem 0xd0000000-0xf7ffffff]
        [    0.000000] PM: Registered nosave memory: [mem 0xf8000000-0xfbffffff]
        [    0.000000] PM: Registered nosave memory: [mem 0xfc000000-0xfebfffff]
        [    0.000000] PM: Registered nosave memory: [mem 0xfec00000-0xfec00fff]
        [    0.000000] PM: Registered nosave memory: [mem 0xfec01000-0xfed07fff]
        [    0.000000] PM: Registered nosave memory: [mem 0xfed08000-0xfed08fff]
        [    0.000000] PM: Registered nosave memory: [mem 0xfed09000-0xfed0ffff]
        [    0.000000] PM: Registered nosave memory: [mem 0xfed10000-0xfed19fff]
        [    0.000000] PM: Registered nosave memory: [mem 0xfed1a000-0xfed1bfff]
        [    0.000000] PM: Registered nosave memory: [mem 0xfed1c000-0xfed1ffff]
        [    0.000000] PM: Registered nosave memory: [mem 0xfed20000-0xfedfffff]
        [    0.000000] PM: Registered nosave memory: [mem 0xfee00000-0xfee00fff]
        [    0.000000] PM: Registered nosave memory: [mem 0xfee01000-0xfeffffff]
        [    0.000000] PM: Registered nosave memory: [mem 0xff000000-0xff000fff]
        [    0.000000] PM: Registered nosave memory: [mem 0xff001000-0xff9fffff]
        [    0.000000] PM: Registered nosave memory: [mem 0xffa00000-0xffffffff]
        [    0.000000] e820: [mem 0xd0000000-0xf7ffffff] available for PCI devices
        [    0.000000] Booting paravirtualized kernel on bare hardware
        [    0.000000] clocksource refined-jiffies: mask: 0xffffffff max_cycles: 0xffffffff, max_idle_ns: 1910969940391419 ns
        [    0.000000] setup_percpu: NR_CPUS:1024 nr_cpumask_bits:8 nr_cpu_ids:8 nr_node_ids:1
        [    0.000000] PERCPU: Embedded 34 pages/cpu @ffff88012ec00000 s101016 r8192 d30056 u262144
        [    0.000000] pcpu-alloc: s101016 r8192 d30056 u262144 alloc=1*2097152
        [    0.000000] pcpu-alloc: [0] 0 1 2 3 4 5 6 7 
        [    0.000000] Built 1 zonelists in Node order, mobility grouping on.  Total pages: 958680
        [    0.000000] Policy zone: Normal
        [    0.000000] Kernel command line: BOOT_IMAGE=/vmlinuz-4.1.6-200.fc22.x86_64 root=/dev/mapper/fedora_192--168--001--109-root ro rd.luks.uuid=luks-f395d3d9-b322-4fe3-94b8-8a74105213f4 rd.lvm.lv=fedora_192-168-001-109/root rd.lvm.lv=fedora_192-168-001-109/swap rhgb quiet LANG=en_US.UTF-8
        [    0.000000] PID hash table entries: 4096 (order: 3, 32768 bytes)
        [    0.000000] xsave: enabled xstate_bv 0x7, cntxt size 0x340 using standard form
        [    0.000000] Memory: 3730572K/3895684K available (7836K kernel code, 1242K rwdata, 3268K rodata, 1516K init, 1524K bss, 165112K reserved, 0K cma-reserved)
        [    0.000000] SLUB: HWalign=64, Order=0-3, MinObjects=0, CPUs=8, Nodes=1
        [    0.000000] Hierarchical RCU implementation.
        [    0.000000] 	RCU dyntick-idle grace-period acceleration is enabled.
        [    0.000000] 	RCU restricting CPUs from NR_CPUS=1024 to nr_cpu_ids=8.
        [    0.000000] RCU: Adjusting geometry for rcu_fanout_leaf=16, nr_cpu_ids=8
        [    0.000000] NR_IRQS:65792 nr_irqs:760 16
        [    0.000000] 	Offload RCU callbacks from all CPUs
        [    0.000000] 	Offload RCU callbacks from CPUs: 0-7.
        [    0.000000] Console: colour VGA+ 80x25
        [    0.000000] console [tty0] enabled
        [    0.000000] clocksource hpet: mask: 0xffffffff max_cycles: 0xffffffff, max_idle_ns: 133484882848 ns
        [    0.000000] hpet clockevent registered
        [    0.000000] tsc: Fast TSC calibration using PIT
        [    0.000000] tsc: Detected 2194.916 MHz processor
        [    0.000032] Calibrating delay loop (skipped), value calculated using timer frequency.. 4389.83 BogoMIPS (lpj=2194916)
        [    0.000034] pid_max: default: 32768 minimum: 301
        [    0.000041] ACPI: Core revision 20150410
        [    0.022207] ACPI: All ACPI Tables successfully acquired
        [    0.022232] Security Framework initialized
        [    0.022238] SELinux:  Initializing.
        [    0.022245] SELinux:  Starting in permissive mode
        [    0.022246] Yama: becoming mindful.
        [    0.022573] Dentry cache hash table entries: 524288 (order: 10, 4194304 bytes)
        [    0.023488] Inode-cache hash table entries: 262144 (order: 9, 2097152 bytes)
        [    0.023896] Mount-cache hash table entries: 8192 (order: 4, 65536 bytes)
        [    0.023902] Mountpoint-cache hash table entries: 8192 (order: 4, 65536 bytes)
        [    0.024115] Initializing cgroup subsys blkio
        [    0.024117] Initializing cgroup subsys memory
        [    0.024124] Initializing cgroup subsys devices
        [    0.024126] Initializing cgroup subsys freezer
        [    0.024129] Initializing cgroup subsys net_cls
        [    0.024131] Initializing cgroup subsys perf_event
        [    0.024133] Initializing cgroup subsys net_prio
        [    0.024135] Initializing cgroup subsys hugetlb
        [    0.024162] CPU: Physical Processor ID: 0
        [    0.024163] CPU: Processor Core ID: 0
        [    0.024167] ENERGY_PERF_BIAS: Set to 'normal', was 'performance'
        [    0.024168] ENERGY_PERF_BIAS: View and update with x86_energy_perf_policy(8)
        [    0.025239] mce: CPU supports 7 MCE banks
        [    0.025252] CPU0: Thermal monitoring enabled (TM1)
        [    0.025261] process: using mwait in idle threads
        [    0.025264] Last level iTLB entries: 4KB 64, 2MB 8, 4MB 8
        [    0.025265] Last level dTLB entries: 4KB 64, 2MB 0, 4MB 0, 1GB 4
        [    0.025627] Freeing SMP alternatives memory: 28K (ffffffff81eb3000 - ffffffff81eba000)
        [    0.030620] ftrace: allocating 28150 entries in 110 pages
        [    0.043354] x2apic: IRQ remapping doesn't support X2APIC mode
        [    0.044020] ..TIMER: vector=0x30 apic1=0 pin1=2 apic2=-1 pin2=-1
        [    0.054035] TSC deadline timer enabled
        [    0.054038] smpboot: CPU0: Intel(R) Core(TM) i5-5200U CPU @ 2.20GHz (fam: 06, model: 3d, stepping: 04)
        [    0.054061] Performance Events: PEBS fmt2+, 16-deep LBR, Broadwell events, full-width counters, Intel PMU driver.
        [    0.054083] ... version:                3
        [    0.054084] ... bit width:              48
        [    0.054085] ... generic registers:      4
        [    0.054086] ... value mask:             0000ffffffffffff
        [    0.054087] ... max period:             0000ffffffffffff
        [    0.054088] ... fixed-purpose events:   3
        [    0.054089] ... event mask:             000000070000000f
        [    0.054863] x86: Booting SMP configuration:
        [    0.054864] .... node  #0, CPUs:      #1
        [    0.069292] NMI watchdog: enabled on all CPUs, permanently consumes one hw-PMU counter.
        [    0.069369]  #2 #3
        [    0.098128] x86: Booted up 1 node, 4 CPUs
        [    0.098131] smpboot: Total of 4 processors activated (17559.32 BogoMIPS)
        [    0.102182] devtmpfs: initialized
        [    0.104214] PM: Registering ACPI NVS region [mem 0xccdff000-0xccf7efff] (1572864 bytes)
        [    0.104304] clocksource jiffies: mask: 0xffffffff max_cycles: 0xffffffff, max_idle_ns: 1911260446275000 ns
        [    0.104390] atomic64_test: passed for x86-64 platform with CX8 and with SSE
        [    0.104393] pinctrl core: initialized pinctrl subsystem
        [    0.104432] RTC time: 18:19:12, date: 09/04/15
        [    0.104550] NET: Registered protocol family 16
        [    0.106961] cpuidle: using governor menu
        [    0.107025] ACPI FADT declares the system doesn't support PCIe ASPM, so disable it
        [    0.107027] ACPI: bus type PCI registered
        [    0.107028] acpiphp: ACPI Hot Plug PCI Controller Driver version: 0.5
        [    0.107222] PCI: MMCONFIG for domain 0000 [bus 00-3f] at [mem 0xf8000000-0xfbffffff] (base 0xf8000000)
        [    0.107224] PCI: MMCONFIG at [mem 0xf8000000-0xfbffffff] reserved in E820
        [    0.107303] PCI: Using configuration type 1 for base access
        [    0.111296] ACPI: Added _OSI(Module Device)
        [    0.111298] ACPI: Added _OSI(Processor Device)
        [    0.111300] ACPI: Added _OSI(3.0 _SCP Extensions)
        [    0.111301] ACPI: Added _OSI(Processor Aggregator Device)
        [    0.113500] ACPI : EC: EC description table is found, configuring boot EC
        [    0.113511] ACPI : EC: EC started
        [    0.119102] [Firmware Bug]: ACPI: BIOS _OSI(Linux) query ignored
        [    0.130706] ACPI: Dynamic OEM Table Load:
        [    0.130719] ACPI: SSDT 0xFFFF8801298A0800 000436 (v01 PmRef  Cpu0Cst  00003001 INTL 20120711)
        [    0.131516] ACPI: Dynamic OEM Table Load:
        [    0.131526] ACPI: SSDT 0xFFFF8801298A1000 0005AA (v01 PmRef  ApIst    00003000 INTL 20120711)
        [    0.132370] ACPI: Dynamic OEM Table Load:
        [    0.132378] ACPI: SSDT 0xFFFF880129B54000 000119 (v02 PmRef  ApCst    00003000 INTL 20120711)
        [    0.133595] ACPI: Interpreter enabled
        [    0.133604] ACPI Exception: AE_NOT_FOUND, While evaluating Sleep State [\_S1_] (20150410/hwxface-580)
        [    0.133612] ACPI Exception: AE_NOT_FOUND, While evaluating Sleep State [\_S2_] (20150410/hwxface-580)
        [    0.133632] ACPI: (supports S0 S3 S4 S5)
        [    0.133633] ACPI: Using IOAPIC for interrupt routing
        [    0.133663] PCI: Using host bridge windows from ACPI; if necessary, use "pci=nocrs" and report a bug
        [    0.139144] ACPI: Power Resource [PUBS] (on)
        [    0.140694] ACPI: Power Resource [AMD3] (on)
        [    0.140720] ACPI: Power Resource [AMD2] (on)
        [    0.147387] ACPI: PCI Interrupt Link [LNKA] (IRQs 3 4 5 6 7 9 10 *11)
        [    0.147455] ACPI: PCI Interrupt Link [LNKB] (IRQs 3 4 5 6 7 9 *10 11)
        [    0.147520] ACPI: PCI Interrupt Link [LNKC] (IRQs 3 4 5 6 7 9 *10 11)
        [    0.147584] ACPI: PCI Interrupt Link [LNKD] (IRQs 3 4 5 6 7 *9 10 11)
        [    0.147647] ACPI: PCI Interrupt Link [LNKE] (IRQs 3 4 5 *6 7 9 10 11)
        [    0.147697] ACPI: PCI Interrupt Link [LNKF] (IRQs 3 4 5 6 7 9 10 11) *0, disabled.
        [    0.147761] ACPI: PCI Interrupt Link [LNKG] (IRQs 3 4 5 6 7 9 10 *11)
        [    0.147825] ACPI: PCI Interrupt Link [LNKH] (IRQs 3 4 5 6 *7 9 10 11)
        [    0.147902] ACPI: PCI Root Bridge [PCI0] (domain 0000 [bus 00-3f])
        [    0.147907] acpi PNP0A08:00: _OSC: OS supports [ExtendedConfig ASPM ClockPM Segments MSI]
        [    0.148005] acpi PNP0A08:00: _OSC: platform does not support [PCIeCapability]
        [    0.148048] acpi PNP0A08:00: _OSC: not requesting control; platform does not support [PCIeCapability]
        [    0.148050] acpi PNP0A08:00: _OSC: OS requested [PCIeHotplug PME AER PCIeCapability]
        [    0.148052] acpi PNP0A08:00: _OSC: platform willing to grant [PCIeHotplug PME AER]
        [    0.148054] acpi PNP0A08:00: _OSC failed (AE_SUPPORT); disabling ASPM
        [    0.148189] PCI host bridge to bus 0000:00
        [    0.148191] pci_bus 0000:00: root bus resource [bus 00-3f]
        [    0.148193] pci_bus 0000:00: root bus resource [io  0x0000-0x0cf7 window]
        [    0.148195] pci_bus 0000:00: root bus resource [io  0x0d00-0xffff window]
        [    0.148197] pci_bus 0000:00: root bus resource [mem 0x000a0000-0x000bffff window]
        [    0.148198] pci_bus 0000:00: root bus resource [mem 0xd0000000-0xfebfffff window]
        [    0.148200] pci_bus 0000:00: root bus resource [mem 0xfed40000-0xfed4bfff window]
        [    0.148207] pci 0000:00:00.0: [8086:1604] type 00 class 0x060000
        [    0.148284] pci 0000:00:02.0: [8086:1616] type 00 class 0x030000
        [    0.148294] pci 0000:00:02.0: reg 0x10: [mem 0xf0000000-0xf0ffffff 64bit]
        [    0.148301] pci 0000:00:02.0: reg 0x18: [mem 0xe0000000-0xefffffff 64bit pref]
        [    0.148306] pci 0000:00:02.0: reg 0x20: [io  0x3000-0x303f]
        [    0.148383] pci 0000:00:03.0: [8086:160c] type 00 class 0x040300
        [    0.148391] pci 0000:00:03.0: reg 0x10: [mem 0xf1230000-0xf1233fff 64bit]
        [    0.148482] pci 0000:00:14.0: [8086:9cb1] type 00 class 0x0c0330
        [    0.148497] pci 0000:00:14.0: reg 0x10: [mem 0xf1220000-0xf122ffff 64bit]
        [    0.148549] pci 0000:00:14.0: PME# supported from D3hot D3cold
        [    0.148575] pci 0000:00:14.0: System wakeup disabled by ACPI
        [    0.148610] pci 0000:00:16.0: [8086:9cba] type 00 class 0x078000
        [    0.148628] pci 0000:00:16.0: reg 0x10: [mem 0xf1239000-0xf123901f 64bit]
        [    0.148688] pci 0000:00:16.0: PME# supported from D0 D3hot D3cold
        [    0.148750] pci 0000:00:19.0: [8086:15a3] type 00 class 0x020000
        [    0.148763] pci 0000:00:19.0: reg 0x10: [mem 0xf1200000-0xf121ffff]
        [    0.148771] pci 0000:00:19.0: reg 0x14: [mem 0xf123e000-0xf123efff]
        [    0.148778] pci 0000:00:19.0: reg 0x18: [io  0x3080-0x309f]
        [    0.148826] pci 0000:00:19.0: PME# supported from D0 D3hot D3cold
        [    0.148853] pci 0000:00:19.0: System wakeup disabled by ACPI
        [    0.148885] pci 0000:00:1b.0: [8086:9ca0] type 00 class 0x040300
        [    0.148900] pci 0000:00:1b.0: reg 0x10: [mem 0xf1234000-0xf1237fff 64bit]
        [    0.148951] pci 0000:00:1b.0: PME# supported from D0 D3hot D3cold
        [    0.149007] pci 0000:00:1c.0: [8086:9c90] type 01 class 0x060400
        [    0.149064] pci 0000:00:1c.0: PME# supported from D0 D3hot D3cold
        [    0.149161] pci 0000:00:1c.2: [8086:9c94] type 01 class 0x060400
        [    0.149221] pci 0000:00:1c.2: PME# supported from D0 D3hot D3cold
        [    0.149279] pci 0000:00:1c.2: System wakeup disabled by ACPI
        [    0.149314] pci 0000:00:1c.5: [8086:9c9a] type 01 class 0x060400
        [    0.149370] pci 0000:00:1c.5: PME# supported from D0 D3hot D3cold
        [    0.149460] pci 0000:00:1d.0: [8086:9ca6] type 00 class 0x0c0320
        [    0.149477] pci 0000:00:1d.0: reg 0x10: [mem 0xf123d000-0xf123d3ff]
        [    0.149552] pci 0000:00:1d.0: PME# supported from D0 D3hot D3cold
        [    0.149581] pci 0000:00:1d.0: System wakeup disabled by ACPI
        [    0.149617] pci 0000:00:1f.0: [8086:9cc3] type 00 class 0x060100
        [    0.149768] pci 0000:00:1f.2: [8086:9c83] type 00 class 0x010601
        [    0.149779] pci 0000:00:1f.2: reg 0x10: [io  0x30a8-0x30af]
        [    0.149786] pci 0000:00:1f.2: reg 0x14: [io  0x30b4-0x30b7]
        [    0.149793] pci 0000:00:1f.2: reg 0x18: [io  0x30a0-0x30a7]
        [    0.149799] pci 0000:00:1f.2: reg 0x1c: [io  0x30b0-0x30b3]
        [    0.149805] pci 0000:00:1f.2: reg 0x20: [io  0x3060-0x307f]
        [    0.149812] pci 0000:00:1f.2: reg 0x24: [mem 0xf123c000-0xf123c7ff]
        [    0.149840] pci 0000:00:1f.2: PME# supported from D3hot
        [    0.149893] pci 0000:00:1f.3: [8086:9ca2] type 00 class 0x0c0500
        [    0.149906] pci 0000:00:1f.3: reg 0x10: [mem 0xf1238000-0xf12380ff 64bit]
        [    0.149924] pci 0000:00:1f.3: reg 0x20: [io  0xefa0-0xefbf]
        [    0.149999] pci 0000:00:1f.6: [8086:9ca4] type 00 class 0x118000
        [    0.150026] pci 0000:00:1f.6: reg 0x10: [mem 0xf123b000-0xf123bfff 64bit]
        [    0.150199] pci 0000:00:1c.0: PCI bridge to [bus 02]
        [    0.150459] pci 0000:04:00.0: [8086:095b] type 00 class 0x028000
        [    0.150547] pci 0000:04:00.0: reg 0x10: [mem 0xf1100000-0xf1101fff 64bit]
        [    0.150816] pci 0000:04:00.0: PME# supported from D0 D3hot D3cold
        [    0.153553] pci 0000:00:1c.2: PCI bridge to [bus 04]
        [    0.153558] pci 0000:00:1c.2:   bridge window [mem 0xf1100000-0xf11fffff]
        [    0.153620] pci 0000:05:00.0: [10ec:5227] type 00 class 0xff0000
        [    0.153643] pci 0000:05:00.0: reg 0x10: [mem 0xf1000000-0xf1000fff]
        [    0.153768] pci 0000:05:00.0: supports D1 D2
        [    0.153770] pci 0000:05:00.0: PME# supported from D1 D2 D3hot D3cold
        [    0.156416] pci 0000:00:1c.5: PCI bridge to [bus 05]
        [    0.156421] pci 0000:00:1c.5:   bridge window [mem 0xf1000000-0xf10fffff]
        [    0.158162] ACPI: Enabled 4 GPEs in block 00 to 7F
        [    0.158227] ACPI : EC: GPE = 0x25, I/O: command/status = 0x66, data = 0x62
        [    0.158331] vgaarb: setting as boot device: PCI:0000:00:02.0
        [    0.158333] vgaarb: device added: PCI:0000:00:02.0,decodes=io+mem,owns=io+mem,locks=none
        [    0.158335] vgaarb: loaded
        [    0.158337] vgaarb: bridge control possible 0000:00:02.0
        [    0.158419] SCSI subsystem initialized
        [    0.158461] libata version 3.00 loaded.
        [    0.158490] ACPI: bus type USB registered
        [    0.158505] usbcore: registered new interface driver usbfs
        [    0.158514] usbcore: registered new interface driver hub
        [    0.158531] usbcore: registered new device driver usb
        [    0.158626] PCI: Using ACPI for IRQ routing
        [    0.159872] PCI: pci_cache_line_size set to 64 bytes
        [    0.160204] e820: reserve RAM buffer [mem 0x0009d000-0x0009ffff]
        [    0.160205] e820: reserve RAM buffer [mem 0xbecd0000-0xbfffffff]
        [    0.160207] e820: reserve RAM buffer [mem 0x12f000000-0x12fffffff]
        [    0.160318] NetLabel: Initializing
        [    0.160319] NetLabel:  domain hash size = 128
        [    0.160320] NetLabel:  protocols = UNLABELED CIPSOv4
        [    0.160331] NetLabel:  unlabeled traffic allowed by default
        [    0.160384] hpet0: at MMIO 0xfed00000, IRQs 2, 8, 0, 0, 0, 0, 0, 0
        [    0.160389] hpet0: 8 comparators, 64-bit 14.318180 MHz counter
        [    0.162419] Switched to clocksource hpet
        [    0.168885] pnp: PnP ACPI init
        [    0.169251] system 00:00: [mem 0x00000000-0x0009ffff] could not be reserved
        [    0.169254] system 00:00: [mem 0x000c0000-0x000c3fff] could not be reserved
        [    0.169256] system 00:00: [mem 0x000c4000-0x000c7fff] could not be reserved
        [    0.169257] system 00:00: [mem 0x000c8000-0x000cbfff] could not be reserved
        [    0.169259] system 00:00: [mem 0x000cc000-0x000cffff] could not be reserved
        [    0.169260] system 00:00: [mem 0x000d0000-0x000d3fff] has been reserved
        [    0.169262] system 00:00: [mem 0x000d4000-0x000d7fff] has been reserved
        [    0.169264] system 00:00: [mem 0x000d8000-0x000dbfff] has been reserved
        [    0.169265] system 00:00: [mem 0x000dc000-0x000dffff] has been reserved
        [    0.169267] system 00:00: [mem 0x000e0000-0x000e3fff] could not be reserved
        [    0.169268] system 00:00: [mem 0x000e4000-0x000e7fff] could not be reserved
        [    0.169270] system 00:00: [mem 0x000e8000-0x000ebfff] could not be reserved
        [    0.169272] system 00:00: [mem 0x000ec000-0x000effff] could not be reserved
        [    0.169273] system 00:00: [mem 0x000f0000-0x000fffff] could not be reserved
        [    0.169275] system 00:00: [mem 0x00100000-0xcfffffff] could not be reserved
        [    0.169277] system 00:00: [mem 0xfec00000-0xfed3ffff] could not be reserved
        [    0.169278] system 00:00: [mem 0xfed4c000-0xffffffff] could not be reserved
        [    0.169282] system 00:00: Plug and Play ACPI device, IDs PNP0c01 (active)
        [    0.169379] system 00:01: [io  0x1800-0x189f] could not be reserved
        [    0.169382] system 00:01: [io  0x0800-0x087f] has been reserved
        [    0.169383] system 00:01: [io  0x0880-0x08ff] has been reserved
        [    0.169385] system 00:01: [io  0x0900-0x097f] has been reserved
        [    0.169387] system 00:01: [io  0x0980-0x09ff] has been reserved
        [    0.169388] system 00:01: [io  0x0a00-0x0a7f] has been reserved
        [    0.169390] system 00:01: [io  0x0a80-0x0aff] has been reserved
        [    0.169391] system 00:01: [io  0x0b00-0x0b7f] has been reserved
        [    0.169393] system 00:01: [io  0x0b80-0x0bff] has been reserved
        [    0.169395] system 00:01: [io  0x1640-0x165f] has been reserved
        [    0.169397] system 00:01: [mem 0xf8000000-0xfbffffff] has been reserved
        [    0.169399] system 00:01: [mem 0xfed1c000-0xfed1ffff] has been reserved
        [    0.169400] system 00:01: [mem 0xfed10000-0xfed13fff] has been reserved
        [    0.169402] system 00:01: [mem 0xfed18000-0xfed18fff] has been reserved
        [    0.169404] system 00:01: [mem 0xfed19000-0xfed19fff] has been reserved
        [    0.169405] system 00:01: [mem 0xfed45000-0xfed4bfff] has been reserved
        [    0.169408] system 00:01: Plug and Play ACPI device, IDs PNP0c02 (active)
        [    0.169476] pnp 00:02: Plug and Play ACPI device, IDs PNP0b00 (active)
        [    0.169500] pnp 00:03: Plug and Play ACPI device, IDs LEN0071 PNP0303 (active)
        [    0.169520] pnp 00:04: Plug and Play ACPI device, IDs LEN200a PNP0f13 (active)
        [    0.171255] pnp 00:05: Plug and Play ACPI device, IDs SMO1200 PNP0c31 (active)
        [    0.171450] system 00:06: [mem 0xd0010000-0xd001ffff] has been reserved
        [    0.171452] system 00:06: [mem 0xd0000000-0xd000ffff] has been reserved
        [    0.171455] system 00:06: Plug and Play ACPI device, IDs PNP0c02 (active)
        [    0.171482] pnp: PnP ACPI: found 7 devices
        [    0.177607] clocksource acpi_pm: mask: 0xffffff max_cycles: 0xffffff, max_idle_ns: 2085701024 ns
        [    0.177635] pci 0000:00:1c.0: PCI bridge to [bus 02]
        [    0.177645] pci 0000:00:1c.2: PCI bridge to [bus 04]
        [    0.177650] pci 0000:00:1c.2:   bridge window [mem 0xf1100000-0xf11fffff]
        [    0.177657] pci 0000:00:1c.5: PCI bridge to [bus 05]
        [    0.177661] pci 0000:00:1c.5:   bridge window [mem 0xf1000000-0xf10fffff]
        [    0.177668] pci_bus 0000:00: resource 4 [io  0x0000-0x0cf7 window]
        [    0.177670] pci_bus 0000:00: resource 5 [io  0x0d00-0xffff window]
        [    0.177671] pci_bus 0000:00: resource 6 [mem 0x000a0000-0x000bffff window]
        [    0.177673] pci_bus 0000:00: resource 7 [mem 0xd0000000-0xfebfffff window]
        [    0.177674] pci_bus 0000:00: resource 8 [mem 0xfed40000-0xfed4bfff window]
        [    0.177676] pci_bus 0000:04: resource 1 [mem 0xf1100000-0xf11fffff]
        [    0.177678] pci_bus 0000:05: resource 1 [mem 0xf1000000-0xf10fffff]
        [    0.177719] NET: Registered protocol family 2
        [    0.177919] TCP established hash table entries: 32768 (order: 6, 262144 bytes)
        [    0.177995] TCP bind hash table entries: 32768 (order: 7, 524288 bytes)
        [    0.178080] TCP: Hash tables configured (established 32768 bind 32768)
        [    0.178106] UDP hash table entries: 2048 (order: 4, 65536 bytes)
        [    0.178121] UDP-Lite hash table entries: 2048 (order: 4, 65536 bytes)
        [    0.178180] NET: Registered protocol family 1
        [    0.178192] pci 0000:00:02.0: Video device with shadowed ROM
        [    0.178618] PCI: CLS 64 bytes, default 64
        [    0.178673] Unpacking initramfs...
        [    0.485647] Freeing initrd memory: 19476K (ffff8800359e7000 - ffff880036cec000)
        [    0.485655] PCI-DMA: Using software bounce buffering for IO (SWIOTLB)
        [    0.485658] software IO TLB [mem 0xbacd0000-0xbecd0000] (64MB) mapped at [ffff8800bacd0000-ffff8800beccffff]
        [    0.485730] RAPL PMU detected, API unit is 2^-32 Joules, 4 fixed counters 655360 ms ovfl timer
        [    0.485731] hw unit of domain pp0-core 2^-14 Joules
        [    0.485732] hw unit of domain package 2^-14 Joules
        [    0.485733] hw unit of domain dram 2^-14 Joules
        [    0.485734] hw unit of domain pp1-gpu 2^-14 Joules
        [    0.485820] microcode: CPU0 sig=0x306d4, pf=0x40, revision=0x1d
        [    0.485826] microcode: CPU1 sig=0x306d4, pf=0x40, revision=0x1d
        [    0.485833] microcode: CPU2 sig=0x306d4, pf=0x40, revision=0x1d
        [    0.485841] microcode: CPU3 sig=0x306d4, pf=0x40, revision=0x1d
        [    0.485887] microcode: Microcode Update Driver: v2.00 <tigran@aivazian.fsnet.co.uk>, Peter Oruba
        [    0.486221] AVX2 version of gcm_enc/dec engaged.
        [    0.486222] AES CTR mode by8 optimization enabled
        [    0.488202] alg: No test for __gcm-aes-aesni (__driver-gcm-aes-aesni)
        [    0.488631] futex hash table entries: 2048 (order: 5, 131072 bytes)
        [    0.488660] Initialise system trusted keyring
        [    0.488686] audit: initializing netlink subsys (disabled)
        [    0.488702] audit: type=2000 audit(1441390752.470:1): initialized
        [    0.489061] HugeTLB registered 2 MB page size, pre-allocated 0 pages
        [    0.490428] zpool: loaded
        [    0.490432] zbud: loaded
        [    0.490594] VFS: Disk quotas dquot_6.6.0
        [    0.490629] VFS: Dquot-cache hash table entries: 512 (order 0, 4096 bytes)
        [    0.491022] Key type big_key registered
        [    0.491025] SELinux:  Registering netfilter hooks
        [    0.491816] alg: No test for stdrng (krng)
        [    0.491826] NET: Registered protocol family 38
        [    0.491838] Key type asymmetric registered
        [    0.491842] Asymmetric key parser 'x509' registered
        [    0.491876] Block layer SCSI generic (bsg) driver version 0.4 loaded (major 252)
        [    0.491915] io scheduler noop registered
        [    0.491918] io scheduler deadline registered
        [    0.491961] io scheduler cfq registered (default)
        [    0.492334] pci_hotplug: PCI Hot Plug PCI Core version: 0.5
        [    0.492348] pciehp: PCI Express Hot Plug Controller Driver version: 0.4
        [    0.492380] intel_idle: MWAIT substates: 0x11142120
        [    0.492381] intel_idle: v0.4 model 0x3D
        [    0.492382] intel_idle: lapic_timer_reliable_states 0xffffffff
        [    0.493102] ACPI: AC Adapter [AC] (on-line)
        [    0.493161] input: Lid Switch as /devices/LNXSYSTM:00/LNXSYBUS:00/PNP0C0D:00/input/input0
        [    0.493677] ACPI: Lid Switch [LID]
        [    0.493714] input: Sleep Button as /devices/LNXSYSTM:00/LNXSYBUS:00/PNP0C0E:00/input/input1
        [    0.493717] ACPI: Sleep Button [SLPB]
        [    0.493771] input: Power Button as /devices/LNXSYSTM:00/LNXPWRBN:00/input/input2
        [    0.493773] ACPI: Power Button [PWRF]
        [    0.499932] thermal LNXTHERM:00: registered as thermal_zone0
        [    0.499935] ACPI: Thermal Zone [THM0] (45 C)
        [    0.499984] GHES: HEST is not enabled!
        [    0.500063] Serial: 8250/16550 driver, 4 ports, IRQ sharing enabled
        [    0.500566] Non-volatile memory driver v1.3
        [    0.500618] Linux agpgart interface v0.103
        [    0.501059] ahci 0000:00:1f.2: version 3.0
        [    0.511800] ahci 0000:00:1f.2: AHCI 0001.0300 32 slots 3 ports 6 Gbps 0x1 impl SATA mode
        [    0.511804] ahci 0000:00:1f.2: flags: 64bit ncq pm led clo only pio slum part deso sadm sds apst 
        [    0.512271] scsi host0: ahci
        [    0.512459] scsi host1: ahci
        [    0.512594] scsi host2: ahci
        [    0.512635] ata1: SATA max UDMA/133 abar m2048@0xf123c000 port 0xf123c100 irq 40
        [    0.512636] ata2: DUMMY
        [    0.512637] ata3: DUMMY
        [    0.512735] libphy: Fixed MDIO Bus: probed
        [    0.512936] xhci_hcd 0000:00:14.0: xHCI Host Controller
        [    0.512974] xhci_hcd 0000:00:14.0: new USB bus registered, assigned bus number 1
        [    0.513046] xhci_hcd 0000:00:14.0: hcc params 0x200077c1 hci version 0x100 quirks 0x00009810
        [    0.513051] xhci_hcd 0000:00:14.0: cache line size of 64 is not supported
        [    0.513123] usb usb1: New USB device found, idVendor=1d6b, idProduct=0002
        [    0.513125] usb usb1: New USB device strings: Mfr=3, Product=2, SerialNumber=1
        [    0.513126] usb usb1: Product: xHCI Host Controller
        [    0.513128] usb usb1: Manufacturer: Linux 4.1.6-200.fc22.x86_64 xhci-hcd
        [    0.513129] usb usb1: SerialNumber: 0000:00:14.0
        [    0.513229] hub 1-0:1.0: USB hub found
        [    0.513240] hub 1-0:1.0: 11 ports detected
        [    0.514246] xhci_hcd 0000:00:14.0: xHCI Host Controller
        [    0.514285] xhci_hcd 0000:00:14.0: new USB bus registered, assigned bus number 2
        [    0.514337] usb usb2: New USB device found, idVendor=1d6b, idProduct=0003
        [    0.514338] usb usb2: New USB device strings: Mfr=3, Product=2, SerialNumber=1
        [    0.514340] usb usb2: Product: xHCI Host Controller
        [    0.514341] usb usb2: Manufacturer: Linux 4.1.6-200.fc22.x86_64 xhci-hcd
        [    0.514342] usb usb2: SerialNumber: 0000:00:14.0
        [    0.514434] hub 2-0:1.0: USB hub found
        [    0.514441] hub 2-0:1.0: 4 ports detected
        [    0.514976] ehci_hcd: USB 2.0 'Enhanced' Host Controller (EHCI) Driver
        [    0.514982] ehci-pci: EHCI PCI platform driver
        [    0.515081] ehci-pci 0000:00:1d.0: EHCI Host Controller
        [    0.515120] ehci-pci 0000:00:1d.0: new USB bus registered, assigned bus number 3
        [    0.515130] ehci-pci 0000:00:1d.0: debug port 2
        [    0.519035] ehci-pci 0000:00:1d.0: cache line size of 64 is not supported
        [    0.519050] ehci-pci 0000:00:1d.0: irq 23, io mem 0xf123d000
        [    0.524833] ehci-pci 0000:00:1d.0: USB 2.0 started, EHCI 1.00
        [    0.524881] usb usb3: New USB device found, idVendor=1d6b, idProduct=0002
        [    0.524883] usb usb3: New USB device strings: Mfr=3, Product=2, SerialNumber=1
        [    0.524885] usb usb3: Product: EHCI Host Controller
        [    0.524886] usb usb3: Manufacturer: Linux 4.1.6-200.fc22.x86_64 ehci_hcd
        [    0.524887] usb usb3: SerialNumber: 0000:00:1d.0
        [    0.525003] hub 3-0:1.0: USB hub found
        [    0.525007] hub 3-0:1.0: 3 ports detected
        [    0.525131] ohci_hcd: USB 1.1 'Open' Host Controller (OHCI) Driver
        [    0.525137] ohci-pci: OHCI PCI platform driver
        [    0.525150] uhci_hcd: USB Universal Host Controller Interface driver
        [    0.525218] usbcore: registered new interface driver usbserial
        [    0.525224] usbcore: registered new interface driver usbserial_generic
        [    0.525230] usbserial: USB Serial support registered for generic
        [    0.525265] i8042: PNP: PS/2 Controller [PNP0303:KBD,PNP0f13:MOU] at 0x60,0x64 irq 1,12
        [    0.534319] serio: i8042 KBD port at 0x60,0x64 irq 1
        [    0.534323] serio: i8042 AUX port at 0x60,0x64 irq 12
        [    0.534426] mousedev: PS/2 mouse device common for all mice
        [    0.534715] rtc_cmos 00:02: RTC can wake from S4
        [    0.534849] rtc_cmos 00:02: rtc core: registered rtc_cmos as rtc0
        [    0.534876] rtc_cmos 00:02: alarms up to one month, y3k, 114 bytes nvram, hpet irqs
        [    0.534928] device-mapper: uevent: version 1.0.3
        [    0.534998] device-mapper: ioctl: 4.31.0-ioctl (2015-3-12) initialised: dm-devel@redhat.com
        [    0.535054] Intel P-state driver initializing.
        [    0.536328] hidraw: raw HID events driver (C) Jiri Kosina
        [    0.536427] usbcore: registered new interface driver usbhid
        [    0.536429] usbhid: USB HID core driver
        [    0.536599] drop_monitor: Initializing network drop monitor service
        [    0.536828] ip_tables: (C) 2000-2006 Netfilter Core Team
        [    0.536939] Initializing XFRM netlink socket
        [    0.537270] NET: Registered protocol family 10
        [    0.537774] mip6: Mobile IPv6
        [    0.537780] NET: Registered protocol family 17
        [    0.538932] Loading compiled-in X.509 certificates
        [    0.541351] Loaded X.509 cert 'Fedora kernel signing key: 95d88b1a623bbfdfefe2586b05ed0ac5c288c13a'
        [    0.541394] registered taskstats version 1
        [    0.542685]   Magic number: 15:498:341
        [    0.542842] rtc_cmos 00:02: setting system clock to 2015-09-04 18:19:13 UTC (1441390753)
        [    0.543105] PM: Hibernation image not present or could not be loaded.
        [    0.553998] ACPI: Battery Slot [BAT0] (battery present)
        [    0.560651] input: AT Translated Set 2 keyboard as /devices/platform/i8042/serio0/input/input3
        [    0.817137] ata1: SATA link up 6.0 Gbps (SStatus 133 SControl 300)
        [    0.827144] usb 3-1: new high-speed USB device number 2 using ehci-pci
        [    0.867184] usb 1-6: new high-speed USB device number 2 using xhci_hcd
        [    0.875657] ata1.00: ACPI cmd ef/02:00:00:00:00:a0 (SET FEATURES) succeeded
        [    0.875661] ata1.00: ACPI cmd f5/00:00:00:00:00:a0 (SECURITY FREEZE LOCK) filtered out
        [    0.920210] ata1.00: ATA-8: ST500LM000-SSHD-8GB, LIV9, max UDMA/133
        [    0.920214] ata1.00: 976773168 sectors, multi 16: LBA48 NCQ (depth 31/32), AA
        [    0.941715] usb 3-1: New USB device found, idVendor=8087, idProduct=8001
        [    0.941718] usb 3-1: New USB device strings: Mfr=0, Product=0, SerialNumber=0
        [    0.942132] hub 3-1:1.0: USB hub found
        [    0.942353] hub 3-1:1.0: 8 ports detected
        [    0.964421] ata1.00: ACPI cmd ef/02:00:00:00:00:a0 (SET FEATURES) succeeded
        [    0.964425] ata1.00: ACPI cmd f5/00:00:00:00:00:a0 (SECURITY FREEZE LOCK) filtered out
        [    1.009049] ata1.00: configured for UDMA/133
        [    1.009234] scsi 0:0:0:0: Direct-Access     ATA      ST500LM000-SSHD- LIV9 PQ: 0 ANSI: 5
        [    1.009542] sd 0:0:0:0: [sda] 976773168 512-byte logical blocks: (500 GB/465 GiB)
        [    1.009545] sd 0:0:0:0: [sda] 4096-byte physical blocks
        [    1.009565] sd 0:0:0:0: Attached scsi generic sg0 type 0
        [    1.009622] sd 0:0:0:0: [sda] Write Protect is off
        [    1.009625] sd 0:0:0:0: [sda] Mode Sense: 00 3a 00 00
        [    1.009686] sd 0:0:0:0: [sda] Write cache: enabled, read cache: enabled, doesn't support DPO or FUA
        [    1.010573]  sda: sda1 sda2
        [    1.010846] sd 0:0:0:0: [sda] Attached SCSI disk
        [    1.011114] Freeing unused kernel memory: 1516K (ffffffff81d38000 - ffffffff81eb3000)
        [    1.011116] Write protecting the kernel read-only data: 12288k
        [    1.011311] Freeing unused kernel memory: 344K (ffff8800017aa000 - ffff880001800000)
        [    1.011490] Freeing unused kernel memory: 828K (ffff880001b31000 - ffff880001c00000)
        [    1.013394] random: systemd urandom read with 28 bits of entropy available
        [    1.014455] systemd[1]: systemd 219 running in system mode. (+PAM +AUDIT +SELINUX +IMA -APPARMOR +SMACK +SYSVINIT +UTMP +LIBCRYPTSETUP +GCRYPT +GNUTLS +ACL +XZ -LZ4 +SECCOMP +BLKID +ELFUTILS +KMOD +IDN)
        [    1.014578] systemd[1]: Detected architecture x86-64.
        [    1.014580] systemd[1]: Running in initial RAM disk.
        [    1.014595] systemd[1]: Set hostname to <192-168-001-109.tele.net>.
        [    1.032471] usb 1-6: New USB device found, idVendor=05e3, idProduct=0608
        [    1.032474] usb 1-6: New USB device strings: Mfr=0, Product=1, SerialNumber=0
        [    1.032476] usb 1-6: Product: USB2.0 Hub
        [    1.032934] hub 1-6:1.0: USB hub found
        [    1.033182] hub 1-6:1.0: 2 ports detected
        [    1.048718] systemd[1]: Reached target Swap.
        [    1.048727] systemd[1]: Starting Swap.
        [    1.048736] systemd[1]: Reached target Local File Systems.
        [    1.048741] systemd[1]: Starting Local File Systems.
        [    1.048910] systemd[1]: Created slice -.slice.
        [    1.048916] systemd[1]: Starting -.slice.
        [    1.048961] systemd[1]: Created slice System Slice.
        [    1.048967] systemd[1]: Starting System Slice.
        [    1.049013] systemd[1]: Created slice system-systemd\x2dcryptsetup.slice.
        [    1.049019] systemd[1]: Starting system-systemd\x2dcryptsetup.slice.
        [    1.049028] systemd[1]: Reached target Slices.
        [    1.049032] systemd[1]: Starting Slices.
        [    1.049091] systemd[1]: Listening on Journal Audit Socket.
        [    1.049097] systemd[1]: Starting Journal Audit Socket.
        [    1.049127] systemd[1]: Listening on Journal Socket.
        [    1.049133] systemd[1]: Starting Journal Socket.
        [    1.049197] systemd[1]: Started Load Kernel Modules.
        [    1.049507] systemd[1]: Starting Create list of required static device nodes for the current kernel...
        [    1.049778] systemd[1]: Starting Apply Kernel Variables...
        [    1.050207] systemd[1]: Starting Setup Virtual Console...
        [    1.050267] systemd[1]: Listening on Journal Socket (/dev/log).
        [    1.050282] systemd[1]: Starting Journal Socket (/dev/log).
        [    1.050745] systemd[1]: Starting Journal Service...
        [    1.050801] systemd[1]: Listening on udev Kernel Socket.
        [    1.050814] systemd[1]: Starting udev Kernel Socket.
        [    1.050862] systemd[1]: Listening on udev Control Socket.
        [    1.050872] systemd[1]: Starting udev Control Socket.
        [    1.050886] systemd[1]: Reached target Sockets.
        [    1.050896] systemd[1]: Starting Sockets.
        [    1.050938] systemd[1]: Started dracut ask for additional cmdline parameters.
        [    1.051486] systemd[1]: Starting dracut cmdline hook...
        [    1.051519] systemd[1]: Reached target Timers.
        [    1.051536] systemd[1]: Starting Timers.
        [    1.051946] systemd[1]: Started Create list of required static device nodes for the current kernel.
        [    1.052808] systemd[1]: Started Apply Kernel Variables.
        [    1.052839] audit: type=1130 audit(1441390754.007:2): pid=1 uid=0 auid=4294967295 ses=4294967295 subj=kernel msg='unit=systemd-sysctl comm="systemd" exe="/usr/lib/systemd/systemd" hostname=? addr=? terminal=? res=success'
        [    1.055867] systemd[1]: Starting Create Static Device Nodes in /dev...
        [    1.059348] systemd[1]: Started Create Static Device Nodes in /dev.
        [    1.059391] audit: type=1130 audit(1441390754.014:3): pid=1 uid=0 auid=4294967295 ses=4294967295 subj=kernel msg='unit=systemd-tmpfiles-setup-dev comm="systemd" exe="/usr/lib/systemd/systemd" hostname=? addr=? terminal=? res=success'
        [    1.074831] systemd[1]: Started Journal Service.
        [    1.074892] audit: type=1130 audit(1441390754.029:4): pid=1 uid=0 auid=4294967295 ses=4294967295 subj=kernel msg='unit=systemd-journald comm="systemd" exe="/usr/lib/systemd/systemd" hostname=? addr=? terminal=? res=success'
        [    1.109572] audit: type=1130 audit(1441390754.064:5): pid=1 uid=0 auid=4294967295 ses=4294967295 subj=kernel msg='unit=systemd-vconsole-setup comm="systemd" exe="/usr/lib/systemd/systemd" hostname=? addr=? terminal=? res=success'
        [    1.151351] audit: type=1130 audit(1441390754.105:6): pid=1 uid=0 auid=4294967295 ses=4294967295 subj=kernel msg='unit=dracut-cmdline comm="systemd" exe="/usr/lib/systemd/systemd" hostname=? addr=? terminal=? res=success'
        [    1.176280] audit: type=1130 audit(1441390754.130:7): pid=1 uid=0 auid=4294967295 ses=4294967295 subj=kernel msg='unit=dracut-pre-udev comm="systemd" exe="/usr/lib/systemd/systemd" hostname=? addr=? terminal=? res=success'
        [    1.179876] audit: type=1130 audit(1441390754.134:8): pid=1 uid=0 auid=4294967295 ses=4294967295 subj=kernel msg='unit=systemd-udevd comm="systemd" exe="/usr/lib/systemd/systemd" hostname=? addr=? terminal=? res=success'
        [    1.187094] usb 1-7: new full-speed USB device number 3 using xhci_hcd
        [    1.191840] audit: type=1130 audit(1441390754.146:9): pid=1 uid=0 auid=4294967295 ses=4294967295 subj=kernel msg='unit=dracut-pre-trigger comm="systemd" exe="/usr/lib/systemd/systemd" hostname=? addr=? terminal=? res=success'
        [    1.210306] audit: type=1130 audit(1441390754.164:10): pid=1 uid=0 auid=4294967295 ses=4294967295 subj=kernel msg='unit=systemd-udev-trigger comm="systemd" exe="/usr/lib/systemd/systemd" hostname=? addr=? terminal=? res=success'
        [    1.241842] pps_core: LinuxPPS API ver. 1 registered
        [    1.241845] pps_core: Software ver. 5.3.6 - Copyright 2005-2007 Rodolfo Giometti <giometti@linux.it>
        [    1.244568] PTP clock support registered
        [    1.249071] rtsx_pci 0000:05:00.0: rtsx_pci_acquire_irq: pcr->msi_en = 1, pci->irq = 42
        [    1.264724] [drm] Initialized drm 1.1.0 20060810
        [    1.275557] alg: No test for crc32 (crc32-pclmul)
        [    1.287634] e1000e: Intel(R) PRO/1000 Network Driver - 2.3.2-k
        [    1.287637] e1000e: Copyright(c) 1999 - 2014 Intel Corporation.
        [    1.287815] e1000e 0000:00:19.0: Interrupt Throttling Rate (ints/sec) set to dynamic conservative mode
        [    1.360039] usb 1-7: No LPM exit latency info found, disabling LPM.
        [    1.360829] usb 1-7: New USB device found, idVendor=8087, idProduct=0a2a
        [    1.360832] usb 1-7: New USB device strings: Mfr=0, Product=0, SerialNumber=0
        [    1.432752] usb 1-6.1: new full-speed USB device number 4 using xhci_hcd
        [    1.447783] psmouse serio1: synaptics: queried max coordinates: x [..5676], y [..4758]
        [    1.485595] psmouse serio1: synaptics: queried min coordinates: x [1266..], y [1096..]
        [    1.487777] tsc: Refined TSC clocksource calibration: 2194.918 MHz
        [    1.487780] clocksource tsc: mask: 0xffffffffffffffff max_cycles: 0x1fa37202099, max_idle_ns: 440795206796 ns
        [    1.520033] usb 1-6.1: New USB device found, idVendor=138a, idProduct=0011
        [    1.520037] usb 1-6.1: New USB device strings: Mfr=0, Product=0, SerialNumber=1
        [    1.520039] usb 1-6.1: SerialNumber: ee6b49cea86c
        [    1.560361] psmouse serio1: synaptics: Touchpad model: 1, fw: 8.1, id: 0x1e2b1, caps: 0xf003a3/0x943300/0x12e800, board id: 3053, fw id: 2560
        [    1.560369] psmouse serio1: synaptics: serio: Synaptics pass-through port at isa0060/serio1/input0
        [    1.593470] e1000e 0000:00:19.0 eth0: registered PHC clock
        [    1.593475] e1000e 0000:00:19.0 eth0: (PCI Express:2.5GT/s:Width x1) 68:f7:28:f4:78:e7
        [    1.593477] e1000e 0000:00:19.0 eth0: Intel(R) PRO/1000 Network Connection
        [    1.593503] e1000e 0000:00:19.0 eth0: MAC: 11, PHY: 12, PBA No: FFFFFF-0FF
        [    1.594217] [drm] Memory usable by graphics device = 4096M
        [    1.594221] [drm] Replacing VGA console driver
        [    1.594530] e1000e 0000:00:19.0 enp0s25: renamed from eth0
        [    1.594962] Console: switching to colour dummy device 80x25
        [    1.601008] [drm] Supports vblank timestamp caching Rev 2 (21.10.2013).
        [    1.601011] [drm] Driver supports precise vblank timestamp query.
        [    1.601122] vgaarb: device changed decodes: PCI:0000:00:02.0,olddecodes=io+mem,decodes=io+mem:owns=io+mem
        [    1.603825] 8021q: 802.1Q VLAN Support v1.8
        [    1.609950] input: SynPS/2 Synaptics TouchPad as /devices/platform/i8042/serio1/input/input5
        [    1.620477] ACPI: Video Device [VID] (multi-head: yes  rom: no  post: no)
        [    1.669987] [drm] GMBUS [i915 gmbus dpb] timed out, falling back to bit banging on pin 5
        [    1.671021] usb 1-8: new high-speed USB device number 5 using xhci_hcd
        [    1.679290] fbcon: inteldrmfb (fb0) is primary device
        [    1.890656] usb 1-8: New USB device found, idVendor=04f2, idProduct=b444
        [    1.890658] usb 1-8: New USB device strings: Mfr=3, Product=1, SerialNumber=2
        [    1.890659] usb 1-8: Product: Integrated Camera
        [    1.890660] usb 1-8: Manufacturer: Chicony Electronics Co.,Ltd.
        [    1.890661] usb 1-8: SerialNumber: 0001
        [    1.921391] input: Video Bus as /devices/LNXSYSTM:00/LNXSYBUS:00/PNP0A08:00/LNXVIDEO:00/input/input7
        [    1.921524] [drm] Initialized i915 1.6.0 20150327 for 0000:00:02.0 on minor 0
        [    2.488922] Switched to clocksource tsc
        [    2.775434] Console: switching to colour frame buffer device 240x67
        [    2.779368] i915 0000:00:02.0: fb0: inteldrmfb frame buffer device
        [    2.779369] i915 0000:00:02.0: registered panic notifier
        [    4.883986] random: nonblocking pool is initialized
        [    6.395059] psmouse serio2: trackpoint: IBM TrackPoint firmware: 0x0e, buttons: 3/3
        [    6.633274] input: TPPS/2 IBM TrackPoint as /devices/platform/i8042/serio1/serio2/input/input6
        [    7.774608] audit_printk_skb: 6 callbacks suppressed
        [    7.774612] audit: type=1130 audit(1441390760.723:13): pid=1 uid=0 auid=4294967295 ses=4294967295 subj=kernel msg='unit=systemd-cryptsetup@luks\x2df395d3d9\x2db322\x2d4fe3\x2d94b8\x2d8a74105213f4 comm="systemd" exe="/usr/lib/systemd/systemd" hostname=? addr=? terminal=? res=success'
        [    8.119023] audit: type=1130 audit(1441390761.067:14): pid=1 uid=0 auid=4294967295 ses=4294967295 subj=kernel msg='unit=systemd-fsck-root comm="systemd" exe="/usr/lib/systemd/systemd" hostname=? addr=? terminal=? res=success'
        [    8.153368] audit: type=1130 audit(1441390761.101:15): pid=1 uid=0 auid=4294967295 ses=4294967295 subj=kernel msg='unit=dracut-initqueue comm="systemd" exe="/usr/lib/systemd/systemd" hostname=? addr=? terminal=? res=success'
        [    8.168951] EXT4-fs (dm-1): mounted filesystem with ordered data mode. Opts: (null)
        [    8.230550] audit: type=1130 audit(1441390761.179:16): pid=1 uid=0 auid=4294967295 ses=4294967295 subj=kernel msg='unit=initrd-parse-etc comm="systemd" exe="/usr/lib/systemd/systemd" hostname=? addr=? terminal=? res=success'
        [    8.230570] audit: type=1131 audit(1441390761.179:17): pid=1 uid=0 auid=4294967295 ses=4294967295 subj=kernel msg='unit=initrd-parse-etc comm="systemd" exe="/usr/lib/systemd/systemd" hostname=? addr=? terminal=? res=success'
        [    8.359141] audit: type=1130 audit(1441390761.307:18): pid=1 uid=0 auid=4294967295 ses=4294967295 subj=kernel msg='unit=dracut-pre-pivot comm="systemd" exe="/usr/lib/systemd/systemd" hostname=? addr=? terminal=? res=success'
        [    8.368121] audit: type=1130 audit(1441390761.316:19): pid=1 uid=0 auid=4294967295 ses=4294967295 subj=kernel msg='unit=systemd-ask-password-plymouth comm="systemd" exe="/usr/lib/systemd/systemd" hostname=? addr=? terminal=? res=success'
        [    8.368144] audit: type=1131 audit(1441390761.316:20): pid=1 uid=0 auid=4294967295 ses=4294967295 subj=kernel msg='unit=systemd-ask-password-plymouth comm="systemd" exe="/usr/lib/systemd/systemd" hostname=? addr=? terminal=? res=success'
        [    8.368471] audit: type=1130 audit(1441390761.316:21): pid=1 uid=0 auid=4294967295 ses=4294967295 subj=kernel msg='unit=initrd-cleanup comm="systemd" exe="/usr/lib/systemd/systemd" hostname=? addr=? terminal=? res=success'
        [    8.368482] audit: type=1131 audit(1441390761.316:22): pid=1 uid=0 auid=4294967295 ses=4294967295 subj=kernel msg='unit=initrd-cleanup comm="systemd" exe="/usr/lib/systemd/systemd" hostname=? addr=? terminal=? res=success'
        [    8.436394] systemd-journald[138]: Received SIGTERM from PID 1 (systemd).
        [    8.610261] SELinux: 32768 avtab hash slots, 105963 rules.
        [    8.623596] SELinux: 32768 avtab hash slots, 105963 rules.
        [    8.646038] SELinux:  8 users, 105 roles, 4976 types, 303 bools, 1 sens, 1024 cats
        [    8.646041] SELinux:  83 classes, 105963 rules
        [    8.649108] SELinux:  Permission audit_read in class capability2 not defined in policy.
        [    8.649112] SELinux:  Class binder not defined in policy.
        [    8.649113] SELinux: the above unknown classes and permissions will be allowed
        [    8.649118] SELinux:  Completing initialization.
        [    8.649118] SELinux:  Setting up existing superblocks.
        [    8.660101] systemd[1]: Successfully loaded SELinux policy in 87.482ms.
        [    8.699788] systemd[1]: Relabelled /dev and /run in 15.039ms.
        [    9.122278] EXT4-fs (dm-1): re-mounted. Opts: (null)
        [    9.164020] RPC: Registered named UNIX socket transport module.
        [    9.164023] RPC: Registered udp transport module.
        [    9.164024] RPC: Registered tcp transport module.
        [    9.164024] RPC: Registered tcp NFSv4.1 backchannel transport module.
        [    9.250640] Installing knfsd (copyright (C) 1996 okir@monad.swb.de).
        [    9.439156] shpchp: Standard Hot Plug PCI Controller Driver version: 0.4
        [    9.488142] i801_smbus 0000:00:1f.3: SMBus using PCI interrupt
        [    9.504098] wmi: Mapper loaded
        [    9.508663] tpm_tis 00:05: 1.2 TPM (device-id 0x0, rev-id 78)
        [    9.527473] thinkpad_acpi: ThinkPad ACPI Extras v0.25
        [    9.527476] thinkpad_acpi: http://ibm-acpi.sf.net/
        [    9.527478] thinkpad_acpi: ThinkPad BIOS JDET50WW (1.12 ), EC unknown
        [    9.527480] thinkpad_acpi: Lenovo ThinkPad L450, model 20DT0003GE
        [    9.528642] thinkpad_acpi: Unsupported brightness interface, please contact ibm-acpi-devel@lists.sourceforge.net
        [    9.528817] thinkpad_acpi: This ThinkPad has standard ACPI backlight brightness control, supported by the ACPI video driver
        [    9.528819] thinkpad_acpi: Disabling thinkpad-acpi brightness events by default...
        [    9.536905] thinkpad_acpi: rfkill switch tpacpi_bluetooth_sw: radio is unblocked
        [    9.546888] tpm_tis 00:05: TPM is disabled/deactivated (0x6)
        [    9.549149] input: ThinkPad Extra Buttons as /devices/platform/thinkpad_acpi/input/input8
        [    9.567859] media: Linux media interface: v0.10
        [    9.578203] Linux video capture interface: v2.00
        [    9.602933] cfg80211: Calling CRDA to update world regulatory domain
        [    9.753913] Bluetooth: Core ver 2.20
        [    9.753932] NET: Registered protocol family 31
        [    9.753934] Bluetooth: HCI device and connection manager initialized
        [    9.753940] Bluetooth: HCI socket layer initialized
        [    9.753943] Bluetooth: L2CAP socket layer initialized
        [    9.753951] Bluetooth: SCO socket layer initialized
        [    9.761279] snd_hda_intel 0000:00:03.0: bound 0000:00:02.0 (ops i915_audio_component_bind_ops [i915])
        [    9.765658] uvcvideo: Found UVC 1.00 device Integrated Camera (04f2:b444)
        [    9.776110] input: Integrated Camera as /devices/pci0000:00/0000:00:14.0/usb1/1-8/1-8:1.0/input/input9
        [    9.776217] usbcore: registered new interface driver uvcvideo
        [    9.776219] USB Video Class driver (1.1.1)
        [    9.783856] Intel(R) Wireless WiFi driver for Linux
        [    9.783859] Copyright(c) 2003- 2015 Intel Corporation
        [    9.790234] usbcore: registered new interface driver btusb
        [    9.797610] iwlwifi 0000:04:00.0: Direct firmware load for iwlwifi-7265D-13.ucode failed with error -2
        [    9.804757] Bluetooth: hci0: read Intel version: 370810011003110e00
        [    9.804910] iwlwifi 0000:04:00.0: loaded firmware version 25.17.12.0 op_mode iwlmvm
        [    9.814338] iTCO_vendor_support: vendor-support=0
        [    9.834812] Bluetooth: hci0: Intel Bluetooth firmware file: intel/ibt-hw-37.8.10-fw-1.10.3.11.e.bseq
        [    9.852116] kvm: disabled by bios
        [    9.863290] iTCO_wdt: Intel TCO WatchDog Timer Driver v1.11
        [    9.863338] iTCO_wdt: Found a Wildcat Point_LP TCO device (Version=2, TCOBASE=0x1860)
        [    9.863539] iTCO_wdt: initialized. heartbeat=30 sec (nowayout=0)
        [    9.913095] cfg80211: World regulatory domain updated:
        [    9.913098] cfg80211:  DFS Master region: unset
        [    9.913100] cfg80211:   (start_freq - end_freq @ bandwidth), (max_antenna_gain, max_eirp), (dfs_cac_time)
        [    9.913102] cfg80211:   (2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A, 2000 mBm), (N/A)
        [    9.913104] cfg80211:   (2457000 KHz - 2482000 KHz @ 40000 KHz), (N/A, 2000 mBm), (N/A)
        [    9.913105] cfg80211:   (2474000 KHz - 2494000 KHz @ 20000 KHz), (N/A, 2000 mBm), (N/A)
        [    9.913107] cfg80211:   (5170000 KHz - 5250000 KHz @ 80000 KHz, 160000 KHz AUTO), (N/A, 2000 mBm), (N/A)
        [    9.913109] cfg80211:   (5250000 KHz - 5330000 KHz @ 80000 KHz, 160000 KHz AUTO), (N/A, 2000 mBm), (0 s)
        [    9.913110] cfg80211:   (5490000 KHz - 5730000 KHz @ 160000 KHz), (N/A, 2000 mBm), (0 s)
        [    9.913111] cfg80211:   (5735000 KHz - 5835000 KHz @ 80000 KHz), (N/A, 2000 mBm), (N/A)
        [    9.913113] cfg80211:   (57240000 KHz - 63720000 KHz @ 2160000 KHz), (N/A, 0 mBm), (N/A)
        [    9.955002] iwlwifi 0000:04:00.0: Detected Intel(R) Dual Band Wireless AC 7265, REV=0x210
        [    9.955394] iwlwifi 0000:04:00.0: L1 Enabled - LTR Enabled
        [    9.955845] iwlwifi 0000:04:00.0: L1 Enabled - LTR Enabled
        [    9.971907] Bluetooth: hci0: Intel Bluetooth firmware patch completed and activated
        [    9.972613] usb 1-7: USB disconnect, device number 3
        [    9.972761] Bluetooth: hci0: Reading Intel device address failed (-19)
        [    9.982318] input: HDA Intel HDMI HDMI/DP,pcm=3 as /devices/pci0000:00/0000:00:03.0/sound/card0/input10
        [    9.982441] input: HDA Intel HDMI HDMI/DP,pcm=7 as /devices/pci0000:00/0000:00:03.0/sound/card0/input11
        [    9.982551] input: HDA Intel HDMI HDMI/DP,pcm=8 as /devices/pci0000:00/0000:00:03.0/sound/card0/input12
        [    9.987118] snd_hda_codec_realtek hdaudioC1D0: autoconfig for ALC3232: line_outs=1 (0x14/0x0/0x0/0x0/0x0) type:speaker
        [    9.987123] snd_hda_codec_realtek hdaudioC1D0:    speaker_outs=0 (0x0/0x0/0x0/0x0/0x0)
        [    9.987126] snd_hda_codec_realtek hdaudioC1D0:    hp_outs=2 (0x16/0x15/0x0/0x0/0x0)
        [    9.987128] snd_hda_codec_realtek hdaudioC1D0:    mono: mono_out=0x0
        [    9.987130] snd_hda_codec_realtek hdaudioC1D0:    inputs:
        [    9.987133] snd_hda_codec_realtek hdaudioC1D0:      Dock Mic=0x19
        [    9.987135] snd_hda_codec_realtek hdaudioC1D0:      Mic=0x1a
        [    9.987137] snd_hda_codec_realtek hdaudioC1D0:      Internal Mic=0x12
        [    9.998291] input: HDA Intel PCH Dock Mic as /devices/pci0000:00/0000:00:1b.0/sound/card1/input13
        [    9.998381] input: HDA Intel PCH Mic as /devices/pci0000:00/0000:00:1b.0/sound/card1/input14
        [    9.998452] input: HDA Intel PCH Dock Headphone as /devices/pci0000:00/0000:00:1b.0/sound/card1/input15
        [    9.998509] input: HDA Intel PCH Headphone as /devices/pci0000:00/0000:00:1b.0/sound/card1/input16
        [   10.031744] ieee80211 phy0: Selected rate control algorithm 'iwl-mvm-rs'
        [   10.035935] intel_rapl: Found RAPL domain package
        [   10.035939] intel_rapl: Found RAPL domain core
        [   10.035942] intel_rapl: Found RAPL domain uncore
        [   10.035945] intel_rapl: Found RAPL domain dram
        [   10.121550] iwlwifi 0000:04:00.0 wlp4s0: renamed from wlan0
        [   10.164899] Adding 3801084k swap on /dev/mapper/fedora_192--168--001--109-swap.  Priority:-1 extents:1 across:3801084k FS
        [   10.425400] EXT4-fs (sda1): mounted filesystem with ordered data mode. Opts: (null)
        [   10.615568] EXT4-fs (dm-3): mounted filesystem with ordered data mode. Opts: (null)
        [   11.301744] systemd-journald[653]: Received request to flush runtime journal from PID 1
        [   11.980354] Bluetooth: hci0 command 0x1009 tx timeout
        [   11.980413] Bluetooth: hci0 sending frame failed (-19)
        [   13.022897] Bluetooth: BNEP (Ethernet Emulation) ver 1.3
        [   13.022900] Bluetooth: BNEP filters: protocol multicast
        [   13.022907] Bluetooth: BNEP socket layer initialized
        [   13.497594] nf_conntrack version 0.5.0 (16384 buckets, 65536 max)
        [   13.517142] ip6_tables: (C) 2000-2006 Netfilter Core Team
        [   13.582020] Ebtables v2.0 registered
        [   13.596557] bridge: automatic filtering via arp/ip/ip6tables has been deprecated. Update your scripts to load br_netfilter if you need this.
        [   13.803745] IPv6: ADDRCONF(NETDEV_UP): enp0s25: link is not ready
        [   14.004472] IPv6: ADDRCONF(NETDEV_UP): enp0s25: link is not ready
        [   14.007050] IPv6: ADDRCONF(NETDEV_UP): wlp4s0: link is not ready
        [   14.008519] iwlwifi 0000:04:00.0: L1 Enabled - LTR Enabled
        [   14.009077] iwlwifi 0000:04:00.0: L1 Enabled - LTR Enabled
        [   14.071298] iwlwifi 0000:04:00.0: L1 Enabled - LTR Enabled
        [   14.072168] iwlwifi 0000:04:00.0: L1 Enabled - LTR Enabled
        [   14.101477] IPv6: ADDRCONF(NETDEV_UP): wlp4s0: link is not ready
        [   14.274279] IPv6: ADDRCONF(NETDEV_UP): wlp4s0: link is not ready
        [   15.823220] tun: Universal TUN/TAP device driver, 1.6
        [   15.823222] tun: (C) 1999-2004 Max Krasnyansky <maxk@qualcomm.com>
        [   15.857579] device virbr0-nic entered promiscuous mode
        [   15.995881] virbr0: port 1(virbr0-nic) entered listening state
        [   15.995893] virbr0: port 1(virbr0-nic) entered listening state
        [   16.028354] virbr0: port 1(virbr0-nic) entered disabled state
        [   17.607980] wlp4s0: authenticate with a0:f3:c1:f2:b5:5c
        [   17.617213] wlp4s0: send auth to a0:f3:c1:f2:b5:5c (try 1/3)
        [   17.620050] wlp4s0: authenticated
        [   17.620959] wlp4s0: associate with a0:f3:c1:f2:b5:5c (try 1/3)
        [   17.625541] wlp4s0: RX AssocResp from a0:f3:c1:f2:b5:5c (capab=0x431 status=0 aid=1)
        [   17.627638] wlp4s0: associated
        [   17.627664] IPv6: ADDRCONF(NETDEV_CHANGE): wlp4s0: link becomes ready
        [   22.907549] Adjusting tsc more than 11% (6595074 vs 8484467)
        [   25.221997] usb 1-6.1: reset full-speed USB device number 4 using xhci_hcd
        [   28.041288] fuse init (API version 7.23)
        [   32.631351] usb 2-2: new SuperSpeed USB device number 2 using xhci_hcd
        [   32.643122] usb 2-2: New USB device found, idVendor=27d1, idProduct=5136
        [   32.643126] usb 2-2: New USB device strings: Mfr=2, Product=3, SerialNumber=1
        [   32.643128] usb 2-2: Product: SSD2go
        [   32.643130] usb 2-2: Manufacturer: Angelbird
        [   32.643132] usb 2-2: SerialNumber: 41494341355358
        [   32.664215] usbcore: registered new interface driver usb-storage
        [   32.669176] scsi host3: uas
        [   32.669647] scsi 3:0:0:0: Direct-Access     SSD2go   Angelbird        0    PQ: 0 ANSI: 6
        [   32.669686] usbcore: registered new interface driver uas
        [   32.670265] sd 3:0:0:0: Attached scsi generic sg1 type 0
        [   32.681533] sd 3:0:0:0: [sdb] 234441648 512-byte logical blocks: (120 GB/111 GiB)
        [   32.681799] sd 3:0:0:0: [sdb] Write Protect is off
        [   32.681801] sd 3:0:0:0: [sdb] Mode Sense: 43 00 00 00
        [   32.681920] sd 3:0:0:0: [sdb] Write cache: enabled, read cache: enabled, doesn't support DPO or FUA
        [   32.683242]  sdb: sdb1
        [   32.683951] sd 3:0:0:0: [sdb] Attached SCSI disk
        [   32.882555] EXT4-fs (sdb1): mounted filesystem with ordered data mode. Opts: (null)
        [   33.476482] sd 3:0:0:0: [sdb] tag#0 data cmplt err -71 uas-tag 1 inflight: CMD 
        [   33.476487] sd 3:0:0:0: [sdb] tag#0 CDB: Read(10) 28 00 04 88 07 00 00 00 20 00
        [   63.997734] sd 3:0:0:0: [sdb] tag#0 uas_eh_abort_handler 0 uas-tag 1 inflight: CMD 
        [   63.997739] sd 3:0:0:0: [sdb] tag#0 CDB: Read(10) 28 00 04 88 07 00 00 00 20 00
        [   69.000730] sd 3:0:0:0: [sdb] tag#1 uas_eh_abort_handler 0 uas-tag 2 inflight: CMD OUT 
        [   69.000735] sd 3:0:0:0: [sdb] tag#1 CDB: Write(10) 2a 00 06 c4 08 00 00 00 08 00
        [   69.000767] scsi host3: uas_eh_bus_reset_handler start
        [   69.103119] usb 2-2: reset SuperSpeed USB device number 2 using xhci_hcd
        [   69.115609] scsi host3: uas_eh_bus_reset_handler success
        [   93.570703] nf_conntrack: automatic helper assignment is deprecated and it will be removed soon. Use the iptables CT target to attach helpers instead.
        [  521.608606] usb 1-6.1: reset full-speed USB device number 4 using xhci_hcd
        [  574.326519] wlp4s0: authenticate with 00:1e:e5:25:e1:70
        [  574.331684] wlp4s0: send auth to 00:1e:e5:25:e1:70 (try 1/3)
        [  574.333524] wlp4s0: authenticated
        [  574.333661] iwlwifi 0000:04:00.0 wlp4s0: disabling HT as WMM/QoS is not supported by the AP
        [  574.333664] iwlwifi 0000:04:00.0 wlp4s0: disabling VHT as WMM/QoS is not supported by the AP
        [  574.334593] wlp4s0: associate with 00:1e:e5:25:e1:70 (try 1/3)
        [  574.337090] wlp4s0: RX AssocResp from 00:1e:e5:25:e1:70 (capab=0x411 status=0 aid=13)
        [  574.338143] wlp4s0: associated
        [  694.406034] wlp4s0: authenticate with a0:f3:c1:f2:b5:5c
        [  694.409140] wlp4s0: send auth to a0:f3:c1:f2:b5:5c (try 1/3)
        [  694.411485] wlp4s0: authenticated
        [  694.411923] wlp4s0: associate with a0:f3:c1:f2:b5:5c (try 1/3)
        [  694.416211] wlp4s0: RX AssocResp from a0:f3:c1:f2:b5:5c (capab=0x431 status=0 aid=1)
        [  694.417346] wlp4s0: associated
        [ 2752.229141] usb 1-6.1: reset full-speed USB device number 4 using xhci_hcd
        [ 2760.329980] usb 2-2: USB disconnect, device number 2
        [ 2760.330611] sd 3:0:0:0: [sdb] Synchronizing SCSI cache
        [ 2760.419985] sd 3:0:0:0: [sdb] Synchronize Cache(10) failed: Result: hostbyte=DID_ERROR driverbyte=DRIVER_OK
        [ 2883.002123] usb 1-6.1: reset full-speed USB device number 4 using xhci_hcd
        [ 2901.702701] usb 1-6.1: reset full-speed USB device number 4 using xhci_hcd
        [ 2939.566432] usb 1-6.1: reset full-speed USB device number 4 using xhci_hcd
        [ 3079.257317] usb 1-6.1: reset full-speed USB device number 4 using xhci_hcd
        [ 3098.286597] wlp4s0: authenticate with 00:1e:e5:25:e1:70
        [ 3098.292411] wlp4s0: send auth to 00:1e:e5:25:e1:70 (try 1/3)
        [ 3098.294298] wlp4s0: authenticated
        [ 3098.294448] iwlwifi 0000:04:00.0 wlp4s0: disabling HT as WMM/QoS is not supported by the AP
        [ 3098.294451] iwlwifi 0000:04:00.0 wlp4s0: disabling VHT as WMM/QoS is not supported by the AP
        [ 3098.295899] wlp4s0: associate with 00:1e:e5:25:e1:70 (try 1/3)
        [ 3098.298465] wlp4s0: RX AssocResp from 00:1e:e5:25:e1:70 (capab=0x411 status=0 aid=13)
        [ 3098.300622] wlp4s0: associated
        [ 3216.903441] wlp4s0: authenticate with a0:f3:c1:f2:b5:5c
        [ 3216.909370] wlp4s0: send auth to a0:f3:c1:f2:b5:5c (try 1/3)
        [ 3216.911730] wlp4s0: authenticated
        [ 3216.912082] wlp4s0: associate with a0:f3:c1:f2:b5:5c (try 1/3)
        [ 3216.919265] wlp4s0: RX AssocResp from a0:f3:c1:f2:b5:5c (capab=0x431 status=0 aid=1)
        [ 3216.920136] wlp4s0: associated
        [ 3284.807831] usb 1-6.1: reset full-speed USB device number 4 using xhci_hcd
        [ 3292.189885] lp: driver loaded but no devices found
        [ 3338.925662] iwlwifi 0000:04:00.0: fail to flush all tx fifo queues Q 2
        [ 3338.925666] iwlwifi 0000:04:00.0: Current SW read_ptr 205 write_ptr 206
        [ 3338.925838] iwl data: 00000000: 00 20 00 00 00 00 00 00 00 00 00 00 00 00 00 00  . ..............
        [ 3338.925850] iwlwifi 0000:04:00.0: FH TRBs(0) = 0x00000000
        [ 3338.925861] iwlwifi 0000:04:00.0: FH TRBs(1) = 0x801020cd
        [ 3338.925873] iwlwifi 0000:04:00.0: FH TRBs(2) = 0x00000000
        [ 3338.925884] iwlwifi 0000:04:00.0: FH TRBs(3) = 0x80300033
        [ 3338.925895] iwlwifi 0000:04:00.0: FH TRBs(4) = 0x00000000
        [ 3338.925907] iwlwifi 0000:04:00.0: FH TRBs(5) = 0x00000000
        [ 3338.925918] iwlwifi 0000:04:00.0: FH TRBs(6) = 0x00000000
        [ 3338.925930] iwlwifi 0000:04:00.0: FH TRBs(7) = 0x00709071
        [ 3338.925978] iwlwifi 0000:04:00.0: Q 0 is active and mapped to fifo 3 ra_tid 0x0000 [52,52]
        [ 3338.926027] iwlwifi 0000:04:00.0: Q 1 is active and mapped to fifo 2 ra_tid 0x0000 [0,0]
        [ 3338.926075] iwlwifi 0000:04:00.0: Q 2 is active and mapped to fifo 1 ra_tid 0x0000 [205,206]
        [ 3338.926124] iwlwifi 0000:04:00.0: Q 3 is active and mapped to fifo 0 ra_tid 0x0000 [0,0]
        [ 3338.926172] iwlwifi 0000:04:00.0: Q 4 is inactive and mapped to fifo 0 ra_tid 0x0000 [0,0]
        [ 3338.926221] iwlwifi 0000:04:00.0: Q 5 is inactive and mapped to fifo 0 ra_tid 0x0000 [0,0]
        [ 3338.926269] iwlwifi 0000:04:00.0: Q 6 is inactive and mapped to fifo 0 ra_tid 0x0000 [0,0]
        [ 3338.926317] iwlwifi 0000:04:00.0: Q 7 is inactive and mapped to fifo 0 ra_tid 0x0000 [0,0]
        [ 3338.926366] iwlwifi 0000:04:00.0: Q 8 is active and mapped to fifo 3 ra_tid 0x0000 [0,0]
        [ 3338.926414] iwlwifi 0000:04:00.0: Q 9 is active and mapped to fifo 7 ra_tid 0x0000 [114,114]
        [ 3338.926462] iwlwifi 0000:04:00.0: Q 10 is inactive and mapped to fifo 0 ra_tid 0x0000 [0,0]
        [ 3338.926511] iwlwifi 0000:04:00.0: Q 11 is inactive and mapped to fifo 0 ra_tid 0x0000 [0,0]
        [ 3338.926559] iwlwifi 0000:04:00.0: Q 12 is inactive and mapped to fifo 0 ra_tid 0x0000 [0,0]
        [ 3338.926665] iwlwifi 0000:04:00.0: Q 13 is inactive and mapped to fifo 0 ra_tid 0x0000 [0,0]
        [ 3338.926713] iwlwifi 0000:04:00.0: Q 14 is inactive and mapped to fifo 0 ra_tid 0x0000 [0,0]
        [ 3338.926761] iwlwifi 0000:04:00.0: Q 15 is active and mapped to fifo 5 ra_tid 0x0000 [0,0]
        [ 3338.926967] iwlwifi 0000:04:00.0: Q 16 is active and mapped to fifo 1 ra_tid 0x0000 [253,253]
        [ 3338.927172] iwlwifi 0000:04:00.0: Q 17 is inactive and mapped to fifo 0 ra_tid 0x0000 [0,0]
        [ 3338.927220] iwlwifi 0000:04:00.0: Q 18 is inactive and mapped to fifo 0 ra_tid 0x0000 [0,0]
        [ 3338.927268] iwlwifi 0000:04:00.0: Q 19 is inactive and mapped to fifo 0 ra_tid 0x0000 [0,0]
        [ 3339.048185] wlp4s0: authenticate with 00:1e:e5:25:e1:70
        [ 3339.054333] wlp4s0: send auth to 00:1e:e5:25:e1:70 (try 1/3)
        [ 3339.056183] wlp4s0: authenticated
        [ 3339.056340] iwlwifi 0000:04:00.0 wlp4s0: disabling HT as WMM/QoS is not supported by the AP
        [ 3339.056343] iwlwifi 0000:04:00.0 wlp4s0: disabling VHT as WMM/QoS is not supported by the AP
        [ 3339.056818] wlp4s0: associate with 00:1e:e5:25:e1:70 (try 1/3)
        [ 3339.059371] wlp4s0: RX AssocResp from 00:1e:e5:25:e1:70 (capab=0x411 status=0 aid=13)
        [ 3339.060040] wlp4s0: associated
        [ 3697.278346] wlp4s0: authenticate with a0:f3:c1:f2:b5:5c
        [ 3697.284749] wlp4s0: send auth to a0:f3:c1:f2:b5:5c (try 1/3)
        [ 3697.288129] wlp4s0: authenticated
        [ 3697.289094] wlp4s0: associate with a0:f3:c1:f2:b5:5c (try 1/3)
        [ 3697.295860] wlp4s0: RX AssocResp from a0:f3:c1:f2:b5:5c (capab=0x431 status=0 aid=1)
        [ 3697.298518] wlp4s0: associated
        [ 3817.297329] usb 1-6.1: reset full-speed USB device number 4 using xhci_hcd
        [ 3818.535171] wlp4s0: authenticate with 00:1e:e5:25:e1:70
        [ 3818.541095] wlp4s0: send auth to 00:1e:e5:25:e1:70 (try 1/3)
        [ 3818.544549] wlp4s0: authenticated
        [ 3818.544686] iwlwifi 0000:04:00.0 wlp4s0: disabling HT as WMM/QoS is not supported by the AP
        [ 3818.544689] iwlwifi 0000:04:00.0 wlp4s0: disabling VHT as WMM/QoS is not supported by the AP
        [ 3818.545614] wlp4s0: associate with 00:1e:e5:25:e1:70 (try 1/3)
        [ 3818.548235] wlp4s0: RX AssocResp from 00:1e:e5:25:e1:70 (capab=0x411 status=0 aid=13)
        [ 3818.548837] wlp4s0: associated
        [ 4057.678526] wlp4s0: authenticate with a0:f3:c1:f2:b5:5c
        [ 4057.684802] wlp4s0: send auth to a0:f3:c1:f2:b5:5c (try 1/3)
        [ 4057.687241] wlp4s0: authenticated
        [ 4057.687945] wlp4s0: associate with a0:f3:c1:f2:b5:5c (try 1/3)
        [ 4057.694636] wlp4s0: RX AssocResp from a0:f3:c1:f2:b5:5c (capab=0x431 status=0 aid=1)
        [ 4057.695194] wlp4s0: associated
        [ 4057.991821] iwlwifi 0000:04:00.0: No association and the time event is over already...
        [ 4057.991837] wlp4s0: Connection to AP a0:f3:c1:f2:b5:5c lost
        [ 4058.145551] wlp4s0: authenticate with 00:1e:e5:25:e1:70
        [ 4058.151750] wlp4s0: send auth to 00:1e:e5:25:e1:70 (try 1/3)
        [ 4058.153704] wlp4s0: authenticated
        [ 4058.153833] iwlwifi 0000:04:00.0 wlp4s0: disabling HT as WMM/QoS is not supported by the AP
        [ 4058.153835] iwlwifi 0000:04:00.0 wlp4s0: disabling VHT as WMM/QoS is not supported by the AP
        [ 4058.154420] wlp4s0: associate with 00:1e:e5:25:e1:70 (try 1/3)
        [ 4058.156993] wlp4s0: RX AssocResp from 00:1e:e5:25:e1:70 (capab=0x411 status=0 aid=13)
        [ 4058.158390] wlp4s0: associated
        [ 5408.661376] usb 1-6.1: reset full-speed USB device number 4 using xhci_hcd
        [ 6706.191974] usb 1-6.1: reset full-speed USB device number 4 using xhci_hcd
        [ 8369.772325] usb 1-6.1: reset full-speed USB device number 4 using xhci_hcd
        [ 8412.286685] usb 1-6.1: reset full-speed USB device number 4 using xhci_hcd
        [ 8470.444540] e1000e: enp0s25 NIC Link is Down
        [ 8470.457460] wlp4s0: deauthenticating from 00:1e:e5:25:e1:70 by local choice (Reason: 3=DEAUTH_LEAVING)
        [ 8471.549458] PM: Syncing filesystems ... done.
        [ 8471.822731] PM: Preparing system for mem sleep
        [ 8471.837896] Freezing user space processes ... (elapsed 0.001 seconds) done.
        [ 8471.839671] Freezing remaining freezable tasks ... (elapsed 0.000 seconds) done.
        [ 8471.840586] PM: Entering mem sleep
        [ 8471.840602] Suspending console(s) (use no_console_suspend to debug)
        [ 8471.992317] sd 0:0:0:0: [sda] Synchronizing SCSI cache
        [ 8472.000547] sd 0:0:0:0: [sda] Stopping disk
        [ 8472.212231] e1000e: EEE TX LPI TIMER: 00000011
        [ 8472.343236] PM: suspend of devices complete after 502.001 msecs
        [ 8472.360260] PM: late suspend of devices complete after 16.980 msecs
        [ 8472.362838] ehci-pci 0000:00:1d.0: System wakeup enabled by ACPI
        [ 8472.363006] xhci_hcd 0000:00:14.0: System wakeup enabled by ACPI
        [ 8472.374063] PM: noirq suspend of devices complete after 13.786 msecs
        [ 8472.374335] ACPI: Preparing to enter system sleep state S3
        [ 8472.434162] ACPI : EC: EC stopped
        [ 8472.434163] PM: Saving platform NVS memory
        [ 8472.434167] Disabling non-boot CPUs ...
        [ 8472.434198] intel_pstate CPU 1 exiting
        [ 8472.435657] smpboot: CPU 1 is now offline
        [ 8472.435986] intel_pstate CPU 2 exiting
        [ 8472.437321] smpboot: CPU 2 is now offline
        [ 8472.438273] intel_pstate CPU 3 exiting
        [ 8472.439544] smpboot: CPU 3 is now offline
        [ 8472.441620] ACPI: Low-level resume complete
        [ 8472.441673] ACPI : EC: EC started
        [ 8472.441673] PM: Restoring platform NVS memory
        [ 8472.442061] Enabling non-boot CPUs ...
        [ 8472.442090] x86: Booting SMP configuration:
        [ 8472.442091] smpboot: Booting Node 0 Processor 1 APIC 0x1
        [ 8472.456470]  cache: parent cpu1 should not be sleeping
        [ 8472.456555] CPU1 is up
        [ 8472.456571] smpboot: Booting Node 0 Processor 2 APIC 0x2
        [ 8472.470941]  cache: parent cpu2 should not be sleeping
        [ 8472.471036] CPU2 is up
        [ 8472.471053] smpboot: Booting Node 0 Processor 3 APIC 0x3
        [ 8472.485448]  cache: parent cpu3 should not be sleeping
        [ 8472.485540] CPU3 is up
        [ 8472.488748] ACPI: Waking up from system sleep state S3
        [ 8472.649180] acpi LNXPOWER:02: Turning OFF
        [ 8472.653501] xhci_hcd 0000:00:14.0: System wakeup disabled by ACPI
        [ 8472.653630] ehci-pci 0000:00:1d.0: System wakeup disabled by ACPI
        [ 8472.670118] PM: noirq resume of devices complete after 16.920 msecs
        [ 8472.676599] PM: early resume of devices complete after 6.446 msecs
        [ 8472.678826] rtc_cmos 00:02: System wakeup disabled by ACPI
        [ 8472.681782] sd 0:0:0:0: [sda] Starting disk
        [ 8472.702273] tpm_tis 00:05: TPM is disabled/deactivated (0x6)
        [ 8472.982540] ata1: SATA link up 6.0 Gbps (SStatus 133 SControl 300)
        [ 8472.983059] ata1.00: ACPI cmd ef/02:00:00:00:00:a0 (SET FEATURES) succeeded
        [ 8472.983061] ata1.00: ACPI cmd f5/00:00:00:00:00:a0 (SECURITY FREEZE LOCK) filtered out
        [ 8472.983673] usb 1-6: reset high-speed USB device number 2 using xhci_hcd
        [ 8472.984091] ata1.00: ACPI cmd ef/02:00:00:00:00:a0 (SET FEATURES) succeeded
        [ 8472.984093] ata1.00: ACPI cmd f5/00:00:00:00:00:a0 (SECURITY FREEZE LOCK) filtered out
        [ 8472.984574] ata1.00: configured for UDMA/133
        [ 8473.301119] usb 1-8: reset high-speed USB device number 5 using xhci_hcd
        [ 8473.510224] psmouse serio1: synaptics: queried max coordinates: x [..5676], y [..4758]
        [ 8473.539334] usb 1-6.1: reset full-speed USB device number 4 using xhci_hcd
        [ 8473.548573] psmouse serio1: synaptics: queried min coordinates: x [1266..], y [1096..]
        [ 8473.614987] PM: resume of devices complete after 937.449 msecs
        [ 8473.615182] PM: Finishing wakeup.
        [ 8473.615183] Restarting tasks ... done.
        [ 8475.617347] systemd[1]: Unit suspend.target is bound to inactive unit systemd-suspend.service. Stopping, too.
        [ 8475.651116] IPv6: ADDRCONF(NETDEV_UP): enp0s25: link is not ready
        [ 8475.849479] IPv6: ADDRCONF(NETDEV_UP): enp0s25: link is not ready
        [ 8475.850545] IPv6: ADDRCONF(NETDEV_UP): wlp4s0: link is not ready
        [ 8475.851845] iwlwifi 0000:04:00.0: L1 Enabled - LTR Enabled
        [ 8475.852296] iwlwifi 0000:04:00.0: L1 Enabled - LTR Enabled
        [ 8475.915017] iwlwifi 0000:04:00.0: L1 Enabled - LTR Enabled
        [ 8475.915631] iwlwifi 0000:04:00.0: L1 Enabled - LTR Enabled
        [ 8475.944034] IPv6: ADDRCONF(NETDEV_UP): wlp4s0: link is not ready
        [ 8475.972049] IPv6: ADDRCONF(NETDEV_UP): wlp4s0: link is not ready
        [ 8476.045868] usb 1-6.1: reset full-speed USB device number 4 using xhci_hcd
        [ 8479.352182] wlp4s0: authenticate with a0:f3:c1:f2:b5:5c
        [ 8479.358286] wlp4s0: send auth to a0:f3:c1:f2:b5:5c (try 1/3)
        [ 8479.459959] wlp4s0: send auth to a0:f3:c1:f2:b5:5c (try 2/3)
        [ 8479.462430] wlp4s0: authenticated
        [ 8479.463047] wlp4s0: associate with a0:f3:c1:f2:b5:5c (try 1/3)
        [ 8479.468621] wlp4s0: RX AssocResp from a0:f3:c1:f2:b5:5c (capab=0x431 status=0 aid=1)
        [ 8479.479585] wlp4s0: associated
        [ 8479.479756] IPv6: ADDRCONF(NETDEV_CHANGE): wlp4s0: link becomes ready
        [crhomber@192-168-001-109 ~]$ 
        


