Vagrant.configure("2") do |config|
    config.vm.synced_folder '.', '/vagrant', disabled: true
    config.ssh.insert_key = false # to use the global key instead of one key per VM
    config.vm.provider :virtualbox do |v|
      v.memory = 512
      v.cpus = 1
    end

    config.vm.define :srv_web do |srv_web|
      srv_web.vm.box = "bento/ubuntu-24.04"
      srv_web.vm.hostname = "app1"
      srv_web.vm.network "private_network", ip: "192.168.56.111"
    end

    config.vm.define :srv_db do |srv_db|
      srv_db.vm.box = "bento/ubuntu-24.04"
      srv_db.vm.hostname = "app2"
      srv_db.vm.network "private_network", ip: "192.168.56.112"
    end

  end

