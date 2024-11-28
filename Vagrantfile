Vagrant.configure("2") do |config|

    config.vm.define "jenkins" do |jenkins|
      jenkins.vm.box = "ubuntu/focal64"
      jenkins.vm.hostname = "web01"
      jenkins.vm.network "private_network", ip: "192.168.56.40"
      jenkins.vm.provider "virtualbox" do |v|
       v.name = "jenkins"
       v.memory = 2048
       v.cpus = 1
    end
end
    config.vm.define "ansible" do |ansible|
      ansible.vm.box = "centos/7"
      ansible.vm.hostname = "ansible"
      ansible.vm.network "private_network", ip: "192.168.56.41"
      ansible.vm.provider "virtualbox" do |v|
       v.name = "ansible"
       v.memory = 2048
       v.cpus = 1
    end
end

    config.vm.define "ansnode01" do |ansnode01| 
      ansnode01.vm.box = "centos/7"
      ansnode01.vm.hostname = "kubenode01"
      ansnode01.vm.network "private_network", ip: "192.168.56.42"
      ansnode01.vm.provider "virtualbox" do |v|
       v.name = "ansible"
       v.memory = 512 
       v.cpus = 1

    end
end
  
    config.vm.define "ansnode02" do |ansnode02|
      ansnode02.vm.box = "centos/7"
      ansnode02.vm.hostname = "ansnode02"
      ansnode02.vm.network "private_network", ip: "192.168.56.43"
      ansnode02.vm.provider "virtualbox" do |v|
       v.name = "ansible"
       v.memory = 512
       v.cpus = 1

    end

end
  
    config.vm.define "ansnode03" do |ansnode03|
       ansnode03.vm.box = "centos/7"
       ansnode03.vm.hostname = "ansnode03"
       ansnode03.vm.network "private_network", ip: "192.168.56.44"
       ansnode03.vm.provider "virtualbox" do |v|
        v.name = "ansible"
        v.memory = 512
        v.cpus = 1
    end

end

    config.vm.define "docker" do |docker|
        docker.vm.box = "ubuntu/focal64"
        docker.vm.hostname = "docker"
        docker.vm.network "private_network", ip: "192.168.56.45"
      end
    config.vm.define "web01" do |web01|
        web01.vm.box = "ubuntu/focal64"
        web01.vm.hostname = "web01"
        web01.vm.network "private_network", ip: "192.168.56.46"
      end
    config.vm.define "web02" do |web02|
        web02.vm.box = "ubuntu/focal64"
        web02.vm.hostname = "web02"
        web02.vm.network "private_network", ip: "192.168.56.47"
      end

    config.vm.define "kubemaster" do |kubemaster|
      kubemaster.vm.box = "centos/7"
      kubemaster.vm.hostname = "kubemaster"
      kubemaster.vm.network "private_network", ip: "192.168.56.50"
    end

    config.vm.define "kubenode01" do |kubenode01|
      kubenode01.vm.box = "centos/7"
      kubenode01.vm.hostname = "kubenode01"
      kubenode01.vm.network "private_network", ip: "192.168.56.52"
      kubenode01.vm.provider "virtualbox" do |v|
       v.name = "ansible"
       v.memory = 5048 
       v.cpus = 2

    end
end

    config.vm.define "kubenode02" do |kubenode02|
      kubenode02.vm.box = "centos/7"
      kubenode02.vm.hostname = "kubenode02"
      kubenode02.vm.network "private_network", ip: "192.168.56.53"
    end

    config.vm.define "kubenode03" do |kubenode03|
        kubenode03.vm.box = "centos/7"
        kubenode03.vm.hostname = "kubenode03"
        kubenode03.vm.network "private_network", ip: "192.168.56.44"
      end

    config.vm.define "db01" do |db01|
      db01.vm.box = "centos/7"
      db01.vm.hostname = "db01"
      db01.vm.network "private_network", ip: "192.168.56.48"
      db01.vm.provision "shell", inline: <<-SHELL
        yum install -y wget unzip mariadb-server -y
        systemctl start mariadb
        systemctl enable mariadb
        # Additional provisioning steps for db01
      SHELL
    end
  end
