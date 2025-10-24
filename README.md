# AI Tools & Tutorials Website

A static website featuring AI development tools and tutorials for Lovable, Replit, and VS Code with GitHub Copilot.

## Deploying to Cloudflare Pages

### Option 1: Deploy via Git (Recommended)

1. **Create a Git Repository**
   - Initialize git in this directory: `git init`
   - Add files: `git add .`
   - Commit: `git commit -m "Initial commit"`
   - Create a repository on GitHub
   - Push to GitHub: 
     ```
     git remote add origin <your-repo-url>
     git push -u origin main
     ```

2. **Deploy on Cloudflare Pages**
   - Log in to [Cloudflare Dashboard](https://dash.cloudflare.com/)
   - Go to "Workers & Pages" > "Create application" > "Pages" > "Connect to Git"
   - Select your GitHub repository
   - Configure build settings:
     - Framework preset: None (static HTML)
     - Build command: (leave empty)
     - Build output directory: `/`
   - Click "Save and Deploy"

### Option 2: Direct Upload via Dashboard

1. **Log in to Cloudflare**
   - Go to [Cloudflare Dashboard](https://dash.cloudflare.com/)
   - Navigate to "Workers & Pages"

2. **Create New Project**
   - Click "Create application" > "Pages" > "Upload assets"
   - Name your project (e.g., "ai-tools-tutorials")
   - Upload all the HTML, CSS files from this directory

3. **Deploy**
   - Click "Deploy site"
   - Your site will be live at: `https://ai-tools-tutorials.pages.dev` (or your custom domain)

### Option 3: Using Wrangler CLI

1. **Install Wrangler**
   ```
   npm install -g wrangler
   ```

2. **Login to Cloudflare**
   ```
   wrangler login
   ```

3. **Deploy**
   ```
   wrangler pages deploy . --project-name=ai-tools-tutorials
   ```

## Local Development

To preview the site locally, you can use any static web server:

```bash
# Using Python
python -m http.server 8000

# Using Node.js (http-server)
npx http-server

# Using PHP
php -S localhost:8000
```

Then open `http://localhost:8000` in your browser.

## Project Structure

```
aitools/
├── index.html                    # Main homepage
├── lovable-tutorial.html         # Lovable tutorial page
├── replit-tutorial.html          # Replit tutorial page
├── vscode-copilot-tutorial.html  # VS Code + Copilot tutorial page
├── styles.css                    # Main stylesheet
├── tutorial.css                  # Tutorial pages stylesheet
└── README.md                     # This file
```

## Next Steps

After deployment:
1. Add custom domain (optional) in Cloudflare Pages settings
2. Fill in the tutorial content in the HTML files
3. Test all links and functionality
4. Set up custom redirects if needed
