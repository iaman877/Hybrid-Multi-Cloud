
# aws CloudTrail | S3 | EBS Volume 

## EBS Volume 
- creating, attaching to OS for persistent storage so that in case if we terminate our OS, our data will be safe in a volume.

#### Key Points :
- aws records all the major logs by CloudTrail service.

### Storage

-[x] Block storage 
- need to create partition for OS installation
- IN aws block storage is provide by  *EBS*
- for installing OS we need Ephemeral block storage (root storage in aws)
- Storage == Volume

- [x] Object storage
- only to store files. example GDrive, Dropbox
- aws provide object storage by S3 (Simple Storage Service) && Swift in Openstack.

-[x] Security Group
- firewall
- no inbound/ingress by default

- [x] Creating Volume
- add new volume to use like a HD/PD
- mount to use
- create partition in OS, format and mount

- [x] cmds
```
- fdisk -l > listing all partitions
- mkfs.ext4 /dev/xvdf > make partition
- mount /dev/xvdf /mydata > to mount
- df -h it will show the amount of free disk space on each mounted disk

```
