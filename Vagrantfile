# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://atlas.hashicorp.com/search.
  config.vm.box = "fiercepunchstudios/vagabond"
  config.vm.hostname = "fiercepunchstudios.github.io"

  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
    v.cpus = 2
  end

  # MIDDLEMAN
  config.vm.provision :shell, privileged: false, inline: <<-MIDDLEMAN
    gem install middleman -v 3.4.0
    npm install -g bower

    git clone git://github.com/axyz/middleman-zurb-foundation.git ~/.middleman/zurb-foundation
    # Or manually instead of template: http://blachniet.com/blog/middleman-foundation/

    echo 'alias bemb="bundle exec middleman -b 0.0.0.0"' >> ~/.profile
  MIDDLEMAN

  config.vm.network "forwarded_port", guest: 4567, host: 4567
end
