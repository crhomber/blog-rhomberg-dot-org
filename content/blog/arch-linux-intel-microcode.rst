Arch Linux Update Intel Microcode
####################################
:date: 2018-01-13 11:50
:slug: arch-linux-intel-microcode
:tags: Arch Linux, Linux, Intel, Microcode, Spectre, Meltdown
:keywords: Video, Firefox, Ruckel, 

Aktuell dreht die Welt ja wegen `Spectre und Meltdown <https://www.heise.de/thema/Meltdown-und-Spectre>`_ durch....zurecht!

Da ich Arch Linux verwende, habe ich mal nachgeschaut wie man den Microcode updaten kann und siehe da, es ist recht einfach und schnell erledigt.

.. code-block:: bash

	sudo pacman -S intel-ucode
	sudo grub-mkconfig -o /boot/grub/grub.cfg


Das war's!
