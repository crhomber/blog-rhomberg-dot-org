Syncthing
#########
:date: 2015-04-25 21:30
:slug: syncthing
:tags: Syncthing
:keywords: Syncthing
:lang: de

Nachdem ich ein Zeit lang Seafile [1] zur Synchronisaton und Datensicherung meines Smartphones benutzt habe, evaliere ich im Moment Syncthing [2].

Die Einrichtung von Syncthing ist im Vergleich zu Seafile um einiges einfacher und dauert nur ca 2 Minuten. Ich verwende Syncthing unter Linux, FreeBSD und Android auf 6 Rechnern.

Der Hauptrechner ist eine FreeBSD-Jail auf unserem Home-Server (HP Microserver), dieser ist nur aus dem LAN erreichbar.

Derzeit sind ca 10 GB an Daten im "Cluster" und es gab noch keine Probleme.

Syncthing verwendet einen etwas ungwohnten Ansatz, es gibt keinen zentralen Server, die Software welche installiert werden muss ist auf allen Rechnern die selbe, also Server und Client sozusagen.

Genaueres muss ich mir die naechsten Tage im Detail anschauen, ich werde weiter berichten.

[1] `Seafile <http://seafile.com/en/home/>`_

[2] `Syncthing <https://syncthing.net/>`_
