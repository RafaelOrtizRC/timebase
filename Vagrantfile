# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    config.vm.box = "bento/ubuntu-20.04"
    config.vm.define "timebase-test"
    config.vm.synced_folder ".", "/home/vagrant/timebase"
    config.vm.provision :shell, path: "vagrant-bootstrap.sh"
    config.vm.provider "vmware_desktop" do |v|
        v.vmx["memsize"] = "8192"
        v.vmx["numvcpus"] = "6"
        v.vmx["ethernet0.pcislotnumber"] = "32"
    end
end
