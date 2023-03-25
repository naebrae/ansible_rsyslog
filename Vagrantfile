# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|


  config.vm.define :logsrv7, autostart: false do |logsrv7_config|
    logsrv7_config.vm.box = "centos/7"
    logsrv7_config.vm.network "private_network", ip: "172.16.1.207"

    logsrv7_config.vm.provider "virtualbox" do |logsrv7_vb|
      logsrv7_vb.name = "logsrv7"
    end
    logsrv7_config.vm.provision "shell", inline: <<-SHELL
      echo "172.16.1.207	logsrv7.lab.local	logsrv7	log.lab.local" >> /etc/hosts
      echo "172.16.1.107	logcli7.lab.local	logcli7" >> /etc/hosts
    SHELL
  end

  config.vm.define :logcli7, autostart: false do |logcli7_config|
    logcli7_config.vm.box = "centos/7"
    logcli7_config.vm.network "private_network", ip: "172.16.1.107"

    logcli7_config.vm.provider "virtualbox" do |logcli7_vb|
      logcli7_vb.name = "logcli7"
    end
    logcli7_config.vm.provision "shell", inline: <<-SHELL
      echo "172.16.1.107	logcli7.lab.local	logcli7" >> /etc/hosts
      echo "172.16.1.207	logsrv7.lab.local	logsrv7	log.lab.local" >> /etc/hosts
      echo "172.16.1.208	logsrv8.lab.local	logsrv8" >> /etc/hosts
      echo "172.16.1.209	logsrv9.lab.local	logsrv9" >> /etc/hosts
      echo "172.16.1.211	logsrv11.lab.local	logsrv11" >> /etc/hosts
      echo "172.16.1.222	logsrv22.lab.local	logsrv22" >> /etc/hosts
    SHELL
  end

  config.vm.define :logsrv8, autostart: false do |logsrv8_config|
    logsrv8_config.vm.box = "almalinux/8"
    logsrv8_config.vm.network "private_network", ip: "172.16.1.208"

    logsrv8_config.vm.provider "virtualbox" do |logsrv8_vb|
      logsrv8_vb.name = "logsrv8"
    end
    logsrv8_config.vm.provision "shell", inline: <<-SHELL
      echo "172.16.1.208	logsrv8.lab.local	logsrv8	log.lab.local" >> /etc/hosts
      echo "172.16.1.108	logcli8.lab.local	logcli8" >> /etc/hosts
    SHELL
  end

  config.vm.define :logcli8, autostart: false do |logcli8_config|
    logcli8_config.vm.box = "almalinux/8"
    logcli8_config.vm.network "private_network", ip: "172.16.1.108"

    logcli8_config.vm.provider "virtualbox" do |logcli8_vb|
      logcli8_vb.name = "logcli8"
    end
    logcli8_config.vm.provision "shell", inline: <<-SHELL
      echo "172.16.1.108	logcli8.lab.local	logcli8" >> /etc/hosts
      echo "172.16.1.208	logsrv8.lab.local	logsrv8	log.lab.local" >> /etc/hosts
      echo "172.16.1.207	logsrv7.lab.local	logsrv7" >> /etc/hosts
      echo "172.16.1.209	logsrv9.lab.local	logsrv9" >> /etc/hosts
      echo "172.16.1.211	logsrv11.lab.local	logsrv11" >> /etc/hosts
      echo "172.16.1.222	logsrv22.lab.local	logsrv22" >> /etc/hosts
    SHELL
  end

  config.vm.define :logsrv9, autostart: false do |logsrv9_config|
    logsrv9_config.vm.box = "almalinux/9"
    logsrv9_config.vm.network "private_network", ip: "172.16.1.209"

    logsrv9_config.vm.provider "virtualbox" do |logsrv9_vb|
      logsrv9_vb.name = "logsrv9"
    end
    logsrv9_config.vm.provision "shell", inline: <<-SHELL
      echo "172.16.1.209	logsrv9.lab.local	logsrv9	log.lab.local" >> /etc/hosts
      echo "172.16.1.109	logcli9.lab.local	logcli9" >> /etc/hosts
    SHELL
  end

  config.vm.define :logcli9, autostart: false do |logcli9_config|
    logcli9_config.vm.box = "almalinux/9"
    logcli9_config.vm.network "private_network", ip: "172.16.1.109"

    logcli9_config.vm.provider "virtualbox" do |logcli9_vb|
      logcli9_vb.name = "logcli9"
    end
    logcli9_config.vm.provision "shell", inline: <<-SHELL
      echo "172.16.1.109	logcli9.lab.local	logcli9" >> /etc/hosts
      echo "172.16.1.209	logsrv9.lab.local	logsrv9	log.lab.local" >> /etc/hosts
      echo "172.16.1.207	logsrv7.lab.local	logsrv7" >> /etc/hosts
      echo "172.16.1.208	logsrv8.lab.local	logsrv8" >> /etc/hosts
      echo "172.16.1.211	logsrv11.lab.local	logsrv11" >> /etc/hosts
      echo "172.16.1.222	logsrv22.lab.local	logsrv22" >> /etc/hosts
    SHELL
  end

  config.vm.define :logsrv11, autostart: false do |logsrv11_config|
    logsrv11_config.vm.box = "debian/bullseye64"
    logsrv11_config.vm.network "private_network", ip: "172.16.1.211"

    logsrv11_config.vm.provider "virtualbox" do |logsrv11_vb|
      logsrv11_vb.name = "logsrv11"
    end
    logsrv11_config.vm.provision "shell", inline: <<-SHELL
      echo "172.16.1.211	logsrv11.lab.local	logsrv11	log.lab.local" >> /etc/hosts
      echo "172.16.1.111	logcli11.lab.local	logcli11" >> /etc/hosts
    SHELL
  end

  config.vm.define :logcli11, autostart: false do |logcli11_config|
    logcli11_config.vm.box = "debian/bullseye64"
    logcli11_config.vm.network "private_network", ip: "172.16.1.111"

    logcli11_config.vm.provider "virtualbox" do |logcli11_vb|
      logcli11_vb.name = "logcli11"
    end
    logcli11_config.vm.provision "shell", inline: <<-SHELL
      echo "172.16.1.111	logcli11.lab.local	logcli11" >> /etc/hosts
      echo "172.16.1.211	logsrv11.lab.local	logsrv11	log.lab.local" >> /etc/hosts
      echo "172.16.1.207	logsrv7.lab.local	logsrv7" >> /etc/hosts
      echo "172.16.1.208	logsrv8.lab.local	logsrv8" >> /etc/hosts
      echo "172.16.1.209	logsrv9.lab.local	logsrv9" >> /etc/hosts
      echo "172.16.1.222	logsrv22.lab.local	logsrv22" >> /etc/hosts
    SHELL
  end

  config.vm.define :logsrv20, autostart: false do |logsrv20_config|
    logsrv20_config.vm.box = "bento/ubuntu-20.04"
    logsrv20_config.vm.network "private_network", ip: "172.16.1.220"

    logsrv20_config.vm.provider "virtualbox" do |logsrv20_vb|
      logsrv20_vb.name = "logsrv20"
    end
    logsrv20_config.vm.provision "shell", inline: <<-SHELL
      echo "172.16.1.220	logsrv20.lab.local	logsrv20	log.lab.local" >> /etc/hosts
      echo "172.16.1.120	logcli20.lab.local	logcli20" >> /etc/hosts
    SHELL
  end

  config.vm.define :logcli20, autostart: false do |logcli20_config|
    logcli20_config.vm.box = "bento/ubuntu-20.04"
    logcli20_config.vm.network "private_network", ip: "172.16.1.120"

    logcli20_config.vm.provider "virtualbox" do |logcli20_vb|
      logcli20_vb.name = "logcli20"
    end
    logcli20_config.vm.provision "shell", inline: <<-SHELL
      echo "172.16.1.120	logcli20.lab.local	logcli20" >> /etc/hosts
      echo "172.16.1.220	logsrv20.lab.local	logsrv20	log.lab.local" >> /etc/hosts
      echo "172.16.1.207	logsrv7.lab.local	logsrv7" >> /etc/hosts
      echo "172.16.1.208	logsrv8.lab.local	logsrv8" >> /etc/hosts
      echo "172.16.1.209	logsrv9.lab.local	logsrv9" >> /etc/hosts
      echo "172.16.1.211	logsrv11.lab.local	logsrv11" >> /etc/hosts
    SHELL
  end

  config.vm.define :logsrv22, autostart: false do |logsrv22_config|
    logsrv22_config.vm.box = "bento/ubuntu-22.04"
    logsrv22_config.vm.network "private_network", ip: "172.16.1.222"

    logsrv22_config.vm.provider "virtualbox" do |logsrv22_vb|
      logsrv22_vb.name = "logsrv22"
    end
    logsrv22_config.vm.provision "shell", inline: <<-SHELL
      echo "172.16.1.222	logsrv22.lab.local	logsrv22	log.lab.local" >> /etc/hosts
      echo "172.16.1.122	logcli22.lab.local	logcli22" >> /etc/hosts
    SHELL
  end

  config.vm.define :logcli22, autostart: false do |logcli22_config|
    logcli22_config.vm.box = "bento/ubuntu-22.04"
    logcli22_config.vm.network "private_network", ip: "172.16.1.122"

    logcli22_config.vm.provider "virtualbox" do |logcli22_vb|
      logcli22_vb.name = "logcli22"
    end
    logcli22_config.vm.provision "shell", inline: <<-SHELL
      echo "172.16.1.122	logcli22.lab.local	logcli22" >> /etc/hosts
      echo "172.16.1.222	logsrv22.lab.local	logsrv22	log.lab.local" >> /etc/hosts
      echo "172.16.1.207	logsrv7.lab.local	logsrv7" >> /etc/hosts
      echo "172.16.1.208	logsrv8.lab.local	logsrv8" >> /etc/hosts
      echo "172.16.1.209	logsrv9.lab.local	logsrv9" >> /etc/hosts
      echo "172.16.1.211	logsrv11.lab.local	logsrv11" >> /etc/hosts
    SHELL
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
    ansible.groups = {
      "logsrv" => ["logsrv7","logsrv8","logsrv9","logsrv11","logsrv20","logsrv22"],
      "logcli" => ["logcli7","logcli8","logcli9","logcli11","logcli20","logcli22"],
    }

  end
  config.vm.synced_folder ".", "/home/vagrant/sync", type: "rsync", disabled: true
  config.vm.synced_folder ".", "/vagrant", disabled: true
end

