Activity Agent (Mac)
====================

Do you sometimes wonder how often your mac is unlocked?
Look no further

Requirements
------------

Python 3.6+ and the pyobjc package.

If pyobjc has not been installed, you get an error about
a missing Quartz import:

```
$ ./activity-agent install
Please install pyobjc to use the Quartz module:
/Applications/Xcode.app/Contents/Developer/usr/bin/python3 -m pip install --user pyobjc
port install py39-pyobjc
brew install pyobjc
```

Use one of the three suggested commands, depending on whether you use
the default Apple Python 3.x, MacPorts, or Homebrew.


Installation
------------

```
chmod a+x ./activity-agent
./activity-agent install
```

This asks launchctl to run activity-agent once every 60 seconds.
Check that log files start to appear in `~/.activity-agent` within the
next minute.

To uninstall, run `./activity-agent uninstall`.


Get logs
--------

```
./activity-agent logs
...
Sat Dec 05 2020 19:05:35  - Active
Sat Dec 05 2020 19:27:07  - Locked

Sun Dec 06 2020 09:55:03  - Active
Sun Dec 06 2020 09:59:07  - Locked
Sun Dec 06 2020 13:15:57  - Active
```
