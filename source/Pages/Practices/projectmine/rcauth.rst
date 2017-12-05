.. _projectmine-rcauth:

******************************
RCAuth on Project_MinE User Interface
******************************

===============
RCAuth authentication
===============
Users need a personal X509 grid certificate to access the grid at SURFsara. Each country may have a central Certificate Authority 
(CA) or multiple CAs, and the CAs may also support Universities from different countries. However, as this process is decentralized
and every country may not have a CA, this can cause delays for users to get a certificate. The NFS mount service on the mine user interface 
enalbed users to copy data from dCache to their local site without a certificate, however these users cannot run their analyses
on the grid.

When users start working on the grid, or interact with dCache for data transfers, a proxy[http://doc.grid.surfsara.nl/en/latest/Pages/Advanced/grid_authentication.html] is createdf based on the user's 
certificate. RCauth is a service that allows users to get this proxy without the actual user certificate but instead with username/password 
authentication provided by SURFsara. This feature will help users to speed up getting access to the data without having to find a 
local Certificate Authority

