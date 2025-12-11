# Chaitanya Allu - Portfolio Website

A modern, responsive portfolio website showcasing skills as a Full Stack Developer and UI/UX Designer. This project features a dynamic single-page application with smooth animations, dark/light theme toggle, and a fully functional contact form with backend integration.

## 🚀 Features

- **Modern Design**: Clean, professional dark theme with cyan accents and light mode support
- **Responsive Layout**: Fully optimized for all devices and screen sizes
- **Interactive Elements**: Smooth animations, typing effects, hover interactions, and scroll animations
- **Dark/Light Theme Toggle**: User preference saved in localStorage
- **Contact Form**: Functional contact form with email integration and validation
- **Project Showcase**: Professional project display with filtering and GitHub links
- **Skills Visualization**: Animated progress bars and radial charts for technical skills and professional strengths
- **Smooth Navigation**: Single-page application with smooth scrolling and active section highlighting
- **Blog Section**: Placeholder for blog articles
- **Testimonials**: Showcase of recommendations and feedback
- **Loading Screen**: Elegant loading animation on page load
- **Google Analytics**: Integrated tracking for website analytics

## 🛠️ Technologies Used

### Frontend Technologies

#### Core Technologies
- **HTML5**: Semantic markup and structure
- **CSS3**: 
  - Custom CSS variables for theming
  - Advanced animations and transitions
  - Flexbox and Grid layouts
  - Responsive design with media queries
  - Keyframe animations
- **JavaScript (ES6+)**:
  - DOM manipulation
  - Event handling
  - Fetch API for backend communication
  - LocalStorage for theme persistence
  - Intersection Observer API for scroll animations

#### External Libraries & CDNs
- **Typed.js** (v2.1.0): Typing animation effect for job titles
  - CDN: `https://unpkg.com/typed.js@2.1.0/dist/typed.umd.js`
- **Boxicons** (v2.1.4): Icon library for social media and UI icons
  - CDN: `https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css`
- **Google Analytics**: Website analytics tracking
  - Tag ID: `G-RQ1W4NYJNH`

### Backend Technologies

This project includes **two backend implementations** - you can choose either one:

#### Option 1: Python Flask Backend (Currently Active)

**Technologies:**
- **Python 3.7+**: Programming language
- **Flask** (v2.3.3): Lightweight web framework
- **Flask-CORS** (v4.0.0): Cross-Origin Resource Sharing support
- **Werkzeug** (v2.3.7): WSGI utility library
- **SMTP**: Email sending functionality
- **Python Standard Library**:
  - `smtplib`: Email server communication
  - `email.mime`: Email message formatting
  - `re`: Regular expressions for validation
  - `os`: Environment variable handling
  - `datetime`: Timestamp generation

**Features:**
- RESTful API endpoint (`/contact`)
- Email validation
- Form data validation
- Health check endpoint (`/health`)
- Error handling and logging
- CORS enabled for cross-origin requests

#### Option 2: Node.js/Express Backend (Alternative)

**Technologies:**
- **Node.js**: JavaScript runtime
- **Express.js** (v4.18.2): Web application framework
- **MongoDB** with **Mongoose** (v7.8.7): Database for storing contact messages
- **bcryptjs** (v3.0.2): Password hashing for admin authentication
- **jsonwebtoken** (v9.0.2): JWT authentication tokens
- **nodemailer** (v6.9.8): Email sending functionality
- **cors** (v2.8.5): Cross-Origin Resource Sharing
- **helmet** (v8.1.0): Security headers
- **dotenv** (v16.3.1): Environment variable management

**Features:**
- RESTful API endpoints (`/contact`, `/auth`)
- MongoDB database integration
- Admin authentication system
- JWT-based authentication
- Contact message storage
- Email notifications
- Security middleware

## 📁 Project Structure

