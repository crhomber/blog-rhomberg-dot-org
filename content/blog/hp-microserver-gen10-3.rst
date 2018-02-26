HP MicroServer Gen10 - FreeBSD laeuft!
#######################################
:date: 2018-02-27 18:05
:slug: hp-microserver-gen10-3
:tags: HP, MicroServer, Gen10, NAS, FreeBSD
:lang: de

Vor gut einem halben Jahr habe ich ja versucht mal ein FreeBSD auf einen HPE MicroServer Gen10 zu installieren.

Heute habe ich es nochmals mit einem FreeBSD 12-CURRENT probiert (r329338) und siehe da, nachdem man in der /boot/loader.conf folgendes eintraegt lauefts:

.. code-block:: bash

	hw.pci.realloc_bars="1"




Will man booten, muss man im Boot-Loader "3" druecken und

.. code-block:: bash

	set hw.pci.realloc_bars="1"
	boot


machen....

