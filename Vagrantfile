VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
	config.vm.box = "ubuntu/bionic64"
	config.vm.network "forwarded_port", guest: 80, host: 80
	config.vm.network "forwarded_port", guest: 3306, host: 3306
	config.vm.synced_folder "./www", "/var/www/html/proyecto"
	config.vm.provision "shell", path: "scripts/provisioner.sh"
end