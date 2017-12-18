Home Lab 3
##################
:date: 2017-05-29 19:50
:slug: home-lab-3
:tags: Netzwerk, Labor, Home, Hardware, SATA, USB, Fantec, HP, Switches
:keywords: Netzwerk Laboraufbau

Letzte Woche hat sich einer meiner beiden Switches irgendwie ins Jenseits befoerdert - jedenfalls funktionierten die VLANs nicht mehr sauber - der Switch hatte da einiges an Paketverlust...jedenfalls - tauschen!

Heute also mal alles neu konfiguriert, habe mich fuer einen HPE 1920-24g und 1920-8g entschieden - der 24er ist im Keller im Rack und der 8er in der Bude und verteilt da an die Clients die entsprechenden Netze.

Es gibt momentan 10 Vlans, hat alles seinen Grund - muss leider so sein.

Weiters nutzte ich die Gelegenheit um die Verkabelung mal etwas aufzuraeumen.

Nach guten 4 Stunden war der Normalbetrieb wieder da, alle VMs waren uebers Netz erreichbar, die VPN Tunnel waren auch da, was will man mehr.

Der Server hat jetzt einen LACP channel mit 2 Links, die HP Workstation (Z600), welche als Notloesung fuer etwaige Ausfaelle an einem anderen Standort dient hat nen LACP Channel ueber 4 Links bekommen.

.. image:: images/thumbs/thumbnail_tall/home-lab-3.jpg
        :target: images/home-lab-3.jpg
        :alt: Foto

