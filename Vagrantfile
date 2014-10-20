# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provision/playbook.yml"
    ansible.sudo = true
  end

  config.vm.define "web" do |web|
    web.vm.box = "ubuntu/trusty64"
  end

  config.vm.define "worker" do |worker|
    worker.vm.box = "ubuntu/trusty64"
  end

end