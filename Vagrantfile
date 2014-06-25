# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    config.vm.box = 'hashicorp/precise64'

    # config.vm.network :forwarded_port, guest: 3306, host: 3306

    config.vm.provider "virtualbox" do |v|
        v.customize ["modifyvm", :id, "--memory", "1024"]
    end

    # install the latest version of chef
    config.omnibus.chef_version = :latest

    # enable berkshelf
    config.berkshelf.enabled = true

    # run chef-solo
    config.vm.provision :chef_solo do |chef|
        chef.data_bags_path = "data_bags"
        chef.add_recipe "redis::install"
        chef.add_recipe "logplex"
    end
end
