---
layout: kba
title:  
date:   2024-01-20 00:00:00 -0800
description:
author: horacio 
image:  '/images/photo-5.jpeg'
tags:   [technology]
tags_color: '#477690'
---
# My favorite linux commands

## Hashing
- ### Get hash from string

```bash
echo -n dogswoof23221 | sha256sum
certutil -hashfile z:\desktop\lsr.exe SHA512
Get-FileHash -Path z:\desktop\lsr.exe -Algorithm SHA512
-hash multiple files
md5sum /*.*
```

## Stenography

```bash
binwalk Stego.jpg (Get list of files within image)
dd if=Stego\ 3.jpg bs=1 skip=559110 of=test.tiff (Extract file from image)
unzip -t Stego.jpg (unzip files from image)
steghide --extract -sf Stego.jpg
```

## Password Cracking
 - ### Mask

```bash
hashcat -a 3 passwords2.txt FLAG-HQNT-?d?d?d?d
```

 - ### Dictionary
```bash
hashcat -a 0 hash1.txt rockyou.txt --force
```

 - ### Hybrid
```bash
hashcat -a 6 example.dict ?d?d?d?d
hashcat -a 0 -o cracked.txt hashes.txt /usr/share/wordlists/sqlmap.txt -O
```

> https://crackstation.net/

## Log Analysis
 - ### Get unique IP addresses

```bash
tshark -r C:\Users\Horacio\Downloads\Exfil.pcap -T fields -e ip.dst | sort | uniq >> C:\Users\Horacio\Downloads\uniq.txt
```

 - ### Count lines

```bash
cat access_log.txt | grep robots.txt | wc -l
```

 - ### count files

```bash
ls -l | wc -l
```

## Wireless

```bash
iwconfig
ifconfig
lsusb
airmon-ng (gets list of interfaces)
airmon-ng stop mon1 (if multiple monitors are running)
airmon-ng start wlan0(interface)
airodump-ng mon0 (monitor)
airodump-ng --channel 1 --bssid [mac address] -w psk mon0
airmon start wlan0
airmon stop wlan0
besside-ng wlan0mon
besside-ng -R 'BSSID' wlan0mon
aireplay-ng --test wlan0mon
aireplay-ng -0 1 -e [BSSID] mon0

aircrack-ng -a2 -b 00:24:01:6b:4c:e8 -w rockyou.txt John-09.cap
aircrack-ng -a2 -b 00:24:01:6b:4c:e8 -w rockyou.txt John-09.cap
hashcat --stdout -a 3 SKY-BOOO-?d?d?d?d | aircrack-ng -w - -b C0:4A:00:80:76:E4 Cracking\ 3.cap

airodump-ng wlan0mon (Get list of ESSIDs)
aircrack-ng pcap.cap (info about capture file)
aircrack-ng -a2 -b B8:D9:4D:38:6C:94 -w rockyou.txt pcap.cap (crack password)
airodump-ng -c 6 --bssid B8:D9:4D:38:6C:94 -w ESSID wlan0mon (get handshake)
```

> https://hashcat.net/cap2hashcat/
>
> https://apackets.com/

## Play music from terminal

### What is mpg123 

> Real time MPEG 1.0/2.0/2.5 audio player/decoder for layers 1, 2 and 3 (most commonly MPEG 1.0 layer 3 aka MP3), as well as re-usable decoding and output libraries.

#### Install mpg123

```bash
sudo dnf -y install mpg123
```

#### Play song using find command

```bash
find ~/Music/Classic\ Rock/ -iname fleetwood*sara*.mp3 -print0 | xargs -0 mpg123
```

## Misc Commands
 - ### Kill program

```bash
ps -A | grep [name]
kill -9 [process id]
```

```
vi /etc/inittab (id:5=desktop, id:3=terminal)
yum update kernel
uname -a
```

 - ### Display OS banner

```bash
screenfetch
neofetch
```

 - ### install a program

```bash
yum --nogpgcheck localinstall packagename.arch.rpm
apt-get install packagename
```

 - ### Create menu applications (*.desktop)

```bash
/home/horacio/.local/share

 # Place apps here:
/usr/local/share
```
 - ### Anaconda

```bash
conda config --set auto_activate_base false
anaconda-navigator #(start anaconda gui)
```
