# -*- mode: ruby -*-
# vi: set ft=ruby :

box = "ubuntu/bionic64"

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://vagrantcloud.com/search.
  config.vm.box = box

  # Disable automatic box update checking. If you disable this, then
  # boxes will only be checked for updates when the user runs
  # `vagrant box outdated`. This is not recommended.
  # config.vm.box_check_update = false

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  # NOTE: This will enable public access to the opened port
  # config.vm.network "forwarded_port", guest: 80, host: 8080

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine and only allow access
  # via 127.0.0.1 to disable public access
  # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  # config.vm.network "private_network", ip: "192.168.33.10"
  config.vm.network "private_network", type: "dhcp"

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  # config.vm.network "public_network"

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  # config.vm.synced_folder "../data", "/vagrant_data"

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:
  #
  # config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
  #   vb.gui = true
  #
  #   # Customize the amount of memory on the VM:
  #   vb.memory = "1024"
  # end
  #
  # View the documentation for the provider you are using for more
  # information on available options.
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
    vb.cpus = 2
  end

  # Enable provisioning with a shell script. Additional provisioners such as
  # Ansible, Chef, Docker, Puppet and Salt are also available. Please see the
  # documentation for more information about their specific syntax and use.
  # config.vm.provision "shell", inline: <<-SHELL
  #   apt-get update
  #   apt-get install -y apache2
  # SHELL
  # config.vm.define "webapp1" do |webapp|
  #   webapp.vm.network :forwarded_port, guest: 22, host: 7001, id: "ssh"
  #   webapp.vm.network :forwarded_port, guest: 80, host: 8301, id: "http"
  #   webapp.vm.network :private_network, ip: "192.168.33.11"
  # end
  # config.vm.define "webapp2" do |webapp|
  #   webapp.vm.network :forwarded_port, guest: 22, host: 7002, id: "ssh"
  #   webapp.vm.network :forwarded_port, guest: 80, host: 8302, id: "http"
  #   webapp.vm.network :private_network, ip: "192.168.33.12"
  # end
  # config.vm.define "webapp3" do |webapp|
  #   webapp.vm.network :forwarded_port, guest: 22, host: 7003, id: "ssh"
  #   webapp.vm.network :forwarded_port, guest: 80, host: 8303, id: "http"
  #   webapp.vm.network :private_network, ip: "192.168.33.13"
  # end
  config.vm.define "webapp1" do |webapp|
    webapp.vm.network :forwarded_port, guest: 22, host: 7101, id: "ssh"
    webapp.vm.network :forwarded_port, guest: 80, host: 8311, id: "http"
    webapp.vm.network :forwarded_port, guest: 8080, host: 18311
    webapp.vm.hostname = "webapp1"
    webapp.vm.network :private_network, ip: "192.168.100.1"
  end
  config.vm.define "webapp2" do |webapp|
    webapp.vm.network :forwarded_port, guest: 22, host: 7102, id: "ssh"
    webapp.vm.network :forwarded_port, guest: 80, host: 8312, id: "http"
    webapp.vm.network :forwarded_port, guest: 8080, host: 18312
    webapp.vm.hostname = "webapp2"
    webapp.vm.network :private_network, ip: "192.168.100.2"
  end
  config.vm.define "webapp3" do |webapp|
    webapp.vm.hostname = "webapp3"
    webapp.vm.network :forwarded_port, guest: 22, host: 7103, id: "ssh"
    webapp.vm.network :forwarded_port, guest: 80, host: 8313, id: "http"
    webapp.vm.network :forwarded_port, guest: 8080, host: 18313
    webapp.vm.network :private_network, ip: "192.168.100.3"
  end
  config.vm.define "bench" do |bench|
    bench.vm.hostname = "bench"
    bench.vm.network :forwarded_port, guest: 22, host: 7104, id: "ssh"
    bench.vm.network :forwarded_port, guest: 80, host: 8314, id: "http"
    bench.vm.network :forwarded_port, guest: 8080, host: 18314
    bench.vm.network :private_network, ip: "192.168.100.4"
  end
end
