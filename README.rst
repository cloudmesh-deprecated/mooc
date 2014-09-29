Cloudmesh MOOC Shell
======================

Documentation:

* http://cloudmesh.github.io/mooc

Quick Start
------------
* Login to india openstack
* Execute the following commands::

   module load heatclient
   export PYTHONPATH=$PYTHONPATH:/N/soft/python/2.7/lib/python2.7/site-packages
   source ~/.futuregrid/openstack_havana/novarc
   source ~/.futuregrid/openstack_havana/fg455
   wget https://github.com/cloudmesh/mooc/archive/fg455.zip -O fg455.zip
   unzip fg455.zip
   cd mooc-fg455
   ./cm-mooc

* Select *3* to start a Cloudmesh VM
* Wait 3-5 minutes until the configuration is completed
* Select *l* to login to the VM
* Execute `cm notebook create` on the VM
  - type your password for IPython Notebook
* Execute `cm notebook start` on the VM
* Acccess to your IPython Notebook via a web browser: https://[ip address]:8888
 
