# GitHub Deployment Instructions

Follow these steps to deploy the FotbPredict Football Score Predictor to your GitHub account.

## 1. Create a GitHub Repository

If you haven't already, create a new repository at https://github.com/new:

- Name: `football-score-predictor`
- Description: Advanced football match score prediction with machine learning
- Visibility: Public (recommended for GitHub Pages, or Private if preferred)
- Do NOT initialize with README, license, or .gitignore

## 2. Push the Code to GitHub

Once you have downloaded the project files from Same.new, push them to your GitHub repository:

```bash
# If you're starting fresh
git clone https://github.com/jerkybutterfly/football-score-predictor.git
cd football-score-predictor

# Copy all the project files to this directory
# Then run:
git add .
git commit -m "Initial commit with PWA capability"
git push -u origin master
```

## 3. Deploy to GitHub Pages

There are two options for deploying to GitHub Pages:

### Option A: Deploy the Full App (Requires Build Setup)

1. Add the GitHub Pages workflow:
   - Go to your repository on GitHub
   - Click on "Actions" tab
   - Choose "New workflow"
   - Search for "Next.js" and select "Deploy Next.js to GitHub Pages"
   - Commit the workflow file

2. Configure the deployment:
   - Go to repository Settings → Pages
   - Under "Source", select "GitHub Actions"
   - The workflow will automatically build and deploy your site

### Option B: Deploy the Landing Page Only (Simpler)

1. Go to repository Settings → Pages
2. Under "Source", select "Deploy from a branch"
3. Choose "master" branch and "/gh-pages" folder
4. Click "Save"
5. Wait for the deployment to complete (check the "Actions" tab)

Your site will be available at: `https://jerkybutterfly.github.io/football-score-predictor/`

## 4. Custom Domain (Optional)

If you have a custom domain:

1. Go to repository Settings → Pages
2. Under "Custom domain", enter your domain name
3. Click "Save"
4. Configure your DNS provider with the appropriate records
5. Wait for HTTPS to be provisioned

## 5. Update the QR Code

After deployment, update the QR code in the `/gh-pages/qr-code.png` file:

1. Generate a QR code for your deployment URL
2. Replace the existing QR code file
3. Commit and push the change

## Troubleshooting

- If your site doesn't appear after deployment, check the "Actions" tab for any errors
- Make sure your repository is public if you're using the free GitHub Pages
- If the PWA doesn't work, check that the manifest and service worker paths are correct
- For any issues with the Next.js build, refer to the Next.js documentation
