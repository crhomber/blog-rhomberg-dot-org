Intel NUC
########################
:date: 2014-03-19 18:00
:slug: intel-nuc 
:tags: Intel, NUC, Hardware

Heute ist er gekommen, der Intel NUC D54250WYKH [1].

.. image:: images/intel-nuc-small.jpg 
	:alt: Intel NUC


Ich verwende das Teil in der Firma als "Workstation",
als Festplatte verwende ich eine SSD von Angelbird [2].

Von der Performance her kann man das Geraet durchaus mit einem PC vergleichen, trotz Luefer ist er NUC quasi lautlos, weiters laesst sich der PC mittels VESA-mount hinter den Monitor montieren.


Ausgabe von lscpi unter ArchLinux

.. code-block:: bash

	[crhomber@crws02 ~]$ lspci
	00:00.0 Host bridge: Intel Corporation Haswell-ULT DRAM Controller (rev 09)
	00:02.0 VGA compatible controller: Intel Corporation Haswell-ULT Integrated Graphics Controller (rev 09)
	00:03.0 Audio device: Intel Corporation Device 0a0c (rev 09)
	00:14.0 USB controller: Intel Corporation Lynx Point-LP USB xHCI HC (rev 04)
	00:16.0 Communication controller: Intel Corporation Lynx Point-LP HECI #0 (rev 04)
	00:19.0 Ethernet controller: Intel Corporation Ethernet Connection I218-V (rev 04)
	00:1b.0 Audio device: Intel Corporation Lynx Point-LP HD Audio Controller (rev 04)
	00:1d.0 USB controller: Intel Corporation Lynx Point-LP USB EHCI #1 (rev 04)
	00:1f.0 ISA bridge: Intel Corporation Lynx Point-LP LPC Controller (rev 04)
	00:1f.2 SATA controller: Intel Corporation Lynx Point-LP SATA Controller 1 [AHCI mode] (rev 04)
	00:1f.3 SMBus: Intel Corporation Lynx Point-LP SMBus Controller (rev 04)
	[crhomber@crws02 ~]$ 

[1] `Intel NUC <http://www.intel.com/nuc/>`_

[2] `Angelbird <http://www.angelbird.com/>`_

