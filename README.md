# Personal Website

A modern personal website built with Jekyll and Tailwind CSS, hosted on GitHub Pages.

## Features

- **Jekyll-based**: Static site generator with blogging capabilities
- **Tailwind CSS**: Modern utility-first CSS framework for styling
- **Responsive Design**: Mobile-friendly layout
- **Blog**: Write and publish blog posts using Markdown
- **Projects**: Showcase your portfolio and projects
- **Talks**: Display your presentations and speaking engagements

## Project Structure

```
├── _config.yml           # Jekyll configuration
├── _layouts/             # Page templates
│   ├── default.html      # Base layout with navigation
│   ├── post.html         # Blog post layout
│   └── page.html         # Standard page layout
├── _includes/            # Reusable components
│   ├── nav.html          # Navigation menu
│   └── footer.html       # Site footer
├── _posts/               # Blog posts (YYYY-MM-DD-title.md)
├── pages/                # Static pages
│   ├── projects.md       # Projects page
│   └── talks.md          # Talks page
├── assets/
│   └── css/
│       └── main.css      # Custom styles
├── index.md              # Home page
├── blog.html             # Blog listing page
└── Gemfile               # Ruby dependencies
```

## Local Development

### Prerequisites

- Ruby (version 2.5.0 or higher)
- Bundler gem

### Setup

1. Install dependencies:
   ```bash
   bundle install
   ```

2. Run the development server:
   ```bash
   bundle exec jekyll serve
   ```

3. Open your browser to `http://localhost:4000`

The site will automatically rebuild when you make changes to files.

## Customization

### Update Site Information

Edit `_config.yml` to customize:
- Site title
- Your email
- Site description
- Base URL

```yaml
title: Your Name
email: your.email@example.com
description: Your site description
```

### Update Home Page

Edit `index.md` to personalize:
- Your name and tagline
- Introduction text
- Call-to-action buttons

### Add Blog Posts

Create a new file in `_posts/` with the format:
```
_posts/YYYY-MM-DD-title-of-post.md
```

Example post structure:
```markdown
---
layout: post
title: "Your Post Title"
date: 2025-11-23
author: Your Name
tags: [tag1, tag2, tag3]
---

Your content here...
```

### Add Projects

Edit `pages/projects.md` to add your projects with:
- Project name
- Description
- Technologies used
- Links to GitHub/Demo

### Add Talks

Edit `pages/talks.md` to add your presentations with:
- Talk title
- Event name and date
- Description
- Links to slides/video/code

### Customize Styling

The site uses Tailwind CSS via CDN. To customize:

1. **Colors and spacing**: Edit Tailwind classes in layout files
2. **Custom CSS**: Add styles to `assets/css/main.css`
3. **Production setup**: For optimized Tailwind (with purging), set up PostCSS

### Update Navigation

Edit `_includes/nav.html` to modify the navigation menu items.

### Update Footer

Edit `_includes/footer.html` to add social links or update copyright information.

## Deployment to GitHub Pages

### Using GitHub Actions (Recommended)

1. Push your changes to the `main` branch:
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

2. Go to your repository settings on GitHub
3. Navigate to **Pages** section
4. Under **Source**, select **GitHub Actions**
5. GitHub will automatically detect Jekyll and deploy your site

### Manual Deployment

Alternatively, GitHub Pages will automatically build and deploy Jekyll sites from the `main` branch.

Your site will be available at: `https://jankaul.github.io`

## Advanced Configuration

### Custom Domain

To use a custom domain:

1. Create a file named `CNAME` in the root directory
2. Add your domain name (e.g., `yourdomain.com`)
3. Configure DNS settings with your domain provider

### Tailwind CSS with PostCSS

For production-optimized Tailwind (smaller file size):

1. Install Node.js dependencies:
   ```bash
   npm init -y
   npm install -D tailwindcss postcss autoprefixer
   ```

2. Create `tailwind.config.js` and configure content paths
3. Set up `postcss.config.js`
4. Update build process in `_config.yml`

### SEO Optimization

The site includes `jekyll-seo-tag` plugin. To optimize:

1. Add description to each page's front matter
2. Add OpenGraph images
3. Update `_config.yml` with social media handles

## Troubleshooting

### Jekyll Build Errors

If you encounter build errors:
```bash
bundle exec jekyll build --trace
```

### Dependency Issues

Update gems:
```bash
bundle update
```

### Tailwind Styles Not Applying

- Check browser console for CSS loading errors
- Verify Tailwind CDN script tag in `_layouts/default.html`
- Clear browser cache

## Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Markdown Guide](https://www.markdownguide.org/)

## License

This project is open source and available under the MIT License.
