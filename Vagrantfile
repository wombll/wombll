# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.define "wombll" do |wombll|
    wombll.vm.box = "ubuntu/trusty64"
    wombll.vm.hostname = "wombll"
    wombll.vm.network :forwarded_port, guest: 80, host: 8000
    wombll.vm.network "private_network", ip: "10.0.0.254", netmask: "255.255.255.0", virtualbox__intnet: "management"
    wombll.vm.provider "virtualbox" do |vb|
      vb.name = "wombll"
      vb.memory = 512
      vb.cpus = 1
      vb.gui = false
    end
    wombll.vm.provision "ansible" do |ansible|
      ansible.playbook = "provision.yaml"
    end
  end

  # config.vm.define "vsrx1" do |vsrx1|
  #   vsrx1.vm.box = "juniper/ffp-12.1X47-D15.4-packetmode"
  #   vsrx1.vm.hostname = "vsrx1"
  #   vsrx1.vm.network "private_network", ip: "10.0.0.1", interface: "1", netmask: "255.255.255.0", virtualbox__intnet: "management"
  #   vsrx1.vm.network "private_network", ip: "10.1.2.1", interface: "2", netmask: "255.255.255.252", virtualbox__intnet: "network1"
  #   vsrx1.vm.network "private_network", ip: "10.1.3.1", interface: "3", netmask: "255.255.255.252", virtualbox__intnet: "network2"
  #   vsrx1.vm.provider "virtualbox" do |vb|
  #     vb.name = "vsrx1"
  #     vb.memory = 512
  #     vb.cpus = 2
  #     vb.gui = false
  #   end
  # end

  # config.vm.define "vsrx2" do |vsrx2|
  #   vsrx2.vm.box = "juniper/ffp-12.1X47-D15.4-packetmode"
  #   vsrx2.vm.hostname = "vsrx2"
  #   vsrx2.vm.network "private_network", ip: "10.0.0.2", interface: "1", netmask: "255.255.255.0", virtualbox__intnet: "management"
  #   vsrx2.vm.network "private_network", ip: "10.1.2.2", interface: "2", netmask: "255.255.255.252", virtualbox__intnet: "network1"
  #   vsrx2.vm.network "private_network", ip: "10.2.3.1", interface: "3", netmask: "255.255.255.252", virtualbox__intnet: "network3"
  #   vsrx2.vm.provider "virtualbox" do |vb|
  #     vb.name = "vsrx2"
  #     vb.memory = 512
  #     vb.cpus = 2
  #     vb.gui = false
  #   end
  # end

  # config.vm.define "vsrx3" do |vsrx3|
  #   vsrx3.vm.box = "juniper/ffp-12.1X47-D15.4-packetmode"
  #   vsrx3.vm.hostname = "vsrx3"
  #   vsrx3.vm.network "private_network", ip: "10.0.0.1", interface: "1", netmask: "255.255.255.0", virtualbox__intnet: "management"
  #   vsrx3.vm.network "private_network", ip: "10.1.3.2", interface: "2", netmask: "255.255.255.252", virtualbox__intnet: "network2"
  #   vsrx3.vm.network "private_network", ip: "10.2.3.2", interface: "3", netmask: "255.255.255.252", virtualbox__intnet: "network3"
  #   vsrx3.vm.provider "virtualbox" do |vb|
  #     vb.name = "vsrx3"
  #     vb.memory = 512
  #     vb.cpus = 2
  #     vb.gui = false
  #   end
  # end

end
