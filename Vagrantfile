hosts = ['centos']

Vagrant.configure('2') do |config|

  config.vm.box = 'centos/7'
  config.vm.define hostname = 'centos'
  config.vm.provider :libvirt do |libvirt|
    libvirt.driver = 'kvm'
    libvirt.cpus = 2
    libvirt.memory = '1024'
  end
  
  config.vm.provision 'ansible' do |ansible|
        ansible.limit = hostname
        ansible.compatibility_mode = '2.0'
        ansible.verbose = false
        ansible.playbook = 'main.yml'
        ansible.vault_password_file = 'secrets/vault_password'
   end
end
