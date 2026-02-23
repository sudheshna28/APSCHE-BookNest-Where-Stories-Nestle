# BookNest: Where Stories Nestle 📚

A full-stack online book shopping platform built with the MERN stack (MongoDB, Express.js, React, Node.js), featuring a modern UI, secure payment integration, comprehensive seller management system, and advanced rating & review functionality for book enthusiasts.



## 👥 Team Members

- **M. Sai Santosh Vamsi** - Full Stack Developer
- **D.V.J. Kranthi Kumar** - Full Stack Developer  
- **D.S.K. Prameela** - Full Stack Developer
- **D. Varthika** - Full Stack Developer

## 🚀 Features

### Customer Features
- **Book Discovery**: Browse books with advanced search and category filtering
- **Shopping Cart**: Add/remove books, quantity management, and coupon support
- **Secure Checkout**: Integrated Cashfree payment gateway with order tracking
- **Book Reviews & Ratings**: 5-star rating system with detailed customer reviews
- **Wishlist Management**: Save favorite books for later purchase
- **Order History**: Track order status and view past book purchases
- **Indian Rupee Support**: Native INR (₹) currency integration throughout the platform

### Seller Features
- **Seller Dashboard**: Comprehensive analytics and order management for book sellers
- **Book Management**: Add, edit, and delete books with image uploads (CRUD operations)
- **Order Management**: Update order status through complete lifecycle
- **Revenue Tracking**: Real-time revenue calculation and monitoring
- **Inventory Management**: Stock monitoring with alerts for low book inventory
- **Order Status Control**: Full control over order lifecycle (Pending → Processing → Shipping → Delivered)

### Admin Features
- **Multi-role System**: Customer, Seller, and Admin role management
- **Analytics Dashboard**: Detailed sales and revenue reports
- **User Management**: Comprehensive user and role administration

## 🛠️ Tech Stack

### Frontend
- **React** with **TypeScript**
- **Vite** for fast development and optimized building
- **Tailwind CSS** for modern styling
- **ShadCN UI** for consistent component library
- **React Router** for client-side navigation
- **Context API** for state management
- **Axios** for API communication

### Backend
- **Node.js** with **Express.js**
- **MongoDB** with **Mongoose** ODM
- **JWT** for secure authentication
- **Cashfree** payment gateway integration
- **Cloudinary** for book image uploads and management

### Key Libraries & Tools
- **@cashfreepayments/cashfree-js**: Secure payment processing
- **bcryptjs**: Password hashing and security
- **jsonwebtoken**: JWT token management
- **multer**: File upload handling for book images
- **mongoose**: MongoDB object modeling

## 📁 Project Structure

```
BookNest/
├── Client/                          # Frontend React Application
│   ├── src/
│   │   ├── components/             # Reusable UI components
│   │   │   ├── Navbar.tsx         # Navigation component
│   │   │   ├── ReviewSection.tsx  # Book reviews component
│   │   │   ├── Cards.tsx          # Book display cards
│   │   │   ├── Toasts.tsx         # Notification system
│   │   │   └── ui/                # ShadCN UI components
│   │   ├── pages/                 # Page components
│   │   │   ├── Home.tsx          # Landing page
│   │   │   ├── Books.tsx         # Book catalog
│   │   │   ├── Cart.tsx          # Shopping cart
│   │   │   ├── Dashboard.tsx     # Seller dashboard
│   │   │   ├── Login.tsx         # User authentication
│   │   │   └── Register.tsx      # User registration
│   │   ├── services/             # API services
│   │   │   └── api.ts            # Axios API handler
│   │   └── App.tsx              # Main app component
│   ├── package.json
│   └── vite.config.ts
├── server/                        # Backend Node.js Application
│   ├── controllers/              # Route controllers
│   │   ├── authController.js     # Authentication logic
│   │   ├── bookController.js     # Book management
│   │   ├── orderController.js    # Order processing
│   │   ├── reviewController.js   # Review system
│   │   └── userController.js     # User management
│   ├── models/                   # MongoDB schemas
│   │   ├── User.js              # User model
│   │   ├── Book.js              # Book model
│   │   ├── Order.js             # Order model
│   │   └── Review.js            # Review model
│   ├── routes/                   # API routes
│   │   ├── auth.js              # Authentication endpoints
│   │   ├── book.js              # Book management endpoints
│   │   ├── order.js             # Order processing endpoints
│   │   ├── review.js            # Review system endpoints
│   │   ├── user.js              # User management endpoints
│   │   └── analytics.js         # Analytics endpoints
│   ├── middleware/               # Custom middleware
│   │   └── auth.js              # JWT authentication middleware
│   ├── index.js                 # Server entry point
│   └── package.json
└── README.md
```

## 🚀 Getting Started

