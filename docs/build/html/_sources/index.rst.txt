.. M documentation master file, created by
   sphinx-quickstart on Fri Oct 16 13:29:38 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.


Introduction
************
The "moths" project serves a purpose of establishing a p2p messaging system.
It includes two applications: for server-side monitoring and client access.


What's included?
****************
.. toctree::
   :maxdepth: 2

   client_pack
   server_pack


Overview
********
This messenger's functionality is solely based on socket dialogue using python's socket library.
Client messages strictly follow jim protocol. Server-side distributes messages according to assigned recipients.
In order to access chatting clients have to pass the registration procedure and log into their accounts.
Client account details are stored in a general database of each server, all passwords are stored and used only hashed.
Each application is accompanied with a graphical interface. Client application allows to cache active chats locally
in order to minimize server requests and save memory.

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
