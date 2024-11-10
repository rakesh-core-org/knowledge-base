# for setting target in kernel argument 

we can use `grubby`

`grubby --update-kernel=ALL --args="systemd-unit=graphical"`

`grubby --update-kernel=ALL --remove-args="systemd-unit=graphical"`

