# Hello World GitHub Pages Deploy

This repository contains a GitHub Actions workflow that automatically creates a "Hello World" HTML page and deploys it to GitHub Pages.

## What it does

The workflow performs the following steps:

1. **Creates HTML Page**: Generates a styled "Hello World" HTML page with:
   - Responsive design
   - Modern gradient background
   - Glass morphism effect
   - Timestamp showing when it was generated

2. **Uploads Artifact**: Saves the HTML page as a GitHub Actions artifact for 30 days

3. **Deploys to GitHub Pages**: Automatically deploys the page to GitHub Pages

## Workflow Triggers

The workflow runs on:
- Push to `main` or `master` branch
- Pull requests to `main` or `master` branch  
- Manual trigger (workflow_dispatch)

## Setup Instructions

1. **Enable GitHub Pages**: 
   - Go to your repository Settings
   - Navigate to "Pages" section
   - Under "Source", select "GitHub Actions"

2. **Push this code**: The workflow will automatically run when you push to the main branch

3. **View your site**: After deployment, your site will be available at:
   `https://[username].github.io/[repository-name]/`

## Workflow File

The main workflow is defined in [`.github/workflows/deploy-hello-world.yml`](.github/workflows/deploy-hello-world.yml)

### Key Features:
- Uses latest Ubuntu runner
- Proper permissions for Pages deployment
- Artifact upload with 30-day retention
- Separate build and deploy jobs for better organization
- Concurrency control to prevent multiple deployments

## Permissions Required

The workflow requires these permissions:
- `contents: read` - To checkout the repository
- `pages: write` - To deploy to GitHub Pages
- `id-token: write` - For secure deployment

## Artifacts

Each workflow run creates an artifact named `hello-world-page` containing the generated HTML file, which you can download from the Actions tab.