# GitHub Pages Deployment Checklist

Use this checklist to ensure GitHub Pages is properly configured for this repository.

## Pre-deployment Checklist

- [ ] Repository is public (or you have GitHub Pro/Team/Enterprise for private repos)
- [ ] You have admin access to the repository
- [ ] Workflow file exists at `.github/workflows/deploy.yml` ✅ (already present)
- [ ] Vite config has correct base path ✅ (already configured)

## GitHub Pages Configuration

### Step 1: Enable GitHub Pages
- [ ] Navigate to repository **Settings**
- [ ] Click on **Pages** in the left sidebar
- [ ] Under **Build and deployment** → **Source**, select **GitHub Actions**
- [ ] Verify the setting is saved (page will show "GitHub Actions" as source)

### Step 2: Initial Deployment
- [ ] Push a commit to `main` branch OR manually trigger workflow
- [ ] Go to **Actions** tab and verify "Deploy to GitHub Pages" workflow runs
- [ ] Wait for workflow to complete successfully (green checkmark)
- [ ] Check the deployment URL: `https://newsocops.github.io/english-phrasal-tree/`

### Step 3: Verification
- [ ] Visit the live site and verify it loads correctly
- [ ] Test navigation and functionality
- [ ] Verify assets (images, styles) load properly
- [ ] Check browser console for any errors

## Post-deployment

- [ ] Update README with live site link ✅ (already done)
- [ ] Document any custom configuration in README
- [ ] Set up branch protection rules if needed (optional)
- [ ] Configure custom domain if desired (optional)

## Troubleshooting

If deployment fails:
1. Check Actions tab for error messages
2. Verify Pages is enabled with GitHub Actions as source
3. Review workflow permissions in Settings → Actions
4. Ensure all dependencies in package.json are correct
5. Verify build succeeds locally with `npm run build`

## Current Status

✅ **Code Configuration Complete**
- Workflow file configured correctly
- Build configuration correct
- Artifact path configured correctly
- Permissions set properly

⏳ **Awaiting Manual Setup**
- GitHub Pages needs to be enabled in repository Settings → Pages
- Source must be set to "GitHub Actions"

---

**Next Action Required:** Enable GitHub Pages in repository settings (Settings → Pages → Source: GitHub Actions)
