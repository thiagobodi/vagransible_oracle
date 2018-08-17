# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
NAME="ol6-orcl11g"
Vagrant.configure("2") do |config|
  config.vm.box = "ol6-latest"
  config.vm.network "forwarded_port", guest: 1521, host: 1531
  config.vm.provider "virtualbox" do |vb|
    vb.name = NAME
    vb.gui = false
    vb.memory = 4096
    vb.cpus = 2
    vb.customize ["modifyvm", :id, "--cpuexecutioncap", "80"]
  end
  config.vbguest.auto_update = true
  config.vbguest.no_remote = true
  config.vm.define NAME do |node|
    node.vm.hostname = NAME+".local"
    node.vm.provision 'ansible' do |ansible|
      ansible.playbook = "main.yml"
    end
  end
end
