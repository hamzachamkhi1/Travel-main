# GitHub Setup Guide

Follow these steps to upload your travel booking website to GitHub and create a live demo link.

## 🚀 Step 1: Create a GitHub Repository

1. **Go to GitHub.com** and sign in to your account
2. **Click the "+" icon** in the top right corner
3. **Select "New repository"**
4. **Fill in the details**:
   - Repository name: `travel-booking-website` (or your preferred name)
   - Description: `A comprehensive travel booking platform built with PHP, HTML, CSS, and JavaScript`
   - Make it **Public** (required for free GitHub Pages)
   - **Don't** initialize with README (we already have one)
5. **Click "Create repository"**

## 📁 Step 2: Upload Your Project

### Option A: Using GitHub Desktop (Recommended for beginners)

1. **Download GitHub Desktop** from [desktop.github.com](https://desktop.github.com/)
2. **Install and sign in** with your GitHub account
3. **Clone the repository**:
   - Click "Clone a repository from the Internet"
   - Select your newly created repository
   - Choose a local path
   - Click "Clone"
4. **Copy your project files**:
   - Copy all files from your `travel-main` folder to the cloned repository folder
   - **Don't copy the `.git` folder** if it exists
5. **Commit and push**:
   - In GitHub Desktop, you'll see all your files
   - Add a commit message like "Initial commit: Travel booking website"
   - Click "Commit to main"
   - Click "Push origin"

### Option B: Using Command Line

1. **Open Command Prompt/Terminal** in your project folder
2. **Initialize Git and add files**:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Travel booking website"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
   git push -u origin main
   ```

## 🌐 Step 3: Enable GitHub Pages

1. **Go to your repository** on GitHub
2. **Click "Settings"** tab
3. **Scroll down to "Pages"** section (in the left sidebar)
4. **Under "Source"**, select **"Deploy from a branch"**
5. **Choose branch**: `gh-pages`
6. **Click "Save"**

## ⏳ Step 4: Wait for Deployment

- GitHub Actions will automatically build and deploy your demo
- This usually takes 2-5 minutes
- You can monitor progress in the "Actions" tab

## 🔗 Step 5: Get Your Live Link

Once deployment is complete:
- Your live demo will be available at: `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/`
- The link will be shown in the "Pages" section of your repository settings

## 📝 Step 6: Update README

1. **Edit the README.md file** in your repository
2. **Replace the demo link** with your actual link:
   ```markdown
   ## 🚀 Live Demo
   
   [View Live Demo](https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/)
   ```

## 🔧 Step 7: Configure Database (For Full Version)

If you want to deploy the full PHP version with database functionality:

1. **Choose a hosting provider** (see `deploy.md` for options)
2. **Upload your files** via FTP/SFTP
3. **Import the database** using phpMyAdmin
4. **Update database.php** with your hosting credentials
5. **Configure email settings** for booking confirmations

## 🎯 What You'll Get

### Static Demo (GitHub Pages)
- ✅ Beautiful UI showcase
- ✅ Responsive design
- ✅ Image galleries and animations
- ✅ Feature demonstrations
- ❌ No database functionality
- ❌ No booking system

### Full Version (Web Hosting)
- ✅ Complete booking system
- ✅ Database integration
- ✅ Email confirmations
- ✅ Admin panel
- ✅ All features working

## 🆘 Troubleshooting

### Common Issues:

1. **Files not showing up**:
   - Make sure you copied all files (including hidden ones)
   - Check that you're in the right directory

2. **GitHub Pages not working**:
   - Ensure repository is public
   - Check that GitHub Actions completed successfully
   - Wait a few minutes for deployment

3. **Images not loading**:
   - Check file paths in your HTML
   - Ensure all image files were uploaded

4. **Database connection errors**:
   - This is expected in the GitHub Pages demo
   - Full functionality requires web hosting with PHP/MySQL

## 📞 Need Help?

- Check the GitHub documentation
- Review the `deploy.md` file for hosting options
- Create an issue in your repository for specific problems

---

**Congratulations!** 🎉 Your travel booking website is now live on GitHub Pages!

**Next Steps:**
- Share your demo link with others
- Consider deploying the full version to a web host
- Add more features and improvements
- Keep your repository updated 