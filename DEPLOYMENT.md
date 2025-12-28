# Deployment Guide

## GitHub Pages Deployment (Recommended)

GitHub Pages automatically builds and deploys your Jekyll site.

### Step 1: Enable GitHub Pages

1. Go to repository settings: https://github.com/CI-codesmith/ml-site/settings
2. Scroll to "Pages" section
3. Source: Select `main` branch
4. Click "Save"
5. Wait 2-3 minutes for build

### Step 2: Access Your Site

Your site will be live at:
```
https://CI-codesmith.github.io/ml-site
```

### Step 3: Monitor Deployments

- Go to "Actions" tab to see build status
- Check for any build errors in the deployment logs

---

## Manual Testing Locally

Before pushing to GitHub, test your site locally:

```bash
# Install Jekyll (requires Ruby)
gem install bundler jekyll

# Navigate to your repo
cd ml-site

# Build and serve
jekyll serve

# Visit: http://localhost:4000
```

---

## Alternative Deployment: Netlify

1. Go to [netlify.com](https://www.netlify.com/)
2. Click "New site from Git"
3. Connect GitHub account
4. Select `CI-codesmith/ml-site` repository
5. Build command: `jekyll build`
6. Publish directory: `_site`
7. Deploy

---

## Alternative Deployment: Vercel

1. Go to [vercel.com](https://vercel.com/)
2. Import GitHub project
3. Deploy

---

## CI/CD Pipeline (GitHub Actions)

The repository includes a GitHub Actions workflow for automatic deployment.

**.github/workflows/jekyll.yml:**
```yaml
name: Build and Deploy

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v3
    
    - name: Setup Ruby
      uses: ruby/setup-ruby@v1
      with:
        ruby-version: '3.1'
        bundler-cache: true
    
    - name: Build Jekyll site
      run: bundle exec jekyll build
    
    - name: Deploy to GitHub Pages
      uses: peaceiris/actions-gh-pages@v3
      with:
        github_token: ${{ secrets.GITHUB_TOKEN }}
        publish_dir: ./_site
```

---

## SEO Optimization

Ensure your site is discoverable:

1. **Sitemap:** Jekyll automatically generates `sitemap.xml`
2. **Robots.txt:** Create file at root
3. **Meta tags:** Added via `jekyll-seo-tag` plugin
4. **Submit to Search Engines:**
   - Google: [Google Search Console](https://search.google.com/search-console)
   - Bing: [Bing Webmaster Tools](https://www.bing.com/webmasters)

---

## Custom Domain (Optional)

1. Purchase a domain (e.g., machinelearningcourse.com)
2. In repository settings → Pages
3. Under "Custom domain," enter your domain
4. Update DNS settings with your domain provider
5. Point to GitHub Pages servers:
   ```
   A records: 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
   ```

---

## Troubleshooting

### Site not building?
- Check GitHub Actions logs for errors
- Ensure `_config.yml` is valid YAML
- Check file paths are relative

### Pages not appearing?
- Ensure pages have front matter: `---`
- Check `_config.yml` for correct baseurl

### Images not loading?
- Use relative paths: `![alt text](../images/image.png)`
- Check baseurl in `_config.yml`

---

## Monitoring & Analytics

### Add Google Analytics

Edit `_config.yml`:
```yaml
google_analytics: YOUR_TRACKING_ID
```

### Monitor Performance

- GitHub Pages has built-in monitoring
- Check monthly bandwidth usage in settings
- View traffic in repository insights

---

## Maintenance

- **Regular Updates:** Keep Jekyll and plugins updated
- **Content Reviews:** Update course content as needed
- **Backup:** Maintain GitHub as your backup
- **Versioning:** Use git tags for releases

```bash
# Create release
git tag -a v1.0.0 -m "First release"
git push origin v1.0.0
```

---

## Support

For deployment issues:
- [GitHub Pages Documentation](https://pages.github.com/)
- [Jekyll Documentation](https://jekyllrb.com/)
- [GitHub Actions Docs](https://docs.github.com/en/actions)

---

[← Back to Resources](resources/)
