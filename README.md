# MERN E-Commerce Web Application

> **Author:** Rahul Seervi

> **Frontend:** Vite JS (React JS)

> **Backend:** Node JS & Express JS

> **Database:** MongoDB

## Installation process

1. #### Clone the repo using this command
   ```bash
   git clone https://github.com/thecreativecodeflow/MERN-E-commerce-web-application.git
   ```
2. #### Install npm packages
   1. Install backend packages
   ```bash
   cd MERN-E-commerce-web-application
   npm install
   ```
   2. Install frontend packages
   ```bash
   cd frontend
   npm install
   ```
3. #### Configure environment variables
   Create a `.env` file in the root folder for MongoDB connection and JWT secret. Braintree credentials are optional (only needed if you want to enable payment processing).

   ```bash
   cd MERN-E-commerce-web-application
   ```

   Create a `.env` file with the following variables:

   ##### Sample code for backend .env

   ```env
   MONGODB_URI=YOUR_MONGODB_URI
   JWT_SECRET=YOUR_JWT_SECRET
   BRAINTREE_MERCHANT_ID=YOUR_BRAINTREE_MERCHANT_ID (optional)
   BRAINTREE_PUBLIC_KEY=YOUR_BRAINTREE_PUBLIC_KEY (optional)
   BRAINTREE_PRIVATE_KEY=YOUR_BRAINTREE_PRIVATE_KEY (optional)
   ```

4. #### Configure frontend

   Update the `config.js` file in the frontend folder:

   ```bash
   cd MERN-E-commerce-web-application/frontend
   ```

   ##### Sample code for frontend config.js

   ```javascript
   export const API = 'http://localhost:5000/api';
   ```

   ##### Important Notes:

   1. For MongoDB Atlas database creation, follow this tutorial: https://www.youtube.com/watch?v=KKyag6t98g8
   2. You can use any random string as JWT_SECRET (e.g., a long random alphanumeric string)
   3. If your backend server is on a different port or domain, update the API URL in config.js accordingly
   4. **Important:** Make sure `.env` is added to `.gitignore` to keep your secrets safe
   5. Braintree credentials are only needed if you want to implement payment processing

5. #### Run the project locally

   Start both backend and frontend servers with a single command:

   ```bash
   cd MERN-E-commerce-web-application
   npm run dev
   ```

   #### Note: This command will start both the backend and frontend servers concurrently.
   
   - **Backend:** http://localhost:5000
   - **Frontend:** http://localhost:5173

6. #### Database Structure: (Schema)
   1. categories: \_id, name, createdAt, updatedAt;
   2. orders: \_id, status, products (Array), transaction_id, amount, address, user (Object), createdAt, updatedAt
   3. products: \_id, photo (Object), sold, name, description, price, category, shipping, quantity, createdAt, updatedAt
   4. users: \_id, role, history (Array), name, email, salt, hashed_password, createdAt, updatedAt

## Features

### User Features:
- View all products with pagination
- View single product details
- Search products by name
- Filter products by category and price range
- Add products to cart
- Checkout products using credit card (requires Braintree configuration)
- User registration and authentication
- View order history

### Admin Features:
- Create, edit, update, and delete products
- Create and manage categories
- View all orders
- Update order status (processing, shipped, delivered, etc.)
- Manage users

## Deployment Status

🚧 **This project is currently not deployed.** It runs locally for development purposes.

---

### Support

If you find this project helpful, please consider giving it a ⭐ on GitHub!
