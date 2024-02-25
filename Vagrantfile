# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # Используем виртуальную машину с ubuntu
  config.vm.box = "ubuntu"
  
  # параметры процессора	
  config.vm.provider "virtualbox" do |vb|
    # процессор
    vb.cpus = 2
    
    #память
    vb.memory = "2048"

    # параметры жесткого диска
    vb.customize ["modifyvm", :id, "--name", "ubuntu-vm", "--memory", "2048", "--cpus", "2"] 
  end

  # параметры сети
  config.vm.network "forwarded_port", guest: 80, host: 8080

  # тип сети
  config.vm.network "private_network", type: "dhcp" 
end
