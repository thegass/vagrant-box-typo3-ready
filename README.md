vagrant-box-typo3-ready
=======================

vagrant file f. setting up a typo3-ready debian-wheezy-lamp box. NO TYPO3 INCLUDED. 

fetches a preconfigured box-file and mounts a shared-directory htdocs (will be created if missind) to /var/www

guest port 80 is mapped to host:8080

virtualbox guest additions f. version 4.2.18 are installed.

users of vagrant version < 1.3.1 must change the line f. config.vm.synced_folder from

config.vm.synced_folder "htdocs", "/var/www",:mount_options => ["uid=33","gid=33","dmode=777","fmode=777"], create: true

to

config.vm.synced_folder "htdocs", "/var/www",extra: "uid=33,gid=33,dmode=777,fmode=777", create: true

