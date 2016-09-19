# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |cluster|

  cluster.vm.define "node-1" do |config|
    config.vm.box = "bento/centos-7.1"
    config.ssh.insert_key = false
    config.vm.provider :virtualbox do |vb, override|
      vb.customize ["modifyvm", :id, "--memory", "128"]
      vb.customize ["modifyvm", :id, "--cpus", "1"]
    end
    config.vm.hostname = "node-1"
    config.vm.network :private_network, ip: "10.42.1.11"
  end

  cluster.vm.define "node-2" do |config|
    config.vm.box = "bento/centos-7.1"
    config.ssh.insert_key = false
    config.vm.provider :virtualbox do |vb, override|
      vb.customize ["modifyvm", :id, "--memory", "128"]
      vb.customize ["modifyvm", :id, "--cpus", "1"]
    end
    config.vm.hostname = "node-2"
    config.vm.network :private_network, ip: "10.42.1.12"
  end

end
