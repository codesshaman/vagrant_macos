# -*- mode: ruby -*-
# vi: set ft=ruby :

IP =  "192.168.58.93"   # Don't change!
CPU_CORES_COUNT = "4"   # Cnahge if necessary
MEMORY_COUNT = "8192"   # Cnahge if necessary

# create machines config
Vagrant.configure(2) do |config|
    config.vm.box = "jhcook/macos-sierra"
    config.vm.provider "virtualbox" do |v|
    end

  # master node config
    config.vm.define 'macos' do |macos|
        macos.vm.network :private_network, ip: IP
        macos.vm.synced_folder "project",
        "/home/vagrant/project"
        macos.vm.hostname = "macos"
        macos.vm.provision "shell",
        privileged: true, path: "setup.sh"
        macos.vm.provider "virtualbox" do |v|
            v.customize ["modifyvm", :id, "--vram", "32"]
            v.name = "macos"
            v.memory = MEMORY_COUNT
            v.cpus = CPU_CORES_COUNT
            v.gui = true
        end
    end

end
