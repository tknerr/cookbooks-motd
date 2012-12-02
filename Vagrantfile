
Vagrant::Config.run do |config|

  config.vm.box = "opscode-ubuntu-12.04"
  config.vm.box_url = "https://opscode-vm.s3.amazonaws.com/vagrant/boxes/opscode-ubuntu-12.04.box"

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