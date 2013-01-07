# -*- mode: ruby -*-
# vi: set ft=ruby :
require File.dirname(__FILE__)+'/copy_my_conf'

#This is a sample vagrant file
Vagrant::Config.run do |config|
  config.vm.box = "precise64"
  config.ssh.forward_agent = true
  
  config.vm.provision CopyMyConf do |copy_conf|
    copy_conf.ssh = true
    copy_conf.vim = true
    copy_conf.git = true
    copy_conf.user_home = "/home/vagrant"
  end

  config.vm.customize ["modifyvm", :id, "--memory", 2048]
  config.vm.customize ["modifyvm", :id, "--cpus", 4]
end

