List block devices & retrieve the usb:
```
lsblk
```

Format a partition:
  - X: identify the device
  - n: identify the partition
```
sudo mkfs.vfat /dev/sdXn
```

Remove all partitions:
```
sudo sfdisk --delete /dev/sdX
```

Copy iso to usb:
- `file.iso`: the iso image
- `X` : the device to copy the iso on
```
sudo dd if=file.iso of=/dev/sdX bs=4M status=progress
```

Empty cache to persistent disk:
```
sync
```

Remove the usb.
