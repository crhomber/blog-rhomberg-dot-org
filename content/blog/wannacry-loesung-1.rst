WannaCry - Loesung
##########################
:date: 2017-05-20 16:00
:slug: wannacry-loesung-1
:tags: WannaCry, Ransomware, Malware, Windows, Crypto, Security
:keywords: WannaCry entschluessen.

Fuer Betroffene von WannaCry gibts jetzt ev. eine funktionierende Loesung wieder an die Daten zu kommen.

`Wannakey <https://github.com/aguinet/wannakey>`_ ermittelt die Primzahlen fuer den RSA private-key welchen Wanacrypt angelegt hat.

Dies funktioniert aber nur wenn der Rechner nach befall noch nicht neu gebootet wurde!

Falls man die Primzahlen gefunden wurden, kann danach mittels `wanadecrypt <https://github.com/gentilkiwi/wanadecrypt>`_ mit dem entschluesseln begonnen werden.


Das Ganze basiert auf einer nicht gepatchen Sicherheitsluecke und funktioniert anscheinen nur bei Windows XP...

Viel Spass!

