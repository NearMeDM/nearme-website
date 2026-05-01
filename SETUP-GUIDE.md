# NearMe Blog — Complete Setup Guide
## Netlify CMS + GitHub → Easy Blog Publishing

---

## What You Get After Setup

- ✅ Blog live at: `https://nearmedigitalagency.com/blog/`
- ✅ CMS admin at: `https://nearmedigitalagency.com/admin/`
- ✅ Write posts in a beautiful editor (no coding needed)
- ✅ Posts auto-save to GitHub
- ✅ Site updates live instantly on Netlify
- ✅ 100% free — GitHub + Netlify free tier

---

## Step 1 — Create a GitHub Account (if you don't have one)

1. Go to **github.com**
2. Click **Sign up** → enter email, password, username
3. Verify your email

---

## Step 2 — Create a New GitHub Repository

1. Go to **github.com/new**
2. Repository name: `nearme-website`
3. Select **Public** (required for free Netlify)
4. Click **Create repository**

---

## Step 3 — Upload All Your Files to GitHub

Upload ALL these files and folders to the repository:

```
nearme-website/
├── index.html              ← Main website
├── nearme-logo.png         ← Logo
├── partha-photo.jpg        ← Your photo
├── netlify.toml            ← Netlify config
├── _redirects              ← URL redirects
├── admin/
│   ├── index.html          ← CMS login page
│   └── config.yml          ← CMS configuration
├── blog/
│   ├── index.html          ← Blog listing page
│   ├── post-template.html  ← Post template
│   └── _posts/
│       ├── README.md
│       └── 2025-04-15-how-to-rank-1-google-maps-kaliyaganj.md
└── images/
    └── uploads/            ← Create this empty folder
```

**To upload:**
1. Open your repository on GitHub
2. Click **Add file → Upload files**
3. Drag all files in
4. Click **Commit changes**

---

## Step 4 — Deploy on Netlify

1. Go to **app.netlify.com** → Sign up with your GitHub account
2. Click **Add new site → Import an existing project**
3. Choose **GitHub** → Select `nearme-website`
4. Build settings:
   - Build command: *(leave empty)*
   - Publish directory: `.`
5. Click **Deploy site**

Your site will be live in ~1 minute at a random URL like `amazing-pasteur-xyz.netlify.app`

### Set Your Custom Domain

1. In Netlify → **Domain settings → Add custom domain**
2. Enter: `nearmedigitalagency.com`
3. Follow the DNS instructions to point your domain to Netlify
4. Enable **HTTPS** (free, automatic with Let's Encrypt)

---

## Step 5 — Enable Netlify Identity (for CMS login)

1. In Netlify → **Site configuration → Identity → Enable Identity**
2. Under **Registration** → Change to **Invite only**
   *(This means only you can log in — no public signups)*
3. Under **Git Gateway** → Click **Enable Git Gateway**

---

## Step 6 — Invite Yourself as CMS User

1. Netlify → **Identity → Invite users**
2. Enter your email → Send invite
3. Check your email → Click the confirmation link
4. Set your password

---

## Step 7 — Log In to Your Blog CMS

1. Go to: `https://nearmedigitalagency.com/admin/`
2. Click **Login with Netlify Identity**
3. Enter your email and password
4. You're in! 🎉

---

## How to Write a New Blog Post

1. Go to `/admin/`
2. Click **Blog Posts → New Blog Post**
3. Fill in:
   - **Title** (under 60 characters)
   - **Description** (150-160 characters — this shows in Google)
   - **Category** (select from dropdown)
   - **Content** (write in the rich text editor)
4. Click **Save** (saves as Draft)
5. When ready → Click **Set status → Ready → Publish**

The post appears live on your blog within seconds.

---

## Folder Structure After First Post

When you publish a post titled "How to Get More Customers", Netlify CMS creates:

```
blog/_posts/2025-04-20-how-to-get-more-customers.md
```

This Markdown file contains all your content. You can also edit it directly on GitHub if needed.

---

## Important Notes

### About the Post Template
The `blog/post-template.html` file is a **manual template** for now.
When you publish posts via CMS, they are saved as `.md` files.

**To display them as HTML pages**, you have two options:

**Option A (Recommended — Simple):**
For each new post, duplicate `post-template.html`, rename it to match the slug, and paste in your content. Example:
- Duplicate → `blog/how-to-get-more-customers.html`
- Replace all `{{PLACEHOLDER}}` text with your actual content

**Option B (Advanced — Fully Automatic):**
Use a static site generator like **Eleventy (11ty)** to auto-convert `.md` files to `.html`:
```bash
npm install -g @11ty/eleventy
eleventy --serve
```
This requires some initial setup but makes publishing fully automatic.

---

## Keeping Posts Updated

Your blog posts are stored as Markdown files in GitHub. You can:
- Edit via Netlify CMS admin panel (easiest)
- Edit directly on GitHub (click the file → pencil icon)
- Edit locally if you use GitHub Desktop app

---

## Getting Help

Contact Partha: +91 7001 069 520 (WhatsApp)
Or email through the website contact form.

---

*Setup guide created by NearMe Digital Marketing Agency, Kaliyaganj*
