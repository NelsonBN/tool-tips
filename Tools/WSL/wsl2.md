# WSL 2



## Index
- [.. Tools](/Tools/README.md)
- [Install docker in WSL](/Tools/WSL/wsl2-docker.md)
- [Reclaim space used by WSL](/Tools/WSL/wsl2-reclaim-space-used.md)



## Requirements
* Windows 10 version 2004 (Build 19041 and higher) or Windows 11
* 4 GB of RAM
* Virtual machine platform enabled



## Installation WSL 2
[Official documentation](https://docs.microsoft.com/en-us/windows/wsl/install)
```bash
wsl --install
```

### Enable the Windows Subsystem for Linux and Virtual Machine feature
First, run [Windows terminal](/Tools/WindowsTerminal.md) As Administrator
```bash
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

### Update the linux kernel
[Official documentation](https://docs.microsoft.com/en-gb/windows/wsl/install-manual#step-4---download-the-linux-kernel-update-package)

### Set WSL 2 as your default version
```bash
wsl --set-default-version 2
```
> Restart your machine to complete the WSL install and update to WSL 2.



## Installation linux distribution

### Check available linux distributions to donwload
```bash
wsl --list --online
```
or
```bash
wsl -l -o
```

### Check linux distribution installed in your machine
```bash
wsl --list
```
or
```bash
wsl -l
```
**Verbose mode**
```bash
wsl -l -v
```

### Install new linux distribution
```bash
wsl --install -d <Distribution Name>
```
*Exmaple:*
```bash
wsl --install -d Ubuntu-20.04
```

### Set the WSL version for a linux distribution
```bash
wsl --set-version <distribution name> 2
```
*Exmaple:*
```bash
wsl --set-version Ubuntu-20.04 2
```

### Check the linux distribution running in your machine
```bash
wsl --list --running
```

### Set default Linux distribution
```bash
wsl -s <DistributionName>
```
or
```bash
wsl --setdefault <DistributionName>
```
*Exmaple:*
```bash
wsl --setdefault Ubuntu-20.04
```



## Set resources limit used by the WSL
### Defaul configuration
* 100% of the available disk space
* All CPU cores
* 80% of the RAM
* 25% of the available SWAP

Create a file with name `.wslconfig` in user home directory `C:\Users\<UserName>\.wslconfig`
*Exmaple:*
```txt
[wsl2]
memory=4GB
processors=4
swap=1GB
```
[Official documentation](https://docs.microsoft.com/en-us/windows/wsl/wsl-config#wsl-2-settings)

> To assume the new settings, you have to turn off all linux distributions. `wsl --shutdown` and next start a linux distribution.



## Unregister a Linux distribution
```bash
wsl --unregister <DistributionName>
```
*Exmaple:*
```bash
wsl --unregister Ubuntu-20.04
```



## Related documentation
* [Install docker](/Tools/WSL/wsl2-docker.md)