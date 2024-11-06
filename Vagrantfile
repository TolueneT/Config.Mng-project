Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"

  # Database Server VM
  config.vm.define "db_server" do |db|
    db.vm.hostname = "db-server"
    db.vm.network "private_network", ip: "192.168.56.10" # Static IP
    db.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
      vb.cpus = 1
    end
  end

  # Web Server VM
  config.vm.define "web_server" do |web|
    web.vm.hostname = "web-server"
    web.vm.network "private_network", ip: "192.168.56.11" # Static IP
    web.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
      vb.cpus = 1
    end
  end

  # NFS Server VM
  config.vm.define "nfs_server" do |nfs|
    nfs.vm.hostname = "nfs-server"
    nfs.vm.network "private_network", ip: "192.168.56.12" # Static IP
    nfs.vm.provider "virtualbox" do |vb|
      vb.memory = "512"
      vb.cpus = 1
    end
  end
end
