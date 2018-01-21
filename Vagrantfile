Vagrant.configure("2") do |config|    
    config.vm.define "proxmox-devel" do |machine|
        machine.vm.provider :virtualbox do |vbox|
            vbox.name = "proxmox_devel"
            vbox.customize ["modifyvm", :id, "--memory", 2048]
            vbox.customize ["modifyvm", :id, "--cpus", 4]
        end
        machine.vm.synced_folder ".", "/vagrant"
        machine.vm.box = "debian/stretch64"
        machine.ssh.insert_key = false
        machine.vm.network "forwarded_port", guest: 8006, host: 8006
        machine.vm.hostname = "proxmox-devel"
        #Install some ansible deps and ansible itself
        machine.vm.provision "shell", inline: "sudo apt-get install -y python-pip python-dev"
        machine.vm.provision "shell", inline: "sudo pip install -U pip"
        machine.vm.provision "shell", inline: "sudo pip install -U setuptools"
        machine.vm.provision "shell", inline: "sudo pip install ansible"
        #And execute ansible when all of this will be done.
        machine.vm.provision :ansible do |ansible|
            ansible.limit = "all"
            ansible.playbook = "pve.yml"
        end
    end
    config.vm.post_up_message = "Proxmox VE Development VM is ready. To access it type vagrant ssh. You should first reboot vm before doing anything"
end
