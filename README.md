# DevOnWindows

Some notes about setting up development environment on Windows 10.

## Git for Windows (git bash)

### How to get python to work properly in git bash
Python requires a win32 console to run, so you need to launch it with winpty, open /etc/profile.d/aliases.sh if you don't see your python executable here, just append it at the end.
```
for name in node ipython php php5 psql python2.7 python
```

You can significantly speed up Git on Windows by running three commands to set some config options:
```
git config --global core.preloadindex true
git config --global core.fscache true
git config --global gc.auto 256
```

Notes:
- core.preloadindex does filesystem operations in parallel to hide latency (update: enabled by default in Git 2.1)
- core.fscache fixes UAC issues so you don't need to run Git as administrator (update: enabled by default in Git for Windows 2.8)
- gc.auto minimizes the number of files in .git/
