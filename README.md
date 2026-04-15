# FitLabX Website

**fitlabx.co** — Science · Precision · Method

Online fitness coaching website for Coach Kobey Silver.

## Project Structure

```
fitlabx-site/
├── public/
│   ├── index.html        # Main site (single page)
│   ├── logo-red.png      # Primary logo (red/white on black)
│   └── logo-blue.png     # Alternate logo (blue/white on black)
├── vercel.json           # Vercel deployment config
├── package.json
└── README.md
```

## Local Development

```bash
npx serve public
```

Then open http://localhost:3000

## Deployment (Vercel)

1. Push this repo to GitHub
2. Go to vercel.com → New Project → Import from GitHub
3. Deploy — no build settings needed, it's static HTML

## TODO: Before Go-Live

### 1. Stripe Payment Links
Replace the placeholder `href="#contact"` on the three service buttons with Stripe Payment Links:
- **Starter Plan**: $140 one-time → `data-plan="starter"`
- **1-on-1 Coaching**: $200/mo recurring → `data-plan="coaching"`
- **Couples Coaching**: $350/mo recurring → `data-plan="couples"`

### 2. Contact Form
The form setup must be completed manually at [formspree.io](https://formspree.io):
1. Sign up at formspree.io
2. Create a new form pointed at kobey.silver@gmail.com
3. Replace `<!-- REPLACE WITH FORMSPREE FORM ID -->` in `public/index.html`

### 3. Domain (fitlabx.co)
- Change Wix nameservers to Cloudflare
- Add fitlabx.co as custom domain in Vercel
- Add CNAME record in Cloudflare pointing to Vercel

### 4. Social Media Links
Replace `#` in footer social links with actual URLs:
- Instagram: `https://instagram.com/USERNAME`
- Facebook: `https://facebook.com/USERNAME`

### 5. Coach Photo
Replace the placeholder in the About section with Kobey's photo:
- Add photo as `public/coach-photo.jpg`
- In index.html, replace the `.about-placeholder` div with:
  `<img src="/coach-photo.jpg" alt="Coach Kobey Silver">`
