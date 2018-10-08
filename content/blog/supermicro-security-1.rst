Supermicro Security
##############################
:date: 2018-10-08 19:15
:author: Christian
:tags: NSA, Supermicro, USA, China, Hardware, Spionage, Geheimdienste, Finanzen, Aktien
:slug: supermicro-security-1

Puh, das Thema ist ganz schon schwierig und es gibt leider immer noch keine Klarheit.
Hintergrund:
Bloomberg `berichtete <https://www.bloomberg.com/news/features/2018-10-04/the-big-hack-how-china-used-a-tiny-chip-to-infiltrate-america-s-top-companies>`_ vom "Big Hack". Es geht darum, dass "irgendwer" in China direkt auf Boards von Supermicro (einer der groessten Hersteller von Serverhardware) "Spionagechips" implantiert hat.

Jetzt hagelt es `Dementis <https://www.bloomberg.com/news/articles/2018-10-04/the-big-hack-amazon-apple-supermicro-and-beijing-respond>`_ und auch die Security-Community ist sich noch nicht ganz sicher ob dies alles technisch wirklich so moeglich war.

Es geht um einen Chip, etwa so gross wie ein Reiskorn, in der Naehe des IPMI-Stacks, also der Ferwartungshardware (Embedded System auf dem Board). Gerade im IPMI-Bereich gibts immer wieder grauslige Fehler, egal von welchem Hersteller - teilweise gibt es dann auch keine Patches mehr dafuer.

Nach der Veroeffentlichung der Meldung ist der Aktienkurs von Supermicro natuerlich gleich mal abgesackt (so ca. 50%) und ich hab mir gleich gedacht dass dies auch eine bewusste Finanzmarktmanipulation sein koennte.

Der grandiose Erich Moechel hat jetzt mal auch einen, wie immer, genialen `Artikel veroeffentlicht <https://fm4.orf.at/stories/2940104/>`_.

Generell sehe ich auch ein riesen Problem in der Supply-Chain von Hardware im Allgemeinen, leider findet man da recht wenig im Netz darueber.

Aja noch wegen IPMI:
Es gibt natuerlich Buden die "stecken" an das IPMI direkt Internet ran, weil ist ja einfach und so, aber die haben generell ein Problem.
IPMI muss immer(!) in einem eigenen Netz betrieben werden, welches nicht ueber andere Netze (nicht nur uebers Internet) erreichbar ist.

Man kann also gespannt sein, was da in den naechsten Tagen noch rauskommt.
