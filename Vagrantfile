
Vagrant.configure("2") do |config|

  config.vm.define "linuxserver" do |linuxserver|

    linuxserver.vm.box = "ubuntu/jammy64"

    linuxserver.vm.network "forwarded_port", guest:8080, host:8083

    linuxserver.vm.network "forwarded_port", guest: 3307, host: 3307 # Pour MySQL

    linuxserver.vm.network "private_network", type: "static", ip:"192.168.0.10"

    linuxserver.vm.synced_folder "tomcatwebapps", "/opt/tomcat/webpps"

    linuxserver.vm.provider "virtualbox" do |vb|

      vb.gui = false
      vb.memory = "1024"
      vb.name = "linuxserver"


    end
  end

  
end
