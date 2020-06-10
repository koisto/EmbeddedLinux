### Embedded Linux
This project aims to capture a series of experiments with embedded Linux using Buildroot.

## Remember!

After making changes to any of the config files the defconfig files need to be updated before commiting.

# buildroot

```
$ make menuconfig
$ make savedefconfig
```

# linux

```
$ make linux-menuconfig
$ make linux-update-defconfig
```

# busybox

```
$ make busybox-menuconfig
$ make busybox-update-config
```

 
