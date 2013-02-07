# Vagrant Box to Showcase Wordpress Deployment

## Using Bundler, Berkshelf and Vagrant to Provision Wordpress

Tested on Debian GNU/Linux with VirtualBox 4.1.18.  Just enter

	bundle exec vagrant up

in your console. This will

1. get all dependencies as stated in `Gemfile`, i.e. [Vagrant](http://www.vagrantup.com) and [Berkshelf](http://www.berkshelf.com)
2. get all needed cookbooks (and their dependencies) as stated in `Berksfile` and
3. start the download of the vagrant box from Opscode (if you not already have it) and immediately provisions a LAMP stack with Wordpress ready to use :-)

## Use the local Wordpress Deployment

Open 

	http://wordpress.42foo.com:4567/wp-admin/install.php

in your Browser.

## Start Over

	bundle exec vagrant destroy
	bundle exec vagrant up


