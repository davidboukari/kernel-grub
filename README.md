# kernel-grub

#Replace ro => rw init=/sysroot/bin/bash

#Manage grub

* Add/Remove options  /etc/default/grub

```bash
$ cat /etc/default/grub
GRUB_TIMEOUT=1
GRUB_DISTRIBUTOR="$(sed 's, release .*$,,g' /etc/system-release)"
GRUB_DEFAULT=saved
GRUB_DISABLE_SUBMENU=true
GRUB_TERMINAL_OUTPUT="console"
GRUB_CMDLINE_LINUX="no_timer_check console=tty0 console=ttyS0,115200n8 net.ifnames=0 biosdevname=0 elevator=noop crashkernel=auto"
GRUB_DISABLE_RECOVERY="true"
```

# /etc/grub2.cfg -> ../boot/grub2/grub.cfg

#Generate grub.cfg

```bash
grub2-mkconfig -o /boot/grub2/grub.cfg
```

