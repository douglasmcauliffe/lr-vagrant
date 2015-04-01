# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|

  config.vm.define "lr49", primary: true do |lr49|
    lr49.vm.box = "lr-49b"
    lr49.vm.host_name = "lr49.local"

    lr49.vm.network "private_network", ip: "10.0.0.49"
    lr49.vm.network "forwarded_port", guest: 80, host: 8080, auto_correct: true
    lr49.ssh.insert_key = false
    lr49.vm.provider "virtualbox" do |vb|
      # Display the VirtualBox GUI when booting the machine
      vb.gui = false
    
      # Customize the amount of memory on the VM:
      vb.memory = "1024"

      vb.name = "LR Node v.49"
   end
  end

  config.vm.define "lr51" do |lr51|
    lr51.vm.box = "lr-51b"
    lr51.vm.host_name = "lr51.local"

    lr51.vm.network "private_network", ip: "10.0.0.51"
    lr51.vm.network "forwarded_port", guest: 80, host: 8080, auto_correct: true
    lr51.ssh.insert_key = false

    lr51.vm.provider "virtualbox" do |vb|
      # Display the VirtualBox GUI when booting the machine
      vb.gui = false
    
      # Customize the amount of memory on the VM:
      vb.memory = "1024"

      vb.name = "LR Node v.51"
    end
  end



  config.vm.define "lruser" do |lruser|
    # lruser.vm.box = "rjkernick/linuxMint17Xfce"
    lruser.vm.box = "lruserb"
    lruser.vm.host_name = "lruser.local"

    # lruser.vm.network "private_network", ip: "10.0.0.5"
    lruser.vm.network "private_network", type: "dhcp"
    lruser.ssh.insert_key = false

    lruser.vm.provider "virtualbox" do |vb|
      # Display the VirtualBox GUI when booting the machine
      vb.gui = true
    
      # Customize the amount of memory on the VM:
      vb.memory = "2048"

      vb.name = "LR User"
    end
  end

  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://atlas.hashicorp.com/search.
  # config.vm.box = "ubuntu-couchdb"

  # config.vm.host_name = "lr49.local"
  # Disable automatic box update checking. If you disable this, then
  # boxes will only be checked for updates when the user runs
  # `vagrant box outdated`. This is not recommended.
  # config.vm.box_check_update = false

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  # config.vm.network "forwarded_port", guest: 80, host: 8080

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  # config.vm.network "private_network", ip: "192.168.33.10"

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
  
   #   # Customize the amount of memory on the VM:
   #   vb.memory = "2048"
   # end
  #
  # View the documentation for the provider you are using for more
  # information on available options.

  # Define a Vagrant Push strategy for pushing to Atlas. Other push strategies
  # such as FTP and Heroku are also available. See the documentation at
  # https://docs.vagrantup.com/v2/push/atlas.html for more information.
  # config.push.define "atlas" do |push|
  #   push.app = "YOUR_ATLAS_USERNAME/YOUR_APPLICATION_NAME"
  # end

  # Enable provisioning with a shell script. Additional provisioners such as
  # Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  # documentation for more information about their specific syntax and use.
  # config.vm.provision "shell", inline: <<-SHELL
  #   sudo apt-get update
  #   sudo apt-get install -y apache2
  # SHELL
end