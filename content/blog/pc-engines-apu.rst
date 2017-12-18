PC Engines APU System-Board
############################
:date: 2014-04-30 13:00
:slug: pc-engines-apu
:tags: PC Engines, APU, Hardware

Heute sind die neuen Boards von `PC Engines <http://www.pcengines.ch/>`_ bei mir eingetroffen.

Bei `Perfany <http://www.perfany.at/>`_ verwenden wir gerne die bekannten ALIX-Boards, welche uns noch nie im Stich gelassen haben.

Jedoch wartete die Community schon lange auf ein Update der vielerorts beliebten Embedded-Boards.

Die Daten der neuen Version:
 * AMD T40E APU mit 1GHZ und 64-Bit Support
 * 2 oder 4 GB DDR3 DRAM
 * m-SATA Support
 * 2x miniPCI express Slots
 * 3x Gigabit Ethernet
 * CoreBoot open source Bios

Wichtig ist jedoch, dass die neuen Boards nicht ohne passende Kuehlung betrieben werden!


Hier noch einige Bilder:

.. image:: images/apu-oberseite.jpg 
	:alt: APU Oberseite

.. image:: images/apu-unterseite.jpg 
	:alt: APU Unterseite

.. image:: images/kuehler.jpg 
	:alt: APU Kuehler

.. image:: images/pci.jpg 
	:alt: PCI


Ausgabe von dmesg unter FreeBSD 8.3 (pfSense)

