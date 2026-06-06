# Crossmember Media LLC — Website

## Deploy to Netlify

### Option A — Drag & Drop (no account needed to test)
1. Run `npm install` then `npm run build` locally
2. Drag the `dist/` folder to **netlify.com/drop**
3. Done — live in 30 seconds

### Option B — GitHub + Netlify (recommended for ongoing updates)

1. **Create a GitHub repo**
   - Go to github.com → New repository → name it `crossmember-media`
   - Don't initialise with a README

2. **Push this folder to GitHub**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/YOUR_USERNAME/crossmember-media.git
   git push -u origin main
   ```

3. **Connect to Netlify**
   - Go to app.netlify.com → Add new site → Import from Git
   - Select your GitHub repo
   - Build command: `npm run build`
   - Publish directory: `dist`
   - Click Deploy

4. **Add your custom domain**
   - In Netlify: Site Settings → Domain Management → Add custom domain
   - Buy your domain at **cloudflare.com/registrar** (~$10/year)
   - In Cloudflare: set nameservers to the ones Netlify gives you
   - SSL certificate provisions automatically (free)

### Local development
```bash
npm install
npm run dev
```
Opens at http://localhost:5173

## Files
- `src/App.jsx` — the full website
- `netlify.toml` — build config and redirect rules
- `public/favicon.svg` — browser tab icon
