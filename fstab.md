`fstab` is a file(`/etc/fstab`) that contains descriptive information about the
filesystems the system can mount.

- a program would never write to `fstab`. It is meant to be read.
- the order of records is important because `fsck`, `mount` and `unmount`
  sequentially iterate through `fstab` to perform their tasks

### Example

```fstab
# Static information about the filesystems.
# See fstab(5) for details.

# <file system> <dir> <type> <options> <dump> <pass>
# /dev/nvme0n1p7
UUID=a4d7ea29-37e9-4326-be28-67c703105ab4	/         	ext4      	rw,relatime	0 1

# /dev/nvme0n1p1 LABEL=SYSTEM
UUID=FE69-C493      	/boot     	vfat      	rw,relatime,fmask=0022,dmask=0022,codepage=437,iocharset=iso8859-1,shortname=mixed,utf8,errors=remount-ro	0 2

# /dev/nvme0n1p6
UUID=9ffe7bfa-bb2f-4c5f-9f15-efbfbd0f1299	none      	swap      	defaults  	0 0
```

- `<file system>`: name of the fs
- `<dir>`: mount point
- `<type>`: type of filesystem
- `<options>`: options for `mount`
- `<dump>`: passed to `dump` utility. `dump` checks `ext2/3` filesystems and
  determine which files need to backed-up..and copies them to given disk
- `<pass>`: this is the order of filesystems `fsck` use to check fs at boottime
