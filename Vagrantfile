Vagrant.configure("2") do |config|

  config.vm.define "ansible-host" do |scriptbox|
    scriptbox.vm.box = "ubuntu/bionic64"
	scriptbox.vm.network "private_network", ip: "192.168.56.12"
	scriptbox.vm.provider "virtualbox" do |vb|
     vb.memory = "1024"
   end
  end

  config.vm.define "web01" do |web01|
    web01.vm.box = "geerlingguy/centos7"
	web01.vm.network "private_network", ip: "192.168.56.13"
  end
  
  config.vm.define "web02" do |web02|
    web02.vm.box = "geerlingguy/centos7"
	web02.vm.network "private_network", ip: "192.168.56.14"
  end

  config.vm.define "db" do |db|
    db.vm.box = "geerlingguy/centos7"
	db.vm.network "private_network", ip: "192.168.56.15"
  end
end
