# dotfiles - for the lazy

This repo acts as the starting point for setting up my dev environment. It consists all of the configuration files and settings needed.

Follow the steps in order:

# OS

My OS of choice is [POP!\_OS](https://pop.system76.com/), download and install it.

# [Optional] Configuring the GRUB Menu

To configure the boot menu in case of dual boot, type the following commands in terminal --> [video for reference](https://youtu.be/vdxMB6qD5rc?feature=shared&t=589):

```
sudo fdisk -l	//get a list of all partitions
sudo mkdir /mnt/windows
sudo mount /dev/sda1 /mnt/windows	//select partition of first EFI block (sda1)
sudo cp -r /mnt/windows/EFI/Microsoft /boot/efi/EFI
sudo ls /boot/efi/EFI	//if you see Microsoft folder, it means it's done
sudo nano /boot/efi/leader/loader.conf	// edit config files, create a new line and write the following:
`timeout 5`	//5 secs waiting time
`console-mode max`	//save the file and exit
```

If you login next time, you'll see a GRUB menu.

# Must-have Apps
