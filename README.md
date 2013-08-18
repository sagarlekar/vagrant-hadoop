vagrant-hadoop
==============

To start Hadoop cluster with Vagrant :
- clone this repository
- [install vagrant](http://www.vagrantup.com/) 
- Download hadoop-1.2.1.tar.gz and place in modules/hadoop/files
- vagrant box add base-hadoop http://files.vagrantup.com/lucid64.box
- vagrant up
- vagrant ssh master
- sudo ssh 192.168.1.10 (to 12) and accept authorization
- cd /opt/hadoop-1.1.0/bin
- sudo ./hadoop namenode -format
- sudo ./start-all.sh