HP xw6600 Workstation - nouveau fan control
##############################################
:date: 2018-02-20 13:30
:slug: hp-xw6600-workstation-3
:tags: Hardware, HP, Workstation, Luefter, NVIDIA, nouveau

Ha!

So klappts auch mit der automatischen Lueftersteuerung.


.. code-block:: bash

	cat /etc/udev/rules.d/50-nouveau-hwmon.rules
        ACTION=="add", SUBSYSTEM=="hwmon", DRIVERS=="nouveau", ATTR{pwm1_enable}="2"

