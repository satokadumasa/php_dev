# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "bento/centos-7.6"
  #config.vm.network "public_network" , ip: "192.168.100.155", bridge: "en0: Wi-Fi (AirPort)"
  config.vm.network "public_network" , ip: "192.168.1.155", bridge: "en0: Wi-Fi (AirPort)"
  config.vm.network "forwarded_port", guest: 80, host: 8081
  config.vm.synced_folder "./Project", "/home/vagrant/Project", owner: "vagrant", group: "vagrant"
  VAGRANTFILE_API_VERSION = "2"
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048"
  end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "site.yml"
    ansible.inventory_path = "hosts"
    ansible.limit = 'all'
  end
end
