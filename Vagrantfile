# -*- mode: ruby -*-
# vi: set ft=ruby :

# Other useful options
# config.vm.network "forwarded_port", guest: 80, host: 8080
# config.vm.network "private_network", ip: "192.168.33.10"
# config.vm.network "public_network"
# config.vm.synced_folder "../data", "/vagrant_data"

Vagrant.configure(2) do |config|
  config.vm.box = "http://opscode-vm-bento.s3.amazonaws.com/vagrant/vmware/opscode_centos-7.1_chef-provisionerless.box"
  config.ssh.insert_key = false
  config.vm.provider "vmware_fusion" do |v|
    v.gui = false
    v.memory = '2048'
    v.cpus = '2'
  end
  config.vm.provision "ansible" do |a|
    a.playbook = "playbook.yml"
  end
end
