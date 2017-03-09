# -*- mode: ruby -*-
# vi: set ft=ruby :

# README
#
# Getting Started:
# 1. vagrant plugin install vagrant-hostmanager
# 2. vagrant up
# 3. vagrant ssh
#
# This should put you at the control host
#  with access, by name, to other vms
Vagrant.configure(2) do |config|
  config.hostmanager.enabled = true

#  config.vm.box = "nrel/CentOS-6.5-x86_64"

  config.vm.define "puppetmaster", primary: true do |h|
    h.vm.box = "aerospike/centos6.5"
    h.vm.network "private_network", ip: "192.168.3.10"
#    h.vm.network "public_network", bridge: "wlo1"
#    h.vm.customize ["modifyvm", :id, "--memory", "2048"]
#    h.vm.memory = 2048
   h.vm.provider :virtualbox do |vb|
          vb.customize ["modifyvm", :id, "--memory", "2048"]
      end
    h.vm.hostname = 'puppetmaster'
    h.vm.synced_folder "puppet_repo", "/etc/puppet"
  end

  config.vm.define "wiki" do |h|
    h.vm.box = "aerospike/centos6.5"
    h.vm.network "private_network", ip: "192.168.3.11"
#    h.vm.network "public_network", bridge: "wlo1"
    h.vm.hostname = 'wiki'
  end

  config.vm.define "wikitest" do |h|
    h.vm.box = "ubuntu/trusty64"
    h.vm.network "private_network", ip: "192.168.3.12"
#    h.vm.network "public_network", bridge: "wlo1"
    h.vm.hostname = 'wikitest'
  end


end
