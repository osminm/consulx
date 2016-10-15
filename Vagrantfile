# -*- mode: ruby -*-
# vi: set ft=ruby :

MASTER_COUNT = 1

Vagrant.configure(2) do |config|

  config.vm.box = "bento/centos-7.1"

  MASTER_COUNT.times do |i|
    config.vm.define "master#{i}" do |master|
      config.vm.network "public_network", ip: "192.168.0.19"
      config.vm.network "forwarded_port", guest:8500, host:8500,protocol:"tcp"
      master.vm.hostname = "master#{i}"
      master.vm.provider "virtualbox" do |vb|
       vb.memory = "2048"
       vb.cpus = 2
      end
    end
  end


end

