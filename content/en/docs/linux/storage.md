
# Resize existing volume 

sudo lvm lvextend -l +100%FREE  /dev/mapper/ubuntu--vg-ubuntu--lv
resize2fs -p /dev/mapper/ubuntu--vg-ubuntu--lv


to list all block devices: 
    lsblk 

fdisk -l 


/media --> temproary drives 
/mnt --> more or less permanent secondary storage 

ncdu --> package to scan and list which directory has larger storage occupied 

/bin --> user commands 
/sbin --> administrative commands 
/boot --> bootable linux kernel 
/dev --> any devices (harddisk, memory, cd-rom, )
/etc --> configuration 
/home
/lib --> shared libraries needed for bin and sbin 
/opt --> store add-on application software
/var --> data used by applications  
/proc --> system resources 
