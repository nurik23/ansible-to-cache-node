Vagrant.configure("2") do |config|
  config.vm.box = "subutai/stretch"
  config.vm.synced_folder "./ansible", "/etc/ansible", disabled: false

   config.vm.provision 'shell', inline: <<-SHELL
    sudo apt-get update
    sudo apt-get install software-properties-common -y
    sudo apt-add-repository ppa:ansible/ansible
    sudo apt-get update
    sudo apt-get install sshpass -y
    sudo apt-get install ansible -y 
    mkdir Peer
    sudo rm -rf /etc/ansible/ansible.cfg.dpkg-new
    sudo rm -rf /etc/ansible/hosts.dpkg-new
    exit 0
  SHELL
end
