# Installation Docker on WSL



### Install the requisites:

**Update the system:**
``` bash
sudo apt update && sudo apt upgrade -y
```

**Remove the old docker:**
``` bash
sudo apt remove docker docker.io containerd runc
```

**Install dependencies:**
```bash
sudo apt-get install apt-transport-https ca-certificates curl gnupg lsb-release -y
```

**Add the Docker repository:**
```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```
```bash
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

**Instale o Docker Engine:**
```bash
sudo apt-get update -y && sudo apt-get install docker-ce docker-ce-cli containerd.io -y
```

**Add permissions to current user to run docker:**
```bash
sudo usermod -aG docker $USER
```

**install docker compose:**
```bash
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose && sudo chmod +x /usr/local/bin/docker-compose && sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
```

**Start Docker:**
```bash
sudo service docker start
```



## Configure the Docker

### Login to Docker
```bash
docker login
```