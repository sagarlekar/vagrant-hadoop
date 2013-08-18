Setup and Installation
======================

We will create 3 Vagrant VMs. Our Hadoop cluster will have 1 master and 3 slaves.

- clone this repository:
  git clone https://github.com/sagarlekar/vagrant-hadoop.git
- [download hadoop-1.2.1.tar.gz](http://www.apache.org/dyn/closer.cgi/hadoop/common/) and place in modules/hadoop/files
- [install vagrant](http://www.vagrantup.com/) 
- vagrant box add base-hadoop http://files.vagrantup.com/lucid64.box
- vagrant up
- vagrant ssh master
- sudo ssh 192.168.1.10 (to 12) and accept authorization
- cd /opt/hadoop-1.1.0/bin
- sudo ./hadoop namenode -format
- sudo ./start-all.sh
