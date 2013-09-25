vagrant-database-server
=======================

Development database server project for vagrant. Contains mysql, redis, mongodb and memcached servers.

This repo depends to my other project, omerucel/vagrant-shell-modules. You can install this two repos in your projects dir. Vagrantfile configs:

$database_server_ip : Database server ip address. This settings could be useful to run multiple servers (ex: web server etc.)

$database_server_path : This config tells where the root dir to sync.

$vagrant_module_path : This config tells where the vagrant-shell-modules project to sync.
