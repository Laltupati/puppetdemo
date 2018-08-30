# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.ssh.insert_key = false
  config.vm.box_check_update = false

# Puppet Master or Server.
 config.vm.define "puppetserver" do |ps|
	ps.vm.hostname = "puppetserver"
	ps.vm.box = "geerlingguy/centos7"
	config.vm.network "public_network"
	config.vm.provider :virtualbox do |v|
     v.memory = 4096
    end	 
 end
 
 # Puppet client or node or slave.
 config.vm.define "puppetclient" do |pc|
	pc.vm.hostname = "puppetclient"
	pc.vm.box = "geerlingguy/centos7"
	config.vm.network "public_network"
	config.vm.provider :virtualbox do |v|
     v.memory = 512
    end	 
 end
 
end 