```
Portfolio-Website-1/
├── index.html              # Main HTML file with all sections
├── stylesheet.css          # Complete CSS styling and animations
├── main.js                 # Frontend JavaScript functionality
├── app.py                  # Flask backend server (Python)
├── requirements.txt        # Python dependencies
│
├── backend/                # Node.js backend (alternative)
│   ├── server.js          # Express server entry point
│   ├── package.json       # Node.js dependencies
│   ├── models/           # MongoDB models
│   │   ├── Admin.js      # Admin user model
│   │   └── Contact.js    # Contact message model
│   ├── routes/           # API routes
│   │   ├── auth.js      # Authentication routes
│   │   └── contact.js   # Contact form routes
│   ├── utils/           # Utility functions
│   │   └── authMiddleware.js  # JWT authentication middleware
│   └── scripts/         # Utility scripts
│       └── createAdmin.js    # Admin user creation script
│
├── home.jpg              # Profile image
├── pro1.png             # Project 1 screenshot
├── pro2.png             # Project 2 screenshot
├── bg.jpg               # Background image
├── Chaitanya_Allu_JavaFullStack.pdf  # Resume PDF
└── README.md            # This file
```

## 🎨 Frontend Architecture

### HTML Structure (`index.html`)

1. **Header Section**
   - Logo
   - Navigation menu (8 sections)
   - Dark/Light theme toggle

2. **Home Section** (`#home`)
   - Animated typing effect for job titles
   - Professional introduction
   - Social media links (LinkedIn, GitHub, Twitter)
   - Profile image

3. **About Section** (`#about`)
   - Personal background
   - Professional summary
   - Profile image

4. **Services Section** (`#services`)
   - UI/UX Design
   - Web Development
   - Deployment and Hosting

5. **Skills Section** (`#skills`)
   - Technical Skills: HTML, CSS, JavaScript, React, Python, Java, Git
   - Professional Strengths: Creativity (85%), Problem Solving (80%), Collaboration (85%)
   - Animated progress bars and circular charts

6. **Testimonials Section** (`#testimonials`)
   - Three testimonial cards
   - Author information

7. **Blog Section** (`#blog`)
   - Three blog article cards
   - Placeholder content

8. **Portfolio Section** (`#portfolio`)
   - Project filtering (All, Web3, Web Development, UI/UX)
   - Project cards with hover effects
   - GitHub links

9. **Contact Section** (`#contact`)
   - Contact information
   - Social media links
   - Contact form
   - Resume download button

10. **Footer**
    - Copyright information
    - Back-to-top button

11. **Loading Screen**
    - Animated loader on page load

### CSS Architecture (`stylesheet.css`)

**Key Features:**
- CSS Custom Properties (Variables) for theming
- Dark and Light theme support via `data-theme` attribute
- Smooth animations and transitions
- Responsive design breakpoints
- Keyframe animations:
  - `slideRight`, `slideLeft`, `slideTop`, `slideBottom`
  - `animate` (progress bars)
  - `showText` (fade-in effects)
  - `spin` (loading spinner)
- Grid and Flexbox layouts
- Backdrop filters for glassmorphism effects
- Box shadows and hover effects

**Color Scheme:**
- **Dark Theme**: `#081b29` (primary), `#051129` (secondary), `#0ef` (accent)
- **Light Theme**: `#f8f9fa` (primary), `#ffffff` (secondary), `#3498db` (accent)

### JavaScript Functionality (`main.js`)

**Core Features:**

1. **Theme Toggle**
   - Dark/Light mode switching
   - LocalStorage persistence
   - Icon updates (moon/sun)

2. **Typing Animation**
   - Typed.js integration
   - Rotating job titles: "Frontend Developer", "UI/UX Designer", "Web Developer"

3. **Contact Form Handling**
   - Form validation (email format, required fields)
   - API communication with Flask backend
   - Loading states
   - Success/error notifications
   - Form reset on success

4. **Smooth Scrolling**
   - Navigation link smooth scrolling
   - Active section highlighting on scroll

5. **Skill Animations**
   - Intersection Observer for scroll-triggered animations
   - Progress bar animations
   - Circular progress bar animations

6. **Project Filtering**
   - Filter buttons for project categories
   - Show/hide project cards based on filter

7. **Back-to-Top Button**
   - Show/hide based on scroll position
   - Smooth scroll to top

8. **Loading Screen**
   - Fade out after page load

9. **Notification System**
   - Toast notifications for form submissions
   - Auto-dismiss after 5 seconds

## 🔧 Backend Architecture

### Flask Backend (`app.py`)

**Endpoints:**

