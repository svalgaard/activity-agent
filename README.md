Activity Agent (Mac)
====================

Do you sometimes wonder how often your mac is unlocked?
Look no further

Requirements
------------

* Python 3.6+
* The pyobjc package. Using macports this can be installed using
  `port require py38-pyobjc` if not already available.

Installation
------------

```
chmod a+x ./activity-monitor
./activity-monitor install
```

This asks launchctl to run activity-monitor once every 60 seconds.
Check that log files start to appear in `~/.activity-monitor` within the
next minute.

To uninstall, run `activity-monitor uninstall`.


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
