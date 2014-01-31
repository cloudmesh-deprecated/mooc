UNIT Overview
======================================================================

This section has two goals. It is meant to

* give you an introduction to FutureGrid, and 
* how to use FutureGrid for the Big Data Course. 

As part of this we will present you with information on how to create
a FutureGrid account, upload OpenID and SSH keys, and manage virtual
machines specifically targeting an IPython and Java environment that
we will use as part of this lesson.

Accessing FutureGrid
====================================================================== 

FutureGrid is a project led by Indiana University and funded by the
National Science Foundation (NSF) to develop a cloud, grid, and high-performance 
test bed that lets scientists collaboratively develop and test
innovative approaches to parallel, grid, and cloud computing. The
ultimate goal is to build a system that helps researchers identify
cyberinfrastructure that best suits their scientific needs.  The
FutureGrid test bed is composed of a high-speed network connected to
distributed clusters of high-performance computers, and is linked to
the Extreme Science and Engineering Discovery Environment
(XSEDE). FutureGrid employs virtualization technology that lets the
test bed support a wide range of operating systems.

FutureGrid has an extensive set of manual pages that is provides the
most up to date information. We recommend that you visit the manual
pages and obtain a further overview of how to use the many services
that FutureGrid offered. However, for this lesson, the information
provided here will be suffient.

You can find the FutureGrid Manual at 

* http://manual.futuregrid.org

Much of the information presented here is directly copied from that
manaul. To indicate where the information is comming from we are
adding to each lesson a resource section, so that you also can visit
the original page.

 
Create a FG Portal Account
----------------------------------------------------------------------

**Overview:** This lesson explains how to create a FutureGrid portal
account, which is the first step in gaining access to the FutureGrid
testbed.

.. sidebar:: |file-image| Resources
   
   * `FutureGrid Portal <https://portal.futuregrid.org/>`_
   * `FutureGrid Manual: Create a portal account <http://manual.futuregrid.org/account.html#create-a-portal-account>`_

Create a Portal account
-------------------------

In order to utilize **any** FutureGrid resource, you must possess a
FutureGrid **portal account**. Thus, *apply for your portal
account* before you attempt anything else. This account is used to
gather some information that we will use in the next steps. You must
make sure that the information is complete before you proceed to the
second step.  FutureGrid performs basic verification of the information
you provide when creating an account, so it may take a little while
before your account is approved. Once you have a portal account, please
proceed.

Please note that you cannot access FutureGrid resources until you
complete the next steps.  

.. sidebar:: |info-image| Hint

   It may take a day or two to get a portal account. Portal
   accounts will not be created over the weekend.

Here are a few tips that make it easy for you

-  On the portal's main page at https://portal.futuregrid.org
   appears
   a :menuselection:`Portal --> Register` :portal:`link <user/register>`. 
-  Following you will be able to **Create a new account** on the
   portal. 
-  Fill in **ALL** fields as much as you can.
-  Note that fields with **\*** are mandatory
-  It is important that you specify your address information completely.
-  If you are a graduate or undergraduate student please fill out your
   advisor's contact information in the field specially dedicated for it.
   If he has a FutureGrid Portal name, please include his portal name
   if you know it.
-  If you have an e-mail address from your institution, we ask that you
   use this address instead of one from gmail, hotmail, or other e-mail
   services that we cannot trace back to your name or institution.
-  Usage of all non institutional addresses will prolong the application
   process.
-  Please note that creating a portal account does not give you access
   to any FutureGrid resources.     
-  Please remember that checking your information will take time. Thus
   we recommend that you wait till you get a message that tells you that
   your portal account has been approved. Then continue to The next
   step. We are not conducting any portal approval outside of 10am-4pm
   EST. If there are no problems verifying your information your
   approval will take 1-2 days; if we have problems verifying your
   data or something else is not right your approval will be
   delayed. If you appear to be a spammer we will not notify you.
