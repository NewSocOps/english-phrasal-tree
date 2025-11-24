# GitHub Pages Setup Guide

This guide will help you enable GitHub Pages for this repository using GitHub Actions.

## Prerequisites

- You must have admin access to the repository
- The repository must be public (or have GitHub Pro/Team for private repos)

## Step-by-Step Instructions

### 1. Navigate to Repository Settings

1. Go to your repository on GitHub: `https://github.com/NewSocOps/english-phrasal-tree`
2. Click on the **Settings** tab (you need admin access)

### 2. Access GitHub Pages Settings

1. In the left sidebar, scroll down to find **Pages** under the "Code and automation" section
2. Click on **Pages**

### 3. Configure Build and Deployment Source

1. Under the **Build and deployment** section, you'll see a **Source** dropdown
2. Select **GitHub Actions** from the dropdown menu
3. The page will automatically save this setting

### 4. Verify Configuration

After enabling GitHub Actions as the source:

- You should see a message confirming GitHub Actions is set as the source
- The workflow in `.github/workflows/deploy.yml` will be used for deployments
- On the next push to the `main` branch, the workflow will automatically deploy

### 5. Trigger First Deployment

The deployment will be triggered automatically on:
- Any push to the `main` branch
- Manual trigger via the "Actions" tab using "workflow_dispatch"

To manually trigger the first deployment:

1. Go to the **Actions** tab in your repository
2. Click on "Deploy to GitHub Pages" workflow in the left sidebar
3. Click the **Run workflow** button
4. Select the `main` branch and click **Run workflow**

### 6. Check Deployment Status

1. Go to the **Actions** tab to monitor the workflow execution
2. Once completed successfully, your site will be live at:
   - `https://newsocops.github.io/english-phrasal-tree/`

## Troubleshooting

### Workflow Fails with "Not Found" Error

If the workflow fails with errors about Pages not being found or not configured:
- Verify that GitHub Pages is enabled in Settings → Pages
- Ensure "GitHub Actions" is selected as the source (not a branch)
- Check that the repository has Pages enabled (may require public repo or GitHub Pro)

### 404 Error After Deployment

If you see a 404 error after successful deployment:
- Verify the `base` path in `vite.config.js` matches your repository name
- Current setting: `base: '/english-phrasal-tree/'`
- Wait a few minutes for DNS propagation

### Permission Errors

If you see permission errors in the workflow:
- The workflow has the correct permissions already configured
- Ensure GitHub Actions has write access to the repository
- Check repository Settings → Actions → General → Workflow permissions

## Current Configuration

This repository is already configured with:

- ✅ Deploy workflow at `.github/workflows/deploy.yml`
- ✅ Correct permissions (pages: write, id-token: write)
- ✅ Proper build configuration (Vite outputs to `./dist`)
- ✅ Correct artifact upload path (`./dist`)
- ✅ Base URL configured in Vite (`/english-phrasal-tree/`)

**The only missing step is enabling GitHub Pages with GitHub Actions as the source in the repository settings.**

## Additional Resources

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Deploying to GitHub Pages with Actions](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#publishing-with-a-custom-github-actions-workflow)
- [Vite Deployment Guide](https://vitejs.dev/guide/static-deploy.html#github-pages)
