# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

    config.vm.box = "creatuity/MageScotchBox"
    config.vm.network "private_network", ip: "192.168.33.10"
    config.vm.provision :shell, path: "bootstrap.sh"
    config.vm.hostname = "scotchbox"
    config.vm.synced_folder ".", "/var/www", :mount_options => ["dmode=777", "fmode=666"]
    
    # Optional NFS. Make sure to remove other synced_folder line too
    #config.vm.synced_folder ".", "/var/www", :nfs => { :mount_options => ["dmode=777","fmode=666"] }
    config.vm.provider "virtualbox" do |v|
  	v.memory = 2048
  	v.cpus = 2
    end
end
