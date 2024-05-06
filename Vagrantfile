
Vagrant.configure("2") do |config|

  # Define Debian 12 virtual machine
  config.vm.define "ansible-kmasing" do |ansible|
    ansible.vm.box = "generic/debian11"
    ansible.vm.hostname = "ansible-kmasing"
    ansible.vm.network "private_network", ip: "172.20.10.100"
    ansible.vm.provider "virtualbox" do |vb|
      vb.name = "ansible-kmasing"
    end
    ansible.vm.provision "shell", inline: <<-SHELL
      apt-get update
      apt-get install -y fish tmux mc git ansible tree sshpass yamllint ansible-lint
    SHELL
  end

  # Define Ubuntu 22.04 virtual machines
  config.vm.define "ubuntu1-kmasing" do |ubuntu1|
    ubuntu1.vm.box = "generic/ubuntu2204"
    ubuntu1.vm.hostname = "ubuntu1-kmasing"
    ubuntu1.vm.network "private_network", ip: "172.20.10.110"
    ubuntu1.vm.provider "virtualbox" do |vb|
      vb.name = "ubuntu1-kmasing"
    end
    ubuntu1.vm.provision "shell", inline: <<-SHELL
      apt-get update
      apt-get install -y fish tmux mc git apache2
    SHELL
  end

  config.vm.define "ubuntu2-kmasing" do |ubuntu2|
    ubuntu2.vm.box = "generic/ubuntu2204"
    ubuntu2.vm.hostname = "ubuntu2-kmasing"
    ubuntu2.vm.network "private_network", ip: "172.20.10.120"
    ubuntu2.vm.provider "virtualbox" do |vb|
      vb.name = "ubuntu2-kmasing"
    end
    ubuntu2.vm.provision "shell", inline: <<-SHELL
      apt-get update
      apt-get install -y fish tmux mc git apache2
    SHELL
  end

  # Define Oracle 9 virtual machines
  config.vm.define "oracle1-kmasing" do |oracle1|
    oracle1.vm.box = "generic-x64/oracle9"
    oracle1.vm.hostname = "oracle1-kmasing"
    oracle1.vm.network "private_network", ip: "172.20.10.200"
    oracle1.vm.provider "virtualbox" do |vb|
      vb.name = "oracle1-kmasing"
    end
    oracle1.vm.provision "shell", inline: <<-SHELL
      dnf install -y fish tmux mc git httpd
    SHELL
  end

  config.vm.define "oracle2-kmasing" do |oracle2|
    oracle2.vm.box = "generic-x64/oracle9"
    oracle2.vm.hostname = "oracle2-kmasing"
    oracle2.vm.network "private_network", ip: "172.20.10.201"
    oracle2.vm.provider "virtualbox" do |vb|
      vb.name = "oracle2-kmasing"
    end
    oracle2.vm.provision "shell", inline: <<-SHELL
      dnf install -y fish tmux mc git httpd
    SHELL
  end

end
