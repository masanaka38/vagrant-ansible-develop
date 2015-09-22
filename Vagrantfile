# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.provider :virtualbox do |vbox|
    vbox.name = "develop"
  end
  config.vm.box = "centos6.5"
  config.vm.network "forwarded_port", guest: 80, host: 8080, id: "http"
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbooks/vagrant.yml"
  end
end
