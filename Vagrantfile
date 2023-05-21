Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.hostname = "employes3"
  config.vm.define "employes3"
  config.vm.synced_folder "html/", "/var/www/html"
  config.vm.network "private_network", ip: "172.16.0.100"
  # Necessari si volem accedir a mariadb des de localhost
  config.vm.network "forwarded_port", guest: 3306, host: 3306
  config.vm.provision "shell", path: "bootstrap.sh"
  config.vm.provider "virtualbox" do |vb|
	vb.name = "employes3"
    vb.memory = "1257"
    vb.cpus = 1
  end
end