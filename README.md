This project is an Express.js application that interacts with multiple external APIs to fetch and merge product data from different companies. It also integrates with MongoDB to store and retrieve product details.
Installation
Clone the Repository

Install Dependencies:npm install

Run the Application:npm start

The server will start on http://localhost:3000.


Endpoints
1. GET /categories/
/products
Fetches products from external APIs for a specific category and merges them.

URL: /categories/:categoryname/products

Query Parameters:

n (optional): Number of products to fetch (default: 10)

Example:
curl --location 'http://localhost:3000/categories/electronics/products?n=10'


To create a README file for your Express.js application and provide examples of cURL commands to interact with your endpoints, follow these steps:

Project README
Project Overview
This project is an Express.js application that interacts with multiple external APIs to fetch and merge product data from different companies. It also integrates with MongoDB to store and retrieve product details.

Installation
Clone the Repository:

bash
Copy code
git clone <repository-url>
cd <project-folder>
Install Dependencies:

bash
Copy code
npm install
Run the Application:

bash
Copy code
npm start
The server will start on http://localhost:3000.

Endpoints
1. GET /categories/
/products
Fetches products from external APIs for a specific category and merges them.

URL: /categories/:categoryname/products

Query Parameters:

n (optional): Number of products to fetch (default: 10)
Example:

bash
Copy code
curl --location 'http://localhost:3000/categories/electronics/products?n=10'
2. GET /categories/
/products/
Fetches a specific product by its productid.

URL: /categories/:categoryname/products/:productid

Example:
curl --location 'http://localhost:3000/categories/electronics/products/c57cc86e-0a91-4a78-9d65-f252075aed9b'
Error Handling
The server handles errors gracefully and returns appropriate HTTP status codes along with error messages when fetching data from external APIs or MongoDB.
Technologies Used
Node.js - JavaScript runtime
Express.js - Web framework for Node.js
MongoDB - NoSQL database for storing product details
axios - HTTP client for making requests to external APIs
uuid - Library for generating UUIDs
Additional Notes
Ensure MongoDB is running locally (mongodb://localhost:27017) or update uri variable in app.js accordingly.
External APIs are mocked URLs (http://20.244.56.144/test/...) and should be replaced with actual endpoints.
Pagination is implemented for results exceeding n > 10.
Products fetched are merged and stored in MongoDB (dev-test-api database, product_details collection).
Future Improvements
Implement caching mechanism for external API responses to improve performance.
Enhance error handling for edge cases and network failures.
Add authentication and authorization for secure endpoints.
