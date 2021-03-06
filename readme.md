# :scroll: ubuntu-scripts readme

A few simple scripts to setup a basic dev environment on Ubuntu.

## status - stable

Tested on Ubuntu 18.04

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

[![Donate](https://img.shields.io/badge/donate-paypal-blue.svg)](https://paypal.me/mrseanryan)

## features

Installs the following:

- docker and docker-compose
- ftp server to easily transfer files
- git and git lfs
- git aliases and credential caching
- graphviz
- network tools like: curl, ifconfig
- npm, yarn
- nvm, node 8 (latest)
- Visual Code

_note: probably NOT suitable for a production box!_

## usage

The 'clever' way:

```
sudo apt install curl

curl -o- https://raw.githubusercontent.com/mrseanryan/ubuntu-scripts/master/install.sh | bash
```

_note: if you also want docker installed, instead use `install-with-docker.sh`_

OR if that fails:

```
sudo apt-get update

sudo apt install git

git clone https://github.com/mrseanryan/ubuntu-scripts.git

cd ubuntu-scripts

./go.sh
```

_note: if you also want docker installed, instead use `go.sh --docker`_

## extras

To install XRDP to allow Remote Desktop from Windows:

```
cd ubuntu-scripts
./extra-install-xrdp.sh
```

## known issues

### Visual Code is not installed

The Visual Code install script involves some prompts which fail to show when installed via `curl`.

To fix, run the script:

```
cd ubuntu-scripts
./install-visual-code.sh
```

### docker-compose version is hard-coded in script

The scripts will install the latest `docker` but not the latest `docker-compose`.

You may need to edit the version of `docker-compose` in this script, and then run it again:

`install-docker-compose.sh`

## authors

Original work by Sean Ryan - mr.sean.ryan(at gmail.com)

## licence = MIT

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
