# Solve space issue

It is known that WSL 2 has a caracteristic that it does not free the space even after recovering some space within WSL distribution. So this will consume space on the host machine that is not being used. So we need to solve this issue manually.
This manual was created based on `Ubuntu 20.04` and `WSL 2`.



## Index
- [.. WSL 2](/Tools/WSL/wsl2.md)
- [Tips to free up space](#tips-free-up-space)
  - [Free up space used by docker](#free-up-space-by-docker)
    - [Free up spaces used by Docker Logs](#free-up-spaces-used-by-docker-logs)
  - [Analyse the space used by distribution](#analyse-the-space-used-by-distribution)
- [Compact the WSL distribution](#compact-the-wsl-distribution)



## Tips to free up space <a name="tips-free-up-space"></a>

### Free up space used by docker <a name="free-up-space-by-docker"></a>

One of the main reason we use WSL is to use docker. Se we end up consuming many spaces in downloading images, volumes, containers, etc. For our tests.

We can check the space used by docker with the following command:

```bash
docker system df

# Only volumes
docker system df -v
```

Can do is to remove all we dot not need anymore. To do this we can use the following commands:

```bash
docker system prune -a --volumes
```
> This will remove all unused containers, networks, and images. By default, the prune command does not remove volumes to prevent data loss. But we can use the `--volumes` flag to remove all unused volumes.

Or remove individually:

```bash
# Remove all unused containers
docker container prune

# Remove all unused networks
docker network prune

# Remove all unused images
docker image prune

# Remove all unused volumes
docker volume prune
```

#### Free up spaces used by Docker Logs <a name="free-up-spaces-used-by-docker-logs"></a>

```bash
truncate -s 0 /var/lib/docker/containers/**/*-json.log
```



### Analyse the space used by distribution <a name="analyse-the-space-used-by-distribution"></a>

The following command will analyse the space used by the distribution and show the top 10 biggest folders:
```bash
du -h <Folder to analyse> | sort -rh | head -n 10

# Example for the root folder
du -h / | sort -rh | head -n 10
```

Normally the WSL distribution has the host machine's disk mounted on `/mnt`
You can prevent the previous command to analyse the host machine's disk by using the following command:

```bash
du -h / --exclude /mnt | sort -rh | head -n 10
```



## Compact the WSL distribution <a name="compact-the-wsl-distribution"></a>

First stop the WSL
```bash
wsl --shutdown
```

Then find the disk of the distribution
```bash
cd C:\Users\%PROFILE%\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu20.04onWindows_79rhkp1fndgsc\LocalState\
```

You will see a file called `ext4.vhdx` that is the disk of the distribution.
You will be able to verify that even after freeing up space within the distribution, the disk is still large.

To compact the disk we can use the following command:

```bash
optimize-vhd -Path .\ext4.vhdx -Mode full
```

Sometimes the previous command may not be available.
In this case we can use the following steps:

First a file script. I am using the vscode but you can use any text editor.

```bash
code ./disk-compression.script
```

Paste the following script and save it:
```bash
select vdisk file="C:\Users\%username%\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu20.04onWindows_79rhkp1fndgsc\LocalState\ext4.vhdx"
attach vdisk readonly
compact vdisk
detach vdisk
```

Then run the script as administrator:
```bash
diskpart /s ./disk-compression.script
```
> IMPORTANT: Make sure the file `ext4.vhdx` is not used during this process so as not to corrupt the disk.
