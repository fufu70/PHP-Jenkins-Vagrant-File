# -*- mode: ruby -*-
# vi: set ft=ruby :
#
# This is a simple PHP jenkins box project assocaited with all PHP projects avaialble inside of SaleCents
# Its assumed that you have included the phpvagrant.box file:
#
#     vagrant box add phpvagrantbox phpvagrant.box
#

def set_hostname(server)
  server.vm.provision 'shell', inline: "hostname #{server.vm.hostname}"
end

Vagrant.configure("2") do |config|
  config.vm.define 'php-jenkins-breakfast-box' do |n|
    n.vm.box = 'fufu70/php-jenkins-breakfast'
    n.vm.hostname = 'php-jenkins-breakfast-box'
    n.vm.network 'private_network', ip: '192.168.205.40'
    set_hostname(n)
  end

  config.vm.post_up_message = "You can access Jenkins at http://192.168.205.40:8080"
end
