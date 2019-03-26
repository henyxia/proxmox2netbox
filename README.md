proxmox2netbox
==============

This script export proxmox VM information in CSV format to be importable by
Netbox.

Example:

```
$ ./proxmox2netbox --host 12.23.34.45:8006 --username $username --password $password  --cluster $cluster
name,cluster,role,vcpus,memory,disk,comments
my-vm,my-cluster,Virtual Machine,2,4096,32,vmid=132
...
```
