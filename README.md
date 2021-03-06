############################################

OUT OF DATE

USE OFFICIAL NODE CONFIGURATION REPO

https://gitlab.com/flarenetwork/node-config

############################################



OUTDATED
-------------------------------------------
# Flare Node Install Script
Flare Networks Node Installation Tools

This script will prepare your Ubuntu environment for the official Flare Networks node.

**Note:** Official Flare Networks Node Git Repo can be found here: https://gitlab.com/flarenetwork/flare

**Requirements:**
 - Hardware per Flare node: 64-bit architecture, 2 GHz or faster CPU, 4 GB RAM, 20 GB hard disk.
 - OS: Ubuntu >= 18.04 (install script tested on Ubuntu 20.04.2).

**To use the script:**

Download install script\
`wget http://cdn.ftso.com.au/public/flarenode/install-latest.sh`

Set Script Permissions\
`sudo chmod +x install-latest.sh`

Run The Script Using Sudo\
`sudo bash install-latest.sh`

All packages will install and allow you to run the `./coston` script within the Flare folder. 

Don't forget to run `source ~/.profile` after running the install script and before starting your Flare Node.

---------------------------------------

The script runs the following commands for you:

Update Apt-get \
`apt-get update`

Install Golang 1.15\
`wget https://golang.org/dl/go1.15.linux-amd64.tar.gz`\
`sudo rm -rf /usr/local/go && sudo tar -C /usr/local -xzf go1.15.linux-amd64.tar.gz`\
`sudo rm go1.15.linux-amd64.tar.gz`

Update Bash Profile with Envrionment Variables\
`echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.profile`\
`echo 'export GOPATH=$HOME/go' >> ~/.profile`\
`echo 'export XRP_APIs="https://xrpl.flare.network:443,https://xrpl-1.flare.network:443,https://xrplcluster.com"' >> ~/.profile`

Source Bash Profile\
`source ~/.profile`

Install NodeJS\
`curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash -`
`sudo apt-get install -y nodejs`

Install Yarn\
`npm install --global yarn`

Install JQ\
`sudo apt-get install -y jq`

Install Build Tools\
`sudo apt update && sudo apt -y install curl && sudo apt -y install gcc`

Clone Flare Repo\
`git clone https://gitlab.com/flarenetwork/flare`

Set Flare Directory Permissions\
`sudo chown $USER flare`

Install NPM packages in Flare Node Directory\
`cd flare`\
`npm install`

Start Coston\
`./coston.sh`

# Postman

Download Postman\
https://www.postman.com/downloads/

**Collection**\
https://raw.githubusercontent.com/ava-labs/avalanche-postman-collection/master/Avalanche.postman_collection.json

**Environment**\
https://raw.githubusercontent.com/ava-labs/avalanche-postman-collection/master/Example-Avalanche-Environment.postman_environment.json

(Source: https://github.com/ava-labs/avalanche-postman-collection)

# Virtual Box

Download Virtualbox\
https://www.virtualbox.org/wiki/Downloads

Download Ubuntu Server ISO\
https://releases.ubuntu.com/20.04/
