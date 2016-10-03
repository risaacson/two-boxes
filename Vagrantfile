# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |cluster|

  cluster.vm.define "node1" do |node1|
    node1.vm.box = "bento/centos-6.7"
    node1.ssh.insert_key = false
    node1.vm.provider :virtualbox do |vb, override|
      vb.customize ["modifyvm", :id, "--memory", "128"]
      vb.customize ["modifyvm", :id, "--cpus", "1"]
    end
    node1.vm.hostname = "node1"
    node1.vm.network :private_network, ip: "10.42.1.11"
    node1.vm.network :forwarded_port, guest: 80, host: 8081
  end

  cluster.vm.define "node2" do |node2|
    node2.vm.box = "bento/centos-6.7"
    node2.ssh.insert_key = false
    node2.vm.provider :virtualbox do |vb, override|
      vb.customize ["modifyvm", :id, "--memory", "128"]
      vb.customize ["modifyvm", :id, "--cpus", "1"]
    end
    node2.vm.hostname = "node2"
    node2.vm.network :private_network, ip: "10.42.1.12"
    node2.vm.network :forwarded_port, guest: 80, host: 8082
  end

end
