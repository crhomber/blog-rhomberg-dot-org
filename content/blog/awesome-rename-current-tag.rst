Aktuellen TAG in Awesome umbenennen
######################################
:date: 2017-11-07 20:30
:slug: awesome-rename-current-tag
:tags: Awesome, WM, Tip
:lang: de

Seit einigen Jahren bin ich schon begeisterter User von `Awesome <https://awesomewm.org/>`_ und habe immer wieder versucht meinen Workflow besser unter Kontrolle zu haben.

Gerade als Admin von zig Systemen, weil man da nichts durcheinander bringen, bei mir sinds eigentlich immer um die 20 Terminal-Sessions (meistens in tmux oder screen) die ich irgendwie sortieren muss.
Gerade virtuelle Desktops, bei Awesome "Tags", helfen hier enorm, mit dem folgenden Snipped in der "global keys" section kann man mittels "Modkey (Windows-Taste) + Shift + F2" den aktuellen Tag umbenennen. Nach einem Neustart von Awesome ist dann alles wieder beim alten. Richtig schneidig!

.. code-block:: bash

	awful.key({ modkey, "Shift",  }, "F2",
              function ()
                    awful.prompt.run {
                      prompt       = "rename current tag: ",
                      text         = awful.tag.selected().name,
                      textbox      = awful.screen.focused().mypromptbox.widget,
                      exe_callback = function (s) awful.tag.selected().name = s end,
                  }
            end,
            {description = "rename tag", group = "awesome"}),

