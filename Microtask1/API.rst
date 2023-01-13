API
+++++

Introduction
=============
The API follows REST. Following are the endpoints with explanation:

API endpoints
=============

To get all users
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
==================== =======================================
**Endpoint:**         ``https://hbnqwi.deta.dev/api/users``
**Local Endpoint:**   ``localhost:{PORT}/api/users`` 
**Method:**           ``GET`` 
**Body Parameters:**  ``None`` 
==================== =======================================

To get a specific user with id
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
==================== ==========================================
**Endpoint:**         ``https://hbnqwi.deta.dev/api/user/:id``
**Local Endpoint:**   ``localhost:{PORT}/api/user/:id`` 
**Method:**           ``GET`` 
**Body Parameters:**  ``None`` 
==================== ==========================================

To add a user
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
==================== =========================================
**Endpoint:**         ``https://hbnqwi.deta.dev/api/addUser``
**Local Endpoint:**   ``localhost:{PORT}/api/addUser`` 
**Method:**           ``POST`` 
**Body Parameters:**  ``JSON``
==================== =========================================

The post request should send a JSON in the format below:

.. note::
        {
        "user#id" : 
        {
        "name": "username",
        "password": "pass",
        "id": #id
        }
        }

To delete a user with id
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
==================== =========================================
**Endpoint:**         ``https://hbnqwi.deta.dev/api/delete/:id``
**Local Endpoint:**   ``localhost:{PORT}/api/delete/:id`` 
**Method:**           ``DELETE`` 
**Body Parameters:**  ``None``
==================== =========================================