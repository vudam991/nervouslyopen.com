# nervouslyopen.com - iOS App Metadata Site

Official support, privacy policies, and app landing pages for:
- **SleepySheepie** 🐑 - A calm bedtime companion for relaxation and sleep
- **Journly** 📔 - A personal journal for reflection and self-discovery

**Live at:** https://nervouslyopen.com

## Repository Structure

```
nervouslyopen.com/
├── index.html                 # Home page with app showcase
├── styles.css                 # Global stylesheet
├── support.md                 # Support page for all apps
├── privacy.md                 # Privacy policy for all apps
├── _config.yml                # Jekyll configuration
├── CNAME                       # Custom domain file
├── apps/
│   ├── sleepysheepie/
│   │   └── index.html         # SleepySheepie app page
│   └── journly/
│       └── index.html         # Journly app page
└── README.md                  # This file
```

## Pages

- **Home** (`/`) - Landing page with app showcase
- **SleepySheepie** (`/apps/sleepysheepie/`) - App details, features, and App Store link
- **Journly** (`/apps/journly/`) - App details, features, and App Store link
- **Privacy Policy** (`/privacy/`) - Comprehensive privacy policy for both apps
- **Support** (`/support/`) - Support contact and FAQ

## Quick Start

### Prerequisites

To run locally:
- Ruby 2.7+
- Bundler

### Local Development

```bash
bundle install
bundle exec jekyll serve
```

The site will be available at `http://localhost:4000/`

### Deployment

The site is automatically deployed to GitHub Pages when changes are pushed to the `main` branch.

## Custom Domain Setup

This repository is configured for **nervouslyopen.com**:

1. **DNS Configuration** - A records pointing to GitHub Pages:
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`

2. **CNAME File** - Automatically maintained by GitHub Pages

3. **HTTPS** - Automatically enabled after DNS verification

## Adding a New App

To add a new app to the site:

1. Create a new directory under `apps/new-app-name/`
2. Copy the structure from an existing app (e.g., `apps/sleepysheepie/`)
3. Update `index.html` with your app's details
4. Update the home page (`index.html`) navigation links
5. Update `support.md` with app-specific support info (if needed)
6. Update `privacy.md` with app-specific privacy details (if needed)
7. Commit and push changes

### App Page Template

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>App Name</title>
  <link rel="stylesheet" href="../../styles.css">
  <meta name="description" content="Brief app description">
</head>
<body>
  <main>
    <nav class="topnav">
      <a href="../../">Home</a>
      <a href="../../privacy/">Privacy</a>
      <a href="../../support/">Support</a>
      <!-- App-specific nav items -->
    </nav>
    <!-- App content -->
  </main>
</body>
</html>
```

## Site Features

✨ **Clean, Modern Design**
- Responsive layout optimized for mobile and desktop
- Professional dark theme with good contrast
- Fast loading times

🔒 **Privacy-First**
- Clear privacy policies for each app
- Support for local-storage apps
- No tracking or analytics

📱 **App Marketing**
- Individual pages for each app
- Feature highlights
- App Store links
- Requirements and details

🛠️ **Easy to Maintain**
- Simple HTML structure
- Centralized styling
- Jekyll for future markdown support
- Clear file organization

## Customization

### Styling
Edit `styles.css` to customize colors, fonts, and layout:

```css
/* Global variables at the top of styles.css */
/* Modify colors, fonts, spacing, etc. */
```

### Content
- Update HTML files directly for structure changes
- Edit markdown files (`.md`) for content changes
- Jekyll will automatically generate HTML from markdown

### Navigation
Update the `<nav class="topnav">` sections in:
- `index.html` (home page)
- `apps/sleepysheepie/index.html`
- `apps/journly/index.html`
- `privacy.md`
- `support.md`

## Files Reference

### index.html
Main landing page showcasing all apps and site sections.

### apps/sleepysheepie/index.html
SleepySheepie app marketing page with:
- App description and features
- Device requirements
- App Store link
- Support and privacy links

### apps/journly/index.html
Journly app marketing page with:
- App description and features
- Device requirements
- App Store link
- Support and privacy links

### privacy.md
Comprehensive privacy policy covering:
- Data collection practices
- Data usage and storage
- User privacy rights
- Contact information

### support.md
Support resources including:
- Contact email
- App-specific FAQs
- Common troubleshooting
- Response time expectations

### styles.css
Global stylesheet with:
- Typography and colors
- Layout and spacing
- Navigation styling
- Card and grid components
- Responsive design

### _config.yml
Jekyll configuration:
- Site metadata
- Remote theme settings
- Build settings
- Plugins

## Local Testing

Before pushing changes:

```bash
# Install dependencies
bundle install

# Build and serve locally
bundle exec jekyll serve

# Visit http://localhost:4000/
```

## Updating App Store Links

When your apps are live on the App Store, update the App Store links in:

1. **apps/sleepysheepie/index.html**
   - Find: `href="https://apps.apple.com/app/sleepysheepie"`
   - Replace with your actual App Store link

2. **apps/journly/index.html**
   - Find: `href="https://apps.apple.com/app/journly"`
   - Replace with your actual App Store link

3. **index.html** (home page)
   - Update both app links if you want home page links

## Git Workflow

```bash
# Clone the repository
git clone https://github.com/vudam991/nervouslyopen.com.git
cd nervouslyopen.com

# Create a feature branch
git checkout -b feature/update-app-details

# Make changes and commit
git add .
git commit -m "Update: App Store links for SleepySheepie"

# Push to GitHub
git push origin feature/update-app-details

# Create a Pull Request on GitHub
# After review, merge to main
```

## Troubleshooting

**Site not updating?**
- GitHub Pages can take 1-2 minutes to rebuild
- Check the "Actions" tab to see build status
- Ensure you pushed to the `main` branch

**Custom domain not working?**
- Verify DNS A records are pointing to GitHub IPs
- Check repository settings > Pages for domain configuration
- Wait up to 24 hours for DNS propagation

**Local site looks different?**
- Ensure you're running the same Jekyll version as GitHub Pages
- Check `Gemfile.lock` for version numbers
- Run `bundle update` to update gems

## Support

For issues with the website, contact: **iam@no-benefit.com**

For app-specific questions, see `/support/`

## License

© 2026 nervouslyopen.com - All rights reserved

---

Built with ❤️ for iOS developers using GitHub Pages