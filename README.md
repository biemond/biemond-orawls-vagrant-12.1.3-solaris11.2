## Oracle Solaris 11.2 with WebLogic 12.1.3

Tested on vagrant 1.7.3 with Oracle virtualbox 5

The reference implementation of https://github.com/biemond/biemond-orawls
optimized for linux, solaris

creates a 12.1.3 WebLogic cluster on 1 machine

###Software
JDK
- jdk-7u71-solaris-i586.gz
- jdk-7u71-solaris-x64.gz

Weblogic 12.1.3
- fmw_12.1.3.0.0_wls.jar

### Vagrant
Update the vagrant /software share to your local binaries folder
- vagrant up adminsol
- vagrant ssh adminsol
- sudo su -
- /opt/csw/bin/puppet apply /vagrant/puppet/manifests/site.pp --trace --verbose --hiera_config /vagrant/puppet/hiera.yaml --modulepath /vagrant/puppet/modules

### Port forwarding
- 7001

### Accounts
- root password vagrant123
- vagrant password 1vagrant
- oracle password oracle