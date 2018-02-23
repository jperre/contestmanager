Vagrant.configure("2") do |config|
  
  config.vm.define "cmtest" do |cmtest|
	cmtest.vm.box = "generic/debian9"
  
	cmtest.vm.network "private_network", ip: "10.0.20.10"
#	config.vm.network "public_network"
	cmtest.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"

	cmtest.vm.provider "virtualbox" do |vb|      
      vb.memory = "2048"
    end
	
#	cmtest.vm.synced_folder "./scripts", "/scripts", disabled: false
    
#    cmtest.vm.provision "1", type: "shell", inline: "/bin/bash /scripts/install.sh "
        
	end
end