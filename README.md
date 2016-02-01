cakephp-vagrant
==============


Vagrantfile with shell script provision will setup you CakePHP 3.x for you.

----------


how it works
-----------------

Clone Repo:

    git clone https://github.com/mbamarante/cakephp-vagrant.git /my/workspace/

Change IP address to avoid conflicts and "app-name" with your project/app name. 

    config.vm.network "private_network", ip: "192.168.33.10"
    config.vm.hostname = "app-name.local"

Start! Your app will be available at http://app-name.local/

    vagrant up

> **Dependencies:**

> - [vagrant-hostupdater](https://github.com/cogitatio/vagrant-hostsupdater) will update your /etc/hosts mapping VM IP address to VM hostname:
> `vagrant plugin install vagrant-hostsupdater`

Possible Issues

vagrant-hostupdate needs zlib1g-dev and nokogiri.

    sudo apt-get install zlib1g-dev
    sudo gem install nokogiri -v '1.6.7.2'
