# Champions CA – Cricket Academy Website (Demo)

Static, no-build website: HTML + Tailwind (CDN) + vanilla JavaScript.

## Structure
- `index.html` – page markup, SEO tags, structured data
- `css/style.css` – custom styles (navy / green / gold theme)
- `js/app.js` – content data, forms + validation, admin dashboard (`#admin`)
- `js/photos.js` – photo slots (`IMG` object), gallery, lightbox
- `images/` – put your photos here
- `netlify.toml` – Netlify config

## Configure the academy
Edit `js/config.js`: WhatsApp number, phone, email, address, `mapQuery` (shows Google Map), social links, `isDemo`.

## Forms
Admission and contact forms post to Netlify Forms (enable under Site settings > Forms; enquiries appear in the Netlify dashboard). If sending fails, visitors get a WhatsApp fallback. Admin dashboard data is demo data stored in the browser only.

## Add real photos
Easiest: follow `images/README.md` (file names) and set `photosReady:true`. Or fill the `IMG` object in `js/photos.js`:
```js
IMG.hero = "images/hero.jpg";
IMG.p0 = "images/beginner.jpg"; // programs p0–p8
IMG.c0 = "images/coach1.jpg";   // coaches c0–c2
IMG.f0 = "images/ground.jpg";   // facilities f0–f6
IMG.g0 = "images/gallery1.jpg"; // gallery g0–g9
```

## Replace placeholders
- WhatsApp number `910000000000` (search in `index.html`, `js/app.js`, `js/photos.js`)
- Phone, email, address, Instagram/Facebook links, Google Maps embed
- Demo stats, coaches, achievements, testimonials and fees – only publish verified data
- Structured data (`index.html`): add address and phone once confirmed

## Run / deploy
Open `index.html` in a browser, or drag the folder to Netlify. Admin demo: `index.html#admin`.
