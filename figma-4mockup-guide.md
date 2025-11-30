# Figma 4 Mockup Guide untuk DailyFlow (Frame HP Included)

## 📱 Ukuran Mockup untuk Figma

### Full Phone Mockup (Frame HP Included)
- **Width**: 280px
- **Height**: 580px
- **Radius**: 40px (2.5rem)
- **Include**: Phone frame yang sudah dirancang di Figma

### Content Area (Aplikasi)
- **Width**: 240px (280px - 40px frame)
- **Height**: 520px (580px - 60px frame)
- **Radius**: 30px
- **Position**: Centered dalam phone frame

## 🎨 4 Desain Mockup yang Diperlukan

### 1. Dashboard Mockup
- **File Name**: `mockup1.png`
- **Konten**: Dashboard utama DailyFlow
  - Header dengan user profile
  - Task list dengan progress indicators
  - Quick stats untuk hari ini
  - Bottom navigation
- **Style**: Clean, modern dengan card-based layout

### 2. Task List Mockup
- **File Name**: `mockup2.png`
- **Konten**: Detail task management
  - Search bar
  - Filter buttons (All, Active, Completed)
  - Task items dengan checkboxes
  - Add task button
- **Style**: Focus pada usability dan clarity

### 3. Statistics Mockup
- **File Name**: `mockup3.png`
- **Konten**: Analytics dan progress tracking
  - Progress charts
  - Completion statistics
  - Habit streak counter
  - Achievement badges
- **Style**: Data visualization yang menarik

### 4. Profile/Settings Mockup
- **File Name**: `mockup4.png`
- **Konten**: User profile dan preferences
  - User avatar dan info
  - Settings menu
  - Theme preferences
  - About section
- **Style**: Personal dan customizable

## 📐 Export Settings dari Figma

### Format Export
- **Format**: PNG
- **Resolution**: 2x (untuk retina display)
- **Compression**: Medium (balance quality vs file size)
- **Transparency**: No (background frame included)

### Ukuran Export Akhir
- **Width**: 560px (280px × 2)
- **Height**: 1160px (580px × 2)
- **File Size**: < 250KB per gambar

## 🎯 Tips Desain Mockup dengan Frame

### Phone Frame Design
- **Frame Color**: Dark gradient #1a1a1a → #2d2d2d
- **Frame Thickness**: 20px di setiap sisi
- **Notch**: Include realistic phone notch di bagian atas
- **Shadow**: Subtle shadow untuk depth effect
- **Radius**: 40px untuk rounded corners

### Content Positioning
- **Top Margin**: 60px (untuk notch dan status bar)
- **Bottom Margin**: 40px (untuk home indicator)
- **Side Margins**: 20px kiri dan kanan
- **Content Area**: 240 × 520px untuk app content

### Color Scheme
- **Primary**: #007aff (iOS blue)
- **Secondary**: #5856d6 (Purple)
- **Accent**: #00b4d8 (Cyan)
- **Success**: #34c759 (Green)
- **Warning**: #ff9500 (Orange)
- **Background**: #f8f9fa (Light gray)
- **Text**: #333333 (Dark gray)

### Typography
- **Headers**: SF Pro Display, Bold, 18-20px
- **Subheaders**: SF Pro Text, Semibold, 16px
- **Body Text**: SF Pro Text, Regular, 14px
- **Buttons**: SF Pro Text, Semibold, 16px
- **Captions**: SF Pro Text, Regular, 12px

## 🔧 Setup di Figma

### 1. Buat Frame Utama
```
Frame: 280 × 580px
Name: "Mockup 1 - Dashboard"
Radius: 40px
```

### 2. Buat Phone Frame
```
Rectangle: 280 × 580px
Radius: 40px
Background: Linear gradient #1a1a1a → #2d2d2d
Position: (0, 0)
```

### 3. Buat Phone Notch
```
Rectangle: 80 × 28px
Radius: 0 0 20px 20px
Background: Linear gradient #000000 → #1a1a1a
Position: (100, 8)
```

### 4. Buat Screen Area
```
Frame: 240 × 520px
Radius: 30px
Position: (20, 30)
Background: White #ffffff
```

### 5. Desain Content
- Gunakan grid system 8px
- Follow iOS design guidelines
- Include realistic data dan interactions
- Add proper shadows dan depth

## 📁 File Structure

Setelah export, simpan di:
```
website/img/
├── mockup1.png (Dashboard)
├── mockup2.png (Task List)
├── mockup3.png (Statistics)
└── mockup4.png (Profile)
```

## ✅ Quality Check

Sebelum export, pastikan:
- [ ] Semua text readable (min 12px)
- [ ] Kontras warna cukup (WCAG AA)
- [ ] Tidak ada pixelated images
- [ ] Consistent spacing (8px grid)
- [ ] Proper touch targets (min 44px)
- [ ] Phone frame terlihat realistis
- [ ] Content tidak terpotong oleh frame
- [ ] Semua 4 mockup memiliki style yang konsisten

## 🚀 Setelah Export

1. Pastikan semua 4 file ada di folder `website/img/`
2. Test di browser untuk responsive behavior
3. Check file sizes (< 250KB each)
4. Verify semua mockup terload dengan benar
5. Test slider functionality

## 💡 Pro Tips untuk Mockup yang Realistis

### Frame Details
- Add subtle gradient ke phone frame
- Include realistic shadows di edges
- Add camera lens dan speaker grill
- Use proper metallic finish

### Screen Realism
- Include time dan battery indicator
- Add realistic notification badges
- Use actual app content, bukan placeholder
- Include proper status bar dengan carrier info

### Content Consistency
- Gunakan user data yang sama di semua mockup
- Maintain consistent color scheme
- Use same typography style
- Keep navigation elements consistent

### 3D Effect Preparation
- Ensure high resolution untuk smooth scaling
- Add proper shadows untuk depth perception
- Use consistent lighting di semua mockup
- Consider how design looks di 3D rotation

---

**Happy Designing!** 🎨✨

**Result**: 4 realistic phone mockups dengan frame included yang perfect untuk 3D slider!
