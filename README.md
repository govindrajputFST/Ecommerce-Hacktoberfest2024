# Ecommerce

## Maintainers
[Aditya Jambhale](https://github.com/Aditya-jambhale)

## Installation

Explain how to install and set up your project locally. Include any prerequisites, dependencies, and step-by-step instructions.

```bash
# Clone the repository
git clone https://github.com/CSI-DMCE-2024/Ecommerce-Hacktoberfest2024.git

# Change directory
cd Ecommerce-Hacktoberfest2024

# Open index.html in your browser
Overview
This project is a full-stack Ecommerce web application that allows users to browse products, add items to a shopping cart, and complete the checkout process. The platform features a user-friendly interface for customers and an admin panel for product and order management.

# Key Features
User registration and authentication (JWT-based)
Product browsing with search and filter options
Shopping cart functionality
Order management and order history for users
Admin panel for managing products, categories, and orders
Payment gateway integration (e.g., Stripe or PayPal)
Responsive design for both mobile and desktop
Screenshots
Add screenshots here if available to showcase different sections of your project (home page, product listing, admin panel, etc.)

Tech Stack
## Frontend
React.js - Frontend framework for building interactive UI
Redux - State management for handling user data and products
CSS/Tailwind CSS - For styling the application
## Backend
Node.js - JavaScript runtime environment for server-side logic
Express.js - Web framework for Node.js to build REST APIs
MongoDB - NoSQL database for storing products, users, and orders
Mongoose - ODM library for MongoDB to model and interact with the database
JWT - JSON Web Tokens for secure authentication
Stripe/PayPal - Payment gateway integration for processing payments
Getting Started
Prerequisites
Make sure you have the following installed:

Node.js (v14 or higher)
MongoDB (Local instance or MongoDB Atlas account)
Git (for version control)
Stripe/PayPal API keys (for payment gateway)

Copy code
cd backend
npm install
Frontend
bash
Copy code
cd ../frontend
npm install
Configure environment variables:

Create a .env file in the backend folder and add your MongoDB connection string, JWT secret, and Stripe/PayPal API keys:

Copy code
PORT=4000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
STRIPE_SECRET_KEY=your_stripe_key
Start the backend server:

bash
Copy code
cd backend
npm start
Start the frontend server:

bash
Copy code
cd frontend
npm start
The app should now be running at http://localhost:3000 (frontend) and http://localhost:4000 (backend).

## Folder Structure
bash
Copy code
ecommerce-project/
├── backend/         # Backend API code
│   ├── controllers/ # Contains business logic for routes
│   ├── models/      # MongoDB models
│   ├── routes/      # API endpoints
│   ├── middleware/  # Middleware (auth, error handling)
│   ├── utils/       # Utility functions
│   └── app.js       # Main entry point
└── frontend/        # Frontend code (React)
    ├── src/         # React components, pages, redux store
    └── public/      # Static files (images, favicon, etc.)
# API Endpoints
# Authentication
POST /api/auth/register - Register a new user
POST /api/auth/login - Login a user
GET /api/auth/profile - Get the logged-in user's profile
## Products
GET /api/products - Get all products
GET /api/products/:id - Get a single product by ID
POST /api/products - Create a new product (admin only)
PUT /api/products/:id - Update a product (admin only)
DELETE /api/products/:id - Delete a product (admin only)
## Cart
POST /api/cart - Add an item to the user's cart
GET /api/cart/:userId - Get items in the user's cart
DELETE /api/cart/:itemId - Remove an item from the cart
# Orders
POST /api/orders - Create a new order
GET /api/orders/:userId - Get user's order history
Features Breakdown
# User Authentication
Users can create an account, log in, and manage their profile.
JWT is used for token-based authentication, and all protected routes require a valid token.
# Product Browsing
Users can view products, search by keywords, and filter by categories.
Pagination is implemented for the product listing page.
# Shopping Cart
Logged-in users can add products to their cart, adjust quantities, and remove items.
Cart data is stored in the database for persistent shopping experience.
# Checkout & Payments
Integrated with Stripe/PayPal for payment processing.
Users can complete the checkout process, and their order is saved in the system.
Admin Panel
Admins can manage products, including adding, editing, and removing items.
Admins can also view and manage customer orders.
Contributing
# Fork the repository.
Create a feature branch (git checkout -b feature/YourFeature).
Commit your changes (git commit -m 'Add some feature').
Push to the branch (git push origin feature/YourFeature).
# Open a pull request.
