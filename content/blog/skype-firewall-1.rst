Skype - Firewall-Regeln
#######################################
:date: 2018-02-26 12:33
:slug: skype-firewall-1
:tags: Skype, IM, Security, end-to-end encryption, Firewall, TCP, UDP

Also, neben TCP 80 und 443 will Skype auch folgende Ports nach aussen offen haben:

.. code-block:: bash

	TCP/UDP: 30000-56535
	UDP: 3478-3481


Dann klappts auch mit der Audio- sowie Videotelefonie.
