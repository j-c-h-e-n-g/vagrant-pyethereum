# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "opscode-centos-6.5"
  config.vm.network :private_network, ip: "192.168.33.22"


  config.vm.provision "ansible" do |ansible|
    ansible.limit = 'all'
    ansible.playbook = "provision/ethereum.yml"
    ansible.inventory_path = "provision/inventory"
    # Run commands as root.
    ansible.sudo = true
    ansible.raw_arguments = ['-v']
  end


end 

