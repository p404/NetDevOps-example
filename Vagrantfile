# -*- mode: ruby -*-
# vi: set ft=ruby :
# 3-router triangle topology 
# vm.network 

Vagrant.configure(2) do |config|
  config.vm.box = "juniper/ffp-12.1X47-D15.4-packetmode"

  config.vm.define "vsrx01" do |vsrx01|
    vsrx01.vm.host_name = "vsrx01"
    vsrx01.vm.network "private_network",
                      ip: "192.168.12.11",
                      virtualbox__intnet: "01-to-02"
    vsrx01.vm.network "private_network",
                      ip: "192.168.31.11",
                      virtualbox__intnet: "03-to-01"
  end

  config.vm.define "vsrx02" do |vsrx02|
    vsrx02.vm.host_name = "vsrx02"
    vsrx02.vm.network "private_network",
                      ip: "192.168.23.12",
                      virtualbox__intnet: "02-to-03"
    vsrx02.vm.network "private_network",
                      ip: "192.168.12.12",
                      virtualbox__intnet: "01-to-02"
  end

  config.vm.define "vsrx03" do |vsrx03|
    vsrx03.vm.host_name = "vsrx03"
    vsrx03.vm.network "private_network",
                      ip: "192.168.31.13",
                      virtualbox__intnet: "03-to-01"
    vsrx03.vm.network "private_network",
                      ip: "192.168.23.13",
                      virtualbox__intnet: "02-to-03"
  end
end