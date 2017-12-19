# proxmox-hetzner-vm-subnet-change

The vm_subnet_change is used inside of VM. It is written for VM which only use ipv6 (there is a ipv4 reverse proxy in front of them).
When the vm migrates obviously also the ipv6 subnet migrates. That script gets exectued, verifies in which subnet it is, and sets the ip address and gateway correctly.
Since we don't support life migration, it is only executed after the network is started. You can easily add it to a cronjob, for live migration.
it also should be easy to extend for ipv4 if wished

