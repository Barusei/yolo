
Vagrant.configure("2") do |config|
  
  config.vm.box = "ubuntu/trusty64"

  config.vm.network "forwarded_port", guest: 80, host: 8080

  config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"

  # Create a private network, which allows host-only access to the machine
  config.vm.network "private_network", ip: "192.168.33.10"

  # Bridged networks make the machine appear as another physical device on
  # your network.
  config.vm.network "public_network"

  # the path on the guest to mount the folder.
  config.vm.synced_folder "../data", "/vagrant_data"

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
 
  # Provisioning configuration for Ansible.
config.vm.provision "ansible" do |ansible|
  ansible.playbook = "playbook.yml"
config.vm.network "forwarded_port", guest: 3000, host: 3000  
  end
end
