Activity Agent (Mac)
====================

Do you sometimes wonder how often you use your mac?
Look no further

Requirements
------------

Python 3.8 or newer. Except for the `logs` subcommand, all subcommands require the `pyobjc` package, which provides the
macOS Quartz module.

If pyobjc is missing, commands that need Quartz print installation
suggestions, including:

```
$ ./activity-agent install
Please install pyobjc to use the Quartz module:
<the Python executable running activity-agent> -m pip install --user pyobjc
port install py<major><minor>-pyobjc
brew install pyobjc
```

Use the appropriate command for your Python installation (Apple Python,
MacPorts, or Homebrew).


Installation
------------

```
chmod a+x ./activity-agent
./activity-agent install
```

This asks launchctl to run activity-agent once every 60 seconds.
Log files are written under `~/.activity-agent/logs-<hostname>/`, with a
new file for each day. Check that a log file appears within the next minute.

To uninstall, run `./activity-agent uninstall`.


Get logs
--------

By default, `logs` combines log files from all host-specific log directories
and shows the most recent 14 days:
```
./activity-agent logs
...
2020-12-05 19:05:35 - Active
2020-12-05 19:27:07 - Locked/off

2020-12-06 09:55:03 - Active
2020-12-06 09:59:07 - Locked/off
2020-12-06 13:15:57 - Active
```

Run `./activity-agent --help` to see the available options for customizing the
output.
