# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.define "puppet" do |puppet|
    puppet.vm.box = "hashicorp/precise64"
    puppet.vm.hostname = "puppet"
    puppet.vm.network "private_network", ip: "192.168.50.10"
    puppet.vm.provision "shell", path: "provision.sh"
  end

  config.vm.define "agent" do |agent|
    agent.vm.box = "hashicorp/precise64"
    agent.vm.hostname = "agent"
    agent.vm.network "private_network", ip: "192.168.50.20"
    agent.vm.provision "shell", path: "provision.sh"
  end
end
