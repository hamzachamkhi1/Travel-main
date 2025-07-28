# Deployment Guide

This guide will help you deploy your travel booking website to various hosting platforms.

## 🚀 Quick Deployment Options

### Option 1: GitHub Pages (Static Version)
Since your project uses PHP, you'll need to create a static version for GitHub Pages:

1. **Convert to Static HTML/JS** (Recommended for GitHub Pages)
   - Create a JavaScript-based version using React, Vue, or vanilla JS
   - Use a backend API service for database operations
   - Deploy frontend to GitHub Pages
   - Use services like Firebase, Supabase, or Heroku for backend

2. **Use GitHub Pages with Jekyll**
   - Convert PHP templates to Jekyll templates
   - Use GitHub's built-in Jekyll support
   - Implement client-side functionality with JavaScript

### Option 2: Traditional Web Hosting
1. **Choose a hosting provider**:
   - Bluehost, HostGator, SiteGround
   - A2 Hosting, InMotion Hosting
   - GoDaddy, Namecheap

2. **Upload files**:
   - Use FTP/SFTP to upload project files
   - Import database using phpMyAdmin
   - Configure domain and SSL

### Option 3: Cloud Platforms

#### Heroku
```bash
# Install Heroku CLI
# Create Procfile
echo "web: vendor/bin/heroku-php-apache2" > Procfile

# Deploy
git add .
git commit -m "Initial deployment"
heroku create your-app-name
git push heroku main
```

#### DigitalOcean App Platform
1. Connect your GitHub repository
2. Choose PHP as the runtime
3. Configure environment variables
4. Deploy automatically

#### AWS Elastic Beanstalk
1. Create an Elastic Beanstalk environment
2. Upload your application
3. Configure RDS for database
4. Set up environment variables

### Option 4: VPS Deployment

#### Ubuntu Server with LAMP Stack
```bash
# Update system
sudo apt update && sudo apt upgrade -y

# Install LAMP stack
sudo apt install apache2 mysql-server php php-mysql php-curl php-gd php-mbstring php-xml php-xmlrpc php-soap php-intl php-zip

# Configure Apache
sudo a2enmod rewrite
sudo systemctl restart apache2

# Configure MySQL
sudo mysql_secure_installation

# Upload files
sudo cp -r /path/to/your/project /var/www/html/

# Set permissions
sudo chown -R www-data:www-data /var/www/html/travel-main
sudo chmod -R 755 /var/www/html/travel-main
```

## 🔧 Configuration Steps

### 1. Database Setup
```sql
-- Create database
CREATE DATABASE TP_web;
USE TP_web;

-- Import SQL files
SOURCE /path/to/TP_web.sql;
SOURCE /path/to/airline.sql;
SOURCE /path/to/airport.sql;
SOURCE /path/to/cities.sql;
SOURCE /path/to/country.sql;
SOURCE /path/to/hotel.sql;
```

### 2. Environment Variables
Create a `.env` file for production:
```env
DB_HOST=localhost
DB_USER=your_db_user
DB_PASS=your_db_password
DB_NAME=TP_web
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your_email@gmail.com
SMTP_PASS=your_app_password
```

### 3. Email Configuration
Update email settings in:
- `email/confirm.php`
- `email/emailConfirmation.php`
- `email/emailConfirmationHotel.php`

## 🌐 Domain and SSL Setup

### Domain Configuration
1. Point your domain to your hosting provider
2. Configure DNS records (A, CNAME)
3. Wait for DNS propagation (24-48 hours)

### SSL Certificate
1. **Let's Encrypt (Free)**:
   ```bash
   sudo apt install certbot python3-certbot-apache
   sudo certbot --apache -d yourdomain.com
   ```

2. **Hosting Provider SSL**: Most providers offer free SSL certificates

## 📊 Performance Optimization

### 1. Enable Caching
```apache
# .htaccess
<IfModule mod_expires.c>
    ExpiresActive On
    ExpiresByType image/jpg "access plus 1 month"
    ExpiresByType image/jpeg "access plus 1 month"
    ExpiresByType image/gif "access plus 1 month"
    ExpiresByType image/png "access plus 1 month"
    ExpiresByType text/css "access plus 1 month"
    ExpiresByType application/javascript "access plus 1 month"
</IfModule>
```

### 2. Enable Compression
```apache
# .htaccess
<IfModule mod_deflate.c>
    AddOutputFilterByType DEFLATE text/plain
    AddOutputFilterByType DEFLATE text/html
    AddOutputFilterByType DEFLATE text/xml
    AddOutputFilterByType DEFLATE text/css
    AddOutputFilterByType DEFLATE application/xml
    AddOutputFilterByType DEFLATE application/xhtml+xml
    AddOutputFilterByType DEFLATE application/rss+xml
    AddOutputFilterByType DEFLATE application/javascript
    AddOutputFilterByType DEFLATE application/x-javascript
</IfModule>
```

