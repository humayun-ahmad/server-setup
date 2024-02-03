
Install WordOps
===================================================
3.1 Add the swap to the server
---------------------------------------------------
```
sudo fallocate -l 1G /swapfile
sudo dd if=/dev/zero of=/swapfile bs=1024 count=1048576
sudo chmod 600 /swapfile
sudo mkswap /swapfile
sudo swapon /swapfile
echo '/swapfile swap swap defaults 0 0' | sudo tee -a /etc/fstab
```
---------------------------------------------------
3.2 Update the VPS
---------------------------------------------------
```
sudo apt update
sudo apt upgrade
reboot
```
---------------------------------------------------
3.3 Install WordOps
---------------------------------------------------
```
sudo apt install unzip
sudo apt install zip
```
-------------------------
```
wget -qO wo wops.cc && sudo bash wo
```
---------------------------------------------------
```
wo stack install
```
---------------------------------------------------
=====================================
```
WordOps Log off
wo debug --all=off
```
