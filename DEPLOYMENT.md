# Deployment to Vercel

## Step 1: Create GitHub Repository

Since I can't create a repository with the current GitHub token permissions, please create one manually:

1. Go to https://github.com/new
2. Repository name: `laravel-school-timetable`
3. Select "Private"
4. Click "Create repository"

## Step 2: Push Code to GitHub

Run these commands in your terminal:

```bash
# Navigate to the project folder
cd /path/to/laravel-school-timetable

# Add your new GitHub repo as remote
git remote add origin https://github.com/YOUR_USERNAME/laravel-school-timetable.git

# Push to GitHub
git push -u origin master
```

## Step 3: Deploy on Vercel

1. Go to https://vercel.com
2. Sign up with GitHub
3. Click "Add New..." → "Project"
4. Import your `laravel-school-timetable` repository
5. Vercel will auto-detect PHP and run composer install

## Step 4: Configure Environment Variables

In Vercel Dashboard → Project → Settings → Environment Variables:

```
APP_KEY=base64:dGhpcyBpcyBhIHBsYWNlaG9sZGVyIGtleSB0aGF0IG5lZWRzIHRvIGJlIHJlZ2VuZXJhdGVk
DB_HOST=localhost
DB_PORT=3306
DB_DATABASE=if0_41878253_school
DB_USERNAME=if0_41878253
DB_PASSWORD=trB41CKa58
```

## Step 5: Create MySQL Database

Since Vercel doesn't include MySQL, you have options:

### Option A: Use InfinityFree MySQL (already configured)
- Keep using your InfinityFree database
- DB_HOST should remain localhost or the InfinityFree MySQL host

### Option B: Use Vercel Postgres (paid)
- Add Vercel Postgres as an add-on

### Option C: Use PlanetScale/Neon (free tiers)
- Sign up for free MySQL hosting

## Your App URL
After deployment: `https://laravel-school-timetable.vercel.app`