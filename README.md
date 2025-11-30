# DailyFlow - GitHub Pages Setup

## 📱 Aplikasi DailyFlow

DailyFlow adalah aplikasi produktivitas untuk mengelola tugas harian dan membangun kebiasaan baik. Dibangun dengan Cordova untuk Android.

## 🚀 Cara Deploy ke GitHub Pages

### 1. Build APK
```bash
# Build aplikasi
cordova build android

# Copy APK ke folder website
cp platforms/android/app/build/outputs/apk/debug/app-debug.apk website/dailyflow.apk
```

### 2. Setup GitHub Repository
```bash
# Initialize git repository
git init
git add .
git commit -m "Initial commit"

# Add remote repository
git remote add origin https://github.com/armanwiranda/dailyflow.git
git push -u origin main
```

### 3. Enable GitHub Pages
1. Go to repository settings
2. Scroll to "GitHub Pages" section
3. Source: Deploy from a branch
4. Branch: `gh-pages` (or `main`)
5. Folder: `/ (root)` or `/docs`

### 4. Automatic Deployment (Optional)
```bash
# Create gh-pages branch
git checkout --orphan gh-pages
git rm -rf .
cp -r website/* .
git add .
git commit -m "Deploy to GitHub Pages"
git push origin gh-pages
```

## 📁 Struktur Folder

```
DailyFlow/
├── website/
│   ├── index.html          # Landing page
│   ├── assets/             # Assets untuk website
│   └── dailyflow.apk       # APK file untuk download
├── www/                    # Cordova app source
├── platforms/              # Platform-specific files
├── config.xml              # Cordova configuration
└── README.md               # This file
```

## 🔧 Konfigurasi Website

### Update Links di `website/index.html`:
```html
<!-- Update dengan GitHub username Anda -->
<meta property="og:image" content="https://armanwiranda.github.io/dailyflow/assets/app-icon.png">

<!-- Update download link -->
<a href="https://github.com/armanwiranda/dailyflow/releases/latest/download/dailyflow.apk">

<!-- Update GitHub link -->
<a href="https://github.com/armanwiranda/dailyflow">
```

### Update Contact Info:
```html
<a href="mailto:your-email@example.com">Contact</a>
```

## 📦 Cara Update APK

### Manual Update:
1. Build new APK: `cordova build android`
2. Copy APK: `cp platforms/android/app/build/outputs/apk/debug/app-debug.apk website/dailyflow.apk`
3. Commit changes: `git add website/dailyflow.apk && git commit -m "Update APK"`
4. Push to GitHub: `git push origin main`

### GitHub Actions (Advanced):
```yaml
# .github/workflows/deploy.yml
name: Deploy APK
on:
  push:
    branches: [ main ]
jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v2
    - name: Setup Node.js
      uses: actions/setup-node@v2
      with:
        node-version: '16'
    - name: Setup Cordova
      run: |
        npm install -g cordova
        npm install
    - name: Build APK
      run: cordova build android
    - name: Copy APK
      run: cp platforms/android/app/build/outputs/apk/debug/app-debug.apk website/dailyflow.apk
    - name: Deploy to GitHub Pages
      uses: peaceiris/actions-gh-pages@v3
      with:
        github_token: ${{ secrets.GITHUB_TOKEN }}
        publish_dir: ./website
```

## 🎨 Customisasi Website

### Update Colors:
```css
:root {
    --primary-color: #007aff;      /* Ganti dengan brand color */
    --secondary-color: #5856d6;    /* Ganti dengan secondary color */
    --accent-color: #ff3b30;       /* Ganti dengan accent color */
}
```

### Update Features:
Edit section `.features-grid` di `index.html` untuk menambahkan atau mengubah fitur.

### Update Logo:
Replace `assets/app-icon.png` dengan logo aplikasi Anda (512x512px).

## 🌐 Domain Custom (Optional)

### Option 1: GitHub Pages Custom Domain
1. Go to repository settings
2. GitHub Pages section
3. Custom domain: `yourdomain.com`
4. Create CNAME file: `echo "yourdomain.com" > website/CNAME`

### Option 2: External DNS
1. A record: `185.199.108.153` (GitHub Pages)
2. CNAME: `armanwiranda.github.io` (if using subdomain)

## 📊 Analytics (Optional)

### Google Analytics:
```html
<!-- Add to <head> section -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_TRACKING_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_TRACKING_ID');
</script>
```

### Download Tracking:
```javascript
// Update download button event listener
document.getElementById('android-download').addEventListener('click', function(e) {
    gtag('event', 'download', {
        'event_category': 'engagement',
        'event_label': 'APK Download'
    });
});
```

## 🔒 HTTPS & Security

GitHub Pages otomatis menyediakan:
- ✅ HTTPS certificate
- ✅ CDN distribution
- ✅ DDoS protection
- ✅ Fast loading globally

## 📱 Mobile Optimization

Website sudah dioptimalkan untuk:
- ✅ Responsive design
- ✅ Touch-friendly buttons
- ✅ Fast loading
- ✅ SEO friendly

## 🚀 Launch Checklist

- [ ] Build APK dan copy ke website folder
- [ ] Update links dengan GitHub username
- [ ] Test semua links di website
- [ ] Enable GitHub Pages
- [ ] Test download functionality
- [ ] Setup custom domain (optional)
- [ ] Add analytics (optional)
- [ ] Test di mobile devices

## 📞 Support

Jika ada masalah dengan deployment:
1. Check GitHub Pages documentation
2. Verify APK file size (< 100MB untuk GitHub)
3. Test semua links
4. Check console untuk JavaScript errors

---

**URL Website:** `https://armanwiranda.github.io/dailyflow`  
**APK Download:** `https://armanwiranda.github.io/dailyflow/dailyflow.apk`  
**Repository:** `https://github.com/armanwiranda/dailyflow`
