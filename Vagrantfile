# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "centos/7"
  config.vbguest.auto_update = true
  config.vm.network "private_network", ip: "192.168.100.10"
  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "vagrant/provision.yml"
  end

  config.vm.synced_folder ".", "/vagrant", type: "virtualbox"
  config.vm.synced_folder "..", "/projects", type: "rsync",
    rsync__auto: true,
    rsync__args: ["--verbose", "--rsync-path='sudo rsync'", "--archive", "-z", "--delete"],
    rsync__exclude: [".git/", ".idea/", ".vagrant/", ".sass-cache/", "venv/"]

  config.vm.provider "virtualbox" do |vb|
    vb.memory = 4096
    vb.cpus = 2
  end
end
