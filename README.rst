Cloudmesh MOOC Shell
======================

Documentation:

* http://cloudmesh.github.io/mooc

Quickstart
------------
* Login to india openstack
* Create 'cloudmesh' secgroup to allow the access of 5000, 8888 ports::

  $ nova secgroup-create cloudmesh "cloudmesh ports 5000, 8888"
  $ nova secgroup-add-rule cloudmesh tcp 8888 8888 0.0.0.0/0
  $ nova secgroup-add-rule cloudmesh tcp 5000 5000 0.0.0.0/0
  $ nova secgroup-list-rules cloudmesh
  
**If you already have `cloudmesh` in your security group, you can skip this section.**

* Execute the following commands::

   module load heatclient
   source ~/.futuregrid/openstack_havana/novarc
   source /share/project/FG455/MOOC/bin/activate
   cm-455 start          # wait approximately 5 minutes
   cm-455 notebook create
   cm-455 notebook start # Acccess to your IPython Notebook via a web browser: https://[ip address]:8888
   cm-355 stop           # Stop the VM

Start Cloudmesh VM
------------------

``cm-455 start``

List VM
--------

``cm-455 list``

Stop Cloudmesh VM
---------------------

``cm-455 stop``

Login Cloudmesh VM
--------------------------

``cm-455 login``

Create IPython Notebook Profile on Cloudmesh VM (Set Password)
------------------------------------------------------------------

``cm-455 notebook create``

or

``cm-455 login``

and call cm on the VM

``cm notebook create``

Setup the password and exit from the VM.

``exit``

Start IPython Notebook on Cloudmesh VM
-----------------------------------------

``cm-455 notebook start``

Stop IPython Notebook on Cloudmesh VM
-----------------------------------------

``cm-455 notebook stop``

If you delete the VM, try:

``cm-455 stop``

Help Message
-------------

``cm-455 -h``
