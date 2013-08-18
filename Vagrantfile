# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|
  config.vm.box = "base-hadoop"
  config.vm.provision :puppet do |puppet|
     puppet.manifests_path = "manifests"
     puppet.manifest_file  = "base-hadoop.pp"
     puppet.module_path = "modules"
  end

  config.vm.define :hadoop1 do |hadoop1_config|
    hadoop1_config.vm.network :hostonly, "192.168.1.11"
    hadoop1_config.vm.host_name = "hadoop1"
  end

  config.vm.define :hadoop2 do |hadoop2_config|
    hadoop2_config.vm.network :hostonly, "192.168.1.12"
    hadoop2_config.vm.host_name = "hadoop2"
  end
  
  config.vm.define :master do |master_config|
    master_config.vm.network :hostonly, "192.168.1.10"
    master_config.vm.host_name = "master"
    master_config.vm.forward_port 50070, 50070
    master_config.vm.network :forwarded_port, guest: 9000, host: 9000
    master_config.vm.network :forwarded_port, guest: 9001, host: 9001
  end

end
