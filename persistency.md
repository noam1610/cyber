# Persistence methods

Among the well known persistency methods we have:
1. Run and RunOnce registries

In this article we will discuss each of them.

## Run and RunOnce

There are several registry that are read at reboot. These registry allow programs that were registered into to be executed automatically at reboot. This mechanism is not obviously malicious. Let's say someone use a lot the windows calculator and would like it to be to loaded each time the computer restart. It is possible thanks to these registries. You just need to add a (subkey, value):
'''
my_favorite_software C:\windows\system32\calc32.exe
'''

All of these registries are available in 32bit:
* HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\RunOnce
* HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\RunOnceEx
* HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Runonce
* HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\RunonceEx

All of these registries are available in 32bit:
* HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Windows\CurrentVersion\RunOnce
* HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Windows\CurrentVersion\RunOnceEx
* HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Windows\CurrentVersion\Runonce
* HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Windows\CurrentVersion\RunonceEx
