Vagrant::Config.run do |config|
  config.vm.box = "precise32"
  config.vm.box_url = "http://files.vagrantup.com/precise32.box"
  config.vm.forward_port 80, 8080

  config.vm.provision :shell, :path => "change_sources_list.sh"

  config.vm.provision :chef_solo do |chef|
    chef.cookbooks_path = "cookbooks"

    chef.json = {
      :java => {
        :install_flavor => "oracle",
        :jdk_version => "7",
        :oracle => {
          :accept_oracle_download_terms => true
        }
      },
      :mysql => {
        :server_root_password => "PASSWORD",
        :server_repl_password => "PASSWORD",
        :server_debian_password => "PASSWORD"
      },
      :postgresql => {
        :password => {
          :postgres => "PASSWORD"
        }
      }
    }

    chef.add_recipe("apt")
    chef.add_recipe("build-essential")
    chef.add_recipe("git")
    chef.add_recipe("java")
    chef.add_recipe("mysql::client")
    chef.add_recipe("mysql::server")
    chef.add_recipe("postgresql::client")
    chef.add_recipe("postgresql::server")
    chef.add_recipe("zsh")
    chef.add_recipe("vim")
  end
end
