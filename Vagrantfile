# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "centos/7"
  config.vbguest.auto_update = true
  config.vm.network "private_network", ip: "192.168.100.10"
  config.vm.synced_folder ".", "/vagrant", type: "virtualbox"
  config.vm.synced_folder "..", "/projects", type: "virtualbox"
  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "vagrant/provision.yml"
  end

  config.vm.provider "virtualbox" do |vb|
    vb.memory = 4096
    vb.cpus = 4
  end
end
