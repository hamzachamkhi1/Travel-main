# Local Setup Guide - Complete PHP Version

This guide will help you run the FULL travel booking website with PHP, MySQL database, and all features working locally.

## 🚀 **Step 1: Install XAMPP**

1. **Download XAMPP**: https://www.apachefriends.org/download.html
2. **Install XAMPP** (choose default options)
3. **Start XAMPP Control Panel**
4. **Start Apache and MySQL** services

## 🗄️ **Step 2: Set Up Database**

1. **Open phpMyAdmin**: http://localhost/phpmyadmin
2. **Create new database**:
   - Click "New" on the left sidebar
   - Database name: `TP_web`
   - Click "Create"

3. **Import database files**:
   - Click on your `TP_web` database
   - Click "Import" tab
   - Import these files in order:
     - `TP_web.sql` (main structure)
     - `airline.sql`
     - `airport.sql`
     - `cities.sql`
     - `country.sql`
     - `hotel.sql`

## 📁 **Step 3: Deploy Your Files**

1. **Copy your project** to XAMPP directory:
   - Go to: `C:\xampp\htdocs\`
   - Create folder: `travel-main`
   - Copy ALL your project files there

2. **Configure database connection**:
   - Edit `database.php`
   - Update with your local settings:
   ```php
   $con = mysqli_connect("localhost","root","","TP_web");
   ```

## 🌐 **Step 4: Access Your Website**

1. **Open browser**
2. **Go to**: http://localhost/travel-main/
3. **Your website should work with all features!**

## 🔧 **Step 5: Test All Features**

✅ **Flight Search**: http://localhost/travel-main/search/flight.php  
✅ **Hotel Search**: http://localhost/travel-main/search/hotel.php  
✅ **Admin Panel**: http://localhost/travel-main/admin/admin.php  
✅ **Booking System**: Full functionality with database  
✅ **Email Confirmations**: Configure SMTP settings  

## 📧 **Step 6: Configure Email (Optional)**

To enable email confirmations:
1. Edit email files in `email/` folder
2. Configure SMTP settings
3. Test booking confirmations

## 🎯 **What You'll Get:**

✅ **Complete booking system** with database  
✅ **Flight and hotel search** with real data  
✅ **Admin panel** to manage bookings  
✅ **Email confirmations** for bookings  
✅ **User registration and login**  
✅ **Payment processing** (if configured)  
✅ **All PHP functionality** working  

## 🆘 **Troubleshooting:**

**Database connection error**:
- Make sure MySQL is running in XAMPP
- Check database name is `TP_web`
- Verify username is `root` and password is empty

**Page not found**:
- Check file paths in XAMPP htdocs folder
- Make sure Apache is running

**PHP errors**:
- Check XAMPP error logs
- Enable error reporting in PHP

---

**Once this is working locally, we can deploy to a real web hosting service!** 