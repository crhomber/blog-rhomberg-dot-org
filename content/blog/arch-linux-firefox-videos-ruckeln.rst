Arch Linux Videos in Firefox ruckeln
####################################
:date: 2016-08-02 19:50
:slug: arch-linux-firefox-videos-ruckeln
:tags: Arch Linux, Linux, X11, Firefox, Intel
:keywords: Video, Firefox, Ruckel, 

Ich hab seit einiger Zeit das Problem, dass Videos im Fullscreen unter Firefox ruckeln. In Chromium laufen sie jedoch ohne Probleme...

Abhilfe schafft das Deinstallieren von xf86-video-intel:

.. code-block:: bash

	sudo pacman -R xf86-video-intel
