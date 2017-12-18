Xorg emulation of 3rd mouse-button
##################################
:date: 2011-06-03 08:04
:author: Christian
:tags: Debian, Fedora, Linux, Mouse, Window-Manager, X, Xorg
:slug: xorg-emulation-of-3rd-button

Yesterday I switched from Debian Squeeze to Fedora 15 (XFCE-spin).

The first thing i recognized was that the 3rd mouse-button is not
emulated anymore, since I'm using the Logitech Marble Mouse (a trackball
with 2 main-buttons) I really need to have some 3rd mouse-button
emulated.

A quick search through the web gave me `this
solution <http://forums.fedoraforum.org/showthread.php?t=257047>`_:

Create a file called "99-mouse-midbuttonemulation.conf" in directory
"/etc/X11/xorg.conf.d" with the following content:

    Section "InputClass"
     Identifier "middle button emulation class"
     MatchIsPointer "on"
     Option "Emulate3Buttons" "on"
     EndSection

Afterwords you just need to restart Xorg.
