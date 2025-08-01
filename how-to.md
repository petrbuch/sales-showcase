# Complete Prototyping Stack Setup Guide

A step-by-step guide to set up Git, GitHub, and Netlify for rapid web prototyping.

## Prerequisites

- A computer with admin rights
- An internet connection
- A web browser

## Step 1: Install Git

### macOS

1. Open Terminal (cmd+space, type "terminal")
2. Check if Git is already installed:
   ```bash
   git --version
   ```
3. If not installed, install via Homebrew:
   ```bash
   # Install Homebrew if you don't have it
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   
   # Install Git
   brew install git
   ```

### Windows

1. Download Git from https://git-scm.com/download/win
2. Run the installer
3. Use recommended settings (keep clicking "Next")
4. Open Git Bash to verify:
   ```bash
   git --version
   ```

## Step 2: Configure Git

Run these commands in Terminal (macOS) or Git Bash (Windows):

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

## Step 3: Create a GitHub Account

1. Go to https://github.com
2. Click "Sign up"
3. Choose a username (e.g., yourname-company)
4. Enter your email
5. Create a strong password
6. Verify your account via email

## Step 4: Set Up SSH Key for GitHub

### macOS

1. Generate SSH key:
   ```bash
   ssh-keygen -t ed25519 -C "your.email@example.com"
   ```
2. Press Enter to accept default location
3. Enter a passphrase (optional but recommended)
4. Start SSH agent:
   ```bash
   eval "$(ssh-agent -s)"
   ```
5. Add key to agent:
   ```bash
   ssh-add ~/.ssh/id_ed25519
   ```
6. Copy public key:
   ```bash
   pbcopy < ~/.ssh/id_ed25519.pub
   ```

### Windows

1. In Git Bash, generate SSH key:
   ```bash
   ssh-keygen -t ed25519 -C "your.email@example.com"
   ```
2. Press Enter for default location
3. Enter passphrase (optional)
4. Start SSH agent:
   ```bash
   eval $(ssh-agent -s)
   ```
5. Add key:
   ```bash
   ssh-add ~/.ssh/id_ed25519
   ```
6. Copy public key:
   ```bash
   cat ~/.ssh/id_ed25519.pub
   ```
   Then manually copy the output

## Step 5: Add SSH Key to GitHub

1. Go to GitHub.com and sign in
2. Click your profile picture → Settings
3. Click "SSH and GPG keys"
4. Click "New SSH key"
5. Title: "Work Laptop" (or similar)
6. Paste your key
7. Click "Add SSH key"

## Step 6: Create Your First Repository

1. On GitHub, click the "+" icon → "New repository"
2. Name: "my-first-prototype"
3. Description: "Testing prototyping workflow"
4. Keep it Public
5. Check "Add a README file"
6. Click "Create repository"

## Step 7: Clone Repository Locally

1. On your repo page, click green "Code" button
2. Select "SSH" tab
3. Copy the URL

### macOS
```bash
cd ~/Desktop
git clone git@github.com:yourusername/my-first-prototype.git
cd my-first-prototype
```

### Windows (Git Bash)
```bash
cd /c/Users/YourName/Desktop
git clone git@github.com:yourusername/my-first-prototype.git
cd my-first-prototype
```

## Step 8: Create a Simple Web App

1. Create index.html:

### macOS
```bash
touch index.html
open -e index.html
```

### Windows
```bash
touch index.html
notepad index.html
```

2. Paste this code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My First Prototype</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f0f0f0;
        }
        .container {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        button {
            background-color: #007bff;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
        }
        button:hover {
            background-color: #0056b3;
        }
        #output {
            margin-top: 20px;
            padding: 10px;
            background-color: #f8f9fa;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Hello, Prototype!</h1>
        <p>This is a simple prototype to test our deployment pipeline.</p>
        <button onclick="showMessage()">Click Me!</button>
        <div id="output"></div>
    </div>

    <script>
        function showMessage() {
            const output = document.getElementById('output');
            const now = new Date().toLocaleString();
            output.innerHTML = `Button clicked at: ${now}`;
        }
    </script>
</body>
</html>
```

3. Save and close the file

## Step 9: Push to GitHub

```bash
git add index.html
git commit -m "Add simple prototype"
git push origin main
```

If prompted for username/password, use your GitHub username and a Personal Access Token (not your password).

## Step 10: Set Up Netlify Account

1. Go to https://netlify.com
2. Click "Sign up"
3. Choose "Sign up with GitHub"
4. Authorize Netlify

## Step 11: Deploy to Netlify

1. In Netlify dashboard, click "Add new site"
2. Choose "Import an existing project"
3. Click "GitHub"
4. Authorize Netlify to access your repos
5. Search for "my-first-prototype"
6. Click on it
7. Keep all default settings
8. Click "Deploy site"

## Step 12: Your Site is Live!

1. Netlify will show a random URL like `amazing-einstein-a1b2c3.netlify.app`
2. Click the URL to see your live site
3. Any changes you push to GitHub will auto-deploy

## Step 13: Make Changes and See Auto-Deploy

1. Edit your local index.html
2. Change the h1 text to "Hello, World!"
3. Save the file
4. Push changes:
   ```bash
   git add index.html
   git commit -m "Update heading"
   git push
   ```
5. Go to Netlify dashboard
6. Watch the deploy happen (takes ~30 seconds)
7. Refresh your site URL

## Bonus: Custom Domain (Optional)

1. In Netlify, go to "Domain settings"
2. Click "Add custom domain"
3. Enter your domain
4. Follow DNS configuration instructions

## Common Issues & Solutions

### Git Push Asks for Password
- You need to use Personal Access Token, not password
- GitHub → Settings → Developer settings → Personal access tokens

### SSH Key Not Working
```bash
ssh -T git@github.com
```
Should say "Hi username! You've successfully authenticated"

### Netlify Deploy Failed
- Check build logs in Netlify dashboard
- Ensure index.html is in root directory
- Make sure you pushed to the main branch

## Next Steps

1. Add CSS file for better styling
2. Add JavaScript functionality
3. Try frameworks (React, Vue) - Netlify handles build process
4. Set up custom deploy previews for branches
5. Add forms (Netlify has built-in form handling)

## Quick Reference Commands

```bash
# Daily workflow
git add .
git commit -m "Description of changes"
git push

# Check status
git status

# See history
git log --oneline

# Create new branch
git checkout -b feature-name

# Switch branches
git checkout main

# Update from remote
git pull
```

## Resources

- Git Documentation: https://git-scm.com/doc
- GitHub Guides: https://guides.github.com
- Netlify Docs: https://docs.netlify.com
- HTML/CSS/JS Reference: https://developer.mozilla.org

---

Congratulations! You now have a complete prototyping pipeline. Every code change automatically deploys to the web!