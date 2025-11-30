# Figma Mockup Guide untuk DailyFlow Phone Slider

## 📱 Ukuran Mockup yang Diperlukan

### Phone Frame (Background Layer)
- **Width**: 280px
- **Height**: 580px
- **Radius**: 40px (2.5rem)
- **Background**: Linear gradient 145deg, #1a1a1a, #2d2d2d
- **Border**: 2px solid rgba(255, 255, 255, 0.1)

### Phone Screen (Content Area)
- **Width**: 264px (280px - 16px padding)
- **Height**: 548px (580px - 32px padding)
- **Radius**: 32px (2rem)
- **Background**: White #ffffff
- **Position**: Centered dalam phone frame

### Status Bar Area
- **Height**: 24px (1.5rem)
- **Background**: Linear gradient 135deg, #f8f9fa, #e9ecef
- **Radius**: 32px 32px 0 0

### Content Area (untuk desain app)
- **Width**: 256px (264px - 8px padding)
- **Height**: 504px (548px - 24px status bar - 20px padding)
- **Radius**: 16px (1rem)
- **Background**: Sesuai desain app Anda

## 🎨 Desain yang Diperlukan (4 Variasi)

### 1. Dashboard Design
- **File Name**: design1.png
- **Konten**: Dashboard utama dengan task list, progress indicators
- **Style**: Clean, modern dengan card-based layout

### 2. Task List Design  
- **File Name**: design2.png
- **Konten**: Detail task list dengan checkboxes, priorities
- **Style**: Fokus pada interaksi dan usability

### 3. Statistics Design
- **File Name**: design3.png
- **Konten**: Charts, graphs, progress tracking
- **Style**: Data visualization yang menarik

### 4. Profile/Settings Design
- **File Name**: design4.png
- **Konten**: User profile, settings, preferences
- **Style**: Personal dan customizable

## 📐 Export Settings dari Figma

### Format Export
- **Format**: PNG
- **Resolution**: 2x (untuk retina display)
- **Compression**: Medium (balance quality vs file size)
- **Transparency**: No (white background)

### Ukuran Export Akhir
- **Width**: 512px (256px × 2)
- **Height**: 1008px (504px × 2)
- **File Size**: < 200KB per gambar

## 🎯 Tips Desain

### Color Scheme
- **Primary**: #007aff (iOS blue)
- **Secondary**: #5856d6 (Purple)
- **Accent**: #00b4d8 (Cyan)
- **Background**: #f8f9fa (Light gray)
- **Text**: #333333 (Dark gray)

### Typography
- **Headers**: SF Pro Display, Bold, 18-24px
- **Body**: SF Pro Text, Regular, 14-16px
- **Buttons**: SF Pro Text, Semibold, 16px

### Components
- **Buttons**: 8px radius, 44px min height
- **Cards**: 12px radius, 8px padding
- **Icons**: 24px size, consistent style
- **Shadows**: Subtle, 0 2px 8px rgba(0,0,0,0.1)

## 📁 Folder Structure
```
website/img/
├── design1.png (Dashboard)
├── design2.png (Task List)
├── design3.png (Statistics)
└── design4.png (Profile)
```

## 🔧 Setup di Figma

### 1. Buat Frame Utama
```
Frame: 280 × 580px
Radius: 40px
Background: #1a1a1a
```

### 2. Buat Screen Area
```
Frame: 264 × 548px
Radius: 32px
Background: #ffffff
Position: (8, 16)
```

### 3. Status Bar
```
Rectangle: 264 × 24px
Radius: 32px 32px 0 0
Background: Linear gradient #f8f9fa → #e9ecef
Position: (8, 16)
```

### 4. Content Area
```
Frame: 256 × 504px
Radius: 16px
Position: (12, 44)
```

## ✅ Quality Check

Sebelum export, pastikan:
- [ ] Semua text readable (min 12px)
- [ ] Kontras warna cukup (WCAG AA)
- [ ] Tidak ada pixelated images
- [ ] Consistent spacing (8px grid)
- [ ] Proper touch targets (min 44px)
- [ ] Mobile-first design principles

## 🚀 Setelah Export

1. Save ke `website/img/` dengan nama yang benar
2. Test di browser untuk responsive behavior
3. Check file sizes (< 200KB each)
4. Verify semua 4 design terload dengan benar

---

**Happy Designing!** 🎨✨
