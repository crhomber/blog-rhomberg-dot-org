WhatsApp - Firewall-Regeln
#######################################
:date: 2018-02-21 19:33
:slug: whatsapp-firewall-1
:tags: WhatsApp, IM, Security, end-to-end encryption, Firewall, TCP, UDP

Also, neben TCP 80 und 443 will WhatsApp auch folgende Ports nach aussen offen haben:

.. code-block:: bash

	TCP: 4244,5222,5223,5228,5242
	TCP/UDP: 59234, 50318
	UDP: 3478,45395


Dann klappts auch mit der Audio- sowie Videotelefonie.
