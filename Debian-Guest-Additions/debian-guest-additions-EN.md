# Install VirtualBox Guest Additions for a Debian Virtual Machine

### Update the system

Update the system:

```
apt update
apt dist-upgrade
```

Reboot to work with the newly installed kernel (if a new kernel was installed):

```
reboot
```

------

### Install the required packages

```
apt install make gcc dkms linux-source linux-headers-$(uname -r)
```

------

### Install Guest Additions

Insert the Guest Additions CD image from **Devices → Insert Guest Additions CD Image**.

Mount the CD, go to its directory, then run the installer script:

```
sudo mount /dev/cdrom /mnt
cd /mnt
./VBoxLinuxAddition.run
```

Finally, reboot the virtual machine:

```

reboot
```

You can now enable **automatic screen resizing**, **shared clipboard**, and **drag and drop**.