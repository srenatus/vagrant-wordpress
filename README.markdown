# Vagrant Box to Showcase Wordpress Deployment

## Install Vagrant and Provision Wordpress

Install Vagrant first (see [http://vagrantup.com](http://vagrantup.com)).
Tested on OSX 10.8 with Virtualbox 4.2.1. Just enter 

	vagrant up

in your console. This will start the download of the vagrant box from Opscode (if you not already have it) and immediately provisions a LAMP stack with Wordpress ready to use :-)

## Use the local Wordpress Deployment

Open 

	http://wordpress.42foo.com:4567/wp-admin/install.php

in your Browser.

## Start Over

	vagrant destroy
	vagrant up


