WhatsApp - WTF?!1
############################
:date: 2017-06-14 19:04
:slug: whatsapp-wtf-1
:tags: whatsapp
:lang: de

Ok, Fefe hat mich informiert, ich gebe es zu,
der `Tweet <https://twitter.com/mulander/status/874370124932943874>`_ musste ueberprueft werden - und siehe da:

.. code-block:: bash

        ==> /var/log/nginx/rhomberg.org-access.log <==
        192.168.1.149 - - [14/Jun/2017:19:02:28 +0200] "GET /shit/this/is/r HTTP/1.1" 404 169 "-" "WhatsApp/2.17.223 A"
        192.168.1.149 - - [14/Jun/2017:19:02:29 +0200] "GET /shit/this/is/re HTTP/1.1" 404 169 "-" "WhatsApp/2.17.223 A"
        192.168.1.149 - - [14/Jun/2017:19:02:29 +0200] "GET /shit/this/is/res HTTP/1.1" 404 169 "-" "WhatsApp/2.17.223 A"
        192.168.1.149 - - [14/Jun/2017:19:02:30 +0200] "GET /shit/this/is/resl HTTP/1.1" 404 169 "-" "WhatsApp/2.17.223 A"
        192.168.1.149 - - [14/Jun/2017:19:02:31 +0200] "GET /shit/this/is/resa HTTP/1.1" 404 169 "-" "WhatsApp/2.17.223 A"
        180.97.106.37 - - [14/Jun/2017:19:02:32 +0200] "HEAD http://180.163.113.82/check_proxy HTTP/1.1" 400 0 "-" "-"
        192.168.1.149 - - [14/Jun/2017:19:02:34 +0200] "GET /shit/this/is/rea HTTP/1.1" 404 169 "-" "WhatsApp/2.17.223 A"
        192.168.1.149 - - [14/Jun/2017:19:02:34 +0200] "GET /shit/this/is/real HTTP/1.1" 404 169 "-" "WhatsApp/2.17.223 A"
        192.168.1.149 - - [14/Jun/2017:19:02:36 +0200] "GET /shit/this/is/real! HTTP/1.1" 404 169 "-" "WhatsApp/2.17.223 A"
        192.168.1.149 - - [14/Jun/2017:19:02:36 +0200] "GET /shit/this/is/real!! HTTP/1.1" 404 169 "-" "WhatsApp/2.17.223 A"
        192.168.1.149 - - [14/Jun/2017:19:02:36 +0200] "GET /shit/this/is/real!!! HTTP/1.1" 404 169 "-" "WhatsApp/2.17.223 A"
        192.168.1.149 - - [14/Jun/2017:19:02:37 +0200] "GET /shit/this/is/real!!!! HTTP/1.1" 404 169 "-" "WhatsApp/2.17.223 A"
        192.168.1.149 - - [14/Jun/2017:19:02:37 +0200] "GET /shit/this/is/real!!!!! HTTP/1.1" 404 169 "-" "WhatsApp/2.17.223 A"
        192.168.1.149 - - [14/Jun/2017:19:02:37 +0200] "GET /shit/this/is/real!!!!!! HTTP/1.1" 404 169 "-" "WhatsApp/2.17.223 A"
        192.168.1.149 - - [14/Jun/2017:19:02:37 +0200] "GET /shit/this/is/real!!!!!!! HTTP/1.1" 404 169 "-" "WhatsApp/2.17.223 A"
        192.168.1.149 - - [14/Jun/2017:19:02:37 +0200] "GET /shit/this/is/real!!!!!!!! HTTP/1.1" 404 169 "-" "WhatsApp/2.17.223 A"
        192.168.1.149 - - [14/Jun/2017:19:02:37 +0200] "GET /shit/this/is/real!!!!!!!!! HTTP/1.1" 404 169 "-" "WhatsApp/2.17.223 A"
        192.168.1.149 - - [14/Jun/2017:19:02:37 +0200] "GET /shit/this/is/real!!!!!!!!!! HTTP/1.1" 404 169 "-" "WhatsApp/2.17.223 A"
        192.168.1.149 - - [14/Jun/2017:19:02:37 +0200] "GET /shit/this/is/real!!!!!!!!!!! HTTP/1.1" 404 169 "-" "WhatsApp/2.17.223 A"
        192.168.1.149 - - [14/Jun/2017:19:02:38 +0200] "GET /shit/this/is/real!!!!!!!!!!!! HTTP/1.1" 404 169 "-" "WhatsApp/2.17.223 A"
        192.168.1.149 - - [14/Jun/2017:19:02:38 +0200] "GET /shit/this/is/real!!!!!!!!!!!!! HTTP/1.1" 404 169 "-" "WhatsApp/2.17.223 A"
        192.168.1.149 - - [14/Jun/2017:19:02:38 +0200] "GET /shit/this/is/real!!!!!!!!!!!!!! HTTP/1.1" 404 169 "-" "WhatsApp/2.17.223 A"



Nur wie soll es anders gehen? Ich mein die user wollen eine Vorschau der versendeten Links....
