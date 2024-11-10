# Yum

Redhat has satelite pository and local repository 

Both YUM and DNF points to the same symbolic link. (dnf-3)

Repository location 

/etc/yum.repos.d/redhat.repo

yum repolist --all

## To mount local DVD or directory as respository 

yum install dnf-plugins-core

yum config-manager --add-repo=/mnt/BaseOS
yum config-manager --add-repo=/mnt/AppStream
yum config-manager --add-repo=http://127.0.0.1/baseOS
yum config-manager --add-repo=http://127.0.0.1/AppStream


Note: this will create a repo file under /etc/yum.repo.d/
yum repolist 

yum makecache

## To disable a repository 
yum config-manager --disable rhel-8 


## Create a local web repository

1. install apache web server running 
`yum install httpd`

Mount the repo directory to /var/www/html

yum config-manager --add-repo=http://x.x.x.x/BaseOS

# Security updates 

## For checking 
yum updateinfo 
yum updateinfo --security 
yum updateinfo --sec-severity

## For pushing the packages 
yum update --advisory RHSA-XXX
yum update --sec-severity Important

# yum modules 

yum module list 

yum module list ruby  --> this will list available streams and profiles 
yum module install ruby:2.6

yum module list mariadb
yum module install mariadb:10.3/client  --> here client is the profile; 10.3 is the stream 