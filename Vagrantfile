# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
   config.vm.box = "chef/centos-6.5"
   config.vm.network "private_network", ip: "192.168.33.10"

   config.omnibus.chef_version = :latest
   config.vm.provision "chef_solo" do |chef|
     chef.log_level = "debug"
     chef.cookbooks_path = "./cookbooks"
     chef.add_recipe "apache"
   end
end
