Drupal 7 behind a reverse proxy
###############################
:date: 2011-07-25 10:42
:author: Christian
:tags: 7, Drupal, reverse proxy
:slug: drupal-7-behind-a-reverse-proxy

It is no problem to run Drupal 7 behind a reverse  proxy.

You just need to set the base\_url (without a trailing slash):

     $base\_url = 'http://example.com/drupal';

 
