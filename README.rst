Cloudmesh MOOC Shell
======================

Documentation:

* http://cloudmesh.github.io/mooc

Quick Start
------------
* Login to india openstack
* Create 'cloudmesh' secgroup to allow the access of 80, 5000, 8888 ports::

  $ nova secgroup-create cloudmesh "cloudmesh ports 80, 5000, 8888"
  $ nova secgroup-add-rule cloudmesh icmp -1 -1 0.0.0.0/0
  $ nova secgroup-add-rule cloudmesh tcp 22 22 0.0.0.0/0
  $ nova secgroup-add-rule cloudmesh tcp 8888 8888 0.0.0.0/0
  $ nova secgroup-add-rule cloudmesh tcp 5000 5000 0.0.0.0/0
  $ nova secgroup-list-rules cloudmesh
  
* Execute the following commands::

   module load heatclient
   export PYTHONPATH=$PYTHONPATH:/N/soft/python/2.7/lib/python2.7/site-packages
   source ~/.futuregrid/openstack_havana/novarc
   wget https://github.com/cloudmesh/mooc/archive/fg455.zip -O fg455.zip
   unzip fg455.zip
   cd mooc-fg455
   ./cm-mooc

* Select **3** to start a Cloudmesh VM
* Wait 3-5 minutes until the configuration is completed
* Select **l** to login to the VM
* Execute `cm notebook create` on the VM
  - type your password for IPython Notebook
* Execute `cm notebook start` on the VM
* Acccess to your IPython Notebook via a web browser: https://[ip address]:8888
 
