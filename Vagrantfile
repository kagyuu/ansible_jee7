# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "centos/7"

  config.vm.define "jee" do |server|
    server.vm.hostname = "jee"
    server.vm.network "forwarded_port", guest: 8080, host: 18080
    server.vm.network "forwarded_port", guest: 4848, host: 14848
    server.vm.network "forwarded_port", guest: 5432, host: 15432
  end
end
