# 🚀 GitHub Pages Setup Instructions

## 📋 Langkah-langkah Deploy

### 1. Build APK
```bash
# Build aplikasi
cordova build android

# Atau gunakan script otomatis
./deploy.sh
```

### 2. Setup GitHub Repository
```bash
# Jika belum ada repository
git init
git add .
git commit -m "Initial commit"

# Add remote (ganti dengan username Anda)
git remote add origin https://github.com/armanwiranda/dailyflow.git
git push -u origin main
```

### 3. Enable GitHub Pages
1. Buka repository GitHub Anda
2. Go to **Settings** → **Pages**
3. **Source**: Deploy from a branch
4. **Branch**: `main` → `/ (root)`
5. Click **Save**

### 4. Deploy Website
```bash
# Gunakan deployment script
./deploy.sh

# Atau manual:
cordova build android
cp platforms/android/app/build/outputs/apk/debug/app-debug.apk website/dailyflow.apk
git add website/
git commit -m "Update APK and website"
git push origin main
```

## 🌐 URL Setelah Deploy

- **Website**: `https://[username].github.io/dailyflow`
- **APK Download**: `https://[username].github.io/dailyflow/dailyflow.apk`
- **Repository**: `https://github.com/[username]/dailyflow`

## 📱 Cara Update APK

### Cara 1: Otomatis (Recommended)
```bash
./deploy.sh
```

### Cara 2: Manual
```bash
# 1. Build APK baru
cordova build android

# 2. Copy ke website folder
cp platforms/android/app/build/outputs/apk/debug/app-debug.apk website/dailyflow.apk

# 3. Commit dan push
git add website/dailyflow.apk
git commit -m "Update APK to version [version]"
git push origin main
```

## 🔧 Konfigurasi

### Update Username di Website
Edit `website/index.html`:
```html
<!-- Ganti dengan username GitHub Anda -->
<meta property="og:image" content="https://[username].github.io/dailyflow/assets/app-icon.png">
<a href="https://github.com/[username]/dailyflow/releases/latest/download/dailyflow.apk" class="download-btn">
<a href="https://github.com/[username]/dailyflow" class="download-btn">
```

### Update Email
```html
<a href="mailto:your-email@example.com">Contact</a>
```

## 📊 Fitur Website

### ✅ Sudah Tersedia:
- 🎨 Modern, responsive design
- 📱 Mobile-optimized
- 🌐 SEO friendly
- ⬇️ Direct APK download
- 📊 Feature showcase
- 🔍 Smooth animations
- 📧 Contact information

### 🔧 Customization:
- 🎨 Brand colors (CSS variables)
- 📝 Custom content
- 🖼️ Logo dan assets
- 📊 Analytics integration
- 🌐 Custom domain

## 🎯 Tips & Tricks

### 1. APK Size Management
```bash
# Check APK size
ls -lh website/dailyflow.apk

# Optimize APK size
cordova build android --release
# atau gunakan ProGuard untuk production
```

### 2. Version Management
```bash
# Update version di config.xml
# Script otomatis akan membaca version

# Check current version
grep 'version="' config.xml
```

### 3. Custom Domain (Optional)
```bash
# Create CNAME file
echo "yourdomain.com" > website/CNAME

# Add to git
git add website/CNAME
git commit -m "Add custom domain"
git push origin main
```

### 4. Analytics (Optional)
```html
<!-- Tambahkan ke <head> di index.html -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_TRACKING_ID"></script>
```

## 🚀 Advanced Deployment

### GitHub Actions (Otomatisasi)
```yaml
# .github/workflows/deploy.yml
name: Deploy to GitHub Pages
on:
  push:
    branches: [ main ]
jobs:
  deploy:
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
    - name: Deploy to GitHub Pages
      uses: peaceiris/actions-gh-pages@v3
      with:
        github_token: ${{ secrets.GITHUB_TOKEN }}
        publish_dir: ./website
```

## 📱 Testing

### Test Website:
1. Buka `https://[username].github.io/dailyflow`
2. Test semua links
3. Test download functionality
4. Test di mobile devices

### Test APK:
1. Download APK dari website
2. Install di Android device
3. Test semua fitur aplikasi

## 🔍 Troubleshooting

### Common Issues:
1. **APK tidak terdownload**: Check file size (<100MB)
2. **Website tidak muncul**: Tunggu 5-10 menit setelah deploy
3. **Links broken**: Check GitHub username di HTML
4. **APK corrupted**: Rebuild dan re-upload

### Commands:
```bash
# Check GitHub Pages status
curl -I https://[username].github.io/dailyflow

# Check APK accessibility
curl -I https://[username].github.io/dailyflow/dailyflow.apk

# Check git status
git status
git log --oneline -n 5
```

## 📞 Support

Jika ada masalah:
1. Check GitHub Pages documentation
2. Verify file paths dan permissions
3. Test dengan manual deployment
4. Check console untuk JavaScript errors

---

**Selamat deploy!** 🎉 Website Anda akan live di GitHub Pages dalam 5-10 menit setelah push.
