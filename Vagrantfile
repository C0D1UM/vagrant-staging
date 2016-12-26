# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.define "app" do |app|
    app.vm.hostname = "app"

    app.vm.network :private_network, ip: "10.134.5.5"
    app.vm.network :public_network
  end

  config.vm.define "database" do |db|
    db.vm.hostname = "database"

    db.vm.network :private_network, ip: "10.134.5.6"
    db.vm.network :public_network
    db.vm.network :forwarded_port, guest: 5432, host: 15432

    db.vm.provision :shell, :path => "bootstrap/postgresql.sh"
  end
end
