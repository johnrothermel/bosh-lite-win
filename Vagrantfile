Vagrant.configure(2) do |config|
  config.vm.box = "base"
    config.vm.define "cf" do |cf|
      cf.vm.provider :virtualbox do |v, override|
        override.vm.box = 'cloudfoundry/bosh-lite'
        override.vm.box_version = '388'
		 
        # To use a different IP address for the bosh-lite director, uncomment this line:
        override.vm.network :private_network, ip: '192.168.50.4', id: :local
        override.vm.network :public_network
      end
    end
					  
    config.vm.define "boshlite" do |boshlite|
      boshlite.vm.provider :virtualbox do |v, override|
        override.vm.box = 'ubuntu/trusty64'
       
        # To use a different IP address for the bosh-lite director, uncomment this line:
        override.vm.network :private_network, ip: '192.168.50.14', id: :local
        override.vm.network :public_network
        v.memory = 6144
        v.cpus = 2
      end
    end
end
