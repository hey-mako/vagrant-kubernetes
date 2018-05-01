Vagrant.require_version ">= 2.0.3"

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"

  (1..3).each do |i|
    config.vm.define "node-#{i}" do |node|
      node.vm.hostname = "node-#{i}"
      node.vm.network "private_network", ip: "192.168.50.#{i + 1}"
    end
  end
end
