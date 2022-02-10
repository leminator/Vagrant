Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.hostname = "Zach"
  config.vm.provision "ansible", playbook: "centos.yml"
  config.vm.provision "ansible", playbook: "nginx.yml"
  config.vm.provider "virtualbox" do |vb|
     vb.memory = "2048"
  config.vm.network "private_network", ip: "192.168.56.0"
  config.vm.network "forwarded_port", guest: 22, host: 2225
  config.vm.network "forwarded_port", guest: 80, host: 8085
  end
end
