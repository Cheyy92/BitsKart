# BitsKart
Course Project for CS F13. 

(Tentative project structure, can and will change as time passes and we keep failing)

BitsKart/
├── .github/
│   └── workflows/
│       └── node.js.yml       # Optional: For CI/CD later
├── backend/
│   ├── config/               # Database connection strings, API keys
│   │   └── db.js
│   ├── controllers/          # Handles the logic for requests
│   │   ├── authController.js   # Logic for Google sign-in
│   │   ├── customerController.js # Logic for search, cart, orders
│   │   └── retailerController.js # Logic for wholesaler interaction
│   ├── middleware/           # Functions for auth checks, validation
│   │   └── authMiddleware.js
│   ├── models/               # Database schemas
│   │   ├── userModel.js        # Defines Customer, Retailer, Wholesaler roles
│   │   ├── productModel.js     # Defines clothing items
│   │   └── orderModel.js       # Defines customer and wholesale orders
│   ├── routes/               # API endpoint definitions
│   │   ├── authRoutes.js
│   │   ├── customerRoutes.js
│   │   └── retailerRoutes.js
│   ├── .env.example          # Example environment variables
│   ├── package.json          # Backend dependencies and scripts
│   └── server.js             # Main server entry point
│
├── frontend/
│   ├── public/               # Static files like index.html, logo
│   │   └── index.html
│   ├── src/
│   │   ├── api/                # Functions to call the backend API
│   │   │   ├── customerService.js
│   │   │   └── retailerService.js
│   │   ├── assets/             # Images, fonts, global CSS
│   │   ├── components/         # Reusable UI parts (e.g., Button, Navbar, ProductCard)
│   │   ├── context/            # For managing global state (e.g., logged-in user, cart)
│   │   │   └── AuthContext.js
│   │   ├── pages/              # Each page of the application
│   │   │   ├── LoginPage.js        # Common login page
│   │   │   ├── Customer/
│   │   │   │   └── HomePage.js       # Shows purchase history, search, etc.
│   │   │   └── Retailer/
│   │   │       └── Dashboard.js    # Shows nearby wholesalers, history
│   │   ├── App.js                # Main app component with routing
│   │   └── index.js              # Frontend entry point
│   └── package.json            # Frontend dependencies and scripts
│
├── .gitignore                  # Files to ignore (node_modules, .env)
├── LICENSE                     # Project license (e.g., MIT)
└── README.md  