-  If you are teaching a class, we have some special
   instructions for you in Section :ref:`s-account-class`.
-  After your account has been approved, you can correct the
   information as part of the portal account :portal:`User Profile
   Management <my>`.

 
Upload an OpenID
----------------------------------------------------------------------

Overview: This lesson explains how to upload and use OpenID to easily
log into the FutureGrid portal

.. sidebar:: |file-image| Resources 

   * `FutureGrid Manual: Upload an OpenID <http://manual.futuregrid.org/account.html#upload-an-openid>`_

Often users may not remember the password or username of the FG
portal. However, they may have an easier time to remember their OpenID
from for example Google. It is possible to use your OpenID account and
register it once you gain access to the portal. Please visit your

* `OpenID Page <https://portal.futuregrid.org/my/openid>`__

to add your favorite OpenID. For example, to add your Google OpenID you simply
click on the Google icon.

 
Upload SSH Key
----------------------------------------------------------------------

Overview: This lesson explains how to upload and use a SSH key to log to the FutureGrid resources.

.. sidebar:: |file-image| Resources 

   * `FutureGrid Manual: Upload a SSH Key <http://manual.futuregrid.org/account.html#upload-a-ssh-public-key>`_


In order to be able to log into the started VMs, among other purposes,
you need to provide FG with a secure-shell (ssh) public key. If you are
already a frequent user of ssh, and have a private and public key pair,
it is perfectly reasonable to provide your public key. It's *public*,
after all.

To upload the chosen public key:

#. Copy your public identity into your system clipboard.
#. Visit the `ssh-key panel of your account <https://portal.futuregrid.org/my/ssh-keys>`__.
#. Click the link that says Add a public key.

If you are not familiar with ssh keys we have provided more indepth information next. It covers 
in detail how to generate SSH Keys and upload into your portal account.

.. sidebar:: |file-image| Resources 
   
   * `FutureGrid Manual: Using SSH <http://manual.futuregrid.org/security.html#s-using-ssh>`_
   * `OpenSSH Manual <http://openssh.com/manual.html>`_

Using SSH 
----------------------------------------------------------------------

SSH functionality by default available in Linux and Mac
terminals. However in windows you need to install either Cygwin or
Putty for the SSH functionality. Instructions for installing Cygwin is
provided at within the more detailed `FutureGrid manual in the
security section <http://manual.futuregrid.org/security.html#id1>`_

Generate a SSH key
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Generate a SSH key
-----------------------

.. sidebar:: |info-image| Hint

   In case you do not want to type in your password everytime,
   please learn about ssh-agent and ssh-add.

First we must generate a ssh key with the tool `ssh-keygen
<http://linux.die.net/man/1/ssh-keygen>`__. This program is commonly
available on most UNIX systems (this includes Cygwin if you installed
the ssh module or use our pre-generated cygwin executable). It will
ask you for the location and name of the new key. It will also ask you
for a passphrase, which you **MUST** provide. Some teachers and teaching 
assistants advice you to not use passphrases. This is **WRONG** as it 
allows someone that gains access to your computer to also gain access to 
all resources that have the public key. Also, please use a strong passphrase 
to protect it appropriately. 

In case you already have a ssh key in your machine, you can reuse it
and skip this whole section.

To generate the key, please type::

Example::

    ssh-keygen -t rsa -C localname@indiana.edu

This command requires the interaction of the user. The first question is::

    Enter file in which to save the key (/home/localname/.ssh/id_rsa): 

We recommend using the default location ~/.ssh/ and the default name id\_rsa. 
To do so, just press the enter key.

.. sidebar:: |info-image| Hint 

   Please note that your *localname* is the username on
   your computer and may be different from your *portalusername*.


The second and third question is to protect your ssh key with a
passphrase. This passphrase will protect your key because you need to
type it when you want to use it. Thus, you can either type a
passphrase or press enter to leave it without passphrase. To avoid
security problems, you **MUST** chose a passphrase. Make sure to not
just type return for an empty passphrase::

    Enter passphrase (empty for no passphrase):

