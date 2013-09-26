$database_server_ip = "192.168.56.10"
$database_server_path = "/Users/omer/Projects/vagrant-database-server"
$vagrant_module_path = "/Users/omer/Projects/vagrant-shell-modules"

Vagrant.configure("2") do |config|
	config.vbguest.auto_update = false

	config.vm.box = "centos_64"
	config.vm.box_url = "http://puppet-vagrant-boxes.puppetlabs.com/centos-64-x64-vbox4210.box"

	config.vm.network :forwarded_port, guest: 3306, host: 3306
	config.vm.network :forwarded_port, guest: 27017, host: 27017
	config.vm.network :forwarded_port, guest: 28017, host: 28017
	config.vm.network :forwarded_port, guest: 6379, host: 6379
	config.vm.network :forwarded_port, guest: 11211, host: 11211

	config.vm.network "private_network", ip: $database_server_ip

 	config.vm.synced_folder $database_server_path, "/vagrant"
 	config.vm.synced_folder $vagrant_module_path, "/vagrant/modules"

 	config.vm.provision :shell, :path => "bootstrap.sh"
end