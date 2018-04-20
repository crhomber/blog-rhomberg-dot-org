Salt - aktueller Status
########################
:date: 2017-11-21 22:20
:slug: salt-1
:tags: Salt, Administrator, Job, Perfany
:keywords: Salt, FreeBSD

Vor ca. einem Jahr habe ich angefangen mich mit Salt/Saltstack zu beschaeftigen.

Ich war damals auf der Suche nach einer Loesung zur zentralen Administration unserer vielen FreeBSD-Jails, weiter war mir wichtig moeglichst viel vom Setup als Code vorzuhalten, damit man reproduzierbare und identische Setup hinbekommt.

Vor ca. einem Jahr habe ich mir gedacht "Bis Silvester migriere ich alles auf Salt!" - So schnell gings dann doch nicht, man hat ja noch anderes um die Ohren.

Mitlerweile haben wir Salt voll in unseren Deployment-Prozess was PERY angeht eingebunden, viele andere Dinge sind auch schon abgedeckt.
Gerade gestern war ich wieder mal froh als auf 70 Kisten ein neuer SSH-User samt Public-Key ausgerollt werden musste, ohne zentrales Management wohl einiges an Arbeit.

Mittlerweile erledigen wir folgende Aufgaben mittels Salt:

 * User anlegen und entfernen
 * SSH-Keys ausrollen (authorized_keys)
 * Pakete installieren
 * Pakete aktualisieren
 * Services verwalten (aktivieren, neu starten,...)
 * Mittels Grains div. Kleinigkeiten auslesen (sehr hilfreich!)
 * Div. Befehle ausfuehren

Rueckblickend muss ich sagen dass sich der Aufwand sich in Salt einzuarbeiten gelohn hat, ich aber noch lange nicht da bin wo ich hinwill ;-). 
