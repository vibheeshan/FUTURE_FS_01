# 🚀 Professional Portfolio Website

A modern, responsive, and feature-rich portfolio website built with HTML, CSS, JavaScript, Node.js, and Express. This portfolio showcases your skills, projects, and provides a contact form with email notifications.

![Portfolio Preview](./assets/preview.png)

## ✨ Features

### Frontend
- **Modern Design**: Clean, professional interface with smooth animations
- **Fully Responsive**: Works seamlessly on desktop, tablet, and mobile devices
- **Interactive Elements**: Smooth scrolling, hover effects, and dynamic navigation
- **SEO Optimized**: Meta tags, semantic HTML, and optimized structure
- **Fast Loading**: Optimized assets and lazy loading for images
- **Accessibility**: WCAG compliant with keyboard navigation support

### Backend
- **Contact Form**: Functional contact form with validation
- **Email Notifications**: Automatic email sending using Nodemailer
- **MongoDB Support**: Optional database integration for storing messages
- **RESTful API**: Clean API structure for potential expansion
- **Error Handling**: Comprehensive error management

### Sections
1. **Hero Section**: Eye-catching introduction with animated code snippet
2. **About Section**: Personal information and highlights
3. **Projects Section**: Showcase your work with links to live demos and GitHub
4. **Skills Section**: Display your technical expertise
5. **Contact Section**: Interactive form for visitors to reach you

## 🛠️ Tech Stack

### Frontend
- HTML5
- CSS3 (Custom animations, Flexbox, Grid)
- Vanilla JavaScript (ES6+)

### Backend
- Node.js
- Express.js
- Nodemailer (Email functionality)
- Mongoose (MongoDB ODM - optional)

### Fonts
- Syne (Headings)
- DM Sans (Body text)

## 📋 Prerequisites

