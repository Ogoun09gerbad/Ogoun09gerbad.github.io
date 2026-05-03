# 🎓 Géraud Badélé Ogounchi — Personal Portfolio

> Personal portfolio website of **Géraud Badélé Ogounchi**, Master's Student in Data Science at AIMS Senegal.  
> Built with **iPortfolio** (Bootstrap 5 template) and fully customized.

---

## 👤 About

| Field | Details |
|---|---|
| **Name** | Géraud Badélé Ogounchi |
| **Title** | Mathematician & Data Scientist |
| **Institution** | African Institute for Mathematical Sciences (AIMS) – Senegal |
| **Email** | ogounchigeraud@gmail.com |
| **LinkedIn** | [linkedin.com/in/gerogounchi2000](https://www.linkedin.com/in/gerogounchi2000) |
| **GitHub** | [github.com/Ogoun09gerbad](https://github.com/Ogoun09gerbad) |

---

## 📁 Project Structure

```
portfolio/
│
├── index.html                  # Main page (Home, About, Skills, Resume, Projects, Services, Contact)
├── portfolio-details.html      # Detailed view of all projects with PDF links
├── service-details.html        # Detailed description of all services
├── starter-page.html           # Research interests page
├── photo.jpeg                  # Profile photo
│
├── forms/
│   └── contact.php             # Contact form handler (requires PHP Email Form lib)
│
├── assets/
│   ├── css/
│   │   └── main.css            # Main stylesheet
│   ├── js/
│   │   └── main.js             # Main JavaScript file
│   ├── img/                    # Images (hero background, portfolio thumbnails)
│   └── vendor/                 # Third-party libraries (Bootstrap, AOS, Swiper, etc.)
│
└── PDF Documents/
    ├── CV_Geraud.pdf                  # Curriculum Vitae
    ├── Master_Thesis_Geraud.pdf       # Master's Thesis (Heat Equation in R^N)
    ├── Projet_CaSEG.pdf               # CaSEG Internship Report
    ├── Projet_Geometrie.pdf           # Geometry Project (Draft)
    ├── Projet_Geometrie_final.pdf     # Geometry Project (Final)
    ├── Diplôme et Relevés de Notes.pdf
    └── Relevés.pdf
```

---

## 🧩 Pages Overview

### `index.html` — Main Page
The single-page portfolio containing all main sections:
- **Hero** — Animated typing intro
- **About** — Personal info, bio, CV download button
- **Stats** — Years of study, projects, skills, languages
- **Skills** — Progress bars for all technical skills
- **Resume** — Full education history + professional experience
- **Projects** — Cards with PDF links for each project
- **Services** — 6 services offered
- **Contact** — Contact form + contact info

### `portfolio-details.html` — Projects Detail Page
Full descriptions of all 5 projects with direct PDF download buttons:
- Master's Thesis
- CaSEG Internship Report
- Geometry Project (Draft + Final)
- Tax Fraud Detection
- Graph Theory & Scheduling

### `service-details.html` — Services Detail Page
Detailed breakdown of all 6 services:
- Mathematics Tutoring
- Data Analysis & Mining
- Machine Learning & AI
- Statistical Modeling
- Scientific Writing (LaTeX)
- Research Collaboration

### `starter-page.html` — Research Page
Research interests and academic work overview:
- PDE & Asymptotic Analysis
- Machine Learning & Statistical Modeling
- Climate Dynamics & High-Dimensional Data
- Graph Theory & Optimization
- AI Club Projects

---

## 🚀 How to Run Locally

No installation required. Simply open the main file in your browser:

```bash
# Option 1: Open directly
double-click index.html

# Option 2: Use VS Code Live Server (recommended)
# Install the Live Server extension in VS Code
# Right-click index.html → "Open with Live Server"

# Option 3: Use Python local server
cd your-portfolio-folder
python -m http.server 8000
# Then open http://localhost:8000
```

---

## 📬 Contact Form Setup

The contact form requires configuration. Choose one of these options:

### ✅ Option 1 — Formspree (Free, No PHP needed)
1. Go to [formspree.io](https://formspree.io) and create a free account
2. Create a new form and copy your Form ID
3. In `index.html`, replace:
```html
<form action="forms/contact.php" method="post" class="php-email-form">
```
with:
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

### Option 2 — PHP Email Form (Pro version)
1. Purchase the Pro template from [bootstrapmade.com](https://bootstrapmade.com)
2. Upload `php-email-form.php` to `assets/vendor/php-email-form/`
3. The `forms/contact.php` file is already configured with your email

### Option 3 — Gmail SMTP
Uncomment the SMTP block in `forms/contact.php` and fill in:
```php
$contact->smtp = array(
  'host'     => 'smtp.gmail.com',
  'username' => 'ogounchigeraud@gmail.com',
  'password' => 'YOUR_GOOGLE_APP_PASSWORD',
  'port'     => '587'
);
```
> Generate an App Password at: [myaccount.google.com/apppasswords](https://myaccount.google.com/apppasswords)

---

## 🌐 Deployment (Free Hosting)

### GitHub Pages (Recommended)
```bash
# 1. Create a repository on GitHub named: yourusername.github.io
# 2. Upload all your portfolio files
# 3. Go to Settings → Pages → Select main branch
# 4. Your site will be live at: https://yourusername.github.io
```

### Netlify (Drag & Drop)
1. Go to [netlify.com](https://netlify.com)
2. Drag and drop your entire portfolio folder
3. Your site is live instantly with a free URL

---

## 🛠️ Customization Guide

### Change Profile Photo
Replace `photo.jpeg` with your own photo (keep the same filename).

### Update Personal Info
Edit `index.html` and search for these fields:
- Name: `Géraud Badélé Ogounchi`
- Email: `ogounchigeraud@gmail.com`
- Phone: `+229 0167138137`

### Update Skills
In `index.html`, find the Skills section and change `aria-valuenow` values (0–100):
```html
<div class="progress-bar" role="progressbar" aria-valuenow="95" ...></div>
```

### Add a New Project
In `index.html`, copy a portfolio item block and update the title, description, and PDF link:
```html
<div class="col-lg-4 col-md-6 portfolio-item isotope-item filter-research">
  <div class="portfolio-content h-100">
    <img src="assets/img/portfolio/app-1.jpg" class="img-fluid" alt="Your Project">
    <div class="portfolio-info">
      <h4>Your Project Title</h4>
      <p>Short description</p>
      <a href="your-project.pdf" target="_blank" class="details-link">
        <i class="bi bi-file-earmark-pdf"></i>
      </a>
    </div>
  </div>
</div>
```

---

## 📦 Technologies Used

| Technology | Purpose |
|---|---|
| HTML5 / CSS3 | Structure & styling |
| Bootstrap 5.3 | Responsive grid & components |
| Bootstrap Icons | Icon library |
| AOS (Animate On Scroll) | Scroll animations |
| Typed.js | Typing animation in hero section |
| Swiper.js | Sliders & carousels |
| GLightbox | Image/PDF lightbox |
| Isotope | Portfolio filtering |
| PureCounter | Animated stat counters |

---

## 📄 License

This portfolio is based on the **iPortfolio** template by [BootstrapMade](https://bootstrapmade.com).  
Template License: [bootstrapmade.com/license](https://bootstrapmade.com/license/)

Personal content (bio, projects, CV) © 2025 **Géraud Badélé Ogounchi** — All Rights Reserved.

---

## 📞 Contact

For any collaboration or inquiry:

- 📧 Email: [ogounchigeraud@gmail.com](mailto:ogounchigeraud@gmail.com)
- 🔗 LinkedIn: [linkedin.com/in/gerogounchi2000](https://www.linkedin.com/in/gerogounchi2000)
- 💻 GitHub: [github.com/Ogoun09gerbad](https://github.com/Ogoun09gerbad)