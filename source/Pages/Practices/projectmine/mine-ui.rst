.. _projectmine-ui:

******************************
Project_MinE User Interface
******************************

==================
Migration from grid-ui to mine-ui
==================
		
If you were accessing the Grid facility at SURFsara via the grid user interface (ui.grid.sara.nl), you should follow the procedure below to migrate to the Project_MinE user interface.

1. As you have access to the grid-ui, the same credentials also provide you have access to the SURFsara user portal https://portal.surfsara.nl/home/.

.. image:: /griddocs/source/Pages/Practices/projectmine/cua-portal.png
	:align: center

On this page, proceed to the tab 'Public ssh keys' as shown above and add your public key here. If you are unfamiliar with ssh keys, you can find some basic information here https://doc.hpccloud.surfsara.nl/SSHkey. You may choose to protect your public key with a passphrase or leave it empty.

2. The Project_MinE user interface can be accessed once the above step is complete. The public key is injected into the Project_MinE user interface and matched with your local private key when you login to the interface

.. code-block:: console

   $ssh user@mine-ui.grid.sara.nl  # replace user with your username 
   