### Prerequisites
- **Node.js** (v16 or higher)
- **MongoDB** (v4.4 or higher)
- **npm** or **yarn** package manager
- **Cashfree** account for payment integration
- **Cloudinary** account for image uploads

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd BookNest
   ```

2. **Install dependencies**
   ```bash
   # Install backend dependencies
   cd server
   npm install

   # Install frontend dependencies
   cd ../Client
   npm install
   ```

3. **Environment Setup**

   Create `.env` file in the **server** directory:
   ```env
   PORT=5000
   MONGODB_URI=mongodb://localhost:27017/booknest
   JWT_SECRET=your_jwt_secret_key
   CASHFREE_CLIENT_ID=your_cashfree_client_id
   CASHFREE_CLIENT_SECRET=your_cashfree_client_secret
   CLOUDINARY_CLOUD_NAME=your_cloudinary_name
   CLOUDINARY_API_KEY=your_cloudinary_api_key
   CLOUDINARY_API_SECRET=your_cloudinary_api_secret
   ```

   Create `.env` file in the **Client** directory:
   ```env
   VITE_API_URL=http://localhost:5000
   VITE_CLOUDINARY_CLOUD_NAME=your_cloudinary_name
   VITE_CLOUDINARY_UPLOAD_PRESET=your_upload_preset
   ```

4. **Start the development servers**
   ```bash
   # Start backend server
   cd server
   npm run dev

   # Start frontend server (in new terminal)
   cd Client
   npm run dev
   ```

5. **Access the application**
   - **Frontend**: http://localhost:5173
   - **Backend API**: http://localhost:5000

## 💳 Payment Integration

BookNest integrates with **Cashfree Payment Gateway** for secure book purchases:

- **Sandbox Mode**: For testing with test credentials
- **Production Mode**: For live book transactions
- **Payment Methods**: Credit/Debit cards, UPI, Net Banking, Digital Wallets
- **Order Tracking**: Real-time payment status updates
- **Indian Rupee Support**: Native INR (₹) currency handling

### Payment Flow
1. Customer adds books to cart
2. Applies coupons if available
3. Proceeds to secure checkout
4. Cashfree payment session initiated
5. Customer completes payment
6. Order status updated to "paid"
7. Order confirmation and receipt sent

## ⭐ Rating & Review System

### Features
- **5-Star Rating System**: Interactive star rating for books
- **Review Management**: Write, edit, and delete book reviews
- **User Validation**: One review per customer per book
- **Real-time Updates**: Automatic book rating recalculation
- **Review Display**: Chronological listing with customer attribution

### Review Workflow
1. Customer purchases a book
2. Can write a review with rating (1-5 stars)
3. Review helps other customers make informed decisions
4. Book's average rating automatically updated
5. Reviews displayed on book detail page

## 📊 Database Schema

### User Model
```javascript
{
  email: String (unique),
  password: String (hashed),
  name: String,
  role: String (customer/seller/admin),
  wishlist: [ObjectId],
  createdAt: Date
}
```

### Book Model
```javascript
{
  title: String,
  author: String,
  description: String,
  price: Number,
  image: String,
  stock: Number,
  sellerId: ObjectId (ref: User),
  category: String,
  ratings: Number,        // Average rating
  reviews: Number,        // Total review count
  createdAt: Date
}
```

### Order Model
```javascript
{
  user: ObjectId (ref: User),
  orderItems: [{
    book: ObjectId (ref: Book),
    quantity: Number,
    price: Number
  }],
  shippingAddress: {
    address: String,
    city: String,
    postalCode: String,
    country: String
  },
  paymentInfo: {
    id: String,
    status: String,
    method: String
  },
  orderStatus: String (pending/processing/shipping/delivered),
  totalPrice: Number,
  createdAt: Date,
  deliveredAt: Date
}
```

### Review Model
```javascript
{
  book: ObjectId (ref: Book),
  user: ObjectId (ref: User),
  rating: Number (1-5),
  comment: String,
  userName: String,
  createdAt: Date
}
```

## 🔐 Authentication & Authorization

### JWT-based Authentication
- Secure token-based authentication system
- Role-based access control for different user types
- Protected routes for sensitive operations
- Automatic token validation and refresh

### User Roles
- **Customer**: Browse books, place orders, write reviews, manage wishlist
- **Seller**: Manage book inventory, view orders, update order status, track revenue
- **Admin**: Full system access, user management, platform analytics

## 🎨 UI/UX Features

### Design System
- **Modern Book Store Interface**: Clean, book-focused design
- **Indian Rupee Integration**: Native INR (₹) currency display
- **Responsive Design**: Mobile-first approach for all devices
- **ShadCN UI Components**: Consistent and accessible component library
- **Toast Notifications**: Real-time feedback for user actions

### Key Components
- **Book Cards**: Cover images, pricing, ratings, and quick actions
- **Shopping Cart**: Real-time updates, quantity controls, coupon application
- **Seller Dashboard**: Order management, revenue tracking, inventory overview
- **Review System**: Star ratings, customer feedback display
- **Search & Filter**: Advanced book discovery tools

## 📈 Business Logic

### Order Lifecycle Management
1. **Pending**: Order placed, awaiting payment
2. **Processing**: Payment confirmed, order being prepared
3. **Shipping**: Books shipped to customer
4. **Delivered**: Order successfully delivered

### Revenue Calculation
- **Seller Revenue**: Calculated from successfully delivered orders
- **Real-time Tracking**: Live revenue updates in seller dashboard
- **Historical Data**: Revenue trends and analytics

### Inventory Management
- **Stock Tracking**: Real-time book inventory updates
- **Low Stock Alerts**: Automatic notifications for sellers
- **Book Performance**: Track best-selling titles

## 🔧 API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user (customer/seller)
- `POST /api/auth/login` - User login with JWT token
- `GET /api/auth/me` - Get current authenticated user

### Books
- `GET /api/books` - Get all books with filtering and search
- `GET /api/books/:id` - Get single book details
- `POST /api/books` - Add new book (seller only)
- `PUT /api/books/:id` - Update book details (seller only)
- `DELETE /api/books/:id` - Delete book (seller only)

### Orders
- `GET /api/orders` - Get orders (filtered by user/seller role)
- `POST /api/orders/create-after-payment` - Create order after payment
- `POST /api/orders/cashfree` - Create Cashfree payment session
- `PUT /api/orders/:id/status` - Update order status (seller)

### Reviews
- `GET /api/reviews/book/:id` - Get reviews for specific book
- `POST /api/reviews` - Create new book review
- `PUT /api/reviews/:id` - Update existing review
- `DELETE /api/reviews/:id` - Delete review

### Users
- `GET /api/users/:id/wishlist` - Get user's wishlist
- `POST /api/users/:id/wishlist` - Add book to wishlist
- `DELETE /api/users/:id/wishlist` - Remove book from wishlist

### Analytics
- `GET /api/analytics` - Get sales and revenue analytics (admin/seller)

## 🚀 Deployment

### Frontend Deployment (Vercel)
```bash
cd Client
npm run build
# Deploy to Vercel (already deployed at booknest.vercel.app)
```

### Backend Deployment
```bash
cd server
# Set production environment variables
npm start
```

### Environment Variables for Production
- Update API URLs to production endpoints
- Configure secure JWT secrets
- Set up production payment gateway credentials
- Configure production MongoDB connection
- Set up production Cloudinary credentials

## 🧪 Testing Checklist

### Core Functionality
- [ ] User registration and authentication
- [ ] Book browsing and search functionality
- [ ] Shopping cart operations
- [ ] Coupon code application
- [ ] Checkout and payment process
- [ ] Order management and status updates
- [ ] Review and rating system
- [ ] Wishlist functionality
- [ ] Seller dashboard operations
- [ ] Inventory management
- [ ] Revenue tracking
- [ ] Currency display (Indian Rupee)

## 🔒 Security Features

- **Password Security**: bcryptjs hashing for user passwords
- **JWT Authentication**: Secure token-based session management
- **Input Validation**: Server-side validation for all user inputs
- **File Upload Security**: Secure image upload handling via Cloudinary
- **Role-based Access**: Proper authorization for different user roles
- **Environment Variables**: Secure credential management

## 📱 Mobile Responsiveness

BookNest is fully responsive and optimized for:
- **Desktop**: Full-featured book shopping experience
- **Tablet**: Touch-optimized interface for book browsing
- **Mobile**: Streamlined mobile book shopping experience

## ⚠️ Known Issues

### Current Limitations
- **Image Upload Issues**: May fail on slow network connections
- **Wishlist Sync**: Not synchronized across multiple devices
- **Payment Gateway**: Limited to Cashfree integration only

### Troubleshooting
- Ensure stable internet connection for image uploads
- Clear browser cache if experiencing loading issues
- Contact support for payment-related problems

## 🎯 Future Enhancements

### Planned Features
- **Razorpay Integration**: Additional payment gateway option
- **React Native Mobile App**: Dedicated mobile application
- **Live Order Tracking**: Real-time shipment tracking
- **Push Notifications**: Order updates and promotional alerts
- **Book Recommendations**: AI-powered book suggestions
- **Advanced Search**: Full-text search with filters
- **Author Profiles**: Dedicated author pages
- **Book Categories**: Enhanced categorization system

### Technical Improvements
- **Performance Optimization**: Caching and lazy loading
- **SEO Enhancement**: Better search engine optimization
- **PWA Support**: Progressive Web App features
- **Real-time Chat**: Customer-seller communication
- **Advanced Analytics**: Detailed sales insights

## 🤝 Contributing

We welcome contributions to BookNest! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 📞 Support & Contact

For support, questions, or collaboration:
- Create an issue in the repository
- Contact the development team
- Visit our live demo: [https://booknest.vercel.app](https://booknest.vercel.app)

## 🏆 Acknowledgments

- **MERN Stack Community** for excellent documentation and resources
- **Cashfree** for secure payment gateway integration
- **Cloudinary** for reliable image hosting services
- **Vercel** for seamless deployment platform

---

**BookNest: Where Stories Nestle** - Bringing book lovers and sellers together through modern technology and exceptional user experience. 📚✨
