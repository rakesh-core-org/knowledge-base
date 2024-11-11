

Install cephadm via repository manager

```
wget -q -O- 'https://download.ceph.com/keys/release.asc' | sudo apt-key add -
sudo apt-add-repository 'deb https://download.ceph.com/debian-reef/ jammy main'
apt-get update
apt-get install cephadm
cephadm version
```

```
apt install ceph-common
```
Reference: https://docs.ceph.com/en/latest/install/get-packages/