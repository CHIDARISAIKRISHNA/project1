# 🍽️ Delicious Bites Restaurant - Full Stack Application

A complete restaurant management system built with vanilla JavaScript, Node.js, Express, and SQLite.

## 📋 Project Overview

**Frontend Features:**
- Interactive menu with categories (Breakfast, Lunch, Dinner, Snacks, Beverages, Ice Creams)
- Real-time order summary and bill generation
- Table booking system with date/time selection
- Customer review and rating system
- Contact forms and newsletter subscription
- Admin dashboard for order management
- Responsive design for all devices

**Backend Features:**
- RESTful API with full CRUD operations
- SQLite database with proper relationships
- Order processing and status tracking
- Table booking management
- Customer review system with approval
- Sales analytics and reporting
- Input validation and error handling

**Database Tables:**
- `menu_items` - Menu management with categories
- `orders` & `order_items` - Order processing
- `bookings` - Table reservations
- `reviews` - Customer feedback
- `contacts` - Contact form submissions
- `newsletter_subscribers` - Email subscriptions

## 🚀 Quick Setup

### Prerequisites
\`\`\`bash
# Check if you have Node.js installed
node --version
npm --version
\`\`\`

### Installation & Setup

**1. Clone the repository**
\`\`\`bash
git clone https://github.com/CHIDARISAIKRISHNA/Restaurant-Website-SQL.git
cd Restaurant-Website-SQL
\`\`\`

**2. Setup Backend**
\`\`\`bash
# Navigate to backend directory
cd backend

# Install dependencies
npm install

# Setup database (creates tables and seeds data)
npm run setup

# Start backend server
npm start
\`\`\`

**3. Setup Frontend (New Terminal)**
\`\`\`bash
# Navigate to frontend directory
cd frontend

# Option 1: Using Node.js http-server
npx http-server -p 8080

# Option 2: Using Python 3
python -m http.server 8080

# Option 3: Using Python 2
python -m SimpleHTTPServer 8080
\`\`\`

**4. Access Application**
- Frontend: http://localhost:8080
- Backend API: http://localhost:3000/api
- Health Check: http://localhost:3000/api/health

## 🔧 Development Commands

### Backend Commands
\`\`\`bash
cd backend

# Start development server with auto-reload
npm run dev

# Reset database completely
npm run reset-db

# Run migrations only
npm run migrate

# Seed data only
npm run seed

# Complete setup (migrate + seed)
npm run setup
\`\`\`

### Database Management
\`\`\`bash
# Reset and recreate database
cd backend
rm -f data/restaurant.db
npm run setup

# Check database health
curl http://localhost:3000/api/health
\`\`\`

## 📡 API Endpoints

### Menu
\`\`\`bash
GET    /api/menu                    # Get all menu items
GET    /api/menu/:category          # Get items by category
POST   /api/menu                    # Create menu item
PUT    /api/menu/:id                # Update menu item
DELETE /api/menu/:id                # Delete menu item
\`\`\`

### Orders
\`\`\`bash
GET    /api/orders                  # Get all orders
POST   /api/orders                  # Create new order
PUT    /api/orders/:id/status       # Update order status
GET    /api/orders/stats/sales      # Get sales statistics
\`\`\`

### Bookings
\`\`\`bash
GET    /api/bookings               # Get all bookings
POST   /api/bookings               # Create new booking
PUT    /api/bookings/:id/status    # Update booking status
\`\`\`

### Reviews
\`\`\`bash
GET    /api/reviews                # Get approved reviews
POST   /api/reviews                # Submit new review
PUT    /api/reviews/:id/status     # Update review status
\`\`\`

## 🛠️ Project Structure

\`\`\`
restaurant-fullstack/
├── backend/
│   ├── config/database.js         # Database configuration
│   ├── models/                    # Data models
│   ├── routes/                    # API routes
│   ├── migrations/                # Database setup
│   ├── data/restaurant.db         # SQLite database
│   └── server.js                  # Main server
├── frontend/
│   ├── index.html                 # Main HTML
│   ├── styles.css                 # All styles
│   └── app.js                     # JavaScript logic
└── README.md
\`\`\`

## 🐛 Troubleshooting

### Common Issues

**Database Error:**
\`\`\`bash
cd backend
rm -f data/restaurant.db
npm run setup
\`\`\`

**Port Already in Use:**
\`\`\`bash
# Kill process on port 3000
lsof -ti:3000 | xargs kill -9

# Or use different port
PORT=3001 npm start
\`\`\`

**Menu Not Loading:**
\`\`\`bash
# Check backend is running
curl http://localhost:3000/api/health

# Check menu endpoint
curl http://localhost:3000/api/menu
\`\`\`

**CORS Issues:**
- Ensure backend runs on port 3000
- Check `API_BASE_URL` in `frontend/app.js`

## 🚀 Deployment

### Backend (Heroku)
\`\`\`bash
# Install Heroku CLI
heroku create your-restaurant-api
git push heroku main
\`\`\`

### Frontend (Netlify)
\`\`\`bash
# Build and deploy frontend folder
# Or drag-drop frontend folder to Netlify
\`\`\`

### Environment Variables
\`\`\`bash
# For production deployment
PORT=3000
NODE_ENV=production
\`\`\`

## 📦 Dependencies

**Backend:**
- express - Web framework
- cors - Cross-origin requests
- sqlite3 - Database

**Frontend:**
- Vanilla JavaScript
- Font Awesome (CDN)
- Google Fonts (CDN)

## 👨‍💻 Author

**Chidari Sai Krishna**
- GitHub: [@CHIDARISAIKRISHNA](https://github.com/CHIDARISAIKRISHNA)

## 📄 License

MIT License - see LICENSE file for details.