Before you begin, ensure you have the following installed:
- [Node.js](https://nodejs.org/) (v14 or higher)
- [Git](https://git-scm.com/)
- A Gmail account (for email functionality)
- [MongoDB](https://www.mongodb.com/) (optional, for database features)

## 🚀 Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/portfolio.git
cd portfolio
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Configure Environment Variables

Create a `.env` file in the root directory:

```bash
cp .env.example .env
```

Edit the `.env` file with your credentials:

```env
PORT=5000
EMAIL_USER=your.email@gmail.com
EMAIL_PASSWORD=your_app_specific_password
MONGODB_URI=mongodb://localhost:27017/portfolio
```

#### Setting up Gmail for Email Notifications:

1. Go to your [Google Account Security Settings](https://myaccount.google.com/security)
2. Enable 2-Factor Authentication
3. Generate an [App Password](https://myaccount.google.com/apppasswords)
4. Use this app password in your `.env` file

### 4. Customize Content

Edit the following files to personalize your portfolio:

#### `index.html`
- Update personal information (name, contact details)
- Add your projects with descriptions and links
- Update social media links
- Modify skills and technologies

#### `styles.css`
- Customize color scheme (see CSS variables at the top)
- Adjust spacing and layout
- Modify animations

#### `server.js`
- Update email templates
- Customize API endpoints

### 5. Add Your Assets

Create an `assets` folder and add:
- `profile.jpg` - Your profile photo
- `project1.jpg`, `project2.jpg`, `project3.jpg` - Project screenshots
- `resume.pdf` - Your resume file
- `favicon.svg` - Website icon
- `og-image.jpg` - Open Graph image for social media

## 🎨 Customization Guide

### Colors

The color scheme is defined in CSS variables at the top of `styles.css`:

```css
:root {
    --color-primary: #FF6B35;
    --color-secondary: #2D3142;
    --color-accent: #4ECDC4;
    /* Modify these to change the entire color scheme */
}
```

### Adding Projects

Add new project cards in the `index.html` projects section:

```html
<article class="project-card">
    <div class="project-image">
        <img src="./assets/your-project.jpg" alt="Project Name">
        <!-- ... -->
    </div>
    <div class="project-content">
        <h3 class="project-title">Your Project Name</h3>
        <p class="project-description">Project description here</p>
        <div class="project-tech">
            <span class="tech-tag">React</span>
            <!-- Add more tags -->
        </div>
    </div>
</article>
```

### Modifying Skills

Update the skills section in `index.html`:

```html
<div class="skill-category">
    <h3 class="skill-title">Your Skill Category</h3>
    <ul class="skill-list">
        <li>Skill 1</li>
        <li>Skill 2</li>
    </ul>
</div>
```

## 🚀 Running the Application

### Development Mode

```bash
npm run dev
```

This uses nodemon for automatic server restart on file changes.

### Production Mode

```bash
npm start
```

Visit `http://localhost:5000` in your browser.

## 📦 Deployment

### Deploy to Heroku

1. Create a Heroku account and install [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli)

2. Login to Heroku:
```bash
heroku login
```

3. Create a new Heroku app:
```bash
heroku create your-portfolio-name
```

4. Set environment variables:
```bash
heroku config:set EMAIL_USER=your.email@gmail.com
heroku config:set EMAIL_PASSWORD=your_app_password
```

5. Deploy:
```bash
git push heroku main
```

### Deploy to Vercel

1. Install [Vercel CLI](https://vercel.com/cli):
```bash
npm i -g vercel
```

2. Deploy:
```bash
vercel
```

3. Add environment variables in Vercel dashboard

### Deploy to Netlify

1. Build frontend only (remove server dependency)
2. Create `netlify.toml`:
```toml
[build]
  publish = "."
```
3. Connect your Git repository to Netlify
4. Deploy!

### Deploy to AWS / DigitalOcean

1. Set up a server with Node.js
2. Clone your repository
3. Install dependencies
4. Use PM2 for process management:
```bash
npm install -g pm2
pm2 start server.js
pm2 startup
pm2 save
```

## 📱 Testing

### Manual Testing Checklist

- [ ] Navigation works smoothly
- [ ] All links are functional
- [ ] Contact form submits successfully
- [ ] Email notifications are received
- [ ] Responsive design works on mobile
- [ ] All images load properly
- [ ] Animations work smoothly
- [ ] SEO meta tags are present

### Browser Testing

Test on:
- Chrome
- Firefox
- Safari
- Edge
- Mobile browsers (iOS Safari, Chrome Mobile)

## 🔧 Troubleshooting

### Email Not Sending

1. Verify Gmail credentials in `.env`
2. Check if 2FA is enabled
3. Ensure app password is correct
4. Check spam folder for test emails

### Server Not Starting

1. Check if port 5000 is available
2. Verify Node.js version (v14+)
3. Ensure all dependencies are installed
4. Check `.env` file exists and is configured

### MongoDB Connection Issues

1. Ensure MongoDB is running locally
2. Check connection string in `.env`
3. For MongoDB Atlas, whitelist your IP address

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

Contributions are welcome! Feel free to submit issues and pull requests.

## 📧 Contact

Your Name - [your.email@example.com](mailto:your.email@example.com)

Project Link: [https://github.com/yourusername/portfolio](https://github.com/yourusername/portfolio)

## 🙏 Acknowledgments

- Font families from [Google Fonts](https://fonts.google.com/)
- Icons inspiration from various open-source projects
- Design inspiration from [Dribbble](https://dribbble.com/) and [Awwwards](https://www.awwwards.com/)

## 📸 Screenshots

### Desktop View
![Desktop Screenshot](./assets/screenshot-desktop.png)

### Mobile View
![Mobile Screenshot](./assets/screenshot-mobile.png)

### Contact Form
![Contact Form](./assets/screenshot-contact.png)

---

⭐ If you found this helpful, please consider giving it a star!

**Built with ❤️ for Future Interns Program**
