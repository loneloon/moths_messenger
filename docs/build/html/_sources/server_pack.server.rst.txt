server module
--------------------------

Server module wields essential Server class which represents server side in a server-client dialogue.
Main.py uses this class as a core connection asset and wraps it with gui.

|
|
.. py:class:: Server(metaclass=ServerVerifier)
|
   *This class uses ServerVerifier from server_pack.metacls module as meta to verify that server is using only allowed methods.*
|
.. py:attribute:: port = PortVerifier()
.. function:: __init__(self, addr=None, port=None)
.. function:: read_requests

   *collects data from all connector-socks available for reading, forms responses using response function and returns a response batch to the mainloop*

.. function:: write_requests

   *sends responses to all socks available for writing, also triggers db function and updates clients' contacts*

.. function:: response

   *forms responses based on the contents of passed jsons(or bytes)*

.. function:: server_authenticate

   *this procedure is initiated for every connected client - server collects credentials and compares received hashes for passwords. if everything is corrects - adds client to verified and sends an authentication confirmation json to client*

.. function:: wipe_user

   *deletes unresponding users and issues logouts through db*

.. function:: mainloop

   *main looping function that initiates reading, writing and authentication*
