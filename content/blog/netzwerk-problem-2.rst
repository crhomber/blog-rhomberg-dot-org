Netzwerkproblem - geloest!
#####################################################
:date: 2018-03-13 19:17
:slug: netzwerk-problem-2
:tags: Netzwerk, Problem, Windows, Unix, Linux, FreeBSD, A1, Kabel
:keywords: 

Ich schrieb ja vor einiger Zeit von einem schraegen Netzwerkproblem bei einem Kunden.
Das Problemt trat nicht immer auf, schien nur Windows zu betreffen und war sehr schwer einzugrenzen.

Jedenfalls lags an dem Wunderbaren A1 Modem, das Pirelli irgendwas...
Ich moechte hierbei erwaehnen, dass es sich hierbei um einen Business Anschluss handelt.

Das Modem, welches eigentlich ein Plasterouter ist (hat sogar USB 3.x!!11) war schuld an dem Problem. Auf der Hinterseite hat die Plastikdose 4 Ethernet-Ports, einen Gbit und 4 FastEthernet....

Der Techniker von A1 hat mir damals ein Kabel in den Gbit-Port gesteckt und mir so die Leitung "uebergeben". Jedenfalls hat dieser Port ein Problem, aber leider nicht nur dieser, bei meinem Kunden funktionierte nur der Eth3 ohne Probleme.

Business ist eben nicht immer Business!

Wir hatten schon Routing-Policies und QoS sowie den Core-Switch in Verdacht, aber naja - man denkt halt nicht immer na den Port "Eth3" am tollen A1 Plastikteil - welches uebrigens immer hochkant aufgestellt werden muss und nicht liegend, wurde mir von A1 gesagt, weil die Dinger sonst abschmieren.

Geil!

A1, UPC, egal wer - immer billige all in one Plasterouter.
Bei Privatkunden verstehe ich das ja, aber im Business-Bereich will man Ethernet uebergeben bekommen und nicht einen Printserver, Hotpsot, wtf...
