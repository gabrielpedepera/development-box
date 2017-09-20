# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = '2'.freeze

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = 'bento/ubuntu-16.04'
  config.vm.network 'private_network', ip: '192.168.50.4'
  config.ssh.forward_agent = true

  config.vm.define 'development' do |dev|
    dev.vm.synced_folder '~/workspace', '/home/vagrant/workspace'

    dev.vm.provision 'ansible' do |ansible|
      ansible.playbook = 'playbook.yml'
      ansible.host_key_checking = false
      ansible.extra_vars = { ansible_ssh_user: 'vagrant' }
      ansible.become = true
    end
  end
end
