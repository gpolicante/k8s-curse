Vagrant.configure("2") do |config|


(1..3).each do |i|  
 
  config.vm.define "node-#{i}" do |node| 
   node.vm.box = "centos/7" 
   node.vm.network "private_network", ip: "192.168.33.12#{i}"
   node.vm.hostname = "node#{i}.olivarius.com.br" 
  
  end 

end

    config.vm.provider "virtualbox" do |vb| 
      vb.memory = "2048"
      vb.cpus = "2"
    end 

   config.vm.provision "ansible" do |ansible| 
   ansible.playbook = "playbook.yaml"
   end


end 
