===============
User Management
===============

Users are managed manually, using Cloud Firecloud as a backend.

backend
=======

Username/passwords are managed manually using a backend Cloud Firestore
_collection_ called `DeviceConnectUsers`.   The collection
has documents named with the user's email address and a
field for `password`.

Users initiate the enrollment process by logging into the website
with their email and the password set in the document::

    DeviceConnectUsers collection
        user1_email
            password - plaintext user password, set prior to enrollment
            name - full name of user, set prior to enrollment
            signature - name as signed by terms of service agreement
            date - date that the user signed the terms of service

Creating New Users
==================

To create a new user, create a new document in the `DeviceConnectUsers`
collection.  The name of the document should be the user's email address
and within that document, create a field named _password_ that will
