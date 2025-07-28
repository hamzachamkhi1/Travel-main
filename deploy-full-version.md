# Deploy Full PHP Version - Complete Guide

This guide will help you deploy your travel booking website with ALL features working (PHP, MySQL, booking system, admin panel).

## 🚀 **Option 1: Free Hosting (Recommended for Students)**

### **InfinityFree (Free)**
1. **Sign up**: https://infinityfree.net/
2. **Create hosting account**
3. **Get free domain** (yourname.infinityfreeapp.com)
4. **Upload files** via File Manager
5. **Import database** via phpMyAdmin

### **000WebHost (Free)**
1. **Sign up**: https://www.000webhost.com/
2. **Create website**
3. **Upload files** via File Manager
4. **Import database** via phpMyAdmin

## 💰 **Option 2: Paid Hosting (Professional)**

### **Hostinger (Cheap & Reliable)**
1. **Sign up**: https://www.hostinger.com/
2. **Choose plan**: Premium ($2.99/month)
3. **Get domain** (free for first year)
4. **Upload files** via File Manager
5. **Import database** via phpMyAdmin

### **Bluehost (Popular)**
1. **Sign up**: https://www.bluehost.com/
2. **Choose plan**: Basic ($2.95/month)
3. **Get domain** (free for first year)
4. **Upload files** via File Manager
5. **Import database** via phpMyAdmin

## 📁 **Step-by-Step Deployment**

### **Step 1: Prepare Your Files**
1. **Download your project** from GitHub
2. **Update database.php** with hosting credentials
3. **Configure email settings** in email files

### **Step 2: Upload Files**
1. **Login to hosting control panel**
2. **Open File Manager**
3. **Upload ALL project files** to public_html folder
4. **Set permissions**: 644 for files, 755 for folders

### **Step 3: Set Up Database**
1. **Open phpMyAdmin** from hosting control panel
2. **Create new database** named `TP_web`
3. **Import SQL files** in this order:
   - `TP_web.sql`
   - `airline.sql`
   - `airport.sql`
   - `cities.sql`
   - `country.sql`
   - `hotel.sql`

### **Step 4: Configure Database Connection**
1. **Edit database.php** with your hosting credentials:
```php
$con = mysqli_connect("localhost","your_db_username","your_db_password","TP_web");
```

### **Step 5: Configure Email**
1. **Edit email files** in `email/` folder
2. **Update SMTP settings** with your hosting email
3. **Test email functionality**

## 🎯 **What You'll Get After Deployment:**

✅ **Complete booking system** with real database  
✅ **Flight search and booking** with live data  
✅ **Hotel search and booking** with real hotels  
✅ **Admin panel** to manage all bookings  
✅ **Email confirmations** for every booking  
✅ **User registration and login system**  
✅ **Payment processing** (if integrated)  
✅ **Responsive design** on all devices  
✅ **Professional domain** (yourdomain.com)  
✅ **SSL certificate** for security  

## 🔧 **Testing Your Deployed Website**

### **Test These Features:**
1. **Homepage**: Your main website
2. **Flight Search**: Search and book flights
3. **Hotel Search**: Search and book hotels
4. **Admin Panel**: Manage bookings
5. **Email Confirmations**: Test booking emails
6. **Mobile Responsiveness**: Test on phone/tablet

### **Admin Access:**
- **URL**: yourdomain.com/admin/admin.php
- **Username**: Check admin.sql file
- **Password**: Check admin.sql file

## 📧 **Email Configuration**

### **Gmail SMTP (Recommended)**
```php
$smtp_host = 'smtp.gmail.com';
$smtp_port = 587;
$smtp_username = 'your-email@gmail.com';
$smtp_password = 'your-app-password';
```

### **Hosting SMTP**
```php
$smtp_host = 'mail.yourdomain.com';
$smtp_port = 587;
$smtp_username = 'noreply@yourdomain.com';
$smtp_password = 'your-email-password';
```

## 🔒 **Security Checklist**

✅ **Change default admin credentials**  
✅ **Use HTTPS/SSL certificate**  
✅ **Set proper file permissions**  
✅ **Enable error logging**  
✅ **Regular database backups**  
✅ **Input validation**  
✅ **SQL injection protection**  

## 🆘 **Common Issues & Solutions**

### **Database Connection Error**
- Check database credentials
- Verify database exists
- Check hosting MySQL support

### **Email Not Sending**
- Configure SMTP settings
- Check hosting email limits
- Test with different email provider

### **Page Not Found (404)**
- Check file paths
- Verify .htaccess configuration
- Check hosting PHP support

### **Images Not Loading**
- Check file permissions
- Verify image paths
- Upload missing images

## 💡 **Recommended Hosting Providers**

### **For Students (Free/Cheap)**
1. **InfinityFree** - Free hosting
2. **000WebHost** - Free hosting
3. **Hostinger** - $2.99/month
4. **A2 Hosting** - $2.99/month

### **For Professionals**
1. **Bluehost** - $2.95/month
2. **SiteGround** - $3.99/month
3. **HostGator** - $2.75/month
4. **InMotion Hosting** - $2.99/month

## 🎯 **Your Live Website Will Be:**

```
https://yourdomain.com/
```

**With ALL features working:**
- ✅ Complete booking system
- ✅ Database functionality
- ✅ Admin panel
- ✅ Email confirmations
- ✅ Professional domain

---

**Choose your hosting option and I'll help you with the specific deployment steps!** 