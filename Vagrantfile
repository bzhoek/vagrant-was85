VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "centos-65-i386-nocm"
  config.vm.box_url = "http://puppet-vagrant-boxes.puppetlabs.com/centos-65-i386-virtualbox-nocm.box"

  config.ssh.forward_agent = true
  config.ssh.forward_x11 = true

  config.vm.network "forwarded_port", guest: 9043, host: 9043 # admin console
  config.vm.network "forwarded_port", guest: 9080, host: 9080 # server1

  config.vm.define 'd-was-01' do |server|
    server.vm.hostname = "d-was-01.localdomain"
    server.vm.network "private_network", ip: "10.0.3.20"
    config.vm.provider :virtualbox do |vb|
      vb.memory = 2048
      vb.cpus = 2
    end
  end

  config.vm.synced_folder ".", "/vagrant", :mount_options => ["dmode=777","fmode=777"]

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "websphere.yml"
    # ansible.tags = "debug"
  end

end
