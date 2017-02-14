VAGRANTFILE_API_VERSION = "2"

# Run $ vagrant plugin install vagrant-vbguest
# See https://github.com/dotless-de/vagrant-vbguest

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

    #config.vm.box = "bento/ubuntu-16.10"
    config.vm.box = "ubuntu/yakkety64"

    config.vm.provider "virtualbox" do |vb|
        # Display the VirtualBox GUI when booting the machine
        vb.gui = true
        vb.memory = 8192
        vb.customize ["modifyvm", :id, "--clipboard", "bidirectional"]
    end

    # Run Ansible from the Vagrant VM
    config.vm.provision "ansible_local" do |ansible|
        ansible.playbook = "ansible/bootstrap.yml"
    end

end
