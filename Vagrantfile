# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |cluster|

  cluster.vm.define "node1" do |node1|
    node1.vm.box = "bento/centos-7.1"
    confnode1ig.ssh.insert_key = false
    confnode1ig.vm.provider :virtualbox do |vb, override|
      vb.customize ["modifyvm", :id, "--memory", "128"]
      vb.customize ["modifyvm", :id, "--cpus", "1"]
    end
    node1.vm.hostname = "node1"
    node1.vm.network :private_network, ip: "10.42.1.11"
  end

  cluster.vm.define "node2" do |node2|
    node2.vm.box = "bento/centos-7.1"
    node2.ssh.insert_key = false
    node2.vm.provider :virtualbox do |vb, override|
      vb.customize ["modifyvm", :id, "--memory", "128"]
      vb.customize ["modifyvm", :id, "--cpus", "1"]
    end
    node2.vm.hostname = "node2"
    node2.vm.network :private_network, ip: "10.42.1.12"
  end

end
