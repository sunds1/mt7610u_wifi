# mt7610u_wifi
Ubuntu 14.10 w/ Kernel 3.16.0-29-generic compatible driver for ASUS Dual-Band Wireless-AC600 Wi-Fi Adapter (USB-AC51)
It should work for later kernels as well. If it stops I will likely end up fixing it or if somoene submits an issue to remind/notify me.
I didn't clean up any of the warnings and I pretty much did the quickest hacks to get this functioning.

sudo apt-get update
sudo apt-get install linux-headers-generic build-essential git
git clone https://github.com/likwidoxigen/mt7610u_wifi.git
cd ~/rtl8812au
make
sudo make install

At this point I did 
sudo modprobe -v mt7650u_sta
iwconfig

I saw the RA0 adapter but I could only configure it manually not in network-mangager. 

Out of frustration I did the "windows fix" and rebooted the thing. That did the trick.
It all popped up in network manager like it was supposed to and I could connect like a boss.



References:
https://wikidevi.com/wiki/ASUS_USB-AC51
ubuntuforums.org/showthread.php?t=2228244&page=1
http://ubuntuforums.org/showthread.php?t=1659919
http://ubuntuforums.org/showthread.php?t=2171240