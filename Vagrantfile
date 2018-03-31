# -*- mode: ruby -*-
# vi: set ft=ruby :

# Create VM, install PHP and minimize it
Vagrant.configure("2") do |config|
  config.vm.box = "bento/debian-8.7"

  # Run Ansible playbook
  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "playbook.yml"
    ansible.install_mode = "pip"
  end

  # Minimize box
  config.vm.provision "shell", path: "minimize.sh"
end
