FreeBSD HAST Teil 1
###################
:date: 2014-03-12 11:25
:slug: freebsd-hast-teil-1
:tags: FreeBSD, HAST, Storage, NFS

Aktuell beschaeftige ich mit HAST[1] unter FreeBSD[2],
die Daten von NFS-Shares sollen repliziert werden.
Soweit eigentlich kein Problem.


Vorgehensweise
 #. Netzwerk entsprechend konfigurieren (eigene NIC fuer HAST, ev. sogar LACP)
 #. /etc/hast.conf entsprechend konfigurieren (auf beiden Nodes identisch, DNS muss passen!)
 #. HAST-Device erstellen (hastctl create ...)
 #. HAST initialisieren
 #. FS (ZFS) auf dem HAST-Device erstellen

[1] `High Available Storage <http://www.freebsd.org/doc/de/books/handbook/disks-hast.html>`_

[2] `FreeBSD <http://www.freebsd.org>`_
