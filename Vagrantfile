VAGRANTFILE_API_VERSION = "2"

# Run $ vagrant plugin install vagrant-vbguest
# See https://github.com/dotless-de/vagrant-vbguest

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

    #config.vm.box = "bento/ubuntu-16.10"
    config.vm.box = "ubuntu/yakkety64"

    config.vm.provider "virtualbox" do |vb|
        # Display the VirtualBox GUI when booting the machine
        vb.gui = true

        # Customize the amount of memory on the VM:
        vb.memory = "4096"
    end

    # Run Ansible from the Vagrant VM
    config.vm.provision "ansible_local" do |ansible|
        ansible.playbook = "playbook.yml"
    end

end
