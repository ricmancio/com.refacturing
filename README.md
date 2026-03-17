# refacturing.com

Personal portfolio site for Riccardo Mancinelli — Freelance Software Engineer & Consultant.

Built with [Astro](https://astro.build), deployed on GitHub Pages.

## Quick Start

```bash
npm install
npm run dev
```

Open `http://localhost:4321` to preview.

## Deploy to GitHub Pages

1. Create a repo on GitHub (e.g. `ricmancio/refacturing-site`)
2. Push the code:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin git@github.com:ricmancio/refacturing-site.git
   git push -u origin main
   ```
3. Go to **Settings > Pages** in your GitHub repo
4. Under **Source**, select **GitHub Actions**
5. The included `.github/workflows/deploy.yml` will build and deploy automatically on each push

### Custom Domain (refacturing.com)

1. In **Settings > Pages > Custom domain**, enter `www.refacturing.com`
2. Add these DNS records at your domain registrar:
   - `A` record for `@` pointing to GitHub Pages IPs:
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`
   - `CNAME` record for `www` pointing to `ricmancio.github.io`
3. Create a `public/CNAME` file containing `www.refacturing.com`
4. Update `astro.config.mjs`:
   ```js
   export default defineConfig({
     site: 'https://www.refacturing.com',
     // remove base
   });
   ```

## Project Structure

```
src/
├── components/
│   ├── Navbar.astro
│   ├── Hero.astro
│   ├── About.astro
│   ├── Projects.astro
│   ├── Experience.astro
│   ├── Contact.astro
│   └── Footer.astro
├── layouts/
│   └── Layout.astro
├── pages/
│   └── index.astro
└── styles/
    └── global.css
```
