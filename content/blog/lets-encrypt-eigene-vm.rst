Let's Encrypt - in eigener VM
#############################
:date: 2015-12-07 22:10
:author: Christian
:tags: Let's Encrypt, HTTPS, Web, Mozilla, EFF
:slug: lets-encrypt-eigene-vm
:lang: de

Kaum ist `Let's Encrypt <https://letsencrypt.org/>`_ gestartet, gibt es schon erste Kritik bzgl. der Code-Qualitaet. 

Ich trau dem Code ja prinzipiell nicht, weiters bin ich nicht in der Lage das alles zu verstehen, also verwende ich Let's Encrypt in einer eigenen VM und kopiere die Zertifikate dann auch den eigentlichen Webserver (eigentlich ein Reverse-Proxy). Somit habe ich zumindest keine Software auf dem produktiven Server.

Die VM wird nur zum anfordern und revoken von Zertifikaten angeworfen, mal abwarten was die Profis meinen.
