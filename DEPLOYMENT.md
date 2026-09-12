# Deployment Guide

This portfolio site is configured to automatically deploy to GitHub Pages using GitHub Actions.

## Live URL

Once GitHub Pages is enabled, the site will be available at:

**https://dt-spec.github.io/portfolio-website/**

## One-Time Setup Required

GitHub Pages needs to be manually enabled in the repository settings. Follow these steps:

### 1. Enable GitHub Pages

1. Go to the repository on GitHub: https://github.com/dt-spec/portfolio-website
2. Click **Settings** (top navigation)
3. Click **Pages** (left sidebar under "Code and automation")
4. Under **Source**, select **GitHub Actions**
5. Click **Save**

### 2. Trigger Deployment

Once Pages is enabled with "GitHub Actions" as the source:

1. The workflow will automatically run on the next push to `main`
2. Or manually trigger it:
   - Go to **Actions** tab
   - Click **Deploy to GitHub Pages** workflow
   - Click **Run workflow**
   - Select `main` branch
   - Click **Run workflow**

### 3. Verify Deployment

1. Go to **Actions** tab
2. Wait for the "Deploy to GitHub Pages" workflow to complete (should take ~30 seconds)
3. The workflow will show a green checkmark when successful
4. Visit https://dt-spec.github.io/portfolio-website/ to see the live site

## Automatic Deployments

After the initial setup, every push to the `main` branch will automatically trigger a new deployment. Changes will be live within 1-2 minutes.

## Troubleshooting

### Workflow fails with "Not Found" error

**Cause**: GitHub Pages is not enabled or not configured to use GitHub Actions.

**Solution**: Follow the "Enable GitHub Pages" steps above, ensuring you select **GitHub Actions** as the source.

### Site shows 404

**Cause**: The deployment hasn't completed yet or there's an issue with the workflow.

**Solution**: 
1. Check the Actions tab for workflow status
2. Ensure the workflow completed successfully (green checkmark)
3. Wait a few minutes for DNS propagation
4. Try a hard refresh (Ctrl+Shift+R or Cmd+Shift+R)

### Workflow is queued but not running

**Cause**: GitHub Actions might be waiting for approval or there's a queue.

**Solution**: 
1. Check the Actions tab for pending approvals
2. If using a free account, check GitHub Actions usage limits
3. Wait a few minutes and check again

## Custom Domain (Optional)

To use a custom domain like `devtiwari.com`:

1. Purchase a domain from a registrar (Namecheap, Google Domains, etc.)
2. In GitHub Pages settings, add your custom domain
3. Configure DNS records at your registrar:
   - Add a CNAME record pointing to `dt-spec.github.io`
   - Or add A records pointing to GitHub Pages IPs (see [GitHub Docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site))
4. Enable "Enforce HTTPS" in Pages settings (after DNS propagates)

## Technical Details

- **Deployment Method**: GitHub Actions (`.github/workflows/deploy.yml`)
- **Branch**: `main`
- **Build Time**: ~30 seconds
- **Technology**: Static HTML/CSS/JS (no build step required)
- **CDN**: GitHub's global CDN (fast worldwide)

## Support

If you encounter issues:

1. Check the [GitHub Pages documentation](https://docs.github.com/en/pages)
2. Review workflow logs in the Actions tab
3. Ensure the repository is public (or you have GitHub Pro for private repo Pages)
