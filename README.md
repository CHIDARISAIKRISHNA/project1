# 🍽️ Delicious Bites Restaurant - Full Stack Application

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Node.js](https://img.shields.io/badge/Node.js-18+-green.svg)](https://nodejs.org/)
[![Express.js](https://img.shields.io/badge/Express.js-4.18+-blue.svg)](https://expressjs.com/)
[![SQLite](https://img.shields.io/badge/SQLite-3.0+-lightgrey.svg)](https://www.sqlite.org/)

A modern, feature-rich restaurant management system built with vanilla JavaScript, Node.js, Express, and SQLite. This application provides a complete solution for restaurant operations including menu management, order processing, table bookings, customer reviews, and administrative controls.

## 🌟 Live Demo

🔗 **[View Live Demo](https://your-demo-link.com)** *(Replace with your actual demo link)*

## 📸 Screenshots

### Welcome Page
![Welcome Page](https://via.placeholder.com/800x400/ff6b35/ffffff?text=Welcome+Page)

### Menu & Ordering
![Menu Page](https://via.placeholder.com/800x400/2c3e50/ffffff?text=Menu+%26+Ordering)

### Admin Dashboard
![Admin Dashboard](https://via.placeholder.com/800x400/27ae60/ffffff?text=Admin+Dashboard)

## ✨ Features

### 🎨 Frontend Features
- **🏠 Beautiful Welcome Page**: Animated hero section with restaurant branding
- **🍽️ Interactive Menu System**: Category-based browsing with real-time order summary
- **📅 Table Booking**: Complete reservation system with date/time selection
- **⭐ Customer Reviews**: Review submission and display with rating system
- **📞 Contact Forms**: Multiple contact methods with form validation
- **📧 Newsletter Signup**: Email subscription with popup notifications
- **📱 Responsive Design**: Perfect experience on all devices
- **🖨️ Print Receipts**: Professional receipt printing functionality
- **🔄 Real-time Updates**: Live order status and admin dashboard
- **🌐 Offline Support**: Basic functionality when connection is lost

### 🔧 Backend Features
- **🚀 RESTful API**: Complete API with all CRUD operations
- **🗄️ SQL Database**: SQLite with proper relationships and constraints
- **📦 Order Management**: Full order lifecycle with status tracking
- **🏢 Booking System**: Table reservation management
- **💬 Review System**: Customer feedback with approval workflow
- **📨 Contact Management**: Message handling and storage
- **📰 Newsletter System**: Email subscription management
- **📊 Analytics**: Sales statistics and reporting
- **✅ Data Validation**: Comprehensive input validation
- **🛡️ Error Handling**: Robust error management and logging

### 🗄️ Database Schema
- **menu_items**: Menu management with categories and pricing
- **orders**: Order processing and tracking
- **order_items**: Detailed order line items with relationships
- **bookings**: Table reservation system
- **reviews**: Customer feedback and rating system
- **contacts**: Contact form submissions
- **newsletter_subscribers**: Email subscription management

## 🚀 Quick Start

### Prerequisites
- **Node.js** (v14.0.0 or higher)
- **npm** (v6.0.0 or higher)
- **Git** (for cloning the repository)

### Installation

1. **Clone the repository**
   \`\`\`bash
   git clone https://github.com/CHIDARISAIKRISHNA/Restaurant-Website-SQL.git
   cd Restaurant-Website-SQL
   \`\`\`

2. **Install dependencies and setup database**
   \`\`\`bash
   # Install backend dependencies
   cd backend
   npm install
   
   # Setup database (create tables and seed data)
   npm run setup
   \`\`\`

3. **Start the backend server**
   \`\`\`bash
   npm start
   # Server will run on http://localhost:3000
   \`\`\`

4. **Start the frontend (in a new terminal)**
   \`\`\`bash
   cd ../frontend
   
   # Option 1: Using Node.js http-server (recommended)
   npx http-server -p 8080
   
   # Option 2: Using Python 3
   python -m http.server 8080
   
   # Option 3: Using the included startup scripts
   # Windows: run start.bat
   # Linux/Mac: run ./start.sh
   \`\`\`

5. **Access the application**
   - 🌐 **Frontend**: http://localhost:8080
   - 📡 **Backend API**: http://localhost:3000/api
   - 📊 **Health Check**: http://localhost:3000/api/health

## 📱 Application Sections

### 🏠 Welcome Page
- Stunning hero section with animations
- Restaurant statistics with counter animations
- Special offers showcase
- Call-to-action buttons for menu and booking

### 🍽️ Menu & Ordering
- **Categories**: Breakfast, Lunch, Snacks, Dinner, Beverages, Ice Creams
- **Real-time Cart**: Live order summary with pricing
- **Customer Info**: Name, phone, and email collection
- **Receipt Generation**: Professional bill with all details
- **Order Placement**: Direct integration with backend API

### 📅 Table Booking
- **Date Selection**: Calendar with availability
- **Time Slots**: Available booking times
- **Guest Management**: Party size selection
- **Special Occasions**: Birthday, anniversary, etc.
- **Special Requests**: Dietary requirements and preferences

### ⭐ Customer Reviews
- **Review Display**: Customer testimonials with ratings
- **Review Submission**: Easy-to-use review form
- **Rating System**: 5-star rating with statistics
- **Admin Approval**: Review moderation system

### 📞 Contact & Info
- **Contact Information**: Address, phone, email
- **Contact Form**: Direct message submission
- **Social Media**: Links to social platforms
- **Opening Hours**: Daily schedule display

## 🔌 API Documentation

### Menu Endpoints
```http
GET    /api/menu                    # Get all menu items grouped by category
GET    /api/menu/:category          # Get items by specific category
GET    /api/menu/item/:id           # Get single menu item
POST   /api/menu                    # Create new menu item (Admin)
PUT    /api/menu/:id                # Update menu item (Admin)
DELETE /api/menu/:id                # Delete menu item (Admin)
