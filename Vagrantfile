# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.network "private_network", ip: "10.0.0.5"

  #config.vm.provision "shell", inline: <<-SHELL
  #   apt-get update
  #   apt-get install -y apache2 mysql-server php5
  #SHELL

  config.vm.provision "ansible_local" do |ansible|
      ansible.playbook = "dev_ansible/deploy_phpipam.yml"
  end
end
