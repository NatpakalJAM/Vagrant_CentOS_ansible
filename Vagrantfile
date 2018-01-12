# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "bento/centos-7.4"
  config.vm.hostname = "CentOS-7.4_Jam"
  config.vm.network "private_network", ip: "192.168.33.10"
  # config.vm.network "public_network"
  config.vm.provider "virtualbox" do |vb|
  #  vb.gui = true
     vb.memory = "1024"
  end
  config.vm.provision "ansible" do |ansible|
         ansible.playbook = "ansible/site.yml"
      end
  config.vm.synced_folder ".", "/var/www/html", :mount_options => ["dmode=775", "fmode=775"]
end
