
Vagrant::Config.run do |config|

  config.vm.box = "ubuntu-12.04-server-amd64-vagrant"
  config.vm.box_url = "W:\\boxes\\ubuntu-12.04-server-amd64-vagrant.box"

  config.vm.host_name = "motd-vm"
  config.vm.network :hostonly, "192.168.33.10"

  config.vm.provision :chef_solo do |chef|
     chef.cookbooks_path = ".."
     chef.add_recipe "vagrant-ohai"
     chef.add_recipe "motd"
  end
end