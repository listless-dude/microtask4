Getting Started
++++++++++++++++

Introduction
=============
Simple API calling using a public geolocation API using latitude and longitude queries to get the address.
Hosted on: https://zkvjpl.deta.dev/

Run locally
=====================

Clone the repository:
---------------------
``https://github.com/mr-oogway/microtask3``

Install npm packages:
----------------------
``npm install``
This will install the required packages such as express.

Modify the code:
----------------
In ``index.js`` file, make changes such that it look like the following

.. code-block:: javascript

    const express = require('express');
    const app = express();

    const PORT = 5000;

    app.use('/api/geolocation', require('./routers/api'))

    app.listen(PORT, () => {
         console.log(`Server listening on port ${PORT}`);
    });

    // module.exports = app;

Run the code:
--------------
``npm run dev``

For API endpoints and methods used, visit the API page.