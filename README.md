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