1. **POST `/contact`**
   - Receives contact form data
   - Validates input (name, email, message)
   - Sends email via SMTP
   - Returns JSON response

2. **GET `/health`**
   - Health check endpoint
   - Returns server status and timestamp

**Configuration:**
- Port: `5001`
- CORS enabled
- Environment variables for email configuration

**Email Setup:**
- SMTP Server: Gmail (configurable)
- Port: 587 (TLS)
- Requires App Password for Gmail

### Node.js Backend (`backend/server.js`)

**Endpoints:**

1. **POST `/contact`**
   - Stores contact messages in MongoDB
   - Sends email notification
   - Returns success response

2. **POST `/auth/login`**
   - Admin authentication
   - JWT token generation

3. **GET `/health`**
   - Health check endpoint

**Database Models:**
- **Contact**: Stores form submissions
- **Admin**: Stores admin credentials

**Security:**
- Helmet.js for security headers
- CORS configuration
- JWT authentication
- Password hashing with bcrypt

## 🚀 Setup Instructions

### Prerequisites

**For Flask Backend:**
- Python 3.7 or higher
- pip (Python package manager)
- Gmail account (for email functionality)

**For Node.js Backend:**
- Node.js 14+ and npm
- MongoDB database (local or cloud)
- Gmail account (for email functionality)

### Installation

#### Option 1: Using Flask Backend (Recommended for Quick Start)

1. **Clone the repository**
   ```bash
   git clone https://github.com/AlluChaitanya/Portfolio-Website-1.git
   cd Portfolio-Website-1
   ```

