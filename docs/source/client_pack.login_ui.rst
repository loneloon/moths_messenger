login_ui module
-----------------------------

This module defines user interface for client log-in procedure.
It's connected to the main module and also controls registration ui.

.. py:class:: Login_Ui
.. function:: setupUi

   *Login window ui setup*

.. function:: retranslateUi()

   *standard PyQT button/label translation function*

.. function:: fetch_details()

   *returns all available inputs from login window back to client instance*

.. function:: launch_main()

   *initiates login-type authentication*

.. function:: launch_register()

   *switches to registration window*

.. function:: register_client()

   *as registration window is not connected directly to the main module, login_ui acts as a middleman to pass registration input to client instance*

.. function:: check_auth()

   *checks if client has connected to server and received authenticated status, if yes - switches to chat and closes self, otherwise displays warning message*


.. function:: warning_message()

   *displays message on a warning label, launches timer to wipe it later*

.. function:: wipe_warning()

   *wipes displayed warning message*
