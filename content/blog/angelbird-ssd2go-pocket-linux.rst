Angelbird SSD2go pocket unter Linux
####################################
:date: 2016-10-19 00:20
:slug: angelbird-ssd2go-pocket-linux
:tags: Hardware, Angelbird, SSD2go, SSD, Linux, UAS

Unter Linux zickt meine Angelbird SSD2go pocket etwas rum, merkbar wird es eigentlich nur wenn ich die Windows 10 VM starte, da ist sehr viel Disk-IO....

Jedenfalls liegt das Problem an UAS, dies laesst sich wie folgt deaktivieren:


.. code-block:: bash
	
	[crhomber@cr-l450-1 ~]$ cat /etc/modprobe.d/ignore_uas.conf 
	options usb-storage quirks=0x27d1:0x5136:u


danach noch ein


.. code-block:: bash

	mkinitcpio -p linux


und die Sache rennt wieder.

