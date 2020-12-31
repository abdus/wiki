Initial RAM FileSystem, or initramfs is a filesystem loaded before the initialization of anything else (except for kernel and bootloader).

initramfs is responsible for bootstrapping the system to the point where it can access root file system. devices like IDE, SCSI, SATA etc must be loadable from initramfs(if not built into kernel, obviously)

the boot loader loads the kernal and possible initramfs and executes it. the kernel unpacks the initramfs archives into **rootfs**.

this extracted initramfs is embedded into kernal during build. once the extraction of embedded initramfs completed, the external initramfs get unpacked. reason, embedded files get overrided by external initramfs files of same name.

initramfs' work is done when the proper modules are loaded, either via a program/script explicitly or by udev implicitly.
