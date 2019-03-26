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

Note
----

This script is just a fork from https://github.com/mrproper/proxmox-ve-api-perl/blob/master/examples/list_qemus.pl
