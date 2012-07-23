Vagrant::Config.run do |config|
  # All Vagrant configuration is done here. For a detailed explanation
  # and listing of configuration options, please view the documentation
  # online.

  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "precise64"                 

  # Forward guest port 80 to host port 4567 and name the mapping "web"
  config.vm.forward_port  80, 4567  
  
  # ensure the latest packages
  config.vm.provision :chef_solo do |chef|  

    # This path will be expanded relative to the project directory
    chef.cookbooks_path = "cookbooks"
  
    #this recipe we want to run
    #chef.add_recipe("apt") 
    chef.add_recipe("wordpress_demo") 
  
    chef.json.merge!({
      :mysql => {
        :server_debian_password => "secure_password",
        :server_root_password => "secure_password",
        :server_repl_password => "secure_password"
      },
      :wordpress_hostname => "wordpress.smackaho.st"
    })
  
  end
end
