# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANT_CONFIG_VERSION=2

Vagrant.configure(VAGRANT_CONFIG_VERSION) do |config|
  config.vm.box = "centos-7.2"
  config.vm.provider "virtualbox" do |vb|
    vb.memory = 4096
    vb.cpus = 2
  end
  config.vm.network "forwarded_port", guest: 8888, host: 8888
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/roles/docker/main.yml"
  end
end
