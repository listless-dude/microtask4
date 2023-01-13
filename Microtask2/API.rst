API
+++++

Introduction
=============
The API follows REST. Following are the endpoints with explanation:

API endpoints
=============

Authentication API
-------------------
The Authentication API uses a MongoDB database with following Schema:

.. code-block:: javascript
    
    const UserSchema = new Schema({
        name: {
            type: String,
            required: true
        },
        email: {
            type: String,
            required: true
        },
        password: {
            type: String,
            required: true
        }
    }, { timestamps: true });


To get all users
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
==================== =======================================
**Endpoint:**         ``https://mz5mm5.deta.dev/api/auth/getAllUsers``
**Method:**           ``GET``
**Body Parameters:**  ``None`` 
==================== =======================================

To get a specific user with id
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
==================== ==========================================
**Endpoint:**         ``https://hbnqwi.deta.dev/api/auth/getUser/:id``
**Method:**           ``GET`` 
**Body Parameters:**  ``None`` 
==================== ==========================================

To add a user
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
==================== =========================================
**Endpoint:**         ``https://hbnqwi.deta.dev/api/auth/createUser``
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