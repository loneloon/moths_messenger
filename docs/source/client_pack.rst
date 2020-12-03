Client package
====================

The client package includes all the necessary assets for client application access.

You will also find a number of subpackages:

* common - includes settings script
* log - includes logging script and client logs
* cache - will store cached chats

Subpackages
-----------

.. toctree::
   :maxdepth: 1

   client_pack.common
   client_pack.log
   client_pack.cache

Submodules
----------

.. toctree::
   :maxdepth: 1

   client_pack.client
   client_pack.main
   client_pack.login_ui
   client_pack.metacls
   client_pack.register_ui

Usage
*****

In unbuilt version run main.py to launch client application.
Other modules support the main script accordingly.

After launch:

* Leave server options blank to use default values 127.0.0.1:7777
* In current version nickname and password length, symbol restrictions are unregulated. In order to avoid connection failure it is recommended to use latin symbols, digits (4-16 symbols).

After login:

* Add new contacts by entering other clients' logins in the top left line input field and clicking "add contact" button.
* The tall blank box on the left will list all contacts that current user has messaged.
* Two wide boxes on the right hand-side (top to bottom) are - chat display and message input field.
* "Clear" button will clear out the input field. "Send" button will confirm and send current message.