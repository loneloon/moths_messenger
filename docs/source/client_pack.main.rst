main module
-------------------------------

.. automodule:: client_pack.main
   :members:
   :undoc-members:
   :show-inheritance:

Main module combines the core client module, login_ui, register_ui into a graphical application.
User interface is based off PyQT library. Most of the code included in this module is ui setup and maintenance.

|
.. py:class:: clickable_Label(QtWidgets.QLabel)

   *widget class, used to create selectable lines in contacts menu*

.. py:attribute:: clicked = QtCore.pyqtSignal()

   *PyQT click listener for a widget*

.. function:: __init__(self, parent=None)
.. function:: check

   *defines label state when pressed*

.. function:: uncheck

   *defines label state when unpressed*

.. function:: mousePressEvent

   *defines mouse-pressed event*

|
.. py:class:: Ui_MainWindow

.. function:: setupUi

   *PyQT gui layout setup*

.. function:: retranslateUi

   *standard PyQT button/label translation function*

.. function:: window_switch

   *hides login interface, shows chat interface*

.. function:: add_contact

   *adds clickable label that represents selectable contact to contact layout*

.. function:: clear_chat

   *clears messages from chat display*

.. function:: choose_contact

   *switches chat display and current message recipient var. to another contact.*

.. function:: refreshScreen

   *refreshes contact list and chat display if incoming message is pending or client just chose another contact*

.. function:: sendMessage

   *gathers message from input field and passes it to send method of client instance*

.. function:: clearInput

   *clears input field*