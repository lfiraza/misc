# misc
Misc utilities for Linux, Raspberry Pi, Python, etc...

## usb_backup
https://github.com/koss822/misc/tree/master/usb_backup
### DESCRIPTION

I wrote this tool because I needed simple utility which will backup
my hardrive to encrypted USB drive with compression and incremental
backups.

There are many backups tools, but many are too complex for just this
task. I mainly use Btrfs snapshot, compression ability with RSync
to make it really easy

### INFO
#### sudo
You do not need to run this script with sudo, it will ask automatically
If you run it with sudo, use sudo -s to preserve $USER variable

#### btrfs
Btrfs is experimental in terms of performance rather than stability
There are available recovery tools that prevents data loss
It is neccesary to use Btrfs for snapshot, and compression abilities

### USAGE
#### initial
1. generate keyfile
2. edit BKP_SOURCE and BKP_TARGET accordingly in usb_backup.sh
3. ./usb_backup.sh format /dev/sdX
4. edit /etc/fstab, see fstab.sample

#### continuous backups
1. ./usb_backup.sh mount /dev/sdX
2. ./usb_backup.sh backup
3. ./usb_backup.sh umount

## rpi_usb_stick
https://github.com/koss822/misc/tree/master/rpi_usb_stick
### DESCRIPTION

These are configuration files for using Raspberry Pi with 3G modem Huawei E173 from CZ O2 (might works with other E173 models)
You can find more information here:
https://www.enigma14.eu/wiki/RPi_3G_Mobile_connection_with_O2_Huawei_E173_%28CZ%29
