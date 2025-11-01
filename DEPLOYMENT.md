# Complete Deployment Guide for mohid.tech

## Step 1: Create GitHub Account & Repository

### 1.1 Create GitHub Account (if you don't have one)
1. Go to [github.com](https://github.com)
2. Click "Sign Up"
3. Create your account (use your email)

### 1.2 Create a New Repository
1. Click the "+" icon (top right) → "New repository"
2. Repository name: `portfolio` (or any name you like)
3. Keep it **PUBLIC** (required for free GitHub Pages)
4. **DO NOT** initialize with README (we already have files)
5. Click "Create repository"

## Step 2: Push Your Code to GitHub

### 2.1 Open PowerShell in your project folder
Right-click in your folder and select "Open PowerShell window here"

### 2.2 Run these commands one by one:

```powershell
# Initialize git repository
git init

# Add all files
git add .

# Commit your files
git commit -m "Initial commit - Portfolio website"

# Add your GitHub repository as remote
# Replace YOUR_USERNAME with your actual GitHub username
git remote add origin https://github.com/YOUR_USERNAME/portfolio.git

# Push to GitHub
git branch -M main
git push -u origin main
```

**Note:** You'll be asked to login to GitHub when you push. Use your GitHub username and password (or personal access token).

## Step 3: Enable GitHub Pages

1. Go to your repository on GitHub: `https://github.com/YOUR_USERNAME/portfolio`
2. Click **Settings** (tab at the top)
3. Scroll down and click **Pages** (in left sidebar)
4. Under "Source":
   - Select branch: **main**
   - Select folder: **/ (root)**
5. Click **Save**
6. Wait 1-2 minutes - your site will be live at: `https://YOUR_USERNAME.github.io/portfolio/`

## Step 4: Purchase Domain Name (mohid.tech)

### 4.1 Buy the Domain
1. Go to one of these registrars:
   - **Namecheap** (recommended): [namecheap.com](https://www.namecheap.com)
   - **Cloudflare**: [cloudflare.com](https://www.cloudflare.com/products/registrar/)
   - **Google Domains**: [domains.google](https://domains.google)
   
2. Search for `mohid.tech`
3. Purchase it (usually $10-15/year)

## Step 5: Configure Custom Domain

### 5.1 In GitHub Repository Settings
1. Go back to **Settings** → **Pages**
2. Under "Custom domain", enter: `mohid.tech`
3. Click **Save**
4. Wait a moment, then check the box "Enforce HTTPS" (may take a few minutes to appear)

### 5.2 Configure DNS at Your Domain Registrar

Go to your domain registrar's DNS settings and add these records:

#### Option A: Using A Records (Recommended)
| Type | Name/Host | Value/Points To | TTL |
|------|-----------|-----------------|-----|
| A    | @         | 185.199.108.153 | 3600 |
| A    | @         | 185.199.109.153 | 3600 |
| A    | @         | 185.199.110.153 | 3600 |
| A    | @         | 185.199.111.153 | 3600 |
| CNAME| www       | YOUR_USERNAME.github.io | 3600 |

**Replace YOUR_USERNAME with your actual GitHub username**

#### Detailed Steps for Common Registrars:

**For Namecheap:**
1. Login to Namecheap
2. Go to "Domain List" → Click "Manage" next to mohid.tech
3. Click "Advanced DNS" tab
4. Add the records above
5. Delete any existing A or CNAME records that conflict

**For Cloudflare:**
1. Add your domain to Cloudflare (if not already)
2. Go to DNS settings
3. Add the records above
4. Make sure proxy status is "DNS only" (gray cloud)

**For GoDaddy:**
1. Go to "My Products" → DNS
2. Add the records above under DNS management

### 5.3 Wait for DNS Propagation
- DNS changes can take 5 minutes to 48 hours
- Usually works within 30 minutes
- Check status at: [whatsmydns.net](https://www.whatsmydns.net)

## Step 6: Verify Everything Works

1. After DNS propagation, visit: `https://mohid.tech`
2. Your portfolio should load with HTTPS (secure)
3. Both `mohid.tech` and `www.mohid.tech` should work

## Troubleshooting

### Issue: "There isn't a GitHub Pages site here"
- Wait 5-10 minutes after enabling GitHub Pages
- Make sure repository is public
- Check that you pushed your code

### Issue: Domain not working
- Wait longer for DNS propagation (up to 24 hours)
- Double-check DNS records
- Make sure CNAME file exists in your repository

### Issue: Not secure / No HTTPS
- Wait 24 hours after adding custom domain
- Uncheck and recheck "Enforce HTTPS" in GitHub settings

## Updating Your Portfolio

Whenever you make changes:

```powershell
git add .
git commit -m "Updated portfolio"
git push
```

Changes will appear on mohid.tech within 1-2 minutes!

## Cost Summary
- GitHub Pages: **FREE** ✅
- Domain (mohid.tech): **$10-15/year**
- SSL Certificate: **FREE** (via GitHub Pages) ✅

Total: Only the domain cost!

---

Need help? Check:
- GitHub Pages Documentation: [docs.github.com/pages](https://docs.github.com/en/pages)
- Your repository Issues tab for support
