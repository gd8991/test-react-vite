# Test React Vite - GitHub Pages Deployment

This is a test React + Vite project set up for GitHub Pages deployment.

## Deployment Steps

### 1. Create GitHub Repository
```bash
cd test-react-vite
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/test-react-vite.git
git push -u origin main
```

### 2. Enable GitHub Pages
1. Go to your repository on GitHub
2. Navigate to **Settings** → **Pages**
3. Under **Source**, select **GitHub Actions**

### 3. Automatic Deployment
The GitHub Actions workflow will automatically:
- Trigger on push to `main` branch
- Build the React app
- Deploy to GitHub Pages

Your site will be available at: `https://YOUR_USERNAME.github.io/test-react-vite/`

## Local Development

```bash
npm install
npm run dev
```

## Build Locally

```bash
npm run build
npm run preview
```

## Configuration

- **Base URL**: Set in [vite.config.js](vite.config.js#L7) as `/test-react-vite/`
- **Workflow**: Configured in [.github/workflows/deploy.yml](.github/workflows/deploy.yml)

## Troubleshooting

If deployment fails:
1. Check the **Actions** tab in your GitHub repository
2. Verify GitHub Pages is enabled and set to "GitHub Actions"
3. Ensure the `base` in vite.config.js matches your repository name
4. Check that repository permissions allow Actions to deploy
