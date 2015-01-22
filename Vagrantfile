VAGRANTFILE_API_VERSION = '2'

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = 'https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box'

  config.vm.network 'private_network', ip: '192.168.33.11'

  config.vm.provider 'virtualbox' do |v|
    v.memory = 2048
    v.cpus = 2
  end

  # `vagrant ssh` したとき `root` でログインする
  config.ssh.username = 'root'

  # rootでSSH接続するためにVagrantが生成したauthorized_keysをrootでも使う
  config.vm.provision 'shell', inline: 'sudo cp -f /home/vagrant/.ssh/authorized_keys /root/.ssh'
end
