Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/focal64"
N = 6
(1..N).each do |machine_id|
  config.vm.define "machine#{machine_id}" do |machine|
    machine.vm.hostname = "machine#{machine_id}"
    machine.vm.network "private_network", ip: "192.168.56.#{20+machine_id}"

    if machine_id == N
      machine.vm.provision :ansible do |ansible|
        ansible.limit = "all"
        ansible.playbook = "playbook.yml"
        end
      end
    end
  end
end