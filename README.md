# homteq-ecommerce-platform

## Overview
homteq is a highly-specialized e-commerce platform for smart home technology products. The website offers a wide range of devices at competitive prices to make homes and lives smarter, including smart security systems, energy management solutions, and smart speakers.

## Features
- Responsive web design for various devices
- Product browsing and categorization
- Detailed product pages with images and descriptions
- Shopping cart functionality
- Session-based user data storage
- Real-time stock quantity tracking
- Streamlined checkout process

## Tech Stack
- **Backend**: PHP
- **Database**: MySQL
- **Frontend**: HTML5, CSS3
- **Additional**: Session management for cart functionality

## Project Structure
```
homteq/
├── images/            # Product images directory
├── aboutus.php        # Company information page
├── basket.php         # Shopping cart functionality
├── db.php             # Database connection configuration
├── footfile.html      # Footer layout component
├── headfile.html      # Header layout component
├── index.php          # Homepage with product listings
├── mystylesheet.css   # CSS styling
├── prodbuy.php        # Individual product page
├── template.php       # Template file for new pages
└── bgimg.jpg          # Background image
```

## Installation Guide

### Prerequisites
- PHP 7.0 or higher
- MySQL 5.7 or higher
- Web server (Apache/Nginx)

### Setup Steps
1. Clone the repository
```bash
git clone https://github.com/yourusername/homteq-ecommerce-platform.git
```

2. Set up the MySQL database
```sql
CREATE DATABASE homteq;
USE homteq;

CREATE TABLE Product (
  prodId INT PRIMARY KEY AUTO_INCREMENT,
  prodName VARCHAR(200) NOT NULL,
  prodPicNameSmall VARCHAR(100),
  prodPicNameLarge VARCHAR(100),
  prodDescripShort VARCHAR(1000),
  prodDescripLong TEXT,
  prodPrice DECIMAL(8,2) NOT NULL,
  prodQuantity INT NOT NULL
);

-- Sample product data can be inserted here
```

3. Configure database connection
   - Open `db.php`
   - Update the database credentials:
```php
$dbhost = 'localhost';  // Your database host
$dbuser = 'root';       // Your database username
$dbpass = '';           // Your database password
$dbname = 'homteq';     // Database name
```

4. Place the project files in your web server directory
5. Access the website via browser (e.g., http://localhost/homteq)

## Key System Components

### Product Browsing
The `index.php` page displays all available products with thumbnails, short descriptions, and prices. Users can click on any product to view detailed information.

### Product Details
The `prodbuy.php` page shows comprehensive product information including larger images, detailed descriptions, pricing, and available stock quantities. Users can select quantities and add items to their shopping cart.

### Shopping Cart
The `basket.php` page manages the user's shopping cart, allowing them to:
- View selected items
- See individual and total prices
- Adjust quantities
- Continue shopping or proceed to checkout

### About Us
The `aboutus.php` page provides information about homteq's mission and the types of smart home technology offered, including smart security, energy solutions, and speakers.

## Future Enhancements
- User registration and authentication system
- Customer profiles with saved preferences
- Order history tracking
- Payment gateway integration
- Admin dashboard for inventory management
- Product reviews and ratings
- Advanced search functionality
- Product comparison tools
- Wishlist feature

## License
MIT License

## Contact
For questions or support, please contact:
- **Address**: 115 New Cavendish Street, London, W1W 6UW, UK
- **Phone**: +442079115000

---

© homteq, 2022-2025
