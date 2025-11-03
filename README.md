# Personal Portfolio Website

A clean, professional portfolio website built with Jekyll and hosted on GitHub Pages.

## Features

- Clean, modern design with responsive layout
- Professional navigation and footer
- Hero section for impactful first impression
- About page for your story and background
- Portfolio page to showcase your work
- Resume/CV page with downloadable links
- SEO optimized with jekyll-seo-tag
- Automatic sitemap generation
- Mobile-friendly design

## Quick Start

### Prerequisites

- Git
- Ruby (version 3.0 or higher)
- Bundler

### Local Development

1. **Install dependencies:**
   ```bash
   bundle install
   ```

2. **Run the site locally:**
   ```bash
   bundle exec jekyll serve
   ```

3. **View your site:**
   Open your browser to `http://localhost:4000`

The site will automatically rebuild when you make changes to files.

## Customization Guide

### 1. Update Site Configuration

Edit `_config.yml` to personalize your site:

```yaml
title: Your Name
email: your.email@example.com
description: Your professional tagline

author:
  name: Your Name
  bio: "Your professional summary"
  location: "Your City, State"
  linkedin: your-linkedin-username
  github: your-github-username
  email: your.email@example.com
```

### 2. Customize Your Home Page

Edit `index.md` to update:
- Your name and headline
- Your professional tagline
- Your summary/introduction
- Call-to-action buttons

### 3. Fill Out Your About Page

Edit `about.md` to add:
- Your background story
- Skills and expertise
- Work experience
- Education
- Contact information

### 4. Showcase Your Work

Edit `portfolio.md` to add:
- Project descriptions
- Your role in each project
- Technologies used
- Links to live projects or case studies

### 5. Update Your Resume

Edit `resume.md` to include:
- Professional summary
- Work experience
- Education
- Skills
- Certifications
- Publications/Awards

**Note:** To add downloadable PDF versions of your resume:
1. Create a folder: `assets/documents/`
2. Add your PDF files (e.g., `resume.pdf`, `cv.pdf`)
3. Update the links in `resume.md`:
   ```markdown
   <a href="{{ '/assets/documents/resume.pdf' | relative_url }}" class="btn">Download Resume (PDF)</a>
   ```

### 6. Add Your Photo

1. Add your professional headshot to `assets/images/`
2. Update `index.md` to include:
   ```markdown
   <img src="{{ '/assets/images/your-photo.jpg' | relative_url }}" alt="Your Name" style="max-width: 300px; border-radius: 50%;">
   ```

### 7. Customize Colors and Styling

Edit `assets/css/main.css` to change:
- Color scheme (update CSS variables in `:root`)
- Fonts
- Layout spacing
- Any other visual elements

## Deploying to GitHub Pages

### Step 1: Create a GitHub Repository

1. Go to [GitHub](https://github.com) and create a new repository
2. Name it `username.github.io` (replace `username` with your GitHub username)
   - This naming convention gives you a clean URL: `https://username.github.io`
   - Alternatively, use any name for a URL like: `https://username.github.io/repo-name`

### Step 2: Push Your Code

```bash
# Initialize git repository (if not already done)
git init

# Add all files
git add .

# Create initial commit
git commit -m "Initial portfolio site"

# Add your GitHub repository as remote
git remote add origin https://github.com/username/username.github.io.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** → **Pages**
3. Under **Source**, select:
   - Source: **GitHub Actions**
4. The site will automatically build and deploy when you push changes

### Step 4: Access Your Site

Your site will be live at:
- `https://username.github.io` (for username.github.io repos)
- `https://username.github.io/repo-name` (for other repos)

## Adding a Custom Domain (Optional)

1. Purchase a domain from a domain registrar
2. Add a `CNAME` file to your repository with your domain:
   ```
   yourdomain.com
   ```
3. Configure DNS settings with your registrar:
   - Add an A record pointing to GitHub's IPs
   - Or add a CNAME record pointing to `username.github.io`
4. In GitHub Settings → Pages, add your custom domain

## Making Updates

After initial setup, updating your site is simple:

```bash
# Make your changes to any files
# Then commit and push:

git add .
git commit -m "Update portfolio with new project"
git push
```

GitHub Actions will automatically rebuild and deploy your site within a few minutes.

## Project Structure

```
.
├── _config.yml           # Site configuration
├── _layouts/             # Page templates
│   ├── default.html      # Base template
│   ├── home.html         # Home page template
│   └── page.html         # Standard page template
├── _includes/            # Reusable components
│   ├── header.html       # Site header/navigation
│   └── footer.html       # Site footer
├── assets/
│   ├── css/
│   │   └── main.css      # Site styles
│   ├── js/               # JavaScript files
│   └── images/           # Images and photos
├── .github/
│   └── workflows/
│       └── jekyll.yml    # GitHub Actions deployment
├── index.md              # Home page
├── about.md              # About page
├── portfolio.md          # Portfolio page
├── resume.md             # Resume page
└── README.md             # This file
```

## Tips for Success

1. **Keep it updated:** Regularly update your portfolio with new projects and experiences
2. **Professional photo:** Use a high-quality, professional headshot
3. **Proofread:** Check for typos and grammatical errors
4. **Mobile test:** Always check how your site looks on mobile devices
5. **Performance:** Keep images optimized and under 500KB when possible
6. **SEO:** Fill out page titles and descriptions in the front matter
7. **Analytics:** Consider adding Google Analytics to track visitors

## Troubleshooting

**Site not building?**
- Check the Actions tab in your GitHub repository for build errors
- Ensure your `_config.yml` is valid YAML
- Check that all file paths are correct

**Styles not loading?**
- Clear your browser cache
- Check that `main.css` exists in `assets/css/`
- Verify the path in `_layouts/default.html`

**Changes not showing?**
- Wait a few minutes for GitHub Actions to rebuild
- Hard refresh your browser (Ctrl+Shift+R or Cmd+Shift+R)
- Check that your changes were committed and pushed

## Need Help?

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Markdown Guide](https://www.markdownguide.org/)

## License

This template is free to use for your personal portfolio. Attribution is appreciated but not required.
