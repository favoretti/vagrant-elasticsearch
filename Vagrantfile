Vagrant.configure(2) do |config|

  config.vm.box = "hashicorp/precise64"
  config.vm.hostname = "ES-2.0.0"
  config.vm.provision :shell, path: "bootstrap.sh"
  config.vm.network :forwarded_port, host: 9200, guest: 9200

  config.vm.provider "virtualbox" do |v|
    v.memory = 1024
    v.cpus = 1
    v.name = config.vm.hostname.to_s
  end

end
