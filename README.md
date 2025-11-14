🍕 UTOPIA - Restaurant Ordering System A modern, full-stack Restaurant Ordering Web Application built with Node.js, Express, SQLite, and Vanilla JavaScript. Features user authentication, real-time order tracking, and an interactive menu browsing experience.

🎯 Key Features User Authentication & Profile ✅ User Registration with email, name, address, and password ✅ Secure Login System ✅ View User Profile (name, email, address, join date) ✅ Session persistence (stay logged in after page refresh) ✅ Logout functionality Menu & Browsing ✅ 6+ Categories of food items: Starters (Paneer Tikka, Chicken Lollipop, etc.) Pizzas (Margherita, BBQ Chicken, Paneer Tandoori, etc.) Breads (Naan, Roti, Kulcha, Paratha) Chaats (Pani Puri, Bhel Puri, Samosa Chaat, etc.) Rice Dishes (Biryani, Fried Rice) Gravies (Butter Chicken, Paneer Butter Masala, etc.) Desserts (Gulab Jamun, Rasgulla, Ice Cream, etc.) ✅ Real Food Images for each dish ✅ Veg/Non-Veg filter system ✅ Search functionality (filter dishes by name) ✅ Collapsible category sections ✅ Dish detail modal with descriptions and pricing Shopping Cart & Orders ✅ Add items to cart with quantity management ✅ Real-time cart badge counter ✅ View order summary with itemized bill ✅ Calculate Subtotal, GST (2.5%), and CGST (2.5%) ✅ Add special cooking instructions ✅ Place orders with Cash on Delivery option ✅ Orders linked to user profiles Order Tracking ✅ Real-time order status tracking ✅ Track last order with unique Order ID ✅ Order status updates: Pending → Preparing → Ready → Delivered ✅ Live polling (updates every 3 seconds) ✅ Order history per user Admin Features (Backend) ✅ View all orders ✅ Update order status ✅ Get order statistics ✅ Delete orders ✅ View today's orders UI/UX ✅ Beautiful gradient design with purple theme (#7B2CBF) ✅ Responsive layout (works on desktop, tablet, mobile) ✅ Smooth animations and transitions ✅ Splash screen with app branding ✅ Notification toasts for cart updates ✅ Confirmation pages for order placement ✅ Professional modal dialogs

🛠️ Technology Stack Frontend HTML5 - Semantic markup CSS3 - Flexbox, Grid, Gradients, Animations Vanilla JavaScript (ES6+) - No frameworks, pure JS Fetch API - For backend communication SessionStorage - For session persistence

Backend Node.js (v14+) - Runtime environment Express.js (v4.18.2) - Web framework SQLite3 (v5.1.6) - Lightweight database CORS - Cross-Origin Resource Sharing Body-Parser - JSON request parsing Database SQLite - File-based relational database

Two Main Tables: users - User registration & authentication orders - Order history with user linkage

📦 Installation & Setup Prerequisites Node.js (v14 or higher) npm (Node Package Manager) Any modern web browser (Chrome, Firefox, Edge, Safari)

Step 1: Backend Setup Navigate to backend folder: bash cd backend

Install dependencies: bash npm install

Start the backend server: bash node server.js

Expected output: text ✅ Database connected ✅ Users table ready ✅ Orders table ready 🚀 Server running at http://localhost:5000

Step 2: Frontend Setup Open index.html in your browser Use Live Server in VS Code (recommended), or Use Python's built-in server: bash python -m http.server 5500

Then open: http://localhost:5500 Start using the app!

📡 API Endpoints User Authentication Method Endpoint Description POST /api/register Register new user POST /api/login Login user GET /api/users/:id Get user profile PUT /api/users/:id Update user profile

Orders Method Endpoint Description POST /api/orders Place new order GET /api/orders Get all orders (Admin) GET /api/orders/:id Get single order GET /api/orders/user/:userId Get user's orders PUT /api/orders/:id Update order status DELETE /api/orders/:id Delete order

Health Check Method Endpoint Description GET /api/health Server health check

💾 Database Schema Users Table sql CREATE TABLE users ( id INTEGER PRIMARY KEY AUTOINCREMENT, name TEXT NOT NULL, email TEXT UNIQUE NOT NULL, address TEXT, password TEXT NOT NULL, created_at DATETIME DEFAULT CURRENT_TIMESTAMP );

Orders Table sql CREATE TABLE orders ( id INTEGER PRIMARY KEY AUTOINCREMENT, user_id INTEGER, items TEXT NOT NULL, subtotal REAL NOT NULL, gst REAL NOT NULL, cgst REAL NOT NULL, total REAL NOT NULL, cooking_instructions TEXT, order_date DATETIME DEFAULT CURRENT_TIMESTAMP, status TEXT DEFAULT 'Pending', FOREIGN KEY(user_id) REFERENCES users(id) );

Uses browser's built-in APIs: Fetch, SessionStorage, DOM API

✅ Frontend: HTML, CSS, Vanilla JavaScript ✅ Backend: Node.js, Express, RESTful API design ✅ Database: SQL, SQLite, data modeling
