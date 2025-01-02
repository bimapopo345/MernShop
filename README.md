# MernShop

A comprehensive e-commerce application built using the MERN stack (MongoDB, Express, React, Node.js). MernShop allows users to browse products, add items to their cart, proceed to checkout, and manage their orders. Admin users have the capability to manage products, orders, and user accounts. The application also integrates PayPal for secure payment processing.

## Features and Functionality

- **User Authentication**: Register and log in using secure JWT-based authentication.
- **Product Management**: View a list of products, search for specific items, and view detailed product information.
- **Shopping Cart**: Add, update, and remove products from the cart.
- **Checkout Process**: Enter shipping information, select payment methods, and place orders.
- **Payment Integration**: Secure payments via PayPal (sandbox environment).
- **Order Tracking**: Users can view their order history and track the status of their orders.
- **Admin Panel**:
  - **Product CRUD**: Create, read, update, and delete products.
  - **User Management**: View all users, promote/demote admin status, and delete users.
  - **Order Management**: View all orders, update payment and delivery statuses.
- **Responsive Design**: Optimized for various devices and screen sizes.
- **Image Uploads**: Upload and manage product images seamlessly.
- **Error Handling**: Comprehensive error handling and user-friendly messages.
- **Loader Indicators**: Visual feedback during data fetching and processing.

## Technology Stack

- **Backend**:
  - **Node.js & Express.js**: Server-side runtime and framework.
  - **MongoDB & Mongoose**: Database and ODM for data modeling.
  - **JWT (JSON Web Tokens)**: Authentication and authorization.
  - **PayPal API**: Payment processing.
  - **Multer**: Handling image uploads.
  - **bcryptjs**: Password hashing.
- **Frontend**:
  - **React**: User interface library.
  - **Redux Toolkit**: State management.
  - **React Router DOM**: Routing.
  - **React Bootstrap**: UI components and styling.
  - **Axios**: HTTP client for API communication.
  - **React Toastify**: Notifications.
  - **PayPal React SDK**: Payment integration.
- **Other Tools**:
  - **dotenv**: Environment variable management.
  - **ESLint & Prettier**: Code quality and formatting.

## Prerequisites

- **Node.js** (v14 or higher)
- **npm** or **pnpm** (Node package manager)
- **MongoDB** instance (local or cloud-based like MongoDB Atlas)
- **PayPal Developer Account** (for sandbox credentials)

## Installation Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/bimapopo345/MernShop.git
cd MernShop
```

### 2. Backend Setup

#### a. Navigate to Backend Directory
```bash
cd backend
```

#### b. Install Dependencies
Using npm:
```bash
npm install
```
Or using pnpm:
```bash
pnpm install
```

#### c. Configure Environment Variables
Create a `.env` file in the backend directory based on the `.env.example` file:
```bash
cp .env.example .env
```

Fill in the required variables in the `.env` file:
```
PORT=5000
MONGO_URI=<Your MongoDB Connection URI>
JWT_SECRET=<Your JWT Secret>
PAYPAL_CLIENT_ID=<Your PayPal Sandbox Client ID>
PAYPAL_APP_SECRET=<Your PayPal Sandbox Secret>
PAYPAL_API_URL=https://api-m.sandbox.paypal.com
NODE_ENV=development
```

#### d. Seed the Database (Optional)
To import dummy data (products and users):
```bash
npm run data:import
```

To destroy existing data:
```bash
npm run data:destroy
```

#### e. Start the Backend Server
```bash
npm run dev
```
The backend server will run on http://localhost:5000.

### 3. Frontend Setup

#### a. Navigate to Frontend Directory
```bash
cd ../frontend
```

#### b. Install Dependencies
Using npm:
```bash
npm install
```
Or using pnpm:
```bash
pnpm install
```

#### c. Start the Frontend Server
```bash
npm start
```
The frontend application will run on http://localhost:3000.

## Usage Guide

1. **Register an Account**: Navigate to the registration page and create a new user account.
2. **Login**: Log in using your registered credentials.
3. **Browse Products**: Explore the list of available products. Use the search bar to find specific items.
4. **Add to Cart**: Select desired products and add them to your shopping cart.
5. **Checkout**:
   - Shipping: Enter your shipping address.
   - Payment: Choose a payment method (PayPal).
   - Place Order: Review your order and complete the purchase.
6. **Order Tracking**: View your order history and track the status of your orders.
7. **Admin Panel** (for Admin Users):
   - Manage Products: Add new products, edit existing ones, or delete products.
   - Manage Users: View all users, promote or demote admin status, and delete users.
   - Manage Orders: View all orders, update payment statuses, and mark orders as delivered.

## API Documentation

Detailed API documentation is available in the source code. Key endpoints include:
- User Authentication (Register, Login)
- Product Management
- Order Creation and Management
- User Management (Admin)
- Image Upload

## Deployment

1. Build the Frontend:
```bash
npm run build --prefix frontend
```

2. Serve Static Files from Frontend:
Configure the backend to serve the frontend build files.

3. Deploy to Your Preferred Hosting Platform:
- Backend: Heroku, DigitalOcean, AWS
- Frontend: Can be served by backend or deployed to Vercel, Netlify

## Contributing

Contributions are welcome! 

1. Fork the Repository
2. Create a New Branch: `git checkout -b feature/YourFeature`
3. Make Your Changes and Commit: `git commit -m "Add your feature"`
4. Push to the Branch: `git push origin feature/YourFeature`
5. Create a Pull Request

## License

This project is licensed under the MIT License.

## Contact/Support

- **GitHub**: bimapopo345
- **Email**: admin@bimashop.com

Happy Shopping and Coding with MernShop! 🚀
