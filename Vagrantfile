# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.vm.box = "bento/ubuntu-16.04"
    config.vm.network "private_network", ip: "192.168.33.10"
    config.vm.synced_folder "shared", "/home/vagrant/projects"
    config.vm.provision "shell", path: "shared/config-ansible.sh"
    config.vm.hostname = "controller"
    config.vm.provider "virtualbox" do |v|
        v.memory = 512
        v.cpus = 1
    end
end