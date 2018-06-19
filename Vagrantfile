# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure('2') do |config|
  config.vm.box = 'bento/centos-7.3'

  config.vm.define :server do |host|
    hostname = 'server'
    private_ip_address = '192.168.33.10'

    host.vm.hostname = hostname
    host.vm.network 'private_network', ip: private_ip_address
    host.vm.provision :shell, path: 'install-common-package.sh'
    host.vm.provision :shell, path: 'stop-security.sh'
    host.vm.provision :shell, path: 'install-elasticsearch.sh'
  end
end
