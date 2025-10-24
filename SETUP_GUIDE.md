# 🚀 GitHub Pages Setup Guide - Göinge Bil Facebook Feed

## Total Time: 10-15 minutes

---

## ✅ Prerequisites

- A GitHub account (free) - Create at https://github.com/signup if you don't have one
- That's it! No coding knowledge needed.

---

## 📋 Step-by-Step Instructions

### Step 1: Create GitHub Repository (2 minutes)

1. Go to https://github.com/new
2. Repository name: `goingebil-facebook-feed`
3. Description: `Facebook Dynamic Ads feed for Göinge Bil vehicles`
4. Select: **Public**
5. ✅ Check "Add a README file"
6. Click **"Create repository"**

---

### Step 2: Upload Files (3 minutes)

1. On your repository page, click **"Add file"** → **"Upload files"**

2. Upload these 4 files (drag and drop):
   ```
   .github/workflows/update-feed.yml
   generate-feed.js
   package.json
   .gitignore
   ```

3. Scroll down and click **"Commit changes"**

---

### Step 3: Enable GitHub Actions (1 minute)

1. Go to the **"Actions"** tab in your repository
2. If you see a message about workflows, click **"I understand my workflows, go ahead and enable them"**
3. Click on **"Update Facebook Feed"** workflow
4. Click **"Run workflow"** → **"Run workflow"** (green button)
5. Wait 30-60 seconds for it to complete (you'll see a green checkmark ✅)

---

### Step 4: Enable GitHub Pages (2 minutes)

1. Go to **"Settings"** tab in your repository
2. Scroll down to **"Pages"** in the left sidebar
3. Under "Build and deployment":
   - **Source**: Deploy from a branch
   - **Branch**: Select `gh-pages` and `/root`
4. Click **"Save"**

5. Wait 1-2 minutes, then refresh the page
6. You'll see a box at the top with your URL:
   ```
   Your site is live at https://USERNAME.github.io/goingebil-facebook-feed/
   ```

---

### Step 5: Get Your Feed URL (1 minute)

Your Facebook feed URL is:

```
https://USERNAME.github.io/goingebil-facebook-feed/feed.xml
```

**Replace `USERNAME` with your actual GitHub username**

Example:
```
https://johndoe.github.io/goingebil-facebook-feed/feed.xml
```

---

### Step 6: Test Your Feed (1 minute)

1. Open your feed URL in a browser
2. You should see XML that starts with:
   ```xml
   <?xml version="1.0" encoding="UTF-8"?>
   <listings>
     <title>Göinge Bil - Begagnade Bilar</title>
   ```
3. If you see vehicles = ✅ SUCCESS!

---

### Step 7: Add to Facebook (5 minutes)

1. Go to [Facebook Commerce Manager](https://business.facebook.com/commerce/)
2. Click **"Create Catalog"**
3. Select **"Vehicles"**
4. Name: `Göinge Bil Inventory`
5. Click **"Create"**

6. Go to **"Data Sources"** → **"Add Items"** → **"Data Feed"**
7. Choose **"Scheduled Feed"**
8. **Feed URL**: Paste your GitHub Pages URL:
   ```
   https://USERNAME.github.io/goingebil-facebook-feed/feed.xml
   ```
9. **Upload frequency**: Every 1 hour
10. **Currency**: SEK
11. Click **"Upload"**

---

## ✅ You're Done!

Your feed is now:
- ✅ Live at your GitHub Pages URL
- ✅ Updating automatically every hour
- ✅ Connected to Facebook
- ✅ 100% free forever

---

## 🔄 How It Works

```
Every hour:
GitHub Actions → Fetches from Wayke API → Generates XML → Updates GitHub Pages → Facebook reads it
```

---

## 📊 Monitoring

### Check if feed is updating:

1. Go to your repository
2. Click **"Actions"** tab
3. See recent workflow runs (should be green ✅)

### View your feed status page:

Visit: `https://USERNAME.github.io/goingebil-facebook-feed/`

This page shows:
- Your feed URL
- Last update time
- Number of vehicles
- Status

---

## 🛠️ Troubleshooting

### Feed not updating?

1. Go to **Actions** tab
2. Check if workflow runs are succeeding (green ✅)
3. If red ❌, click on it to see the error

### Facebook says "invalid feed"?

1. Open your feed URL in browser
2. Make sure you see XML with `<listings>`
3. Wait 5 minutes and try again in Facebook

### Workflow not running?

1. Go to **Actions** → **Update Facebook Feed**
2. Click **"Enable workflow"** if you see that button
3. Click **"Run workflow"** manually

---

## 🔧 Advanced

### Change update frequency

Edit `.github/workflows/update-feed.yml`:

```yaml
# Every hour
- cron: '0 * * * *'

# Every 30 minutes
- cron: '*/30 * * * *'

# Every 6 hours
- cron: '0 */6 * * *'
```

### Manual update

1. Go to **Actions** → **Update Facebook Feed**
2. Click **"Run workflow"** → **"Run workflow"**

---

## 💰 Cost

**$0 forever**

GitHub provides:
- ✅ Free GitHub Actions (2,000 minutes/month - you use ~1 minute/day)
- ✅ Free GitHub Pages (100GB bandwidth/month)
- ✅ Free hosting

You'll never hit the limits! ✅

---

## 📞 Support

### GitHub Actions not working?
- Check: https://www.githubstatus.com

### Wayke API issues?
- The script will retry next hour automatically

### Facebook feed issues?
- Check Facebook Commerce Manager diagnostics tab

---

## 🎉 Success Checklist

- [ ] Repository created
- [ ] Files uploaded
- [ ] GitHub Actions enabled and running
- [ ] GitHub Pages enabled
- [ ] Feed URL accessible (shows XML)
- [ ] Feed added to Facebook Commerce Manager
- [ ] First ad campaign created

---

**Congratulations! Your feed is live and updating automatically!** 🚗💨

---

## 📱 Next Steps

1. Install Meta Pixel on goingebil.se
2. Create your first Dynamic Ads campaign
3. Set up product sets (Electric cars, SUVs, etc.)
4. Monitor performance in Facebook Ads Manager

See the main README for detailed Facebook ad setup instructions.
