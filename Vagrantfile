# # -*- mode: ruby -*-
# # vi: set ft=ruby :

# # All Vagrant configuration is done below. The "2" in Vagrant.configure
# # configures the configuration version (we support older styles for
# # backwards compatibility). Please don't change it unless you know what
# # you're doing.
# Vagrant.configure("2") do |config|
#   # The most common configuration options are documented and commented below.
#   # For a complete reference, please see the online documentation at
#   # https://docs.vagrantup.com.

#   # Every Vagrant development environment requires a box. You can search for
#   # boxes at https://vagrantcloud.com/search.
#   config.vm.box = "ubuntu/jammy64"

#   # Disable automatic box update checking. If you disable this, then
#   # boxes will only be checked for updates when the user runs
#   # `vagrant box outdated`. This is not recommended.
#   # config.vm.box_check_update = false

#   # Create a forwarded port mapping which allows access to a specific port
#   # within the machine from a port on the host machine. In the example below,
#   # accessing "localhost:8080" will access port 80 on the guest machine.
#   # NOTE: This will enable public access to the opened port
#   # config.vm.network "forwarded_port", guest: 80, host: 8080

#   # Create a forwarded port mapping which allows access to a specific port
#   # within the machine from a port on the host machine and only allow access
#   # via 127.0.0.1 to disable public access
#   # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"

#   # Create a private network, which allows host-only access to the machine
#   # using a specific IP.
#   # config.vm.network "private_network", ip: "192.168.33.10"

#   # Create a public network, which generally matched to bridged network.
#   # Bridged networks make the machine appear as another physical device on
#   # your network.
#   # config.vm.network "public_network"

#   # Share an additional folder to the guest VM. The first argument is
#   # the path on the host to the actual folder. The second argument is
#   # the path on the guest to mount the folder. And the optional third
#   # argument is a set of non-required options.
#   # config.vm.synced_folder "../data", "/vagrant_data"

#   # Disable the default share of the current code directory. Doing this
#   # provides improved isolation between the vagrant box and your host
#   # by making sure your Vagrantfile isn't accessible to the vagrant box.
#   # If you use this you may want to enable additional shared subfolders as
#   # shown above.
#   # config.vm.synced_folder ".", "/vagrant", disabled: true

#   # Provider-specific configuration so you can fine-tune various
#   # backing providers for Vagrant. These expose provider-specific options.
#   # Example for VirtualBox:
#   #
#   # config.vm.provider "virtualbox" do |vb|
#   #   # Display the VirtualBox GUI when booting the machine
#   #   vb.gui = true
#   #
#   #   # Customize the amount of memory on the VM:
#   #   vb.memory = "1024"
#   # end
#   #
#   # View the documentation for the provider you are using for more
#   # information on available options.

#   # Enable provisioning with a shell script. Additional provisioners such as
#   # Ansible, Chef, Docker, Puppet and Salt are also available. Please see the
#   # documentation for more information about their specific syntax and use.
#   # config.vm.provision "shell", inline: <<-SHELL
#   #   apt-get update
#   #   apt-get install -y apache2
#   # SHELL
# end



Vagrant.configure("2") do |config|
  # Use the Ubuntu 22.04 LTS (Jammy Jellyfish) box
  config.vm.box = "ubuntu/jammy64"

  # Set VM name
  config.vm.define "ubuntu"

  # Configure VM resources
  config.vm.provider "virtualbox" do |vb|
    vb.name = "Ubuntu"
    vb.memory = "8192" # Set the amount of RAM
    vb.cpus = 6        # Set the number of CPUs
  end

  # Forward ports
  config.vm.network "forwarded_port", guest: 9300, host: 9300
  config.vm.network "forwarded_port", guest: 9200, host: 9200
  config.vm.network "forwarded_port", guest: 5601, host: 5601
  # config.vm.network "forwarded_port", guest: 8080, host: 8081
  config.vm.network "forwarded_port", guest: 6379, host: 6379
  config.vm.network "forwarded_port", guest: 9042, host: 9042
  config.vm.network "forwarded_port", guest: 5044, host: 5044
  config.vm.network "forwarded_port", guest: 9601, host: 9601


  config.vm.network "forwarded_port", guest: 9092, host: 9092
  config.vm.network "forwarded_port", guest: 9101, host: 9101
  config.vm.network "forwarded_port", guest: 9021, host: 9021
  config.vm.network "forwarded_port", guest: 8080, host: 8080
  config.vm.network "forwarded_port", guest: 9090, host: 9090
  config.vm.network "forwarded_port", guest: 7077, host: 7077
  config.vm.network "forwarded_port", guest: 9042, host: 9042
  config.vm.network "forwarded_port", guest: 2181, host: 2181
  config.vm.network "forwarded_port", guest: 29092, host: 29092


   
  # Provisioning: Install Docker
#   config.vm.provision "shell", inline: <<-SHELL
#   # Update package list and install necessary packages
#   apt-get update
#   apt-get upgrade -y

#   # Install Java (OpenJDK 11)
#   apt-get install -y openjdk-11-jdk

#   # Install Python 3.11
#   # apt-get install -y software-properties-common
#   # add-apt-repository ppa:deadsnakes/ppa
#   # apt-get update
#   # apt-get install -y python3.11 python3.11-distutils python3.11-venv

#   # Install pip for Python 3.11
#   # curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
#   # python3.11 get-pip.py

#   # Verify installations
#   java -version
#   sudo apt-get install python3-pip -y
#   # python3.11 --version
#   # pip3.11 --version 

#   # Install prerequisite packages for Docker
#   apt-get install -y apt-transport-https ca-certificates curl gnupg lsb-release

#   # Add Docker’s official GPG key
#   curl -fsSL https://download.docker.com/linux/ubuntu/gpg | gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

#   # Set up the Docker stable repository
#   echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | tee /etc/apt/sources.list.d/docker.list > /dev/null

#   # Update package list and install Docker
#   apt-get update
#   apt-get install -y docker-ce docker-ce-cli containerd.io docker-compose-plugin

#   # Add user to the Docker group and restart shell
#   usermod -aG docker ${USER}
#   su - ${USER} -c "vagrant"

#   # Install Minikube (requires Docker to be running)
#   curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
#   chmod +x minikube-linux-amd64
#   sudo mv minikube-linux-amd64 /usr/local/bin/minikube
# SHELL

end

