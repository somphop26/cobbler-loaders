### #Setup
#### yum install -y grub2-efi-x64-modules grub2-pc-modules
#### cd
#### git clone https://github.com/somphop26/cobbler-loaders.git
#### cd cobbler-loaders/files  
#### tar xvf cobbler-loaders.tar.gz
#### cp -r ~/cobbler-loaders/files/var/lib/cobbler/loaders /var/lib/cobbler/

#### systemctl restart cobblerd
#### systemctl restart tftp
#### cobbler sync
