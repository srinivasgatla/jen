Vagrant.configure("2") do |config|

#Ansible control server, ubuntu trusty64 OS
#  config.vm.define "control" do |control|
#    control.vm.box = "nrel/CentOS-6.5-x86_64"
#    control.vm.hostname = 'control'
#    control.vm.network "public_network", bridge: "wlo1"
#    control.vm.network "private_network", ip: "192.168.2.5"

#  end

#Webserver node, ubuntu OS
  config.vm.define "webcent" do |webcent|
    webcent.vm.box = "nrel/CentOS-6.5-x86_64"
    webcent.vm.hostname = 'webcent'
    webcent.vm.network "public_network", bridge: "wlo1"
  end

#DBserver node, ubuntu OS
  config.vm.define "dbcent" do |dbcent|
    dbcent.vm.box = "nrel/CentOS-6.5-x86_64"
    dbcent.vm.hostname = 'dbcent'
   dbcent.vm.network "public_network", bridge: "wlo1"
  end

#Webserver node, ubuntu OS
  config.vm.define "webubuntu" do |webubuntu|
    webubuntu.vm.box = "ubuntu/trusty64"
    webubuntu.vm.hostname = 'webubuntu'
    webubuntu.vm.network "public_network", bridge: "wlo1"
  end

#DBserver node, ubuntu OS
  config.vm.define "dbubuntu" do |dbubuntu|
    dbubuntu.vm.box = "ubuntu/trusty64"
    dbubuntu.vm.hostname = 'dbubuntu'
   dbubuntu.vm.network "public_network", bridge: "wlo1"
  end
end

