# DevOnWindows

Some notes about setting up development environment on Windows 10.

## Git for Windows (git bash)

### How to get python to work properly in git bash
Python requires a win32 console to run, so you need to launch it with winpty, open /etc/profile.d/aliases.sh if you don't see your python executable here, just append it at the end.
```
for name in node ipython php php5 psql python2.7 python
```
