X11-Config
###########
:date: 2016-06-25 08:30
:slug: x11-config
:tags: Unix, Linux, X11
:keywords: X11 middle mouse button


Ich hatte in letzter Zeit etwas Probleme mit der beschleunigung des Mauszeigers, normalerweise verwendete ich "xset m 1 1" in meinem Startscript von Awesome, da ich jedoch einen KVM-Switch betreibe muss der Befehl bei jedem reconnecten der USB-Maus neu ausgefuehrt werden.
Mit xf86-input-libinput habe ich die Loesung gefunden


.. code-block:: bash

	[crhomber@cr-z600-1 ~]$ cat /etc/X11/xorg.conf.d/50-mouse-acceleration.conf 
	Section "InputClass"
		Identifier "My Mouse"
		Driver "libinput"
		MatchIsPointer "yes"
		Option "AccelProfile" "flat"
	EndSection
	[crhomber@cr-z600-1 ~]$ 




.. code-block:: bash

	[crhomber@cr-z600-1 ~]$ cat /etc/X11/xorg.conf.d/99-mouse-midbuttonemulation.conf 
	Section "InputClass"
       		Identifier "middle button emulation class" 
		MatchIsPointer "on"
		Option "MiddleEmulation" "on"
	EndSection
	[crhomber@cr-z600-1 ~]$ 

