# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
  # https://docs.vagrantup.com.
	config.vm.box = "ubuntu/bionic64"
  config.vm.box_check_update = true
	config.vm.hostname = "djmsuman-me"
	config.vm.define "djmsuman-me"
  config.vm.network "private_network", ip: "192.168.15.10"
  config.vm.provider "virtualbox" do |vb|
    vb.name = "djmsuman-me"
    vb.memory = "2048"
  end
  config.vm.provision :shell, path: 'scripts/provisioner.sh', run: 'initial'
	config.vm.provision :shell, path: 'scripts/bootstrap.sh', run: 'always'
end
