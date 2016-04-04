Vagrant.configure("2") do |config|
  config.vm.box = "fgrehm/trusty64-lxc"
  config.vm.provider :lxc do |lxc|
    lxc.customize 'cgroup.memory.limit_in_bytes', '1024M'
  end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "vagrant.yml"
  end
end
