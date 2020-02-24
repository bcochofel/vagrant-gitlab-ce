# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-18.04
    config.vm.hostname = "gitlab.local.dev"

    config.vm.network :private_network, ip: "192.168.77.100"
    config.vm.network :forwarded_port, guest: 80, host: 8080

    config.vm.provider "virtualbox" do |vb|
        vb.name = "GitLab Server"
        vb.memory = "2048"
        vb.cpus = "2"
    end

    config.vm.provision :docker
    config.vm.provision "shell", path: "install_gitlab.sh"
end
