# LinguaFlow Landing Page

Static landing page for lingua-flow.app hosted on Cloudflare Pages.

## Structure

```
landing/
├── index.html          # Main landing page
├── privacy.html        # Privacy Policy
├── terms.html          # Terms of Service
├── images/
│   ├── logo.png        # App logo (add your logo)
│   ├── favicon.png     # Favicon
│   ├── phone-mockup.png # App screenshot mockup
│   ├── og-image.png    # Open Graph image (1200x630)
│   └── apple-touch-icon.png
└── _redirects          # Cloudflare redirects (optional)
```

## Required Images

Before deploying, add these images to the `images/` folder:

1. **logo.png** - Your app logo (recommended: 200x200px)
2. **favicon.png** - Favicon (32x32 or 16x16)
3. **phone-mockup.png** - Screenshot of app in phone frame
4. **og-image.png** - Social sharing image (1200x630px)
5. **apple-touch-icon.png** - iOS home screen icon (180x180)

## Deploying to Cloudflare Pages

### Option 1: Direct Upload (Easiest)

1. Go to [Cloudflare Dashboard](https://dash.cloudflare.com)
2. Navigate to **Workers & Pages** > **Pages**
3. Click **Create a project** > **Direct Upload**
4. Drag and drop the `landing` folder
5. Set project name (e.g., `linguaflow-landing`)
6. Deploy!

### Option 2: Connect Git Repository

1. Push this folder to a separate GitHub repo (or use a monorepo)
2. Go to Cloudflare Pages > Create a project
3. Connect your GitHub account
4. Select the repository
5. Build settings:
   - Build command: (leave empty - static HTML)
   - Build output directory: `/` or `/landing`
6. Deploy!

## Custom Domain Setup

1. In Cloudflare Pages, go to your project
2. Click **Custom domains** tab
3. Click **Set up a custom domain**
4. Enter `lingua-flow.app`
5. Cloudflare will automatically configure DNS

## Updating App Store Links

Edit `index.html` and update the store button links:

```html
<!-- Find these lines and add your actual store URLs -->
<a href="https://play.google.com/store/apps/details?id=com.linguaflow.app" class="store-btn" id="playstore-btn">
<a href="https://apps.apple.com/app/linguaflow/id123456789" class="store-btn" id="appstore-btn">
```

## Apple Sign-In Domain Verification

For Apple Sign-In to work on this domain:

1. Create file: `/.well-known/apple-developer-domain-association.txt`
2. Add the verification content from Apple Developer Console
3. Redeploy

## Contact

- Privacy inquiries: privacy@lingua-flow.app
- Legal inquiries: legal@lingua-flow.app
