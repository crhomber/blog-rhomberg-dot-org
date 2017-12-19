Server migriert
########################
:date: 2017-12-19 22:20
:slug: server-migration-2
:tags: Administrator, IBM, Server, x3690x5, Infrastruktur
:keywords: Server, FreeBSD

In den letzten Naechten habe ich meine Webprojekte auf eine neue Kiste umgezogen, die IP hat sich auch gaendert somit sind die Probleme mit den dynamischen IPs von UPC erstmal erledigt.

Vorher lief ja alles auf einem HP Microserver (altes Teil, aber tut was es soll!) jetzt isch das Zeugs auf einem IBM x3690x5 mit guter Ausstattung und im RZ in Lustenau. 
Jedes Web-Projekt hat ne eigene Jail bekommen, mit eigener interner IP, der Reverse-Proxy ist weiterhin ein abgespeckter NGINX mit Let's Encrypt Zertifikaten (dehydrated).
Musste eh mal dehydrated testen, weil da so ne Anfrage reingekommen ist.

Jedenfalls ist der Microserver daheim jetzt weniger ausgelastet (gerade das PHP zeugs frisst doch einiges an RAM) und kuemmert sich nur noch um die Backups und ums Monitoring.

Mal schauen, wie lange die x3690x5 noch rennt, wir haben einige davon gebraucht gekauft, erfahrungsgemaess sind die Kisten aber sehr robust und halten lange.
Sicherheitshalber habe ich die Platten erneuert und natuerlich redundant ausgelegt (ZFS - eh klar) und eine Kiste ist als cold-standby im Lager.

so long...
