# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|

  config.vm.box = "debian/jessie64"
  config.vm.network "public_network"
  config.ssh.insert_key = false

   config.vm.provider "virtualbox" do |vb|
     vb.cpus = 2
     vb.name = "Gitlab"
     vb.memory = "2048"
   end

  config.vm.provision "shell", path: "./shared/install.sh"
  config.vm.synced_folder "./shared", "/vagrant", :mount_options => ["dmode=777", "fmode=666"]
end
