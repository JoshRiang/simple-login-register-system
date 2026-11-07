# Simple Login & Register System

An Instagram-inspired authentication system built with HTML, CSS, JavaScript, and Supabase. Users can register, login, and manage their profiles.

![Login Page](https://user-images.githubusercontent.com/placeholder/login.png)

## Features

- **User Registration** - Sign up with email validation and password strength requirements
- **Secure Login** - MD5 password hashing with Supabase authentication
- **Password Recovery** - Email-based password reset flow
- **Profile Management** - Edit username, full name, and profile picture
- **Responsive Design** - Mobile-friendly with Bootstrap 5

## Tech Stack

- **Frontend**: HTML5, CSS3 (SCSS), JavaScript (jQuery)
- **UI Framework**: Bootstrap 5, Font Awesome
- **Backend**: Supabase (PostgreSQL + Auth)
- **Password Hashing**: MD5

## Project Structure

```
├── index.html           # Home page (dashboard)
├── login.html           # Login page
├── signup.html          # Registration page
├── forgotpass.html      # Password recovery
├── 404.html             # Error page
├── style/
│   └── s.css            # Main stylesheet
├── script/
│   ├── dataParser.js    # Supabase client & data functions
│   ├── login.js         # Login logic
│   ├── signup.js        # Registration logic
│   ├── home.js          # Dashboard logic
│   └── forgotPass.js    # Password reset logic
└── script/lib/
    ├── jquery-3.6.0.min.js
    └── md5.min.js
```

## Getting Started

1. Clone the repository
2. Configure Supabase credentials in `script/dataParser.js`:
   ```javascript
   const database = supabase.createClient("YOUR_SUPABASE_URL", "YOUR_ANON_KEY");
   ```
3. Open any HTML file directly in a browser

## Database Schema

The system requires a `profiles` table with:
- `id` (UUID, primary key)
- `email` (text)
- `username` (text)
- `full_name` (text)
- `profile_pic` (text, URL)

## Requirements

Passwords must meet these criteria:
- Minimum 8 characters
- At least 1 uppercase letter
- At least 1 lowercase letter
- At least 1 number
- At least 2 special characters

## Live Demo

Available on GitHub Pages at the main repository.

## License

MIT License