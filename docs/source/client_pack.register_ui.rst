register_ui module
--------------------------------

This module defines user interface for client registration procedure.
|
.. py:class:: Register_Ui()

.. function:: back_to_login()

   *switches window back to Sign In*

.. function:: fetch_details()

   *returns all available inputs from registration window back to client instance*

.. function:: register()

   *initiates registration-type authentication*

.. function:: retranslateUi(MainWindow)

   *standard PyQT button/label translation function*

.. function:: setupUi(MainWindow, main_ui, login_ui)

   *Registration window ui setup*

.. function:: warning_message(warning)

   *displays message on a warning label, launches timer to wipe it later*

.. function:: wipe_warning()

   *wipes displayed warning message*