and::

    Enter same passphrase again:


If executed correctly, you will see some output similar to::

    Generating public/private rsa key pair.
    Enter file in which to save the key (/home/localname/.ssh/id_rsa): 
    Enter passphrase (empty for no passphrase):
    Enter same passphrase again:
    Your identification has been saved in /home/localname/.ssh/id_rsa.
    Your public key has been saved in /home/localname/.ssh/id_rsa.pub.
    The key fingerprint is:
    34:87:67:ea:c2:49:ee:c2:81:d2:10:84:b1:3e:05:59 localname@indiana.edu
    The key's random art image is::

    +--[ RSA 2048]----+
    |.+...Eo= .       |
    | ..=.o + o +o    |
    |O.  o o +.o      |
    | = .   . .       |
    +-----------------+


Once, you have generated your key, you should have them in the .ssh
directory. You can check it by ::

    $ cat ~/.ssh/id_rsa.pub

If everything is normal, you will see something like::

    ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCXJH2iG2FMHqC6T/U7uB8kt6KlRh4kUOjgw9sc4Uu+Uwe/EwD0wk6CBQMB+HKb9upvCRW/851UyRUagtlhgythkoamyi0VvhTVZhj61pTdhyl1t8hlkoL19JVnVBPP5kIN3wVyNAJjYBrAUNW4dXKXtmfkXp98T3OW4mxAtTH434MaT+QcPTcxims/hwsUeDAVKZY7UgZhEbiExxkejtnRBHTipi0W03W05TOUGRW7EuKf/4ftNVPilCO4DpfY44NFG1xPwHeimUk+t9h48pBQj16FrUCp0rS02Pj+4/9dNeS1kmNJu5ZYS8HVRhvuoTXuAY/UVcynEPUegkp+qYnR user@myemail.edu



Upload the key to the FutureGrid Portal
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


.. sidebar:: |file-image| Resources

   * `FutureGrid Manual: Upload a ssh public key <http://manual.futuregrid.org/account.html#upload-a-ssh-public-key>`_

Next you need to upload the key to the portal. You must be logged into
the portal to do so

* Step 1: Log into the portal

* Step 2: Click in the “ssh key” button. or go directly to https://portal.futuregrid.org/my/ssh-keys

* Step 3: Click in the “add a public key” link.

* Step 4: Paste your ssh key into the box marked Key. Use a text
  editor to open the “id_rsa.pub”. Copy the entire contents of
  this file into the ssh key field as part of your profile
  information. Many errors are introduced by users in this step
  as they do not paste and copy correctly 

* Step 5: Click the submit button. IMPORTANT: Leave the Title field blank. Make
  sure that when you paste your key, it does not contain
  newlines or carriage returns that may have been introduced by
  incorrect pasting and copying. If so, please remove them.

At this point you have uploaded your key. However you will still need
to wait till all accounts have been set up to use the key, or if you
did not have an account till it has been created by an
administrator. Please, check your email for further updates. You can
also refresh this page and see if the boxes in your account status
information are all green. Then you can continue   

Joining the FG Project for the MOOC
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Overview: This lesson explains how to join a FutureGrid project

.. sidebar:: |file-image| Resources

   * `FutureGrid Project 380 <https://portal.futuregrid.org/projects/380>`_

Upon successful creation of your account, you will be able to join the
existing FutureGrid projects. For this course, you have to join the
Big Data Course project. The project is located at

* https://portal.futuregrid.org/projects/380

If you are interested in other projects on FutureGrid you can find a list of them at

* https://portal.futuregrid.org/projects/all 

Our MOOC project has the title “Big Data Application and
Analytics”. In order for you to be added to the project, you have to
click the link “Join this project” in the right side of the project
details page. After verifying your account and course enrollment
details, you will be granted the permission by the course
administrator to join the project.

