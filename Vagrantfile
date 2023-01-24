# -*- mode: ruby -*-
# vi: set ft=ruby :

IP =  "192.168.58.93"   # Don't change!
CPU_CORES_COUNT = "8"   # Cnahge if necessary
MEMORY_COUNT = "16384"   # Cnahge if necessary

Vagrant.configure("2") do |macos|
    macos.vm.box = "jhcook/macos-sierra"
    macos.vm.synced_folder ".", "/vagrant", disabled: true
    macos.vm.network :private_network, ip: IP
    macos.vm.provider "virtualbox" do |vb|
        vb.name = "macos"
        vb.memory = MEMORY_COUNT
        vb.cpus = CPU_CORES_COUNT
        vb.gui = true
    end
  end