# ubuntu-setup
Ubuntu machine setup for web development

## Essential
You need compiling C at sometimes and you definitely need git
```
sudo apt install git build-essential
```
## General Utils
Clipboard in terminal
```
sudo apt install xclip
```

## ZSH
```
sudo apt install zsh
```
and the `.oh my zsh` from official site
https://ohmyz.sh/#install
```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## Node.js
Should be from node source
https://github.com/nodesource/distributions/blob/master/README.md
```
curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -
sudo apt-get install -y nodejs
```
and yarn should be from the official sites
https://classic.yarnpkg.com/en/docs/install/#debian-stable

## Docker
from the official site
https://docs.docker.com/engine/install/ubuntu/
```
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo apt-key fingerprint 0EBFCD88
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
sudo docker run hello-world
sudo usermod -aG docker <your-user> // solve permission problem
newgrp docker // force re-evaluate to login to the new group
```

compose is merely download binary and move to the binary dir
```
sudo curl -L https://github.com/docker/compose/releases/download/1.27.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

## Gimp
snap is default to ubuntu and very convenient
```
sudo snap install gimp
```

## Font
Copy to `/usr/local/share/fonts` then force the cache
```
fc-cache -fv
```
