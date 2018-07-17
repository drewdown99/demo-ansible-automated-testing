# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.network "forwarded_port", guest: 3000, host: 3000

  # config.vm.provider "virtualbox" do |vb|
  #   vb.memory = "1024"
  # end

	config.vm.provision "ansible" do |ansible|
		ansible.playbook = "main.yml"
		ansible.compatibility_mode = "2.0"
		#ansible.verbose = "v"
	end

end
