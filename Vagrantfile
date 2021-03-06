# not tested!!!!!!!

Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
    config.vm.provider "virtualbox" do |v|
        v.memory = 2048
        v.cpus = 2
    end
   config.vm.synced_folder "./", "/etc/ansible"

   config.vm.provision "shell", privileged: true, inline: <<-SHELL
      yum update
	  yum install ansible
      export ANSIBLE_HOST_KEY_CHECKING=False
  	  cp /etc/ansible/keys/private.pem /etc/private.pem
	    chmod 400 /etc/private.pem
   SHELL
end
