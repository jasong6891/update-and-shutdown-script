#! /bin/bash

release_file=/etc/os-release

if grep -q "Ubuntu" $release_file || grep -q "Mint" $release_file
then
#run script
date 
sudo apt update && sudo apt dist-upgrade -y
sudo apt autoremove -y
shutdown
fi
