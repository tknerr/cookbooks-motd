
Vagrant::Config.run do |config|

  config.vm.box = "ubuntu-12.04-server-amd64-vagrant"
  config.vm.box_url = "http://dl.dropbox.com/u/13494216/ubuntu-12.04-server-amd64-vagrant.box"

  config.vm.host_name = "motd-vm"
  config.vm.network :hostonly, "192.168.33.10"

  config.vm.provision :chef_solo do |chef|
     chef.cookbooks_path = ".."
     chef.add_recipe "vagrant-ohai"
     chef.add_recipe "motd"
  end

  #config.vm.provision :chef_client do |chef|
  #   chef.chef_server_url = "http://33.33.3.10:4000"
  #   chef.validation_key_path = "W:\\repo\\my-chef-repo\\.chef\\validation.pem"
  #   chef.environment = "_default"  
  #
  #   chef.add_recipe "vagrant-ohai"
  #   chef.add_recipe "motd"
  #end

end