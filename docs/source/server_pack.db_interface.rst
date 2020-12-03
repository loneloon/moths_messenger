db_interface module
---------------------------------

This module initiates server-database dialogue based on SqlAlchemy library.
Main module class - ServerDB has 4 subclasses which describe separate db tables that store user activity records.

.. py:class:: ServerDB

   ::

    class ActiveUsers(user_id, ip_address, port, login_time)
    class AllUsers(username, password, fullname=None, email=None)
    class Contacts(user_id)
    class LoginHistory(name, date, ip, port)

.. function:: active_users_list()

   *returns active user list*

.. function:: add_contact(username, other)

   *updates user client list (triggered by write_requests on server side whenever someone sends message to the other client)*

.. function:: fetch_contacts(username)

   *returns client's current contact list*

.. function:: fetch_userhash(username)

   *returns client's password hash to the server for client authentication*

.. function:: login_history(username=None)

   *returns login history*

.. function:: user_login(username, ip_address, port)

   *records client's login action*

.. function:: user_logout(username)

   *records client's logout action*

.. function:: user_register(username, password, fullname, email, ip_address, port)

   *creates new client record in a database*

.. function:: users_list()

   *returns a list of all clients*