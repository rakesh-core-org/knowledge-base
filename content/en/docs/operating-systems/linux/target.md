# Systemctl target 
 
targets were previously called as runlevels 

Targets are group of many units in linux 

runlevels are described using numbers 0,1,2 and so on.

`systemctl list-units --type target --state active`
`systemctl get-default`


## For legacy 
`runlevel`

only one target can be active at a single point of time 

