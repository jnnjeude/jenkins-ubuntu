Vagrant.configure("2") do |config| 

    config.vm.define "jenkins" do |jenkins|  
      jenkins.vm.box = "generic/ubuntu2004"   
      jenkins.vm.hostname = "jenkins" 
      jenkins.vm.network "private_network", ip: "192.168.56.8"   
       
      jenkins.vm.provider :virtualbox do |v| 
        v.customize ["modifyvm", :id, "--memory", 4096 ] 
        v.customize ["modifyvm", :id, "--name", "jenkins-host"] 
        v.customize ["modifyvm", :id, "--cpus", "4"]
        
       end 
      jenkins.vm.provision "shell", path: "jenkins.sh"
     end 
   end