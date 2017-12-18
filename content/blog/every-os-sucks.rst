Every OS sucks!
########################
:date: 2014-02-20 19:25
:slug: every-os-sucks
:tags: Betriebssysteme, FreeBSD, Linux

Als Sysadmin bin ich ja unterschiedliche Betriebssysteme gewohnt,
fuer jeden Anwendungsfall habe ich das passende OS parat, doch welches verwendet der Sysadmin auf der eigenen Workstation?!

Diese Frage hat mich die letzten Wochen doch sehr beschaeftigt,
seit ca 2007 verwende ich kein Windows mehr - aus Prinzip.

Apple kommt fuer mich aus Gruenden der Bedienung und des Arbeitsflusses nicht in Frage,
auch wenns noch so toll ausschaut und "immer funktioniert". 

Serverseitig verwende ich Debian GNU/Linux und FreeBSD, am Laptop ArchLinux,
dieses habe ich auch lange am Desktop eingesetzt.

Da ich jedoch die Features von ZFS sehr schaetze und die Stabilitaet von FreeBSD meiner Meinung nach ungeschlagen ist
habe ich mich entschlossen auch auf dem Desktop FreeBSD zu verwenden, genauer gesagt PC-BSD welches auf FreeBSD basiert.

Gesagt - getan, ich migrierte meine Workstation auf PC-BSD, arbeitet einige Tage und habe mir dann durch das installieren
div. Ports und einigen Anpassungen (die sich wohl als "unschlau" herausstellten) das System zerschossen.

Was machen?
Gute Frage - da das Installieren von FreeBSD unter PC-BSD nicht wirklich von den PC-BSD leuten supported wird habe ich mich
entschlossen komplett auf FreeBSD zu migrieren, dank ZFS ja kein problem mehr, einfach ein

.. code-block:: identifier

	zpool export ZPOOL

und nach der FreeBSD-Installation ein


.. code-block:: identifier

        zpool import ZPOOL


und schon hat man alle Daten wieder im Zugriff.

Doch unter FreeBSD 10 ist es mir nicht gelungen Xorg ohne grossen Aufwand in ordentlicher Performance ans laufen zu bekommen,
ganz zuschweigen von Flash - welches hier nicht ganz sauber funktionert - Java das Selbe.

Klar wuerde es funktionieren, doch hatte ich jetzt nicht die Zeit xorg komplett neu zu bauen.

Somit habe ich die Workstation auf FreeBSD gelassen (auf dieser laufen einige virt. Maschinen) und verwende nun den Laptop unter ArchLinux.

Lange Geschichte - das Ergebnis:
EVERY OS SUCKS!!!1!

.. raw:: html

	<iframe width="420" height="315" src="//www.youtube.com/embed/d85p7JZXNy8" frameborder="0" allowfullscreen></iframe>
