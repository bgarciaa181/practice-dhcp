Vagrant.configure("2") do |config|
  config.vm.box = "debian/bullseye64"

  # Servidor DHCP
  config.vm.define "srv" do |srv|
    srv.vm.network "public_network", bridge: "enp4s0"
    srv.vm.network "private_network", ip: "192.168.57.10", virtualbox__intnet: "intnet"
  end

  # Cliente DHCP
  config.vm.define "c1" do |c1|
    c1.vm.network "private_network", type: "dhcp", virtualbox__intnet: "intnet"
  end
end
