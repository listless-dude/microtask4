Getting Started
++++++++++++++++

Introduction
=============
This is a simple API made using **Node/Express**. This microtask demonstrates the use of endpoints to ``read`` and ``write`` a JSON file store locally.
Hosted on: https://hbnqwi.deta.dev

.. warning::
    This is hosted on ``deta.sh`` which doesn't support writing of files.

Run locally
=====================
As the deta.sh server doesn't support writing file, so run locally to check the output.

Clone the repository:
---------------------
``https://github.com/mr-oogway/Backend-Practice``

Install npm packages:
----------------------
``npm install``
This will install the required packages such as express.

Modify the code:
----------------
In ``index.js`` file, make changes such that it look like the following

.. code-block:: javascript

    const express = require('express');
    const http =  require('http');
    const operations = require('./routes/operations');

    const HOST_NAME = 'localhost';
    const PORT = 3000;

    const app = express();
    app.use(express.json());

    app.use('/api', operations);

    // module.exports = app;
    const server = http.createServer(app);
    server.listen(PORT, HOST_NAME, () => {
    console.log(`Server running at http://${HOST_NAME}:${PORT}`);
    });

Run the code:
--------------
``npm start``

For API endpoints and methods used, visit the API page.