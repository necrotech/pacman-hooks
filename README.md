# pacman-hooks
Personal pacman hooks

Look at these before using them.

Modified from https://github.com/mar04/lgc-hooks (no license specified upstream):
* deleted_files.hook - lists processes using deleted or older version of system files (similar to 'zypper ps'), requires lsof.
* paccache.hook - cleans up pacman's cache, by default keeping up to 2 versions of each package.
* pacdiff.hook - lists pacnew and pacsave files

Modified from an old version of https://aur.archlinux.org/packages/pacman-boot-backup-hook/ (MIT licensed as specified upstream):
* boot_backup.hook - backs up /boot before upgrading the kernel.

Modified from https://wiki.archlinux.org/title/Dynamic_Kernel_Module_Support (GNU FDL 1.3 as specified upstream):
* zfs_rebuild_initcpio.hook - run mkinitcpio if the ZFS dkms package was upgraded.  Needed for root on ZFS.

Original.  (public domain):
* grub_zfs_fix.hook - Patch /etc/grub.d/10_linux to work around grub bug 59614, which prevents it from rebuilding properly with root on zfs.
* zfs_fix.hook - replace /bin/sh with /bin/bash in the shebang of the zfs configure script.  This will be useful for systems using a non-bash shell as /bin/sh until ZOL removes the bash-isms.
* updatedb-mlocate.hook - Run updatedb after installing/removing/updating packages.  Depends on mlocate.
* updatedb-plocate.hook - Run updatedb after installing/removing/updating packages.  Depends on plocate.

Modified from https://gitlab.com/renyuneyun/pacman-ps  (GPLv2 as specified upstream):
* pacman-ps-post.hook - Update and optimize the pacman-ps database. Runs on upgrade and install.
* pacman-ps-pre.hook - Update the pacman-ps database. Runs on upgrade and remove.

From https://github.com/Strykar/pacman-hooks (no license specified upstream):
* orphans.hook - display orphaned packages

Unknown (Please create a pull request if you know where these came from, so I can properly credit them.):
* kernel_updated.hook - Displays a message that a reboot is needed if a newer kernel has been installed.
