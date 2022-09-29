
yum install -y grub2-efi-x64-modules grub2-pc-modules
cd
git clone git@github.com:somphop26/cobbler-loaders.git
cd cobbler-loaders/files  
tar xvf cobbler-loaders.tar.gz
cp -r ~/cobbler-loaders/files/var/lib/cobbler/loaders /var/lib/cobbler/

systemctl restart cobblerd
systemctl restart tftp
cobbler sync



$ ls -alR /var/lib/cobbler/loaders/
/var/lib/cobbler/loaders/:
total 1228
drwxr-xr-x  3 root root   4096 Jun 12  2021 .
drwxr-xr-x. 9 root root   4096 Sep 28 17:01 ..
-rw-r--r--  1 root root    631 Apr 28  2009 COPYING.elilo
-rw-r--r--  1 root root  18007 Mar  6  2020 COPYING.syslinux
-rw-r--r--  1 root root    626 Mar  6  2020 COPYING.yaboot
-rw-r--r--  1 root root 356493 Apr 28  2009 elilo-ia64.efi
drwxr-xr-x  2 root root    112 Jan 22  2021 grub
-rw-r--r--  1 root root 243679 Mar  6  2020 grub-x86_64.efi
-rw-r--r--  1 root root 237224 Mar  6  2020 grub-x86.efi
-rw-r--r--  1 root root  91550 Apr 18  2020 lpxelinux.0
-rw-r--r--  1 root root  54964 Mar  6  2020 menu.c32
-rw-r--r--  1 root root  16794 Mar  6  2020 pxelinux.0
-rw-r--r--  1 root root   1054 Mar  6  2020 README
-rw-r--r--  1 root root 198236 Mar  6  2020 yaboot

/var/lib/cobbler/loaders/grub:
total 1496
drwxr-xr-x 2 root root     112 Jan 22  2021 .
drwxr-xr-x 3 root root    4096 Jun 12  2021 ..
-rw-r--r-- 1 root root  294327 Jan 22  2021 grub.0
-rw-r--r-- 1 root root       0 Jan 22  2021 grubaa64.efi
-rw-r--r-- 1 root root       0 Jan 22  2021 grub.ppc64le
-rw-r--r-- 1 root root 1231360 Jan 22  2021 grubx64.efi
lrwxrwxrwx 1 root root      21 Jan 22  2021 i386-pc -> /usr/lib/grub/i386-pc
lrwxrwxrwx 1 root root      24 Jan 22  2021 x86_64-efi -> /usr/lib/grub/x86_64-efi
