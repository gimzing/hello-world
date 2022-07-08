# Setup

## WSL2 and Ubuntu

Open Powershell as Administrator

`wsl --install`

Download Ubuntu from Microsoft Store and open it which starts the installation process

Check that you're running WSL2

`wsl -l -v`

If it says 2 then you are running WSL2

Download Windows Terminal and set Ubuntu (the one with the Linux symbol) as the default

`sudo apt-get update`

`sudo apt-get upgrade`

## VS Code

Download [Visual Studio Code](https://code.visualstudio.com) in Windows

Install the "Remote - WSL" VS Code Extension

## Go

Get the latest version of [Go](https://go.dev/dl/)

```
wget https://dl.google.com/go/go1.18.linux-amd64.tar.gz
sudo tar -xvf go1.18.linux-amd64.tar.gz
sudo mv go /usr/local
```

```
cd ~
explorer.exe .
```

Add the following three lines to the bottom of your .bashrc file and save it

```
export GOROOT=/usr/local/go
export GOPATH=$HOME/go
export PATH=$GOPATH/bin:$GOROOT/bin:$PATH
```

Check that Go has installed by checking the version

`go version`

## Git

`git config --global credential.helper store`

`git config --global user.email EMAIL`

`git config --global user.name USER_NAME`

Generate a personal access token from github and use it as the password when you do a push and it prompts you

# Linux Mint

`sudo apt-get update`

`sudo apt-get upgrade`

## Git

`sudo apt-get install git`

`git config --global credential.helper store`

`git config --global user.email EMAIL`

`git config --global user.name USER_NAME`

## VS Code

Download ubuntu/debian file from website

`sudo apt install ./code_1.68.1-1655263094_amd64.deb`

Install Remote Containers extension and open platform-frontend in a new container with Nodejs 16 and Typescript

## Go

`sudo apt-get install build-essential`

Same as above

## Docker Engine

https://docs.docker.com/engine/install/ubuntu/

`sudo apt-get update`

```
sudo apt-get install \
  ca-certificates \
  curl \
  gnupg \
  lsb-release
```

`sudo mkdir -p /etc/apt/keyrings`

`curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gp`
 
 ```
 echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  focal stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

`sudo apt-get update`

`sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin`

`sudo groupadd docker`

`sudo usermod -aG docker $USER`

`newgrp docker`

## Postgres via Docker backend-tools/postgres
```
cd backend-tools/postgres
mkdir data
mkdir pgadmin
chmod 777 -R data
chmod 777 -R pgadmin
```
`docker-compose up`

## Firebase

`curl -sL https://firebase.tools | bash`

Then in firebase folder in platform-backend: `firebase emulators:start`

## Minikube

`curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube_latest_amd64.deb`

`sudo dpkg -i minikube_latest_amd64.deb`

`minikube start`

## Kubectl

https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/#install-using-native-package-management/

`sudo apt-get install apt-transport-https ca-certificates gnupg`

`echo "deb [signed-by=/usr/share/keyrings/cloud.google.gpg] https://packages.cloud.google.com/apt cloud-sdk main" | sudo tee -a /etc/apt/sources.list.d/google-cloud-sdk.list`

`curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key --keyring /usr/share/keyrings/cloud.google.gpg add -`

`sudo apt-get update && sudo apt-get install google-cloud-cli`

`kubectl`

`sudo apt-get update`

`sudo apt-get install -y apt-transport-https ca-certificates curl`

`sudo curl -fsSLo /usr/share/keyrings/kubernetes-archive-keyring.gpg https://packages.cloud.google.com/apt/doc/apt-key.gpg`

`echo "deb [signed-by=/usr/share/keyrings/kubernetes-archive-keyring.gpg] https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee /etc/apt/sources.list.d/kubernetes.list`

`sudo apt-get update`

`sudo apt-get install -y kubectl`

`kubectl version`