## 🔒 Security Measures

### 1. File Permissions
```bash
# Set proper permissions
find /var/www/html/travel-main -type f -exec chmod 644 {} \;
find /var/www/html/travel-main -type d -exec chmod 755 {} \;
chmod 600 /var/www/html/travel-main/database.php
```

### 2. Hide Sensitive Files
```apache
# .htaccess
<Files "database.php">
    Order allow,deny
    Deny from all
</Files>

<Files ".env">
    Order allow,deny
    Deny from all
</Files>
```

### 3. Input Validation
Ensure all user inputs are properly validated and sanitized in your PHP files.

## 📱 Mobile Optimization

### 1. Responsive Design
Your CSS already includes responsive design. Test on various devices.

### 2. Progressive Web App (PWA)
Consider adding PWA features:
- Service Worker for offline functionality
- Web App Manifest
- Push notifications

## 🔍 Monitoring and Maintenance

### 1. Error Logging
```php
// Add to your PHP files
error_reporting(E_ALL);
ini_set('display_errors', 0);
ini_set('log_errors', 1);
ini_set('error_log', '/path/to/error.log');
```

### 2. Regular Backups
```bash
# Database backup script
#!/bin/bash
mysqldump -u username -p TP_web > backup_$(date +%Y%m%d_%H%M%S).sql
```

### 3. Performance Monitoring
- Use tools like Google PageSpeed Insights
- Monitor server resources
- Set up uptime monitoring

## 🆘 Troubleshooting

### Common Issues

1. **Database Connection Error**:
   - Check database credentials
   - Ensure MySQL service is running
   - Verify database exists

2. **Email Not Sending**:
   - Check SMTP settings
   - Verify email credentials
   - Check server firewall settings

3. **404 Errors**:
   - Check .htaccess configuration
   - Verify file permissions
   - Check Apache mod_rewrite

4. **Performance Issues**:
   - Enable caching
   - Optimize images
   - Use CDN for static assets

## 📞 Support

For deployment issues:
1. Check hosting provider documentation
2. Review error logs
3. Contact hosting support
4. Create GitHub issues for code-related problems

---

**Remember**: Always test your deployment in a staging environment before going live! 

## 🚀 **QUICK SOLUTION - Create Repository First:**

**Please do this right now:**

1. **Open your browser**
2. **Go to**: https://github.com/new
3. **Fill in**:
   - Repository name: `travel-booking-website`
   - Description: `A comprehensive travel booking platform`
   - Make it **Public**
   - **Don't** initialize with README
4. **Click "Create repository"**

**Once you've created the repository, your live link will be:**
```
https://hamzachamkhi1.github.io/travel-booking-website/
```

## 🔐 **If you get authentication errors:**

You might need to set up a Personal Access Token:

1. Go to GitHub → Settings → Developer settings → Personal access tokens
2. Generate a new token with `repo` permissions
3. Use the token as your password when pushing

## 📋 **After creating the repository:**

Come back here and I'll help you push your code and get your live demo working!

**Have you created the repository on GitHub yet?** If yes, let me know and I'll help you push the code immediately! 

## 🚀 **YOUR CODE IS NOW ON GITHUB!**

Your repository is at: `https://github.com/hamzachamkhi1/Travel-main`

## 🌐 **NOW SET UP GITHUB PAGES FOR YOUR LIVE DEMO:**

### **Step 1: Enable GitHub Pages**
1. **Go to**: https://github.com/hamzachamkhi1/Travel-main
2. **Click "Settings"** tab
3. **Scroll down to "Pages"** in the left sidebar
4. **Under "Source"**, select **"Deploy from a branch"**
5. **Choose branch**: `gh-pages`
6. **Click "Save"**

### **Step 2: Wait for GitHub Actions**
- GitHub Actions will automatically build and deploy your demo
- This usually takes 2-5 minutes
- You can monitor progress in the "Actions" tab

### **Step 3: Get Your Live Demo Link**
Once deployment is complete, your live demo will be available at:

## 🚀 **YOUR FULL LIVE DEMO LINK:**
```
<code_block_to_apply_changes_from>
```

## 📋 **What You'll Get:**

✅ **Beautiful UI showcase** with your existing design  
✅ **Responsive layout** and animations  
✅ **Image galleries** and interactive elements  
✅ **Feature demonstrations**  
✅ **Professional portfolio** ready to share  

## 🔧 **If you want the full PHP version with database:**

Follow the `deploy.md` guide to deploy to:
- Traditional web hosting (Bluehost, HostGator, etc.)
- Cloud platforms (Heroku, DigitalOcean, AWS)
- VPS with LAMP stack

**Go ahead and enable GitHub Pages now, then check your live demo at:**
```
https://hamzachamkhi1.github.io/Travel-main/
```

Let me know when you've enabled GitHub Pages and I'll help you with any issues! 🎯 