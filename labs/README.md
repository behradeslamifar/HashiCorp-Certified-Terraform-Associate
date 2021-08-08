# Terraform Lab

## Install Proxmox
* Download latest version of Proxmox Virtual Environment (PVE) from [Download page](https://www.proxmox.com/en/downloads/category/iso-images-pve).
* Write ISO file on USB drive
```
cat proxmox-ve_6.4-1.iso > /dev/sdb
```
* Boot your machine with proxmox bootable USB drive and install with it's installer. 

## Build Proper Image
* Download Ubuntu Cloud Image from [Ubuntu website](https://cloud-images.ubuntu.com/focal/current/focal-server-cloudimg-amd64.img)
* Change directory to `build_image`
* Change variables base on you environment: `iso_url` and `iso_checksum`
* Start build image
```
packer build template.json
```

* Copy builded image to PVE machine
```
scp output/ubuntu-focal-${timestamp} root@pve_ip:
```

## Create Proxmox Template
* ssh to PVE host
* Create basic virtual machine
```
qm create 9000 --name 'ubuntu2004-template' --description 'Ubuntu 20.04 Template' \
  --ostype l26 \
  --bios seabios \
  --boot c \
  --bootdisk scsi0 \
  --agent 1 \
  --cpu cputype=kvm64 --sockets 1 --cores 2 --vcpu 2 --memory 2048 --balloon 0 \
  --net0 virtio,bridge=vmbr0 \
  --scsihw virtio-scsi-pci \
  --scsi0 local-lvm:vm-9000-disk-0 \
  --vga qxl \
  --hotplug disk,network,usb --serial0 socket \
  --ide2 local-lvm:cloudinit
```

* Import builded image in first step
```
qm importdisk 9000 packer-ubuntu-focal-1627752719 local-lvm
```

* Resize image
```
qm resize 9000 scsi0 15G
```

* Convert basic vm to template
```
qm template 9000
```
