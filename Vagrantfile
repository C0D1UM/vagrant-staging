# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.define "proxy" do |proxy|
    proxy.vm.hostname = "nginx"

    proxy.vm.network :private_network, ip: "10.134.5.7"
  end

  config.vm.define "app" do |app|
    app.vm.hostname = "app"

    app.vm.network :private_network, ip: "10.134.5.5"
  end

  config.vm.define "database" do |db|
    db.vm.hostname = "database"

    db.vm.network :private_network, ip: "10.134.5.6"
  end


  # config.vm.provision "shell", inline: <<-SHELL
  #   apt-get update
  #   apt-get install -y apache2
  # SHELL
end
