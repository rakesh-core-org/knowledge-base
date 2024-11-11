MBR and  GPT



## For partitioning manually

use fdisk or parted or gdisk depending on the disk size


lsblk --fs

## Via gdisk





## Via parted
parted /dev/sda unit GB  print

parted /dev/sda mkpart primary ext4 1MiB 20GB
sudo mkfs.ext4 /dev/sda1
mount /dev/sda1 /data



# resize partition 

parted /dev/sda resizepart 1 210GB
udevadm settle
resize2fs /dev/sda1

# Create swap partitioning 
