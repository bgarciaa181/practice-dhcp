Vagrant.configure("2") do |config|
  config.vm.define "srv" do |srv|
    srv.vm.box = "debian/bullseye64"

    srv.vm.network "public_network", bridge: "enp4s0"
    srv.vm.network "private_network",
      ip: "192.168.57.10",
      virtualbox__intnet: "intnet"
  end
end
