# GAMING AVIYA - Installation Guide

## Quick Start Guide

Follow these simple steps to get your GAMING AVIYA website up and running!

---

## Method 1: Using XAMPP (Recommended for Beginners)

### Step 1: Install XAMPP
1. Download XAMPP from [https://www.apachefriends.org/](https://www.apachefriends.org/)
2. Install XAMPP on your computer
3. Launch XAMPP Control Panel

### Step 2: Deploy the Website
1. Extract the `gaming-aviya` folder
2. Copy the entire `gaming-aviya` folder to:
   - **Windows**: `C:\xampp\htdocs\`
   - **Mac**: `/Applications/XAMPP/htdocs/`
   - **Linux**: `/opt/lampp/htdocs/`

### Step 3: Start Services
1. Open XAMPP Control Panel
2. Click **Start** next to **Apache**
3. Click **Start** next to **MySQL**
4. Wait for both services to show green status

### Step 4: Access the Website
1. Open your web browser
2. Go to: `http://localhost/gaming-aviya/`
3. You should see the GAMING AVIYA homepage!

### Step 5: Test Registration & Login
1. Click "Sign Up" or go to `http://localhost/gaming-aviya/register.html`
2. Create a test account:
   - Username: `testuser`
   - Email: `test@example.com`
   - Password: `Test@123`
3. After registration, you'll be automatically logged in
4. Try logging out and logging back in

---

## Method 2: Using PHP Built-in Server

### Requirements
- PHP 7.4 or higher installed on your system
- MySQL server running

### Step 1: Extract Files
```bash
# Extract the gaming-aviya folder to any location
cd /path/to/gaming-aviya
```

### Step 2: Configure Database
1. Create a MySQL database named `gaming_aviya`
2. Update credentials in `php/config.php` if needed

### Step 3: Start PHP Server
```bash
php -S localhost:8000
```

### Step 4: Access Website
Open browser and go to: `http://localhost:8000/`

---

## Method 3: Using WAMP Server

### Step 1: Install WAMP
1. Download WAMP from [http://www.wampserver.com/](http://www.wampserver.com/)
2. Install and launch WAMP

### Step 2: Deploy Files
1. Copy `gaming-aviya` folder to `C:\wamp64\www\`

### Step 3: Start Services
1. Left-click WAMP icon in system tray
2. Ensure all services are green
3. Access via `http://localhost/gaming-aviya/`

---

## Database Configuration

### Automatic Setup (Default)
The database and tables are created automatically on first run. No manual setup needed!

### Manual Setup (Optional)
If you prefer manual setup:

1. Open phpMyAdmin: `http://localhost/phpmyadmin/`
2. Create database: `gaming_aviya`
3. The tables will be created automatically when you first access the site

### Database Credentials
Default credentials in `php/config.php`:
```php
DB_HOST: localhost
DB_USER: root
DB_PASS: (empty)
DB_NAME: gaming_aviya
```

**Change these if your setup is different!**

---

## Troubleshooting

### Problem: "Database connection failed"
**Solution:**
1. Make sure MySQL is running in XAMPP/WAMP
2. Check database credentials in `php/config.php`
3. Verify database `gaming_aviya` exists

### Problem: "Page not found" or 404 error
**Solution:**
1. Check that Apache is running
2. Verify the folder is in the correct location (`htdocs`)
3. Make sure you're using the correct URL: `http://localhost/gaming-aviya/`

### Problem: CSS/JS not loading
**Solution:**
1. Check browser console for errors (F12)
2. Verify all files are extracted properly
3. Clear browser cache (Ctrl+F5)

### Problem: Registration/Login not working
**Solution:**
1. Check browser console for errors
2. Verify MySQL is running
3. Check that `php/config.php` has correct database credentials
4. Make sure PHP version is 7.4 or higher

### Problem: Blank page after submitting forms
**Solution:**
1. Enable PHP error reporting
2. Check PHP error logs in XAMPP/WAMP
3. Verify database tables were created

---

## Testing Checklist

After installation, test these features:

- [ ] Homepage loads correctly
- [ ] Navigation menu works
- [ ] Animations are smooth
- [ ] Registration page opens
- [ ] Can create a new account
- [ ] Login page opens
- [ ] Can login with created account
- [ ] Password visibility toggle works
- [ ] Password strength indicator works
- [ ] Form validation works
- [ ] Responsive design on mobile

---

## File Permissions (Linux/Mac)

If you encounter permission issues:

```bash
cd /path/to/gaming-aviya
chmod -R 755 .
chmod -R 777 php/
```

---

## Port Conflicts

If port 80 is already in use:

### XAMPP
1. Open XAMPP Control Panel
2. Click "Config" next to Apache
3. Select "httpd.conf"
4. Change `Listen 80` to `Listen 8080`
5. Save and restart Apache
6. Access via: `http://localhost:8080/gaming-aviya/`

---

## Security Notes

### For Development
Current settings are fine for local development.

### For Production
Before deploying to a live server:

1. **Update Database Credentials**
   ```php
   // Use strong passwords
   define('DB_PASS', 'your-strong-password');
   ```

2. **Enable HTTPS**
   ```php
   // In config.php
   ini_set('session.cookie_secure', 1);
   ```

3. **Update CORS Settings**
   ```php
   // Restrict to your domain
   header('Access-Control-Allow-Origin: https://yourdomain.com');
   ```

4. **Disable Error Display**
   ```php
   ini_set('display_errors', 0);
   error_reporting(0);
   ```

---

## System Requirements

### Minimum
- PHP 7.4+
- MySQL 5.7+
- 50MB disk space
- Modern web browser

### Recommended
- PHP 8.0+
- MySQL 8.0+
- 100MB disk space
- Chrome/Firefox latest version

---

## Getting Help

If you encounter issues:

1. Check the troubleshooting section above
2. Review the README.md file
3. Check browser console for JavaScript errors (F12)
4. Check PHP error logs in XAMPP/WAMP
5. Verify all files are extracted correctly

---

## Next Steps

After successful installation:

1. **Customize the Design**
   - Edit `css/style.css` to change colors and styles
   - Modify HTML files to update content

2. **Add Your Content**
   - Replace placeholder images
   - Update game information
   - Add your contact details

3. **Configure Email**
   - Set up email verification (future feature)
   - Configure password reset emails

4. **Deploy to Production**
   - Choose a web hosting provider
   - Upload files via FTP/cPanel
   - Configure production database

---

## Success! 🎉

If you can see the GAMING AVIYA homepage and create an account, you're all set!

Enjoy your new gaming platform! 🎮

---

**Need more help?** Check the README.md file for detailed documentation.
