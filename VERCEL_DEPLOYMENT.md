# Deploy to Vercel - Simple Steps

## Quick Deployment (5 minutes):

### Step 1: Sign Up on Vercel
1. Go to [vercel.com](https://vercel.com)
2. Click **Sign Up**
3. Choose **Continue with GitHub**
4. Login with your GitHub account: **mohidasmat**
5. Authorize Vercel to access your GitHub

### Step 2: Import Your Project
1. After login, click **Add New** → **Project**
2. Vercel will show your GitHub repositories
3. Find **portfolio** repository
4. Click **Import**

### Step 3: Configure & Deploy
1. **Project Name**: Keep it as `portfolio` (or change to `mohid-portfolio`)
2. **Framework Preset**: Leave as `Other` (it's just HTML)
3. **Root Directory**: `./` (leave default)
4. **Build Settings**: Leave empty (no build needed)
5. Click **Deploy** button

⏳ Wait 30 seconds...

🎉 **Your site is LIVE!** at: `https://portfolio-xyz.vercel.app`

### Step 4: Add Custom Domain (mohid.tech)
1. After deployment, click **View Project**
2. Go to **Settings** → **Domains**
3. Add domain: `mohid.tech`
4. Vercel will show you DNS records to add

**Configure DNS at your domain registrar:**
- **Type**: A Record or CNAME
- Vercel will tell you exactly what to add
- Usually: CNAME → `cname.vercel-dns.com`

### Step 5: Add www subdomain (optional)
1. Also add: `www.mohid.tech`
2. Follow same DNS instructions

---

## Even Faster: Use Vercel CLI (Optional)

If you want to deploy from terminal:

```powershell
# Install Vercel CLI
npm install -g vercel

# Login
vercel login

# Deploy
vercel

# Add domain
vercel domains add mohid.tech
```

---

## Summary:
✅ **Free hosting forever**
✅ **Automatic HTTPS**
✅ **Custom domain included**
✅ **Auto-deploy on git push**
✅ **Takes 2 minutes**

**Start here**: [vercel.com/new](https://vercel.com/new)
