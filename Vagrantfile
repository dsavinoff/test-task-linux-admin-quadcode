Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/focal64"

  (1..6).each do |i|
    config.vm.define "vm#{i}" do |vm|
      vm.vm.hostname = "vm#{i}"
      vm.vm.network "private_network", type: "dhcp"
      vm.vm.provider "virtualbox" do |v|
        v.name = "vm#{i}"
        v.memory = 1024
        v.cpus = 1
      end
    end
  end

end