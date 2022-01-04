# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.ssh.insert_key = false
  config.vm.box = "ubuntu/focal64"

  (1..3).each do |i|
    config.vm.define "vagrant#{i}" do |node|
    end
  end
  
  config.vm.network "forwarded_port", id:"http:",guest: 80, host: 8080, host_ip: "127.0.0.1"
  config.vm.network "forwarded_port", id:"https",guest: 443, host: 8443, host_ip: "127.0.0.1"

  
end
