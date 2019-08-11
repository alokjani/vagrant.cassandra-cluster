=================
Cassandra Cluster
=================

Overview
========
Simple method to provision 3 node Apache Cassandra Cluster wtih Vagrant, Ansible & Virtualbox. 

Methodology
===========

To start a local cluster on your computer, ensure you have installed Vagrant, Ansible and Virtuabox running.

To start the cluster, download the repo and execute `vagrant up` 

.. code-block::

  git clone https://github.com/alokjani/vagrant.cassandra-cluster.git
  cd vagrant.cassandra-cluster/
  vagrant up

To Switch-Off VMs use `vagrant halt`

To Destroy the VMs (requires re-provisioning) use `vagrant destory`

Cluster Topology
================

The nodes will have IP as 192.168.56.11, 192.168.56.12, 192.168.56.13 and so on.

From the `N` nodes, node{1,2,3} will be the cluster seeds.

To access the CQLSH prompt, login into a node, say node1 using `vagrant ssh node1`.

.. code-block::

  [vagrant@node1 ~]$ cqlsh 192.168.56.11
  Connected to Cluster22 at 192.168.56.11:9042.
  [cqlsh 5.0.1 | Cassandra 3.11.4 | CQL spec 3.4.4 | Native protocol v4]
  Use HELP for help.
  cqlsh> 


