.. _projectmine-rcauth:

******************************
RCauth on Project_MinE User Interface
******************************

===============
RCauth authentication
===============
Users need a personal X509 grid certificate to access the grid at SURFsara. Each country may have a central Certificate Authority 
(CA) or multiple CAs, and the CAs may also support Universities from different countries. However, as this process is decentralized
and every country may not have a CA, this can cause delays for users to get a certificate. The NFS mount service on the mine user interface 
enabled users to copy data from dCache to their local site without a certificate, however these users could not use grid clients for more efficient data transfers or run their analyses on the grid.

When users start working on the grid, or interact with dCache for data transfers, a [proxy](http://doc.grid.surfsara.nl/en/latest/Pages/Advanced/grid_authentication.html) is created based on the user's 
certificate. RCauth is a service that allows users to get this proxy without the actual user certificate but instead with username/password 
authentication provided by SURFsara. This feature will help users to speed up getting access to the data without worrying about grid certificates! This document provides information on how to use the RCAuth service.

=============
How to use RCAuth
=============

SURFsara will provide entitlement to enable existing users to use this service. Future incoming users will be automatically  provided with this entitlement when their accounts are created. 

* Create a RCauth proxy
Similar to creating a proxy based on the certificate, you can create a proxy by runing the following command:

 .. code-block:: console

     $startGridSessionRCauth lsgrid:/lsgrid/Project_MinE 
     
This will promt you for the following response:

 .. code-block:: console

    Please enter the authentication hash that you retrieved from https://rcdemo.nikhef.nl/projectmine/. 

From a browser please proceed to the above link. You will be directed to the following page:

Click on the start button upon which you will be redirected to the following pages for agreeing to the user terms and conditions. Please click yes and remember me (so you will not be asked again) and proceed till you reach the following page:



If you already have a grid certificate, you may still continue to use it.
