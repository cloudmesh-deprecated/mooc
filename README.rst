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
  
**If you already have `cloudmesh` in your security group, you can skip this section.**

* Execute the following commands::

   module load heatclient
   source ~/.futuregrid/openstack_havana/novarc
   source /share/project/FG455/MOOC/bin/activate
   cm-mooc start
   # wait approximately 5 minutes
   cm-mooc notebook create
   cm-mooc notebook start
   # Acccess to your IPython Notebook via a web browser: https://[ip address]:8888
   cm-mooc stop # Stop the VM

Start Cloudmesh VM
------------------

``cm-mooc start``

List VM
--------

``cm-mooc list``

Stop Cloudmesh VM
---------------------

``cm-mooc stop``

Login Cloudmesh VM
--------------------------

``cm-mooc login``

Create IPython Notebook Profile on Cloudmesh VM (Set Password)
------------------------------------------------------------------

``cm-mooc notebook create``

Start IPython Notebook on Cloudmesh VM
-----------------------------------------

``cm-mooc notebook start``

Stop IPython Notebook on Cloudmesh VM
-----------------------------------------

``cm-mooc notebook stop``

Help Message
-------------

``cm-mooc -h``