2. **Install Python dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure environment variables**
   
   Set the following environment variables:
   ```bash
   export SMTP_SERVER=smtp.gmail.com
   export SMTP_PORT=587
   export EMAIL_USER=your-email@gmail.com
   export EMAIL_PASSWORD=your-app-password
   export RECIPIENT_EMAIL=chaiallu2025@gmail.com
   ```
   
   **For Gmail:**
   - Enable 2-factor authentication
   - Generate an App Password: [Google App Passwords](https://myaccount.google.com/apppasswords)
   - Use the App Password instead of your regular password

4. **Run the Flask server**
   ```bash
   python app.py
   ```
   Server will run on `http://127.0.0.1:5001`

5. **Open the website**
   - Open `index.html` in your browser
   - Or use a local server: `python -m http.server 8000`
   - Then visit `http://localhost:8000`

#### Option 2: Using Node.js Backend

1. **Clone the repository**
   ```bash
   git clone https://github.com/AlluChaitanya/Portfolio-Website-1.git
   cd Portfolio-Website-1
   ```

2. **Install Node.js dependencies**
   ```bash
   cd backend
   npm install
   ```

3. **Set up MongoDB**
   - Install MongoDB locally or use MongoDB Atlas (cloud)
   - Get your MongoDB connection string

4. **Configure environment variables**
   
   Create a `.env` file in the `backend` directory:
   ```env
   PORT=5001
   MONGODB_URI=your-mongodb-connection-string
   JWT_SECRET=your-secret-key-here
   EMAIL_USER=your-email@gmail.com
   EMAIL_PASSWORD=your-app-password
   RECIPIENT_EMAIL=chaiallu2025@gmail.com
   ```

5. **Create admin user** (optional)
   ```bash
   node scripts/createAdmin.js
   ```

6. **Run the Node.js server**
   ```bash
   npm start
   # or for development with auto-reload:
   npm run dev
   ```
   Server will run on `http://localhost:5001`

7. **Update frontend API URL** (if needed)
   
   In `main.js`, update the `API_BASE_URL` if your backend runs on a different port.

## 🎯 Key Features Explained

### Dark/Light Theme Toggle

- Uses CSS custom properties (variables)
- Theme preference saved in browser localStorage
- Smooth transitions between themes
- Icon changes (moon ↔ sun)

### Animated Skills Section

- **Technical Skills**: Horizontal progress bars with percentages
- **Professional Strengths**: Circular progress charts
- Animations trigger on scroll using Intersection Observer
- Smooth fill animations

### Project Filtering

- Filter buttons: All, Web3, Web Development, UI/UX
- JavaScript filters project cards based on `data-category` attribute
- Smooth show/hide animations

### Contact Form

- Client-side validation (email format, required fields)
- Server-side validation (Flask backend)
- Email notifications sent to configured recipient
- Success/error toast notifications
- Loading states during submission

### Responsive Design

- Mobile-first approach
- Breakpoints at 768px and 900px
- Flexible grid layouts
- Touch-friendly navigation
- Optimized images

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 🔒 Security Features

- Input validation (client and server-side)
- CORS configuration
- Helmet.js security headers (Node.js backend)
- Password hashing (Node.js backend)
- JWT authentication (Node.js backend)
- Email validation regex
- XSS prevention

## 📊 Performance Optimizations

- Lazy loading animations (Intersection Observer)
- CSS animations (hardware-accelerated)
- Optimized images
- Minimal external dependencies
- Efficient DOM manipulation

## 🚢 Deployment

### Frontend Deployment

**GitHub Pages:**
1. Push code to GitHub repository
2. Go to Settings → Pages
3. Select source branch
4. Update API URL in `main.js` to production backend URL

**Netlify/Vercel:**
1. Connect GitHub repository
2. Build command: None (static site)
3. Publish directory: Root
4. Update API URL in `main.js`

### Backend Deployment

**Flask Backend:**
- **Heroku**: Add `Procfile` and `requirements.txt`
- **Railway**: Connect GitHub repo, set environment variables
- **PythonAnywhere**: Upload files, configure WSGI

**Node.js Backend:**
- **Heroku**: Add `Procfile`, set environment variables
- **Railway**: Connect repo, configure MongoDB, set env vars
- **Render**: Connect repo, set environment variables

**Environment Variables to Set:**
- `SMTP_SERVER`
- `SMTP_PORT`
- `EMAIL_USER`
- `EMAIL_PASSWORD`
- `RECIPIENT_EMAIL`
- `MONGODB_URI` (Node.js only)
- `JWT_SECRET` (Node.js only)

## 🎨 Customization Guide

### Changing Colors

Edit CSS variables in `stylesheet.css`:
```css
:root {
    --bg-primary: #081b29;
    --accent-color: #0ef;
    /* ... */
}
```

### Adding Projects

In `index.html`, add a new project card:
```html
<div class="project-card" data-category="web">
    <div class="image-wrapper">
        <img src="project-image.png" alt="Project Name">
    </div>
    <div class="layer">
        <h5>Project Name</h5>
        <p>Project description</p>
        <a href="https://github.com/username/repo" target="_blank">
            <i class='bx bx-link-external'></i>
        </a>
    </div>
</div>
```

### Updating Skills

Edit progress bar percentages in `stylesheet.css`:
```css
.progress-line.html span { width: 90%; }
```

Update circular progress in `index.html`:
```html
<div class="circle-progress" data-percent="85">
```

### Modifying Content

- Personal info: Edit `index.html` sections
- Images: Replace `home.jpg`, `pro1.png`, `pro2.png`
- Resume: Replace `Chaitanya_Allu_JavaFullStack.pdf`

## 🐛 Troubleshooting

### Contact Form Not Working

1. Check backend server is running
2. Verify API URL in `main.js` matches backend port
3. Check browser console for errors
4. Verify CORS is enabled on backend
5. Check email credentials are correct

### Theme Not Persisting

- Clear browser cache
- Check localStorage is enabled
- Verify JavaScript is running

### Animations Not Working

- Check browser supports Intersection Observer
- Verify JavaScript is enabled
- Check for console errors

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 👤 Author

**Chaitanya Allu**

- **Email**: chaiallu2025@gmail.com
- **Phone**: +1 806-730-5847
- **Location**: Lubbock, TX, USA
- **GitHub**: [@AlluChaitanya](https://github.com/AlluChaitanya)
- **LinkedIn**: [chaitanya-allu](https://linkedin.com/in/chaitanya-allu)
- **Twitter**: [@chaitanya_allu](https://twitter.com/chaitanya_allu)

## 🙏 Acknowledgments

- [Typed.js](https://github.com/mattboldt/typed.js/) for typing animations
- [Boxicons](https://boxicons.com/) for icon library
- [Google Fonts](https://fonts.google.com/) for Poppins font
- Flask and Express.js communities

---

_Developed with ❤️ by Chaitanya Allu - 2025_
