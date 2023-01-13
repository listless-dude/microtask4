Getting Started
++++++++++++++++

Introduction
=============
This is a microservice which performs user authentication and count the number of visitors. In this we we use ``Node/Express`` and database ``MongoDB``. The database is hosted on the MongoDB atlas cluster.
This microtask demonstrates the use of
Hosted on: https://mz5mm5.deta.dev/

Run locally
=====================

Clone the repository:
---------------------
``https://github.com/mr-oogway/microtask2``

Install npm packages:
----------------------
``npm install``
This will install the required packages such as express, nodemon, mongoose etc.

Modify the code:
----------------
In ``index.js`` file, make changes such that it look like the following

.. code-block:: javascript

    const express = require('express');
    const mongoose = require('mongoose');

    const app = express();
    const mongoURI = 'mongodb+srv://{username}:{password}@cluster0.yubrivh.mongodb.net/?retryWrites=true&w=majority';
    const PORT = 5000;
    app.use(express.json());

    mongoose.connect(mongoURI, () => {
        console.log('Connected to mongo successfully');
    });

    app.use('/api/auth', require('./routes/authenticate'));
    app.use('/api/visitor', require('./routes/visitorCount'));
    app.listen(PORT, () => {
        console.log(`Server running on the port: ${PORT}`);
    });
    // module.exports = app;

.. note::
    Haven't provided the username and password of the mongodb cluster because of security reasons. 
    You can create your own shared cluster and then allow all IP address and then use your username and password instead.

Run the code:
--------------
``npm run dev``

For API endpoints and methods used, visit the API page.