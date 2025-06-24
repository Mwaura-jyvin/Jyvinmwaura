# Mkristoh Rental - Car Rental Website

A full-featured car rental website built with HTML, CSS, JavaScript, PHP, and Bootstrap. The system includes user registration, car browsing, rental booking, and an admin panel for management.

## Features

### User Features

- **User Registration & Login**: Secure user authentication with PHP validation
- **Car Browsing**: View available cars with detailed information
- **Rental Booking**: Book cars with date selection and price calculation
- **Rental History**: View past and current rentals
- **Profile Management**: Update personal information

### Admin Features

- **Dashboard Overview**: Statistics and recent activity
- **User Management**: View, edit, and manage user accounts
- **Car Management**: Add, edit, and remove cars from the fleet
- **Rental Management**: Manage all rental requests and statuses
- **Reports**: View revenue and rental statistics

### Technical Features

- **Responsive Design**: Mobile-friendly interface using Bootstrap 5
- **PHP Validation**: Server-side validation for all forms
- **MySQL Database**: Secure data storage with mysqli
- **Session Management**: Secure user sessions
- **Modern UI**: Beautiful design with car-themed background

## Requirements

- **XAMPP** (Apache, MySQL, PHP)
- **PHP 7.4+**
- **MySQL 5.7+**
- **Web Browser** (Chrome, Firefox, Safari, Edge)

## Installation

### 1. Setup XAMPP

1. Download and install XAMPP from [https://www.apachefriends.org/](https://www.apachefriends.org/)
2. Start Apache and MySQL services
3. Open phpMyAdmin at `http://localhost/phpmyadmin`

### 2. Project Setup

1. Clone or download this project
2. Place the project folder in `C:\xampp\htdocs\rental\`
3. The project will be accessible at `http://localhost/rental/`

### 3. Database Setup

1. Open phpMyAdmin at `http://localhost/phpmyadmin`
2. Create a new database named `mkristoh_rental`
3. Import the `youngyou.sql` file into the database
4. The system will be ready to use

### 4. First Access

1. Go to `http://localhost/rental/`
2. Login as admin using the default credentials:
   - **Email**: `admin@mkristohrental.com`
   - **Password**: `admin123`

## File Structure

```
rental/
├── index.html              # Homepage
├── login.html              # Login page
├── register.html           # Registration page
├── dashboard.php           # User dashboard
├── rental-form.php         # Car rental form
├── youngyou.sql            # Database file
├── css/
│   └── style.css          # Custom styles
├── js/
│   └── main.js            # JavaScript functionality
├── php/
│   ├── config.php         # Database configuration
│   ├── register.php       # User registration processing
│   ├── login.php          # User login processing
│   ├── logout.php         # Logout processing
│   ├── update-profile.php # Profile update processing
│   └── process-rental.php # Rental booking processing
├── admin/
│   └── dashboard.php      # Admin dashboard
└── README.md              # This file
```

## Database Schema

### Users Table

- `id` - Primary key
- `first_name` - User's first name
- `last_name` - User's last name
- `email` - Unique email address
- `phone` - Phone number
- `address` - User's address
- `password` - Hashed password
- `role` - User role (user/admin)
- `created_at` - Account creation timestamp
- `updated_at` - Last update timestamp

### Cars Table

- `id` - Primary key
- `name` - Car name/model
- `category` - Car category (Sedan, SUV, Luxury, etc.)
- `price` - Daily rental price
- `image_url` - Car image URL
- `features` - Car features (comma-separated)
- `available` - Availability status
- `created_at` - Car addition timestamp
- `updated_at` - Last update timestamp

### Rentals Table

- `id` - Primary key
- `user_id` - Foreign key to users table
- `car_id` - Foreign key to cars table
- `start_date` - Rental start date
- `end_date` - Rental end date
- `total_price` - Total rental cost
- `status` - Rental status (pending/confirmed/active/completed/cancelled)
- `pickup_location` - Pickup location
- `return_location` - Return location
- `notes` - Additional notes
- `created_at` - Rental creation timestamp
- `updated_at` - Last update timestamp

## Default Data

### Admin Account

- **Email**: `admin@mkristohrental.com`
- **Password**: `admin123`

### Sample Users

- **Email**: `lingolingoskii@example.com` | **Password**: `Password123`
- **Email**: `mwaurajyvin@example.com` | **Password**: `Password123`
- **Email**: `mkristoh@example.com` | **Password**: `Password123`

### Sample Cars

- Toyota Camry (Sedan) - $50/day
- Honda CR-V (SUV) - $70/day
- BMW 3 Series (Luxury) - $120/day
- Ford Mustang (Sports) - $150/day
- Mercedes-Benz S-Class (Luxury) - $200/day
- Jeep Wrangler (Off-Road) - $80/day
- Tesla Model 3 (Electric) - $180/day
- Audi A4 (Sedan) - $90/day

## Usage

### For Users

1. **Register**: Create a new account at the registration page
2. **Login**: Access your account using email and password
3. **Browse Cars**: View available cars in the dashboard
4. **Rent a Car**: Select a car and choose rental dates
5. **View Rentals**: Check your rental history and status

### For Admins

1. **Login**: Use admin credentials to access admin panel
2. **Manage Users**: View and manage user accounts
3. **Manage Cars**: Add, edit, or remove cars from the fleet
4. **Manage Rentals**: Approve, reject, or update rental statuses
5. **View Reports**: Check revenue and rental statistics

## Security Features

- **Password Hashing**: All passwords are hashed using PHP's password_hash()
- **SQL Injection Prevention**: Prepared statements for all database queries
- **Input Sanitization**: All user inputs are sanitized
- **Session Management**: Secure session handling
- **Form Validation**: Server-side validation for all forms

## Customization

### Adding New Cars

1. Login as admin
2. Go to "Manage Cars" section
3. Click "Add Car" button
4. Fill in car details and save

### Modifying Styles

- Edit `css/style.css` to customize the appearance
- The website uses Bootstrap 5 for responsive design
- Custom CSS classes are available for specific styling

### Database Configuration

- Edit `php/config.php` to modify database settings
- Default settings work with XAMPP's default configuration

## Troubleshooting

### Common Issues

1. **Database Connection Error**

   - Ensure MySQL is running in XAMPP
   - Check database credentials in `php/config.php`
   - Import the `youngyou.sql` file properly

2. **Page Not Found**

   - Verify project is in correct directory (`htdocs/rental/`)
   - Check Apache is running in XAMPP

3. **Login Issues**

   - Clear browser cache and cookies
   - Check if session is working properly
   - Verify database is properly imported

4. **Image Not Loading**

   - Ensure internet connection for external images
   - Check image URLs in car data

5. **Database Import Issues**
   - Ensure MySQL service is running
   - Check if you have proper permissions
   - Try importing the SQL file manually in phpMyAdmin

### Support

For technical support or questions, please check:

- XAMPP documentation
- PHP documentation
- MySQL documentation

## Quick Start Guide

1. **Install XAMPP** and start Apache + MySQL
2. **Place project** in `C:\xampp\htdocs\rental\`
3. **Import database** using `youngyou.sql` in phpMyAdmin
4. **Login as admin** using the default credentials
5. **Start using** the rental system!

## License

This project is created for educational purposes. Feel free to modify and use as needed.

## Credits

- **Bootstrap 5** - Frontend framework
- **Font Awesome** - Icons
- **Unsplash** - Car images
- **PHP** - Backend language
- **MySQL** - Database system

---

**Mkristoh Rental** - Premium Car Rental Services
