Home Lab 4 - Modemprobleme
###########################
:date: 2017-07-01 11:30
:slug: home-lab-4
:tags: Netzwerk, Labor, Home, Hardware, UPC, WAN, SATA, USB, Fantec, HP, Switches
:keywords: Netzwerk Laboraufbau

In letzter Zeit gab es immer wieder kurze Ausfaelle der UPC-Verbindung,
ich vermute, dass das Modem durch den Provider in der Nacht neu gestartet oder umkonfiguriert wurde.
Wie auch immer - jedenfalls war danach auf der pfSense die Verbindung zum Modem kaputt, sobald ich das Interface neu gestartet habe war alles wieder gut.

Einige Zeit habe ich dann mit div. DHCP-Parametern rumexperimentiert, leider hat dies auch nichts gebracht.

Also wurde ich etwas kreativer...
Das Modem steht bei uns in der Abstellkammer in der Wohnung, die Firewall ist im Keller, bisher hatte ich das Netz einfach runtergepatched und in ein Interface der FW gesteckt. Jetzt habe ich das WAN in ein eigenes VLAN gepackt, also durch die Switches gepatched und dies scheint jetzt mal das Problem behoben zu haben.

Das wuerde auch meine Vermutung auf DHCP-Probleme bestaetigen, denn in dem neuen Setup ist das WAN-Interface auf der Firewall immer noch "up", auch wenn das Modem "weck" ist.

Mal schaun, wies sich entwickelt....
