Vagrant.configure("2") do |config|
  config.vagrant.plugins = "vagrant-env" # Install plugin to support .env files
  config.env.enable # enable .env support plugin (it will let us easily enable cloud_init support)

  # Give a custom name for a VM created by this script for a Vagrant CLI
  config.vm.define "focal-server-cloudimg-amd64-vagrant"

  # Name for the box image downloaded from the box_url
  # it will be used to create a folder inside ~/.vagrant.d/boxes to avoid re-downloading
  config.vm.box = "focal-server-cloudimg-amd64-vagrant"

  # URL used as a source for the vm.box defined above
  config.vm.box_url = "https://cloud-images.ubuntu.com/focal/current/focal-server-cloudimg-amd64-vagrant.box"

  config.vm.provider "virtualbox" do |v|
    # Name visible inside your Virtualbox UI
    v.name = "cloud-init-ubuntu-test"
  end

  # cloud-init script
  config.vm.cloud_init do |cloud_init|
    # With Ubuntu cloud images you have to use cloud_init to get an access
    cloud_init.content_type = "text/cloud-config"
    cloud_init.path = "cloud-init-test.yml"
  end
end
