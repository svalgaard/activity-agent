Activity Agent (Mac)
====================

Do you sometimes wonder how often your mac is unlocked?
Look no further

Requirements
------------

Python 3.6+ and the pyobjc package.

If you use the default Apple Python 3.x, you can install pyobjc using this command:
```
/usr/bin/python3 -m pip install --user pyobjc
```

If you are using MacPorts, pyobjc can be installed using this command:
```
sudo port install py38-pyobjc
````

Installation
------------

```
chmod a+x ./activity-monitor
./activity-monitor install
```

This asks launchctl to run activity-monitor once every 60 seconds.
Check that log files start to appear in `~/.activity-monitor` within the
next minute.

To uninstall, run `./activity-monitor uninstall`.


Get logs
--------

```
./activity-monitor logs
...
Sat Dec 05 2020 19:05:35  - Active
Sat Dec 05 2020 19:27:07  - Locked

Sun Dec 06 2020 09:55:03  - Active
Sun Dec 06 2020 09:59:07  - Locked
Sun Dec 06 2020 13:15:57  - Active
```
