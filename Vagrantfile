# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "centos/7"

  config.vm.provider "virtualbox" do |vb|
    vb.cpus = 2
    vb.memory = 1024
  end

  config.vm.define "jee" do |server|
    server.vm.hostname = "jee"
    server.vm.network "forwarded_port", guest: 8080, host: 8080, host_ip: "127.0.0.1"
    server.vm.network "forwarded_port", guest: 4848, host: 4848, host_ip: "127.0.0.1"
    server.vm.network "forwarded_port", guest: 5432, host: 5432, host_ip: "127.0.0.1"
  end
end
