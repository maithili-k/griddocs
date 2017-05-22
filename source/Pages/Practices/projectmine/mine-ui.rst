.. _projectmine-ui:

******************************
Project_MinE User Interface
******************************

==================
Migration from grid-ui to mine-ui
==================
		
If you were accessing the Grid facility at SURFsara via the grid user interface (ui.grid.sara.nl), you should follow the procedure below to migrate to the Project_MinE user interface.

1. As you have access to the grid-ui, the same credentials also provide you have access to the SURFsara user portal https://portal.surfsara.nl/home/. On this page, proceed to the tab 'Public ssh keys' and add your public key here. If you are unfamiliar with ssh keys, you can find some basic information here https://doc.hpccloud.surfsara.nl/SSHkey. You may choose to protect your public key with a passphrase or leave it empty.

2. The MinE user interface can be accessed once the above step is complete. The public key is injected into the MinE user interface and matched with your local private key when you login to the interface

.. code-block:: console

   $ssh user@mine-ui.grid.sara.nl  # replace user with your username 
   
3. To migrate the contents of your home folder from ui.grid.sara.nl to the Project_MinE user interface, you may use the following command from the MinE user interface:

.. code-block:: console

   $rsync -a --exclude='.*' user@ui.grid.sara.nl:/home/user/ /home/user/   # replace user with your username 

Please note that this will only copy the data files from your home folder. You can copy the .globus folder which contains the grid certificate and key with the following command:

.. code-block:: console
   
   $rsync -a user@ui.grid.sara.nl:/home/user/.globus/ /home/user/.globus

4. Software environment set-up on the Project_MinE user interface and ui.grid.sara.nl are similar. Access to the softdrive.nl service is also availabe from the MinE user interface through the same path viz. /cvmfs/softdrive.nl/. Grid tools that were available on the ui.grid.sara.nl (e.g., glite-* tools, storage clients, etc.) are also availabe on the Mine user interface. 

5. Please remember to 

