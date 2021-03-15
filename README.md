proxmox2netbox
==============

These scripts export proxmox VM information in CSV format to be importable by
Netbox. These two scripts works in the same way but rely on different
libraries. For `Net::Proxmox::VE`, use the `-cpan` version, as for the
`libpve-apiclient-perl` one, use `-pve`.

Example:

```
$ ./proxmox2netbox-cpan --host 12.23.34.45:8006 --username $username --password $password  --cluster $cluster
name,cluster,role,vcpus,memory,disk,comments
my-vm,my-cluster,Virtual Machine,2,4096,32,vmid=132
$ ./proxmox2netbox-pve --host my.pve.com --username $username --password $password --cluster $cluster
name,cluster,role,vcpus,memory,disk,comments
my-vm,my-cluster,Virtual Machine,2,4096,32,vmid=132
```

Note
----

This script is just a fork from https://github.com/mrproper/proxmox-ve-api-perl/blob/master/examples/list_qemus.pl
