# Important registry

In this article we will deal with some important registry that can be sometime a bit difficult to deep in clearly.

Among them : 
	1. CurrentControlSet


## CurrentControlSet

A link to the [Microsoft](https://docs.microsoft.com/en-us/windows-hardware/drivers/install/hklm-system-currentcontrolset-control-registry-tree) documentation.

HKLM\SYSTEM\CurrentControlSet contains 3 main keys:
- Control
- services
- Enum

The CurrentControlSet key is not a phisical key. It is a symbolic link to *ControlSet00x* where x can be 1, 2 etc...
Generally *HKLM\System* contains ControlSet001, ControlSet002, CurrentControlSet.
In addition to these keys,  *HKLM\System*  contains *Select*. *Select* contains subkeys that will defined the role of each ControlSet00x.
	For example: 
- current : the current ControlSet00x to use (generally ControlSet001)
- default : the default ControlSet00x to use (generally ControlSet001)
- LastKnownGood : the ControlSet00x to use (generally ControlSet002) for backups.