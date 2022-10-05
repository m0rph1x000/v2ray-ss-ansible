# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|
  config.ssh.insert_key = false
  config.vm.provider "virtualbox" do |v|
    v.memory = 1024
    v.cpus = 1
  end

  config.vm.define "internal" do |int|
    int.vm.box = "geerlingguy/ubuntu2004"
    int.vm.hostname = "internal"
    int.vm.network "private_network", ip: "192.168.56.11"
  end

  config.vm.define "external" do |ext|
    ext.vm.box = "geerlingguy/ubuntu2004"
    ext.vm.hostname = "external"
    ext.vm.network "private_network", ip: "192.168.56.21"
  end
end
