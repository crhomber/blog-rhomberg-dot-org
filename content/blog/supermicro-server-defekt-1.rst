Supermicro Server - Ausfall nach nur 6 Monaten
################################################
:date: 2018-12-24 11:10
:slug: supermicro-server-defekt-1
:tags: Hardware, Supermicro, Job, Server, Defekt, 5028D-TN4T

Ich habe im Keller einen 5028D-TN4T mit viel RAM und Platten.

Auf der Kiste laufen seit Sommer div. Dienste (einige Jails, div. Bhyve VMs) ohne Probleme.

Gestern wollte ich die jaehrliche Reinigung des Racks erledigen, habe deshalb den Server runtergefahren und vom Netz getrennt.

Auch die USV wurde gereinigt, man will ja sicherstellen dass das alles sauber laeuft.

Nach der Wartung habe ich den Rechner ans Netz genommen und uebers IPMI wieder gestartet. Soweit so gut...nach einigen Minuten wunderte ich mich warum die Meldungen vom Monitoring nicht verschwinden und habe mal aufs IPMI geschaut um zu sehen, was die Kiste so treibt.

Tja, die Maschine startet nicht, kein POST, nix aufm Schirm, im IPMI steht power on failed....Luefter laufen - komisch.

Ich hab mal ein Ticket beim Lieferanten aufgemacht, mal schauen - ich vermute die CPU oder das Board sind defekt.
Ev. auch nur das Netzteil, also abwarten.
Deshalb sind div. Dienste im Moment nicht erreichbar...
