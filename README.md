# Web-dev-Assignment-3 
Inventory and Data Management System
RESTful API backend for inventory management built for Assignment 3 (Web Dev III - Unit 3) using Node.js, Express.js, MongoDB, Mongoose, and dotenv.

📸 Postman Output Screenshots (Mandatory)
Note: Below are the screenshots demonstrating successful execution and response validation across all required endpoints via Postman.

1. Create Product (POST /api/products) <img width="1920" height="1080" alt="01-create-product" src="https://github.com/user-attachments/assets/b486fcaf-c13c-4760-9d37-bbcfb004b38a" />
2. Get All Products — Filtering, Sorting & Pagination (GET /api/products)
<img width="1920" height="1080" alt="02-get-all-products" src="https://github.com/user-attachments/assets/4b5f30f4-c7c6-4749-bdef-04e550544034" />
3. Update Product Details (PUT /api/products/:id)
<img width="1920" height="1080" alt="03-update-product" src="https://github.com/user-attachments/assets/252d92d1-2598-4b70-be4f-f8710b7c0d57" />
4. Low-Stock Alert Report (GET /api/products/low-stock)<img width="1920" height="1080" alt="05-low-stock-report" src="https://github.com/user-attachments/assets/288e4e21-9222-44ef-ac65-819c65fe24cc" />
5.Category-wise Summary Aggregation (GET /api/products/summary)<img width="1920" height="1080" alt="06-category-summary" src="https://github.com/user-attachments/assets/60de8cbb-a321-4bed-a75f-e5d77f7d90cc" />
6.Delete Product (DELETE /api/products/:id)<img width="1920" height="1080" alt="07-delete-product" src="https://github.com/user-attachments/assets/e9f200ae-cc4e-47f7-86ca-8958fbd9f1a8" />

🛠 Tech Stack
Node.js – Server-side JavaScript runtime
Express.js – Minimal web application framework
MongoDB – NoSQL database
Mongoose – Object Data Modeling (ODM) library
dotenv – Environment configuration management
🚀 Setup & Installation
1. Clone the repository
git clone https://github.com/shreshthkchaudhary/inventory-and-data-management-system.git
cd inventory-and-data-management-system
2. Install dependencies
npm install
3. Configure environment variables
Create a .env file in the root directory (or copy from .env.example):

cp .env.example .env
Ensure your MongoDB connection string and port are set:

PORT=5000
MONGO_URI=mongodb://127.0.0.1:27017/inventory_db
4. (Optional) Seed sample data
To load initial mock products into the database:

npm run seed
5. Start the server
npm start
The server will start at http://localhost:5000.

📡 API Endpoints Reference
Base URL: http://localhost:5000/api/products

HTTP Method	Endpoint	Description
POST	/	Create a new product with field validations
GET	/	Retrieve products with filtering, search, sorting & pagination
GET	/:id	Retrieve single product details by MongoDB ID
PUT	/:id	Update product details
PATCH	/:id/stock	Increment (restock) or decrement (sale) stock safely
DELETE	/:id	Delete a product by ID
GET	/low-stock	Retrieve products with quantity <= reorderLevel
GET	/summary	Aggregation pipeline: category-wise counts, stock values & average prices
