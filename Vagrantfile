# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|

  # config.vm.box = 'centos/7'
  config.vm.box = 'ubuntu/trusty64'

  config.vm.synced_folder "./data", "/vagrant_data"

  config.vm.define :srvubuntu_01 do |srvubuntu_01_config|
    srvubuntu_01_config.vm.hostname = 'srvubuntu01'
    srvubuntu_01_config.vm.network :private_network, ip: '192.168.30.10'
    # centos7_config_config :shell, path: "boot.sh"
    srvubuntu_01_config.vm.provision "shell", inline: <<-SHELL
      echo "Treinamento ansible" > /tmp/ansible.txt
      apt-get update && apt upgrade -y
    SHELL
  end
  config.vm.define :srvubuntu_02 do |srvubuntu_02_config|
    srvubuntu_02_config.vm.hostname = 'srvubuntu02'
    srvubuntu_02_config.vm.network :private_network, ip: '192.168.30.20'
    # centos7_config_config :shell, path: "boot.sh"
    srvubuntu_02_config.vm.provision "shell", inline: <<-SHELL
      echo "Treinamento ansible" > /tmp/ansible.txt
      apt-get update && apt upgrade -y
    SHELL
  end  
end
