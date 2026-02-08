# Netlify Environment Variables Setup

## ⚠️ Important: Netlify doesn't use .env files!

Netlify builds from your GitHub repository, but **it doesn't have access to your local `.env` files**. You must set environment variables in the Netlify dashboard.

## 🔧 Step-by-Step Setup

### Step 1: Go to Netlify Dashboard

1. Log in to [Netlify](https://app.netlify.com)
2. Select your site
3. Go to **Site settings** → **Environment variables**

### Step 2: Add Required Environment Variables

Click **"Add a variable"** and add each of these:

#### Required Supabase Variables:

```
VITE_SUPABASE_URL = https://gtzbjzsjeftkgwvvgefp.supabase.co
```

```
VITE_SUPABASE_ANON_KEY = eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6Imd0emJqenNqZWZ0a2d3dnZnZWZwIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NTY5OTU3ODIsImV4cCI6MjA3MjU3MTc4Mn0.wRqsArrjXE1AIgMtXaqvzKTOkdQULCYntq8N3c_rYik
```

```
VITE_SUPABASE_PUBLISHABLE_KEY = sb_publishable_VUJBiFw6N4Kfeh1gCRoXZQ_-stK7oOf
```

#### Optional (if needed):

```
VITE_APP_ENV = production
```

```
VITE_APP_URL = http://dcodesystems.infinityfree.me
```

```
VITE_BACKEND_URL = http://dcodesystems.infinityfree.me
```

### Step 3: Trigger a New Build

After adding the environment variables:

1. Go to **Deploys** tab
2. Click **"Trigger deploy"** → **"Clear cache and deploy site"**
3. Wait for the build to complete

### Step 4: Verify

After deployment, check your site's browser console. You should see:

```
🔧 Supabase Configuration:
URL: https://gtzbjzsjeftkgwvvgefp.supabase.co
Key: eyJhbGciOiJIUzI1NiIs...
Environment: production
✅ Supabase client created successfully
```

## 📝 Quick Copy-Paste Values

Copy these exact values into Netlify:

**VITE_SUPABASE_URL:**
```
https://gtzbjzsjeftkgwvvgefp.supabase.co
```

**VITE_SUPABASE_ANON_KEY:**
```
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6Imd0emJqenNqZWZ0a2d3dnZnZWZwIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NTY5OTU3ODIsImV4cCI6MjA3MjU3MTc4Mn0.wRqsArrjXE1AIgMtXaqvzKTOkdQULCYntq8N3c_rYik
```

**VITE_SUPABASE_PUBLISHABLE_KEY:**
```
sb_publishable_VUJBiFw6N4Kfeh1gCRoXZQ_-stK7oOf
```

## 🔍 Troubleshooting

### Still seeing old URL?

1. **Clear Netlify build cache**: Deploys → Trigger deploy → Clear cache and deploy site
2. **Check environment variables**: Make sure they're set for "Production" scope
3. **Verify variable names**: Must start with `VITE_` (not `REACT_APP_`)
4. **Check build logs**: Look for any errors about missing environment variables

### Build failing?

- Make sure all required `VITE_*` variables are set
- Check that variable names match exactly (case-sensitive)
- Verify no extra spaces in variable values

