Vagrant.configure("2") do |config|
  config.vm.box = "debian/bullseye64"

  # Servidor DHCP
  config.vm.define "srv" do |srv|
    srv.vm.hostname = "srv"
    srv.vm.network "private_network", ip: "192.168.57.10", virtualbox__intnet: "intnet"
  end

  # Cliente c1
  config.vm.define "c1" do |c1|
    c1.vm.hostname = "c1"
    c1.vm.network "private_network", 
      type: "dhcp", 
      virtualbox__intnet: "intnet",
      mac: "0800275CF431"
  end

  # Cliente printer
  config.vm.define "printer" do |printer|
    printer.vm.hostname = "printer"
    printer.vm.network "private_network", 
      type: "dhcp", 
      virtualbox__intnet: "intnet",
      mac: "0800275CF437"
  end
end
