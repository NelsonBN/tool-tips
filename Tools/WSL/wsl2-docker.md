# Installation Docker on WSL



## Index
- [.. Tools](/Tools/README.md)


## Install the requisites:

##### Update the system:
``` bash
sudo apt update && sudo apt upgrade -y
```

##### Remove the old docker:
``` bash
sudo apt remove docker docker.io containerd runc
```

##### Install dependencies:
```bash
sudo apt-get install apt-transport-https ca-certificates curl gnupg lsb-release -y
```

##### Add the Docker repository:
```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```
```bash
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

##### Instale o Docker Engine:
```bash
sudo apt-get update -y && sudo apt-get install docker-ce docker-ce-cli containerd.io -y
```

##### Add permissions to current user to run docker:
```bash
sudo usermod -aG docker $USER
```

##### Install docker compose:
```bash
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose && sudo chmod +x /usr/local/bin/docker-compose && sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
```

##### Start Docker:
```bash
sudo service docker start
```



## Configure the Docker

### Login to Docker
```bash
docker login
```

### Auto start Docker when it enters the linux distribution:
Allow start Docker without password.
```bash
sudo visudo
```

Add the following line to the bottom
```text
{username} ALL=(ALL) NOPASSWD: /usr/bin/dockerd
```
Overwrite the ***{username}*** with your username.

Go to the user's home directory and edit the file .bashrc and add the following lines to the bottom
```bash
# Start Docker daemon automatically when logging in if not running.
RUNNING=`ps aux | grep dockerd | grep -v grep`
if [ -z "$RUNNING" ]; then
    sudo dockerd > /dev/null 2>&1 &
    disown
fi
```

[Original document](https://blog.nillsf.com/index.php/2020/06/29/how-to-automatically-start-the-docker-daemon-on-wsl2/)