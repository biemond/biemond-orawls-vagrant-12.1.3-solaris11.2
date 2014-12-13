# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define "adminsol" , primary: true do |adminsol|
    adminsol.vm.box = "solaris11_2-x86_64"
    adminsol.vm.box_url = "https://dl.dropboxusercontent.com/s/uxe9huy08gziwx1/solaris11_2-x86_64.box"

    adminsol.vm.hostname = "adminsol.example.com"

    adminsol.vm.synced_folder ".", "/vagrant", :mount_options => ["dmode=777","fmode=777"]
    adminsol.vm.synced_folder "/Users/edwin/software", "/software"

    adminsol.vm.network "forwarded_port", guest: 7001, host: 7001

#    adminsol.vm.network :private_network, ip: "10.10.10.10"

    adminsol.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "4032"]
      vb.customize ["modifyvm", :id, "--name", "adminsol"]
    end

#    adminsol.vm.provision :shell, :inline => "ln -sf /vagrant/puppet/hiera.yaml /etc/puppet/hiera.yaml"
#
#    adminsol.vm.provision :puppet do |puppet|
#      puppet.manifests_path    = "puppet/manifests"
#      puppet.module_path       = "puppet/modules"
#      puppet.manifest_file     = "site.pp"
#      puppet.options           = "--verbose --trace --debug --hiera_config /vagrant/puppet/hiera.yaml"
#
#      puppet.facter = {
#        "environment" => "development",
#        "vm_type"     => "vagrant",
#      }
#
#    end

  end


end