Please note that the account activation takes a usually a working
day. Not that join requests over a weekend or holiday will be handled
at the next buisiness day.   

Using FutureGrid
======================================================================

Overview: This lesson explains our customized shell that will simplify
management of the VMs for this upcomming lessons. The VM will start an
IPython IPython Notebook.


Login to a FutureGrid 
----------------------------------------------------------------------

First you need to login to the FutureGrid machine called india. This
is done with the following command::

  ssh -X username@india.futuregrid.org

Note: Your username will be the FutuerGrid portal name.

If your connection is successful, you should see output similar to below::

  Last login: Wed Jan  8 10:57:32 2014 from 156-56-93-235.dhcp-bl.indiana.edu
  -------------------------------------------------------------

  Please do not run large jobs on the login nodes.  Large jobs are subject
  to termination without warning.

  Jobs run outside the job scheduler are subject to termination without
  notice.

  ------------------------------------------------------------

  Welcome to India.FutureGrid.Org

  ============================================================================
  torque/2.5.5 version 2.5.5 loaded
  moab version 5.4.0 loaded

.. sidebar:: |info-image| Hint

   All the programs of the course have graphs as output and to view the graphs use –X option while logging  

   * Unix Users::

  		$ ssh –X username@india.futuregrid.org

   * Windows Users::

		$ startxwin
		$ ssh –X username@india.futuregrid.org


For more information on cygwin we also recommend the following manuals (a) `Using Cygwin for X11 Forwarding <https://www.cs.virginia.edu/~csadmin/wiki/index.php/Using_Cygwin_for_X11_Forwarding>`_
(b)  `Cygwin Manual<http://rcc.its.psu.edu/user_guides/remote_display/cygwin/>`_


Activating the MOOC tools
----------------------------------------------------------------------

We have created for you a simple way of activating some default
environment that will help you to more easily interact with the
virtual machines that will be hosted on FutureGrid's OpenStack
infrastructure. Instead of overwhelming you with details of how to
manage the VM with lengthy OpenStack shell commands, we are using for
this lesson a customized shell environment that allows you via a menu
to interact with the system easily. After every log into india you
need to start every time the command::

   module load fg380

If you like to automatically do this you can also edit your ~/.bashrc
file and add the above command at the end of that file. This way you
do not have to remember it.

Starting the MOOC Shell
----------------------------------------------------------------------

Next you can start the MOOC shell with the command::

   cm-mooc

