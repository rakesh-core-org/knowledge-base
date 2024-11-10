# 

systemctl status mariadb 

systemctl cat chrony 

systemctl edit chrony 


## For disabling and stoping in single command 
systemctl disable --now chrony 

## For enabling and starting in single command 
systemctl enable --now chrony 

# Systemd 

systemctl mask/unmask service 

mask disables the unit completely. it cannot be started without unmasking it.

