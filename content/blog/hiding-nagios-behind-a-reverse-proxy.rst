Hiding Nagios behind a reverse proxy
####################################
:date: 2011-08-04 08:38
:author: Christian
:tags: Apache, Nagios, Proxy, Reverse
:slug: hiding-nagios-behind-a-reverse-proxy

If you want to hide your Nagios Web interface behind a reverse proxy you
can use this config (for Apache 2):

    ProxyRequests Off
     ProxyPass /nagios3 http://nagiosip/nagios3
     ProxyPassReverse /nagios3 http://nagiosip/nagios3
     ProxyPass /cgi-bin/nagios3 http://nagiosip/cgi-bin/nagios3
     ProxyPassReverse /cgi-bin/nagios3 http://nagiosip/cgi-bin/nagios3

It is important to include the /cgi-bin/nagios3 directory, otherwise
only the static part of Nagios will work.