This will bring up a menu with a number of useful commands to manage
the vm for this lesson. You will see something like this::

   ./cm-mooc 

		 FutureGrid - Cloud Mesh MOOC Shell
   ------------------------------------------------------
      ____ _                 _   __  __           _
     / ___| | ___  _   _  __| | |  \/  | ___  ___| |__
    | |   | |/ _ \| | | |/ _` | | |\/| |/ _ \/ __| '_ \ 
    | |___| | (_) | |_| | (_| | | |  | |  __/\__ \ | | |
     \____|_|\___/ \__,_|\__,_| |_|  |_|\___||___/_| |_|
   ======================================================

   Cloudmesh MOOC FG380 Menu
   ----------------------------------------------------------------------
   user  : username
   tenant: fg380
   key   : username-key
   ----------------------------------------------------------------------

       == Keys ==================     == VM ====================

	  1) upload                      3) start  
	  2) delete                      4) suspend 
					 5) resume 
       == Login =================        6) list 
					 7) delete
	  9) login 

       == Quit =================      == IP =====================

	  q) Quit cm-mooc               8) list public ip


You can now press the numbers and an acction according to the
description takes place. Please watch the response carefully. The menu
can be left with the key ``q``

A typical workflow for a new user looks like this:

  ``1`` upload key > ``3`` start vm > 
  ``wait`` for vm to be started > ``6`` check the status > if not
  started continue to wait and repeat checcking with ``6`` >
  ``9`` login into the vm

To suspend and resume use ``4`` or ``5``

We explain important steps of this workflow in more detail next.



Key Management
----------------------------------------------------------------------

The first time you must add a key to OpenStack that will be used to
log into the virtual machine. Please press ``1`` on your
keyboard. This will create a key for you and place it in the home
directory. The key is called username-key, where username is your
username in india. The username can be displayed also with the
command::

  echo $USER

If you execute the command twice it will warn you that you already
have uploaded and created a key. If for some reason you need to
recreate the key, you will need to first delete it and then call the
upload command again. To show you that the key is indeed uploaded to
OpenStack the cm-mooc command will show you alse the list of keys on
the terminal. You will see somthing like this::

  +--------------+-------------------------------------------------+
  | Name         | Fingerprint                                     |
  +--------------+-------------------------------------------------+
  | USERNAME-key | d8:bb:f0:c5:bf:ba:7d:22:51:7b:25:15:fe:e4:b9:7a |
  +--------------+-------------------------------------------------+


VM Management
----------------------------------------------------------------------

Next you need to boot the image that you will use for running IPython.

This is achieved by pressing the number ``3`` on your keyboard 

It will take some time till the image is uploaded. To see the status,
you can invoke the list function with the key ``6``.

Sometimes you may get an error or the start will take a long time. Be
not alarmed about this. OpenStack resources are limited, and sometimes
ther may just not be eonugh resources to start another VM. Especially
if other users start VMS that they may not use. Thus we ask you that
once you are done with your activities to suspend with ``4`` the VM
and when you come back to resume it with ``5``.

As it will take some time to get everything activated you need to wait
a moment before you can proceed.

The image wil be ready when the login command works and you can login
into the VM. You can login into the image with ``9``. If it does not
work, you may want to wait a minute or two and try again.    In case
the shell gets stuck and you like to interrup you can user ``CTRL-C``
However note that this doe snot stop a command that is already started
and runs in the background. Sometimes you may want to cancel a login
which you can do this way.

Accessing IPython and running Python examples
----------------------------------------------------------------------

Overview: This lesson discusses the use of IPython, how to open the
existing notebooks and modification and creation of new files.

To open IPython, we need first to find the public IP of the VM. We
have provided you with a simple tool to do that that is called when
you press in the cm-mooc shell the key ``8``. You will see something
like this on your screen::

  retreiving public ip ...
  Public IP:  149.165.159.255

If you do not see it scroll the window up. Copy this address and type
into a web browser the following (assuming your address is
149.165.159.255)::

   http://149.165.159.22/#notebooks

You should be able to see and modify the course python files. When
prompted for password enter your password that is given out by the
course instructor. Please keep this password confidential. In future
versions, this password can be set by you.

NOTE:  It may take some time (3-4) mins for the server to get everything loaded. 


Course Related Files in the VM
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Overview: In this lesson we discuss important folders regarding the
course that are contained in the VM.

Once you have logged into VM, you can find the course related files
under /home/ipynb

NOTE: It will take some time (2-4 Mins) for all the course materials to be loaded. 
 
Running Java and Python on FG
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Overview: This lesson explains how to run Java and Python on the VM

In the previous sections we have covered on how to log into the
Virtual Machine. After logging into the VM, navigate to the
/home/ipynb directory.

The directory:: 

   /home/ipynb 

has the course programs in both Java and Python.  To view the Java
programs navigate to the directory with::

  cd  /home/ipynb/java 

Below are the steps to execute the java programs::

    javac <ClassName>.java
    java  <ClassName> 

Similarly for python navigate to home/ipynb/python directory first cd into the directory::

    cd  /home/ipynb/python

and than execute the desired program with::

    python  <FileName>.py

NOTE: If you are not able to view these directories, please
logout and wait for some time before logging again. As mentioned
before it would take some time to load the files to VM.


.. |info-image| image:: images/glyphicons_195_circle_info.png 

.. |file-image| image:: images/glyphicons_036_file.png
