uWSGI - the way to go...
########################
:date: 2013-04-04 06:58
:author: Christian
:tags: Django, Perfany, Python, SaaS, uWSGI
:slug: uwsgi-the-way-to-go

Currently we at `Perfany <http://www.perfany.at>`_ are working on the
migration from Apache 22 to `uWSGI <http://projects.unbit.it/uwsgi/>`_.

Since we need to host several - let's say - vHosts on a few machines
we've been looking for a accurate solution to provide performance and
stability  to our customers. It seems uWSGI and
`nginx <http://nginx.org/>`_ will fit very well.
