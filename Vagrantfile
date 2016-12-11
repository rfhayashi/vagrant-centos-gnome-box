Vagrant.configure('2') do |config|
  config.vm.box = 'bento/centos-7.2'

  # workaround for centos (see: https://github.com/mitchellh/vagrant/issues/7610)
  config.ssh.insert_key = false

  config.vm.provision 'ansible_local' do |a|
    a.sudo = true
    a.playbook = 'vagrant.yml'
    a.galaxy_role_file = 'requirements.yml'
    a.verbose = 'vv'
  end
end