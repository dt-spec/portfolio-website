# Quick Setup — Enable GitHub Pages (2 minutes)

The portfolio is **ready to deploy**. All code and infrastructure is in place. Only one manual step remains: enabling GitHub Pages in repository settings.

## ⚡ Quick Steps (2 minutes)

### 1️⃣ Go to Repository Settings

Visit: **https://github.com/dt-spec/portfolio-website/settings/pages**

Or navigate manually:
1. Open https://github.com/dt-spec/portfolio-website
2. Click the **Settings** tab (top right)
3. Click **Pages** in the left sidebar (under "Code and automation")

### 2️⃣ Enable GitHub Pages

Under **"Build and deployment"**:
- **Source**: Select **"GitHub Actions"** from the dropdown
- Click **Save** (or it may auto-save)

That's it! ✅

### 3️⃣ Wait for Deployment (~1 minute)

1. Go to the **Actions** tab: https://github.com/dt-spec/portfolio-website/actions
2. Watch the "Deploy to GitHub Pages" workflow run
3. Wait for the green checkmark (typically 30-60 seconds)

### 4️⃣ Access Your Live Site

Once the workflow completes:

**🌐 Live URL: https://dt-spec.github.io/portfolio-website/**

## ✅ What You'll See

Your portfolio will be live with:
- **Featured project**: Koffeeyap prominently displayed
- **5 case studies** with detailed problem → process → outcome format
- **Modern, minimal design** suitable for design/PM roles
- **Fully responsive** on mobile, tablet, and desktop
- **Professional content** — no placeholder text or fake metrics

## 🔄 Automatic Updates

After this one-time setup:
- Every push to `main` branch automatically deploys
- Changes go live in 1-2 minutes
- No manual steps required ever again

## ❓ Troubleshooting

### "I don't see the Pages option"
- Make sure you're logged into the correct GitHub account
- You need **admin access** to the repository
- If the repo is private, you need GitHub Pro or a paid plan (or make the repo public)

### "Workflow failed"
- Check that you selected "GitHub Actions" as the source (not "Deploy from branch")
- Wait a minute and manually trigger the workflow from the Actions tab
- Check workflow logs for specific error messages

### "Site shows 404"
- Wait 2-3 minutes for DNS propagation
- Try a hard refresh: `Ctrl+Shift+R` (Windows/Linux) or `Cmd+Shift+R` (Mac)
- Check that the workflow completed successfully (green checkmark)

## 📚 Additional Documentation

- **[DEPLOYMENT.md](DEPLOYMENT.md)** — Full deployment guide with troubleshooting
- **[README.md](README.md)** — Project overview and tech stack

## 🆘 Still Stuck?

Check the GitHub Pages documentation: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#publishing-with-a-custom-github-actions-workflow

---

**Questions?** Contact Dev Tiwari at [devkumar@ualberta.ca](mailto:devkumar@ualberta.ca)