.. code-block:: bash
	
	.
	Copyright (c) 1979, 1980, 1983, 1986, 1988, 1989, 1991, 1992, 1993, 1994
	        The Regents of the University of California. All rights reserved.
	FreeBSD is a registered trademark of The FreeBSD Foundation.
	FreeBSD 8.3-RELEASE-p16 #0: Thu May  1 16:19:14 EDT 2014
	    root@pf2_1_1_amd64.pfsense.org:/usr/obj.amd64/usr/pfSensesrc/src/sys/pfSense_SMP.8 amd64
	Timecounter "i8254" frequency 1193182 Hz quality 0
	CPU: AMD G-T40E Processor (1000.01-MHz K8-class CPU)
	  Origin = "AuthenticAMD"  Id = 0x500f20  Family = 14  Model = 2  Stepping = 0
	  Features=0x178bfbff<FPU,VME,DE,PSE,TSC,MSR,PAE,MCE,CX8,APIC,SEP,MTRR,PGE,MCA,CMOV,PAT,PSE36,CLFLUSH,MMX,FXSR,SSE,SSE2,HTT>                                            
	  Features2=0x802209<SSE3,MON,SSSE3,CX16,POPCNT>                                                                                                                        
	  AMD Features=0x2e500800<SYSCALL,NX,MMX+,FFXSR,Page1GB,RDTSCP,LM>                                                                                                      
	  AMD Features2=0x35ff<LAHF,CMP,SVM,ExtAPIC,CR8,ABM,SSE4A,MAS,Prefetch,IBS,SKINIT,WDT>                                                                                  
	  TSC: P-state invariant                                                                                                                                                
	real memory  = 4815060992 (4592 MB)                                                                                                                                     
	avail memory = 4076978176 (3888 MB)
	ACPI APIC Table: <CORE   COREBOOT>
	FreeBSD/SMP: Multiprocessor System Detected: 2 CPUs
	FreeBSD/SMP: 1 package(s) x 2 core(s)
	 cpu0 (BSP): APIC ID:  0
	 cpu1 (AP): APIC ID:  1
	ioapic0 <Version 2.1> irqs 0-23 on motherboard
	wlan: mac acl policy registered
	ipw_bss: You need to read the LICENSE file in /usr/share/doc/legal/intel_ipw/.
	ipw_bss: If you agree with the license, set legal.intel_ipw.license_ack=1 in /boot/loader.conf.
	module_register_init: MOD_LOAD (ipw_bss_fw, 0xffffffff804abaf0, 0) error 1
	ipw_ibss: You need to read the LICENSE file in /usr/share/doc/legal/intel_ipw/.
	ipw_ibss: If you agree with the license, set legal.intel_ipw.license_ack=1 in /boot/loader.conf.
	module_register_init: MOD_LOAD (ipw_ibss_fw, 0xffffffff804abb90, 0) error 1
	ipw_monitor: You need to read the LICENSE file in /usr/share/doc/legal/intel_ipw/.
	ipw_monitor: If you agree with the license, set legal.intel_ipw.license_ack=1 in /boot/loader.conf.
	module_register_init: MOD_LOAD (ipw_monitor_fw, 0xffffffff804abc30, 0) error 1
	kbd1 at kbdmux0
	cryptosoft0: <software crypto> on motherboard
	padlock0: No ACE support.
	acpi0: <CORE COREBOOT> on motherboard
	acpi0: [ITHREAD]
	acpi0: Power Button (fixed)
	Timecounter "ACPI-fast" frequency 3579545 Hz quality 1000                                                                                                               
	acpi_timer0: <32-bit timer at 3.579545MHz> port 0x808-0x80b on acpi0                                                                                                    
	cpu0: <ACPI CPU> on acpi0                                                                                                                                               
	cpu1: <ACPI CPU> on acpi0                                                                                                                                               
	acpi_hpet0: <High Precision Event Timer> iomem 0xfed00000-0xfed003ff on acpi0                                                                                           
	Timecounter "HPET" frequency 14318180 Hz quality 900                                                                                                                    
	pcib0: <ACPI Host-PCI bridge> port 0xcf8-0xcff iomem 0xa0000-0xbffff on acpi0
	pci0: <ACPI PCI bus> on pcib0
	pcib1: <ACPI PCI-PCI bridge> irq 16 at device 4.0 on pci0
	pci1: <ACPI PCI bus> on pcib1
	re0: <RealTek 8168/8111 B/C/CP/D/DP/E/F PCIe Gigabit Ethernet> port 0x1000-0x10ff mem 0xf7a00000-0xf7a00fff,0xf7900000-0xf7903fff irq 16 at device 0.0 on pci1
	re0: Using 1 MSI-X message
	re0: ASPM disabled
	re0: Chip rev. 0x2c000000
	re0: MAC rev. 0x00000000
	miibus0: <MII bus> on re0
	rgephy0: <RTL8169S/8110S/8211B media interface> PHY 1 on miibus0
	rgephy0:  none, 10baseT, 10baseT-FDX, 10baseT-FDX-flow, 100baseTX, 100baseTX-FDX, 100baseTX-FDX-flow, 1000baseT, 1000baseT-master, 1000baseT-FDX, 1000baseT-FDX-master, 1000baseT-FDX-flow, 1000baseT-FDX-flow-master, auto, auto-flow
	re0: [ITHREAD]
	pcib2: <ACPI PCI-PCI bridge> irq 17 at device 5.0 on pci0
	pci2: <ACPI PCI bus> on pcib2
	re1: <RealTek 8168/8111 B/C/CP/D/DP/E/F PCIe Gigabit Ethernet> port 0x2000-0x20ff mem 0xf7c00000-0xf7c00fff,0xf7b00000-0xf7b03fff irq 17 at device 0.0 on pci2
	re1: Using 1 MSI-X message
	re1: ASPM disabled
	re1: Chip rev. 0x2c000000
	re1: MAC rev. 0x00000000
	miibus1: <MII bus> on re1
	rgephy1: <RTL8169S/8110S/8211B media interface> PHY 1 on miibus1
	rgephy1:  none, 10baseT, 10baseT-FDX, 10baseT-FDX-flow, 100baseTX, 100baseTX-FDX, 100baseTX-FDX-flow, 1000baseT, 1000baseT-master, 1000baseT-FDX, 1000baseT-FDX-master, 1000baseT-FDX-flow, 1000baseT-FDX-flow-master, auto, auto-flow
	re1: [ITHREAD]
	pcib3: <ACPI PCI-PCI bridge> irq 18 at device 6.0 on pci0
	pci3: <ACPI PCI bus> on pcib3
	re2: <RealTek 8168/8111 B/C/CP/D/DP/E/F PCIe Gigabit Ethernet> port 0x3000-0x30ff mem 0xf7e00000-0xf7e00fff,0xf7d00000-0xf7d03fff irq 18 at device 0.0 on pci3
	re2: Using 1 MSI-X message
	re2: ASPM disabled
	re2: Chip rev. 0x2c000000
	re2: MAC rev. 0x00000000
	miibus2: <MII bus> on re2
	rgephy2: <RTL8169S/8110S/8211B media interface> PHY 1 on miibus2
	rgephy2:  none, 10baseT, 10baseT-FDX, 10baseT-FDX-flow, 100baseTX, 100baseTX-FDX, 100baseTX-FDX-flow, 1000baseT, 1000baseT-master, 1000baseT-FDX, 1000baseT-FDX-master, 1000baseT-FDX-flow, 1000baseT-FDX-flow-master, auto, auto-flow
	re2: [ITHREAD]
	atapci0: <ATI IXP700/800 SATA300 controller> port 0x4010-0x4017,0x4020-0x4023,0x4018-0x401f,0x4024-0x4027,0x4000-0x400f mem 0xf7f08000-0xf7f083ff irq 19 at device 17.0 on pci0
	atapci0: [ITHREAD]
	atapci0: AHCI v1.20 controller with 6 6Gbps ports, PM supported
	ata2: <ATA channel> at channel 0 on atapci0
	ata2: [ITHREAD]
	ata3: <ATA channel> at channel 1 on atapci0
	ata3: [ITHREAD]
	ata4: <ATA channel> at channel 2 on atapci0
	ata4: [ITHREAD]
	ata5: <ATA channel> at channel 3 on atapci0
	ata5: [ITHREAD]
	ata6: <ATA channel> at channel 4 on atapci0
	ata6: [ITHREAD]
	ata7: <ATA channel> at channel 5 on atapci0
	ata7: [ITHREAD]
	ohci0: <OHCI (generic) USB controller> mem 0xf7f04000-0xf7f04fff irq 18 at device 18.0 on pci0
	ohci0: [ITHREAD]
	usbus0: <OHCI (generic) USB controller> on ohci0
	ehci0: <EHCI (generic) USB 2.0 controller> mem 0xf7f08400-0xf7f084ff irq 17 at device 18.2 on pci0
	ehci0: [ITHREAD]
	usbus1: EHCI version 1.0
	usbus1: <EHCI (generic) USB 2.0 controller> on ehci0
	ohci1: <OHCI (generic) USB controller> mem 0xf7f05000-0xf7f05fff irq 18 at device 19.0 on pci0
	ohci1: [ITHREAD]
	usbus2: <OHCI (generic) USB controller> on ohci1
	ehci1: <EHCI (generic) USB 2.0 controller> mem 0xf7f08500-0xf7f085ff irq 17 at device 19.2 on pci0
	ehci1: [ITHREAD]
	usbus3: EHCI version 1.0
	usbus3: <EHCI (generic) USB 2.0 controller> on ehci1
	pci0: <serial bus, SMBus> at device 20.0 (no driver attached)
	isab0: <PCI-ISA bridge> at device 20.3 on pci0
	isa0: <ISA bus> on isab0
	pcib4: <ACPI PCI-PCI bridge> at device 20.4 on pci0
	pci4: <ACPI PCI bus> on pcib4
	ohci2: <OHCI (generic) USB controller> mem 0xf7f06000-0xf7f06fff irq 18 at device 20.5 on pci0
	ohci2: [ITHREAD]
	usbus4: <OHCI (generic) USB controller> on ohci2
	pcib5: <ACPI PCI-PCI bridge> at device 21.0 on pci0
	pci5: <ACPI PCI bus> on pcib5
	pcib6: <ACPI PCI-PCI bridge> at device 21.1 on pci0
	pci0: couldn't attach pci bus
	device_attach: pcib6 attach returned 6
	pcib7: <ACPI PCI-PCI bridge> at device 21.2 on pci0
	pci0: couldn't attach pci bus
	device_attach: pcib7 attach returned 6
	pcib8: <ACPI PCI-PCI bridge> at device 21.3 on pci0
	pci0: couldn't attach pci bus
	device_attach: pcib8 attach returned 6
	ohci3: <OHCI (generic) USB controller> mem 0xf7f07000-0xf7f07fff at device 22.0 on pci0
	ohci3: [ITHREAD]
	usbus5: <OHCI (generic) USB controller> on ohci3
	ehci2: <EHCI (generic) USB 2.0 controller> mem 0xf7f08600-0xf7f086ff at device 22.2 on pci0
	ehci2: [ITHREAD]
	usbus6: EHCI version 1.0
	usbus6: <EHCI (generic) USB 2.0 controller> on ehci2
	acpi_button0: <Power Button> on acpi0
	atrtc0: <AT realtime clock> port 0x70-0x71 irq 8 on acpi0
	orm0: <ISA Option ROM> at iomem 0xee800-0xeffff on isa0
	atkbdc0: <Keyboard controller (i8042)> at port 0x60,0x64 on isa0
	atkbd0: <AT Keyboard> irq 1 on atkbdc0
	kbd0 at atkbd0
	atkbd: unable to get the current command byte value.
	atkbd0: [GIANT-LOCKED]
	atkbd0: [ITHREAD]
	psm0: unable to get the current command byte value.
	ppc0: cannot reserve I/O port range
	uart0: <16550 or compatible> at port 0x3f8-0x3ff irq 4 flags 0x10 on isa0
	uart0: [FILTER]
	uart0: console (9600,n,8,1)
	uart1: <16550 or compatible> at port 0x2f8-0x2ff irq 3 on isa0
	uart1: [FILTER]
	acpi_throttle0: <ACPI CPU Throttling> on cpu0
	acpi_throttle1: <ACPI CPU Throttling> on cpu1
	acpi_throttle1: failed to attach P_CNT
	device_attach: acpi_throttle1 attach returned 6
	RTC BIOS diagnostic error ff<clock_battery,ROM_cksum,config_unit,memory_size,fixed_disk,invalid_time>
	Timecounters tick every 1.000 msec
	IPsec: Initialized Security Association Processing.
	usbus0: 12Mbps Full Speed USB v1.0
	usbus1: 480Mbps High Speed USB v2.0
	usbus2: 12Mbps Full Speed USB v1.0
	usbus3: 480Mbps High Speed USB v2.0
	usbus4: 12Mbps Full Speed USB v1.0
	usbus5: 12Mbps Full Speed USB v1.0
	usbus6: 480Mbps High Speed USB v2.0
	SMP: AP CPU #1 Launched!
	Root mount waiting for: usbus6 usbus5 usbus4 usbus3 usbus2 usbus1 usbus0
	ugen0.1: <ATI> at usbus0
	uhub0: <ATI OHCI root HUB, class 9/0, rev 1.00/1.00, addr 1> on usbus0
	ugen2.1: <ATI> at usbus2ugen1.1: <ATI> at usbus1
	uhub1: 
	<ATI OHCI root HUB, class 9/0, rev 1.00/1.00, addr 1> on usbus2
	uhub2: <ATI EHCI root HUB, class 9/0, rev 2.00/1.00, addr 1> on usbus1
	ugen3.1: <ATI> at usbus3
	uhub3: <ATI EHCI root HUB, class 9/0, rev 2.00/1.00, addr 1> on usbus3
	ugen5.1: <ATI> at usbus5ugen4.1: <ATI> at usbus4
	uhub4: 
	<ATI OHCI root HUB, class 9/0, rev 1.00/1.00, addr 1> on usbus5
	uhub5: <ATI OHCI root HUB, class 9/0, rev 1.00/1.00, addr 1> on usbus4
	ugen6.1: <ATI> at usbus6
	uhub6: <ATI EHCI root HUB, class 9/0, rev 2.00/1.00, addr 1> on usbus6
	uhub0: 5 ports with 5 removable, self powered
	uhub1: 5 ports with 5 removable, self powered
	uhub4: 4 ports with 4 removable, self powered
	uhub5: 2 ports with 2 removable, self powered
	Root mount waiting for: usbus6 usbus3 usbus1
	uhub6: 4 ports with 4 removable, self powered
	uhub3: 5 ports with 5 removable, self powered
	uhub2: 5 ports with 5 removable, self powered
	ugen6.2: <Generic> at usbus6
	umass0: <Generic Flash Card ReaderWriter, class 0/0, rev 2.01/1.00, addr 2> on usbus6
	umass0:  SCSI over Bulk-Only; quirks = 0x4001
	umass0:0:0:-1: Attached to scbus0
	da0 at umass-sim0 bus 0 scbus0 target 0 lun 0
	da0: <Multiple Card  Reader 1.00> Removable Direct Access SCSI-4 device 
	da0: 40.000MB/s transfers
	da0: 15193MB (31116288 512 byte sectors: 255H 63S/T 1936C)
	GEOM: da0s1: geometry does not match label (16h,63s != 255h,63s).
	GEOM: da0s2: geometry does not match label (16h,63s != 255h,63s).
	Trying to mount root from ufs:/dev/ufs/pfsense0
	re0: link state changed to DOWN
	re1: link state changed to UP
	pflog0: promiscuous mode enabled
	re0: link state changed to UP
	re0: link state changed to DOWN

