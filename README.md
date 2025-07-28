# Travel Booking Website

A comprehensive travel booking platform built with PHP, HTML, CSS, and JavaScript that allows users to search and book flights and hotels.

## 🌟 Features

- **Flight Search & Booking**: Search for flights with filters and make reservations
- **Hotel Search & Booking**: Find and book hotels with detailed information
- **Admin Panel**: Manage reservations, flights, and hotels
- **Email Confirmations**: Automated email notifications for bookings
- **Responsive Design**: Modern UI that works on all devices
- **Interactive Maps**: Integration with Google Maps for location services

## 🚀 Live Demo

[View Live Demo](https://your-username.github.io/travel-main/)

## 📋 Prerequisites

- PHP 7.4 or higher
- MySQL/MariaDB database
- Web server (Apache/Nginx)
- SMTP server for email functionality

## 🛠️ Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/travel-main.git
   cd travel-main
   ```

2. **Set up the database**
   - Create a MySQL database named `TP_web`
   - Import the SQL files from the `database/` folder:
     - `TP_web.sql` (main database structure)
     - `airline.sql`, `airport.sql`, `cities.sql`, `country.sql`, `hotel.sql` (data)

3. **Configure database connection**
   - Edit `database.php` with your database credentials:
   ```php
   $con = mysqli_connect("localhost","your_username","your_password","TP_web");
   ```

4. **Set up email configuration**
   - Configure SMTP settings in the email files for booking confirmations

5. **Deploy to web server**
   - Upload files to your web server
   - Ensure PHP and MySQL are properly configured

## 📁 Project Structure

```
travel-main/
├── aboutus/          # About us page
├── admin/           # Admin panel and management
├── css/             # Stylesheets
├── database/        # Database SQL files
├── email/           # Email templates and functionality
├── img/             # Images and assets
├── includes/        # PHP includes and actions
├── js/              # JavaScript files
├── search/          # Search functionality
└── index.php        # Main entry point
```

## 🎨 Features Overview

### Flight Booking System
- Search flights by destination, date, and preferences
- View flight details and pricing
- Make reservations with passenger information
- Email confirmation system

### Hotel Booking System
- Search hotels by location and dates
- View hotel details, amenities, and pricing
- Book rooms with guest information
- Confirmation emails

### Admin Panel
- Manage flight reservations
- Handle hotel bookings
- View and export booking data
- User management

## 🔧 Configuration

### Database Setup
1. Import `TP_web.sql` to create the main database structure
2. Import additional data files for airlines, airports, cities, etc.
3. Update database connection in `database.php`

### Email Configuration
Configure SMTP settings in email files for booking confirmations:
- `email/confirm.php`
- `email/emailConfirmation.php`
- `email/emailConfirmationHotel.php`

## 🌐 Deployment Options

### Option 1: Traditional Web Hosting
- Upload files to a web hosting service with PHP/MySQL support
- Configure database and email settings
- Access via your domain

### Option 2: Local Development
- Use XAMPP, WAMP, or similar local server
- Configure local database
- Access via `localhost/travel-main`

### Option 3: Cloud Deployment
- Deploy to services like Heroku, DigitalOcean, or AWS
- Configure environment variables for database and email
- Set up SSL certificates for security

## 📧 Email Setup

The application sends confirmation emails for bookings. Configure your SMTP settings:

```php
// Example SMTP configuration
$smtp_host = 'smtp.gmail.com';
$smtp_port = 587;
$smtp_username = 'your-email@gmail.com';
$smtp_password = 'your-app-password';
```

## 🔒 Security Considerations

- Change default database credentials
- Use HTTPS in production
- Implement proper input validation
- Regular security updates
- Backup database regularly

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Authors

- **Your Name** - *Initial work* - [YourGitHub](https://github.com/your-username)

## 🙏 Acknowledgments

- Icons and images used in the project
- Open source libraries and frameworks
- Community contributors

## 📞 Support

If you encounter any issues or have questions:
- Create an issue on GitHub
- Contact: your-email@example.com

---

**Note**: This is a PHP-based application that requires a web server with PHP and MySQL support. For a static version that can run on GitHub Pages, consider converting to a JavaScript-based solution or using a static site generator. 