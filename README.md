# jetson-vanilla-boot

In L4T version 23.5, all Jetson-nano versions have the ability to move boot flow partitions to qspi. We use this to run any possible EFI-enabled Linux distributions without modification. For jetson nano we built kernel dtb and u-boot from sources and flash it to qspi.

### Supprted
* Jetson nano developer's kit with 4GB of ram.

### Dependencies

* make
* bc 
* curl 
* bison 
* flex 
* python3-dev 
* swig

### How to:

We can set u-boot and kernel dtb versions.
```sh
./get-bsp 210
./make-u-boot v2021.01
./make-kernel-dtbs 5.4.51
```

Go to bsp by platform Linux_for_Tegra folder and flash jetson:

```sh
cd BSP/t210/Linux_for_Tegra/
sudo ./flash.sh jetson-nano-qspi mmcblk0p1
```
