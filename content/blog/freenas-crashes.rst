FreeNAS crashes
###############
:date: 2011-06-07 19:22
:author: Christian
:tags: CIFS, FreeBSD, FreeNAS, Problem, ZFS
:slug: freenas-crashes

First of all: I love `FreeNAS <http://www.freenas.org>`_! ;-)

But one customer had a weird problem, sometimes the FreeNAS Host
(running on VMware ESXi) crashed and there was no error message at the
console.

Today  I `found <http://support.freenas.org/ticket/368>`_ a
solution/workaround for this
problem.\ `|image0| <http://www.sysadmin.cc/wp-content/uploads/2011/06/Screenshot-FreeNAS-8.0-RELEASE-amd64.png>`_

Just disable "Send files with sendfile(2)" and the problem is solved.

Never the less you should make sure to use the 64-bit Version and assign
enough memory to the machine (`more
information <http://lists.freebsd.org/pipermail/freebsd-fs/2011-February/010647.html>`_).

.. |image0| image:: http://www.sysadmin.cc/wp-content/uploads/2011/06/Screenshot-FreeNAS-8.0-RELEASE-amd64.png
