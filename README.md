# synokvm
Libvirt, Qemu for Synology DSM X86 platform(with kvm support).

Tested on DSM v6.0/6.1. Try this on your own risk.

# Usage:
> 1. Install spk first;
> 2. use virsh or virt-manager to setup and manager your vm images.

# Building tips
```bash
Qemu build with:
./configure --prefix=/usr/local --target-list="x86_64-softmmu arm-softmmu" \
--disable-gtk --disable-xen --enable-{kvm,linux-aio,vhost-net,vnc,vnc-png,vnc-jpeg,guest-agent} \
--enable-{spice,coroutine-pool,libiscsi,libusb,curl,libssh2,tpm} \
--enable-{modules,usb-redir,vhost-vsock,virglrenderer,replication,bzip2,rbd,attr,virtfs,vnc-sasl,tcmalloc,jemalloc,lzo} \
--audio-drv-list='sdl oss alsa pa'


```

```bash
Libvirt build with: 
./configure --prefix=/usr/local --with-yajl --with-openssl --with-blkid \
--with-curl --with-ssh2  --with-qemu --with-lxc --with-remote --with-libvirtd \
--with-pm-utils --with-sysctl --with-network  --with-storage-scsi  --with-virtualport \
--with-esx --with-blkid --with-hal --with-avahi --with-udev  --with-storage-iscsi

```

> 1. Build these on Debian jessie distribution, 
     and made packages with this amazing tool https://github.com/rednoah/ant-spk, thanks to rednoah.
> 2. Devlepment tutorial: https://developer.synology.com/developer-guide/getting_started/index.html
    
# 中文教程参考 
  http://koolshare.cn/thread-76860-1-2.html
