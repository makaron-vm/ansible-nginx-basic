# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.ssh.insert_key = false
  config.vm.box = "ubuntu/focal64"

  (1..3).each do |i|
    config.vm.define "vagrant#{i}" do |node|
    node.vm.network "forwarded_port", id:"http:",guest: 80, host: "808#{i}", host_ip: "127.0.0.1"
    node.vm.network "forwarded_port", id:"https",guest: 443, host: "844#{i}", host_ip: "127.0.0.1"
    end
  end

  config.vm.define "fedora" do |fedora|

    fedora.vm.box = "generic/fedora28"
  end
  
end
