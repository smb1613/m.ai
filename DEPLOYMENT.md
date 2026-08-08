# Deployment Guide for M.ai Downloads Page

This guide explains how to deploy the M.ai downloads page to GitHub Pages.

## Prerequisites

- GitHub account with access to the repository
- Repository at `https://github.com/smb1613/m.ai`

## Deployment Steps

### 1. GitHub Pages Configuration

The repository is already configured for GitHub Pages deployment. The site is built from the `/docs` directory.

### 2. Enable GitHub Pages

1. Go to repository **Settings** → **Pages**
2. Under "Build and deployment":
   - **Source**: Select `Deploy from a branch`
   - **Branch**: Select `main` 
   - **Folder**: Select `/docs`
3. Click **Save**

### 3. Verify Deployment

Once saved, GitHub will automatically:
- Build the site
- Deploy to `https://smb1613.github.io/m.ai`
- Show a green checkmark when deployment is complete

You can monitor deployment progress under **Settings** → **Pages** → **GitHub Pages** section.

## File Structure

```
m.ai/
├── docs/
│   ├── index.html          # Main downloads page
│   ├── 404.html            # Custom error page
│   └── .nojekyll           # Disables Jekyll processing
├── _config.yml             # GitHub Pages configuration
├── DOWNLOADS.md            # Markdown version of downloads
└── DEPLOYMENT.md           # This file
```

## Making Updates

### To Update Release Information

1. Edit `docs/index.html`
2. Update the version number and download link
3. Commit and push to `main` branch
4. GitHub Pages will automatically redeploy

### To Add New Release

Update the following:
1. **Version number** in the HTML
2. **Release date** 
3. **Download link** pointing to the new release executable
4. **Changelog link** to the latest commit

Example:
```html
<h3>M.ai v1.2</h3>
<div class="release-date">📅 Released: August 15, 2026</div>

<div>
    <a href="https://github.com/smb1613/m.ai/releases/download/1.2/M.ai.exe" class="download-btn">
        ⬇️ Download M.ai.exe
    </a>
</div>
```

## Domain Configuration (Optional)

To use a custom domain:

1. Go to **Settings** → **Pages**
2. Under "Custom domain", enter your domain
3. Add DNS records as instructed by GitHub
4. Enable HTTPS when ready

## Troubleshooting

### Site Not Updating

1. Go to **Settings** → **Pages**
2. Check the deployment status
3. Click "Visit site" to test
4. Clear browser cache (Ctrl+Shift+Del)

### 404 Errors

- Ensure files are in `/docs` directory
- Check file names match links in HTML
- Verify `.nojekyll` file exists

### Deployment Failed

1. Check **Settings** → **Actions** for error logs
2. Ensure HTML is valid: https://validator.w3.org/
3. Check for special characters in file names

## Performance Tips

- The HTML page is lightweight (~5KB)
- Images are loaded from external sources
- CSS is inline for faster rendering
- Site is fully responsive and mobile-friendly

## Statistics

Monitor your deployment with GitHub Analytics:
1. Go to **Settings** → **Pages**
2. View traffic and deployment history
3. Track download page visits over time

## Support

For issues or questions:
- Check [GitHub Pages Documentation](https://docs.github.com/en/pages)
- Report issues in the [repository issues page](https://github.com/smb1613/m.ai/issues)
- Visit [GitHub Discussions](https://github.com/smb1613/m.ai/discussions)

---

**Next Steps**: After deployment, share your downloads page link with users:
- Direct link: `https://smb1613.github.io/m.ai`
- Add to README.md
- Link from social media
- Include in release notes
