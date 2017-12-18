pfSense auf PC-Engines APU-Board
################################
:date: 2014-08-05 16:05
:slug: pf-sense-auf-pc-engines-apu.rst
:tags: pfSense, APU, PC-Engines, Freebsd
:keywords: pfSense, APU, PC-Engines, Freebsd, Boot, Problem, Root, Partition

Manchmal bekommt der FreeBSD-Kernel von pfSense beim Booten auf den neuen APU-Boards von PC-Engines keine Root-Partition.

Dies wird wohl durch den SD-Card Reader, welcher über USB angebunden ist, verursacht.
Dies stellt aber kein großes Problem dar, ein einzelner Boot-Parameter reicht aus.

Den Boot-Vorgang unterbrechen, dann bekommt man eine Shell (OK), hier folgenden Befehl eingeben:

.. code-block:: bash

	set kern.cam.boot_delay=10000

Danach den Boot-Befehl eingeben:

.. code-block:: bash

	boot


Sobald pfSense gebootet ist, auf eine Konsole wechseln und das Dateisystem rw-remounten:

.. code-block:: bash

	/etc/rc.conf_mount_rw 


Jetzt in der Datei /boot/loader.conf den Parameter eintragen

.. code-block:: bash

	kern.cam.boot_delay=10000

Danach das Dateisystem wieder read-only mounten:

.. code-block:: bash

	/etc/rc.conf_mount_ro


Das Problem sollte jetzt behoben sein.
