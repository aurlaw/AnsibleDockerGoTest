VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.network "forwarded_port", guest: 9090, host: 9090

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "site.yml"
  end


  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
    v.cpus = 2
  end  
end