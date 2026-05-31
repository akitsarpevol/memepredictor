# MONITORING BERKAS TAGIHAN UTANG PROYEK INFRA 3

## 📊 Interactive Dashboard untuk Monitoring Tagihan Utang Proyek Infrastruktur

Dashboard interaktif yang dirancang khusus untuk memantau, menganalisis, dan mengelola data tagihan utang proyek infrastruktur dengan tampilan profesional dan fitur-fitur canggih.

## ✨ Fitur Utama

### 1. **Header Section**
- Judul dashboard yang jelas dan profesional
- Filter tanggal rentang untuk analisis periode tertentu

### 2. **KPI Scorecards**
- **Saldo Utang**: Total utang dengan format currency yang terformat
- **Jumlah Tagihan**: Jumlah total tagihan/records

### 3. **Global Filters**
Enam filter dropdown interaktif:
1. Nama Vendor
2. Nama Proyek
3. Status Tagihan
4. Keterangan Singkat
5. G/L Account
6. PIC (Person In Charge)

### 4. **Data Tables**

#### Table 1: Data Tagihan (Main Table)
- Row Number
- Nama Vendor
- Nama Proyek
- Status Tagihan
- Tahun Berkas
- Kategori Utang
- Saldo Utang (Sorted: Descending)
- Pagination: 100 rows per page

#### Table 2: Analisis Aging
- Kategori Aging otomatis (Dibawah 1 Tahun, 1 Tahun, 2 Tahun, ... 7 Tahun)
- Saldo Utang per kategori
- Sorted: Descending

#### Table 3: Analisis Keterangan Singkat
- Keterangan Singkat
- Saldo Utang per keterangan
- Sorted: Descending

#### Table 4: Swap Utang Detail
- Filtered view untuk "Swap Utang" entries
- Row Number, Nama Vendor, Status Tagihan, Saldo Utang
- Pagination: 32 rows per page
- Dedicated KPI scorecard menampilkan total Saldo Utang untuk Swap Utang

## 🎨 Design & Styling

### Dark Mode Theme
- **Background**: Dark Charcoal (#1E1E1E)
- **Card Backgrounds**: Slightly lighter gray (#252526)
- **Text**: White untuk primary text, light gray untuk secondary
- **Font**: Roboto/Arial (modern, clean sans-serif)
- **Currency Format**: Indonesian style dengan separator titik (.)

### Responsive Design
- Mobile-friendly layout
- Tablet optimization
- Adaptive grid system

## 📈 Data Integration

Dashboard terhubung langsung dengan Google Sheet:
- **URL**: CSV export dari Google Spreadsheet
- **Automatic Updates**: Data dimuat saat page load
- **Real-time Filtering**: Semua filter berjalan real-time di client-side

## 🚀 Cara Penggunaan

### 1. Buka Dashboard
```bash
# Clone repository
git clone https://github.com/akitsarpevol/memepredictor.git

# Buka file index.html di browser
open index.html
```

### 2. Gunakan Filters
- Pilih dari dropdown untuk filter data
- Kombinasikan multiple filters untuk analisis lebih detail
- Filter tanggal untuk periode tertentu

### 3. Navigate Pagination
- Gunakan tombol Previous/Next untuk navigasi table
- Info pagination menunjukkan posisi dan total records

## 🔧 Technical Stack

- **Frontend**: HTML5, CSS3, Vanilla JavaScript (ES6+)
- **Data Source**: Google Sheets (CSV export)
- **Styling**: CSS Grid & Flexbox untuk responsive layout
- **Features**: 
  - Client-side data processing
  - Real-time aggregation & calculations
  - Dynamic filtering & sorting
  - Pagination system

## 📋 Column Requirements

Google Sheet harus memiliki kolom berikut:
- `Nama Vendor`
- `Nama Proyek`
- `Status Tagihan`
- `Tahun Berkas`
- `Kategori Utang`
- `Saldo Utang`
- `Keterangan Singkat`
- `G/L Account`
- `PIC`

## 🔄 Data Flow

```
Google Sheet (CSV)
        ↓
   Fetch Data
        ↓
   Parse CSV
        ↓
   Populate Filters
        ↓
   Apply Filters
        ↓
   Render Tables & KPIs
```

## ⚙️ Calculations

### Aging Categories
Dihitung otomatis berdasarkan Tahun Berkas:
- **Dibawah 1 Tahun**: Current Year - Tahun Berkas < 1
- **1 Tahun**: Current Year - Tahun Berkas = 1
- **2-7 Tahun**: Sesuai perhitungan tahun

### KPI Calculations
- **Saldo Utang**: SUM dari kolom 'Saldo Utang'
- **Jumlah Tagihan**: COUNT of rows
- **Swap Utang KPI**: SUM 'Saldo Utang' WHERE 'Keterangan Singkat' = 'Swap Utang'

## 🌐 Browser Compatibility

✅ Chrome/Chromium
✅ Firefox
✅ Safari
✅ Edge
✅ Mobile Browsers

## 📱 Responsive Breakpoints

- **Desktop**: Full layout dengan grid 2 kolom
- **Tablet**: Layout adjusted untuk tampilan optimal
- **Mobile**: Single column, optimized untuk kecil screen

## 🔐 Notes

- Semua data processing dilakukan di client-side
- Tidak ada server-side dependencies
- CSV data di-cache di browser untuk performa lebih baik
- Filter tidak memerlukan page refresh

## 📞 Support

Untuk pertanyaan atau issue, silakan buat GitHub Issue atau hubungi tim development.

## 📄 License

Internal Use Only - PT [Company Name]

---

**Version**: 1.0.0
**Last Updated**: 2026
**Maintained By**: Development Team