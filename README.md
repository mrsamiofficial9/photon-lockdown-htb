![[photon-lockdown-htb.png]]
#### Categories: Hardware
#### Challenge Info: Device Firmware
#### Challenge Level: Very Easy

##          Challenge Description
##### * We've located the adversary's location and must now secure access to their Optical Network Terminal to disable their internet connection. Fortunately, we've obtained a copy of the device's firmware, which is suspected to contain hard coded credentials. Can you extract the password from it?

##           Solution
##### filename: Photon Lockdown.zip
##### password: hackthebox

```bash
unzip Photon\ Lockdown.zip  
```

```bash
cd ONT
```

```bash
ls -la
```
  
![./list-dir.png]
```bash
file *
```

![./file-command.png]
![./wikipedia.png]
```bash
sudo apt install squashfs-tools
```
#### *Read about unsquashs tool on man page*
![./man-unsquashfs.png]

```bash
unsquashfs -d file rootfs
```

```bash
cd file
```

```bash
ls -la
```
![./Pasted image 20240304015120.png]

```bash
grep -r "HTB" 2>/dev/null
```
![./flag.png]

finally we get, the flag
##### flag: *HTB{N0w_Y0u_C4n_L0g1n}*
