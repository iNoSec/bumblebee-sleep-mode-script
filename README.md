# bumblebee-sleep-mode-script
A script for creating a service because bumblebee stop nvidia working after sleep mode


First of all make sure you have write access to /sys/bus/pci/rescan by doing :
echo 1 > /sys/bus/pci/rescan

if you dont :
su
Type your root password
chmod 777 /sys/bus/pci/rescan

So when you can write to /sys/bus/pci/rescan 
cp gpu-fix /usr/local/bin
cp gpu-fix.service /etc/systemd/system/
systemctl enable gpu-fix.service 

You have to type the sudo password 2 times and two services are created to make it work
Done!

Tested on parrotOS, debian stretch, ubuntu 17.X
