client module
-------------

.. automodule:: client_pack.client
   :members:
   :undoc-members:
   :show-inheritance:


Client module wields essential Client class which represents client side in a server-client dialogue.
Main.py uses this class as a core connection asset and wraps it with gui.



.. py:class:: login_required()
.. function:: __init__()
.. function:: __call__(*args, **kwargs)

* *this is a decorator class which restricts messaging unless client is logged in*
* *it wraps function (using functools wraps) and checks for client.gui_out.authenticated value. if True - original args are passed to the function and it is returned intact, otherwise function will not be executed*
|
|
.. py:class:: Client(metaclass=ClientVerifier)

   *This class uses ClientVerifier from client_pack.metacls module as meta to verify that client is using only allowed methods.*

.. function:: __init__(server=None, port=None, username=None, password=None, fullname=None, email=None, gui_out=None)
.. function:: connect

    *initial connection to host server socket*

.. function:: client_authenticate

   *client authentication procedure - series of socket send/recv exchange with the server*

.. function:: read

   *looped function, constantly reading socket if open. initiated in a separate thread within mainloop function*

.. function:: poke

   *tests server connection if client packages can't reach it, initiated by presence function*

.. function:: send

   *forms a queue of client messages (if multiple are attempted at a time) and sends them gradually if connection is active*

.. function:: message

   *forms a client-client message based on jim protocol and passes it to send function*

.. function:: contacts

   *returns contacts list for the main module*

.. function:: load_chat

   *reads cached chat and passes it to display in the main module*

.. function:: cache_message

   *caches incoming message*

.. function:: presence

   *forms a presence message to server (if no client messages have been sent in the previous five seconds) to test connection and inform server that client is online*

.. function:: mainloop

   *uses connect function to establish client-server connection, launches separate threads to read and form presence messages*