# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|

  config.vm.box = 'centos/7'

  config.vm.synced_folder "./data", "/vagrant_data"

  config.vm.define :centos7 do |centos7_config|
    centos7_config.vm.hostname = 'srvcentos7_01'
    centos7_config.vm.network :private_network, ip: '192.168.50.52'
    # centos7_config_config :shell, path: "boot.sh"
    centos7_config.vm.provision "shell", inline: <<-SHELL
      echo "Treinamento ansible" > /tmp/ansible.txt
    SHELL
  end
end
