# Personal Portfolio & Content Management Platform

A modern, full-stack personal website showcasing technical expertise, projects, and writings with a secure content management system built on Flask and Firebase.

## 🎯 Overview

This platform serves as a comprehensive digital presence that combines portfolio presentation with blogging capabilities, demonstrating both front-end design sensibility and back-end architecture skills.

**Live Site**: [Your Domain Here]

## ✨ Features

### Public-Facing
- **Dynamic Homepage** - Hero section, featured projects, expertise showcase, latest writings
- **Projects Portfolio** - Filterable project showcase with live demos and GitHub links
- **Technical Blog** - Markdown-powered writing platform with series support
- **Professional Work Page** - Clear engagement terms and contact information
- **Fully Responsive** - Mobile-first design optimized for all devices

### Admin Panel
- **Secure Authentication** - Firebase-powered login system
- **Content Management** - CRUD operations for writings, projects, and products
- **Markdown Editor** - Live preview for blog posts
- **Intuitive Dashboard** - Quick access to all content management features

## 🛠️ Tech Stack

**Backend**
- Flask 3.0 (Python 3.8+)
- Firebase Admin SDK
- Python-Markdown for content rendering

**Database & Auth**
- Firebase Firestore (NoSQL)
- Firebase Authentication

**Frontend**
- Jinja2 Templates
- Modern CSS3 with custom properties
- Vanilla JavaScript
- Mobile-first responsive design

**Deployment**
- [Platform TBD - Heroku/Railway/Google Cloud Run]

## 📋 Prerequisites

- Python 3.8 or higher
- Firebase account with project setup
- pip (Python package manager)

## 🚀 Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/portfolio-platform.git
cd portfolio-platform
```

### 2. Set Up Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Firebase Configuration

1. Create a Firebase project at [Firebase Console](https://console.firebase.google.com/)
2. Enable Firestore Database
3. Enable Authentication (Email/Password)
4. Download service account key JSON file
5. Place it in the project root (add to .gitignore)

### 5. Environment Variables

Create a `.env` file in the project root:

```env
FLASK_ENV=development
SECRET_KEY=your-secret-key-here
GOOGLE_APPLICATION_CREDENTIALS=path/to/firebase-key.json
FIREBASE_DATABASE_URL=https://your-project.firebaseio.com
```

### 6. Initialize Firebase Admin User

```bash
# Create your admin user in Firebase Console
# Authentication > Users > Add User
```

### 7. Run the Application

```bash
flask run
```

Visit `http://localhost:5000` to view the site.
Visit `http://localhost:5000/admin/login` to access the admin panel.

## 📁 Project Structure

```
portfolio-platform/
├── app/
│   ├── __init__.py          # Flask app initialization
│   ├── routes/              # Route handlers
│   │   ├── public.py        # Public-facing routes
│   │   └── admin.py         # Admin panel routes
│   ├── models/              # Data models
│   ├── templates/           # Jinja2 templates
│   │   ├── public/          # Public site templates
│   │   └── admin/           # Admin panel templates
│   ├── static/              # CSS, JS, images
│   │   ├── css/
│   │   ├── js/
│   │   └── images/
│   └── utils/               # Helper functions
├── config.py                # Configuration
├── requirements.txt         # Python dependencies
├── .env.example             # Environment variables template
├── .gitignore
└── README.md
```

## 🗄️ Database Schema

### Collections

**writings**
```json
{
  "title": "string",
  "content": "string (markdown)",
  "date": "string (ISO 8601)",
  "tags": ["array"],
  "series": "string | null",
  "slug": "string"
}
```

**projects**
```json
{
  "title": "string",
  "description": "string",
  "demo_url": "string | null",
  "github_url": "string | null",
  "tech_stack": ["array"],
  "status": "active | archived | wip",
  "slug": "string"
}
```

**products**
```json
{
  "title": "string",
  "description": "string",
  "price": "number",
  "url": "string | null",
  "active": "boolean",
  "slug": "string"
}
```

## 🎨 Design System

**Color Scheme**
- Primary Gradient: `#667eea` → `#764ba2`
- Clean, minimal aesthetic with card-based layouts
- Generous whitespace and subtle animations

**Typography**
- System font stack for optimal performance

**Breakpoints**
- Mobile: `480px`
- Tablet: `768px`
- Desktop: `1024px+`

## 🔐 Security

- HTTPS-only in production
- Firebase handles password hashing and authentication
- Session cookies with `httpOnly` and `sameSite` flags
- Admin routes protected with `@login_required` decorator
- Environment variables for sensitive configuration
- `.gitignore` configured to exclude secrets

## 🚢 Deployment

### Pre-Deployment Checklist

- [ ] Set production environment variables
- [ ] Configure Firebase security rules
- [ ] Enable Firestore backups
- [ ] Set up SSL certificate
- [ ] Configure custom domain (optional)
- [ ] Run load testing
- [ ] Add SEO meta tags
- [ ] Test all features on production environment

### Environment Variables (Production)

```env
FLASK_ENV=production
SECRET_KEY=<strong-random-key>
GOOGLE_APPLICATION_CREDENTIALS=<path-to-firebase-key>
FIREBASE_DATABASE_URL=<firebase-db-url>
```

## 📊 Performance Goals

- Page Load: < 2 seconds on 3G
- Time to Interactive: < 3 seconds
- Lighthouse Score: > 90 (Performance, Accessibility, Best Practices)
- Uptime: 99.9%

## 🧪 Testing

```bash
# Run tests
python -m pytest

# Run with coverage
python -m pytest --cov=app
```

## 📈 Roadmap

### Phase 1: MVP (Current)
- ✅ Core portfolio features
- ✅ Blog with markdown support
- ✅ Admin content management
- ✅ Firebase integration

### Phase 2 (Months 2-3)
- Analytics integration
- Search functionality
- Contact form with email
- Newsletter signup
- RSS feed

### Phase 3 (Months 4-6)
- Comment system
- Social sharing
- Advanced metrics dashboard
- Image upload capability
- Detailed case studies

### Phase 4 (6+ Months)
- API endpoints
- Headless CMS capabilities
- Multi-language support
- Content scheduling

## 🤝 Contributing

This is a personal portfolio project, but feedback and suggestions are welcome! Please open an issue for discussion.

## 📄 License

[Choose Your License - MIT, Apache 2.0, etc.]

## 👤 Author

**Sahil Sharma**

- Website: [Your Website]
- GitHub: [Developer-Sahil](https://github.com/yourusername)
- LinkedIn: [Your LinkedIn](https://linkedin.com/in/yourprofile)

## 🙏 Acknowledgments

- Firebase for backend infrastructure
- Flask community for excellent documentation
- [Any other acknowledgments]

---

**Version**: 1.0.0  
**Last Updated**: January 15, 2026  
**Status**: In Development
