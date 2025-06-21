# Express-RESTAPI
My Express.js REST API A simple Express.js app demonstrating routing, 404 handling, and error middleware.

Setup Instructions

git clone https://github.com/AsRealTech/restapi.git cd restapi npm install npm start

Server will run at http://localhost:5000

API Routes

GET /items Returns a hello world message.
Request:

GET /items HTTP/1.1 Host: localhost:5000

Response (HTTP 200):

{ "message": "Hello World!" }

GET /itemserror
Simulates a server error.

Request:

GET /itemserror HTTP/1.1 Host: localhost:5000

Response (HTTP 500):

{ "error": "Intentional server error", "status": 500 }

Invalid Route Example
Request:

GET /items/unknown HTTP/1.1 Host: localhost:5000

Response (HTTP 404):

{ "error": "Route not found", "status": 404, "path": "/items/unknown" }

Testing with Postman

Open Postman.
Use GET http://localhost:5000/items
Test GET http://localhost:5000/itemserror for error handling.
Test any unknown route like GET http://localhost:5000/items/404test
Built With:

Node.js Express js
