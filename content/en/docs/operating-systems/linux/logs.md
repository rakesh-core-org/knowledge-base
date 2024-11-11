# Journalctl

Usually after reboot journal logs are cleanedup. To persist the logs 

```
cat  /etc/systemd/journald.conf | grep -i storage
#Storage=auto
```

Change `Storage=persistent`

For cheking logs before reboot use below option

`journalctl -b -1 -p err`


# For opening unauthenticated shell

`systemctl enable debug-shell.service`

