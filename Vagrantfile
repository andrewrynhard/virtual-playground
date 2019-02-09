# Network Diagram
# https://drive.google.com/open?id=15pEGT6TB5kWFl9kXrpdu7VqCEHKykfuj

Vagrant.configure("2") do |config|
  config.vm.provision "shell", inline: "echo Hello"

  config.vm.box = "geerlingguy/centos7"

  config.vm.define "client" do |client|
    client.vm.hostname = "client"
    client.vm.network "private_network", ip: "192.168.101.2",
        virtualbox__intnet: true
  end

  config.vm.define "infra" do |infra|
    infra.vm.hostname = "infra"
    infra.vm.network "private_network", ip: "192.168.102.2",
        virtualbox__intnet: true
  end
#
#  config.vm.define "cin" do |cin|
#    cin.vm.hostname = "cin"
#    cin.vm.network "private_network", ip: "192.168.103.2"
#  end
#
  config.vm.define "router" do |router|
    router.vm.hostname = "router"
    router.vm.network "private_network", ip: "192.168.101.1",
        virtualbox__intnet: true
    router.vm.network "private_network", ip: "192.168.102.1",
        virtualbox__intnet: true
    router.vm.network "private_network", ip: "192.168.103.1",
        virtualbox__intnet: true
  end
end

