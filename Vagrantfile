# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "ubuntu/trusty64"

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. 
  # Accessing "localhost:10042" will access port 10042 on the guest machine.
  # 10042 is the default port that Mathoid runs on.
  config.vm.network "forwarded_port", guest: 10042, host: 10042

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  # NOTE: required for the config.vm.synced_folder below
  #config.vm.network "private_network", ip: "192.168.33.10"

  # Share the home directory for access to host source code
  # and use NFS for 10-100x speedup:
  # NOTE: you must have a network configured above, such as config.vm.network
  #config.vm.synced_folder "~/", "/host", nfs: true

  config.vm.provision "chef_solo" do |chef|
    chef.add_recipe "nodejs"
    chef.add_recipe "phantomjs"
    chef.add_recipe "nfs"
    chef.add_recipe "git"
  end

  # Copy the user's .gitconfig (if it exists) so they don't
  # have to reconfigure Git in the VM:
  config.vm.provision "file", source: "~/.gitconfig", destination: "/home/vagrant/.gitconfig"

  # Install Mathoid PPA and distribution:
  config.vm.provision "shell", inline: "add-apt-repository -y ppa:physikerwelt/mathoid"
  config.vm.provision "shell", inline: "apt-get -y update"
  config.vm.provision "shell", inline: "apt-get install -y mathoid"

end
