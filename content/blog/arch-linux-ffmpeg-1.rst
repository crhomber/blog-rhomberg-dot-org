Arch Linux - ffmpeg Problem
####################################
:date: 2018-05-29 20:50
:slug: arch-linux-ffmpeg
:tags: Arch Linux, Linux, ffmpeg, pacman
:keywords: Video, ffmpeg

Aktuell gibts unter Arch Linux Probleme beim Updaten, weil Abhaenigkeiten von ffmpeg kaputt sind.

Fehler:

.. code-block:: bash

	ffmpeg2.8: installing x265 (2.8-1) breaks dependency 'libx265.so=151-64

Loesung:

.. code-block:: bash

	sudo pacman -Sy vlc
	sudo pacman -R ffmpeg2.8
	sudo pacman -Syu

Das war's!
