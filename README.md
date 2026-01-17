# GAMING AVIYA 🎮

A modern, feature-rich gaming platform website with beautiful animations, user authentication, and responsive design.

## 🌟 Features

### Frontend Features
- **Modern UI/UX Design** - Sleek gaming-themed interface with gradient effects
- **Beautiful Animations** - Smooth transitions, particle effects, and interactive elements
- **Responsive Design** - Fully responsive across all devices (mobile, tablet, desktop)
- **Interactive Elements** - Hover effects, tilt animations, and ripple effects
- **Smooth Scrolling** - Seamless navigation with scroll animations
- **Custom Cursor** - Enhanced user experience with custom cursor effects
- **Parallax Effects** - Dynamic background animations
- **AOS (Animate On Scroll)** - Elements animate as you scroll

### Authentication System
- **User Registration** - Secure user sign-up with validation
- **User Login** - Secure authentication system
- **Password Strength Checker** - Real-time password strength indicator
- **Remember Me** - Optional persistent login
- **Session Management** - Secure session handling
- **Social Login Placeholders** - Ready for Google, Discord, and Steam integration

### Security Features
- **Password Hashing** - Bcrypt password encryption
- **SQL Injection Prevention** - Prepared statements
- **XSS Protection** - Input sanitization
- **CSRF Protection** - Session token validation
- **Secure Headers** - Security headers implementation

## 📁 Project Structure

```
gaming-aviya/
├── index.html              # Main landing page
├── login.html              # Login page
├── register.html           # Registration page
├── css/
│   └── style.css          # Main stylesheet with animations
├── js/
│   ├── animations.js      # Animation and interaction scripts
│   ├── auth.js            # Authentication handling
│   └── main.js            # Main page functionality
├── php/
│   ├── config.php         # Database configuration
│   ├── login.php          # Login handler
│   ├── register.php       # Registration handler
│   └── logout.php         # Logout handler
├── images/                # Image assets directory
└── README.md              # This file
```

## 🚀 Installation & Setup

### Prerequisites
- Web server (Apache/Nginx)
- PHP 7.4 or higher
- MySQL 5.7 or higher
- Modern web browser

### Step 1: Database Setup

1. Create a MySQL database named `gaming_aviya`
2. The database tables will be created automatically on first run
3. Update database credentials in `php/config.php` if needed:

```php
define('DB_HOST', 'localhost');
define('DB_USER', 'root');
define('DB_PASS', '');
define('DB_NAME', 'gaming_aviya');
```

### Step 2: Server Configuration

#### Using XAMPP/WAMP
1. Copy the `gaming-aviya` folder to `htdocs` directory
2. Start Apache and MySQL services
3. Access via `http://localhost/gaming-aviya/`

#### Using PHP Built-in Server
```bash
cd gaming-aviya
php -S localhost:8000
```
Access via `http://localhost:8000/`

### Step 3: Testing
1. Open `http://localhost/gaming-aviya/` in your browser
2. Navigate to the registration page
3. Create a test account
4. Login with your credentials

## 🎨 Customization

### Colors
Edit CSS variables in `css/style.css`:
```css
:root {
    --primary: #6366f1;
    --secondary: #00d4ff;
    --accent: #ff6b6b;
    /* Add more custom colors */
}
```

### Animations
Modify animation settings in `js/animations.js`:
- Particle count and behavior
- Scroll animation triggers
- Transition timings

### Content
- Update text content in HTML files
- Replace placeholder images in the games section
- Modify navigation links and footer information

## 🔐 Security Recommendations

For production deployment:

1. **Enable HTTPS** - Set `session.cookie_secure = 1` in `php/config.php`
2. **Update Database Credentials** - Use strong passwords
3. **Configure CORS** - Restrict allowed origins in `config.php`
4. **Add Rate Limiting** - Prevent brute force attacks
5. **Enable Error Logging** - Monitor application errors
6. **Regular Updates** - Keep PHP and MySQL updated

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Opera (latest)

## 🎯 Features Breakdown

### Pages

#### 1. Index Page (index.html)
- Hero section with animated background
- Features showcase
- Popular games grid
- Statistics counter
- Footer with social links

#### 2. Login Page (login.html)
- Email/password authentication
- Remember me option
- Password visibility toggle
- Social login buttons (placeholder)
- Forgot password link

#### 3. Register Page (register.html)
- Username, email, password fields
- Password strength indicator
- Password confirmation
- Terms & conditions checkbox
- Social registration buttons (placeholder)

### Database Schema

#### Users Table
```sql
- id (INT, PRIMARY KEY, AUTO_INCREMENT)
- username (VARCHAR(50), UNIQUE)
- email (VARCHAR(100), UNIQUE)
- password (VARCHAR(255))
- created_at (TIMESTAMP)
- last_login (TIMESTAMP)
- status (ENUM: active, inactive, banned)
```

#### User Sessions Table
```sql
- id (INT, PRIMARY KEY, AUTO_INCREMENT)
- user_id (INT, FOREIGN KEY)
- session_token (VARCHAR(255), UNIQUE)
- ip_address (VARCHAR(45))
- user_agent (TEXT)
- created_at (TIMESTAMP)
- expires_at (TIMESTAMP)
```

## 🛠️ Technologies Used

### Frontend
- HTML5
- CSS3 (with CSS Variables and Animations)
- JavaScript (ES6+)
- Font Awesome Icons
- Google Fonts (Orbitron, Poppins)

### Backend
- PHP 7.4+
- MySQL
- Session Management
- Password Hashing (Bcrypt)

## 📝 API Endpoints

### POST /php/register.php
Register a new user
```json
{
    "username": "string",
    "email": "string",
    "password": "string",
    "confirm_password": "string",
    "terms": "boolean"
}
```

### POST /php/login.php
Authenticate user
```json
{
    "email": "string",
    "password": "string",
    "remember": "boolean"
}
```

### GET /php/logout.php
Logout current user

## 🎮 Future Enhancements

- [ ] Email verification
- [ ] Password reset functionality
- [ ] User profile page
- [ ] Game top-up integration
- [ ] Payment gateway integration
- [ ] Tournament system
- [ ] Rewards and points system
- [ ] Admin dashboard
- [ ] Real-time notifications
- [ ] Chat system

## 📄 License

This project is created for educational purposes. Feel free to use and modify as needed.

## 👨‍💻 Author

Created with ❤️ for GAMING AVIYA

## 🤝 Support

For issues or questions, please contact support or create an issue in the repository.

---

**Enjoy your gaming platform! 🎮🚀**
