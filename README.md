# PiutangKu - Sistem Manajemen Piutang

Aplikasi web untuk manajemen piutang (receivables management) yang berjalan sepenuhnya di client-side menggunakan teknologi lokal.

## 🚀 Live Demo

**https://angganurfirmansah3-dot.github.io/piutangku/**

## Fitur

- 📊 Dashboard dengan statistik piutang real-time
- 📈 Dashboard Eksekutif
- 👥 Manajemen Pengguna (Admin, Sales, Finance, Manager, Owner)
- 🏢 Data Pelanggan
- 🧾 Manajemen Piutang/Invoice
- 💳 Pencatatan Pembayaran
- 📄 Laporan Piutang
- 📋 Generate Laporan PDF
- 📚 Riwayat Laporan PDF
- ⚙️ Pengaturan Profil

## Teknologi

- **Frontend**: HTML5 + CSS3 + JavaScript
- **Database**: SQLite (via sql.js) disimpan di IndexedDB
- **Charts**: Chart.js
- **Styling**: Custom CSS (Responsive Design)
- **Hosting**: GitHub Pages (Gratis)

## Demo Accounts

| Email | Password | Role |
|-------|----------|------|
| admin@piutangku.local | admin123 | Admin |
| sales@piutangku.local | sales123 | Staf Penjualan |
| keuangan@piutangku.local | keuangan123 | Staf Keuangan |
| manager@piutangku.local | manager123 | Manajer Keuangan |
| owner@piutangku.local | owner123 | Pemilik Perusahaan |

## Cara Menggunakan

1. Buka https://angganurfirmansah3-dot.github.io/piutangku/
2. Login dengan salah satu akun demo di atas
3. Navigasi menggunakan menu sidebar (dapat mengakses semua fitur)
4. Semua data tersimpan lokal di browser (IndexedDB)
5. Data persistent dan tidak hilang meski browser ditutup

## Akses Penuh

**Semua role memiliki akses penuh ke semua menu:**
- ✅ Dashboard
- ✅ Dashboard Eksekutif
- ✅ Manajemen Pengguna
- ✅ Data Pelanggan
- ✅ Piutang/Invoice
- ✅ Pembayaran
- ✅ Laporan
- ✅ Generate PDF
- ✅ Riwayat PDF
- ✅ Pengaturan

## Data Storage

Data disimpan menggunakan:
- **IndexedDB** untuk database SQLite
- **Local Storage** untuk session management
- Tidak ada koneksi ke server, semua data offline-first
- Data aman dan private (hanya tersimpan di device Anda)

## Browser Support

- Chrome/Chromium ✓
- Firefox ✓
- Safari ✓
- Edge ✓

## Fitur Utama

### Dashboard
- Total piutang
- Sisa piutang
- Total pelanggan
- Piutang jatuh tempo
- Transaksi terbaru

### Manajemen Data
- Tambah/hapus pengguna
- Tambah/hapus pelanggan
- Buat invoice
- Catat pembayaran

### Laporan
- Filter laporan berdasarkan periode
- Filter berdasarkan status piutang
- Export ke PDF
- Riwayat laporan

## Struktur Database

```
users (id, name, email, password, role, status)
customers (id, name, phone, email, address, created_at)
invoices (id, invoice_no, customer_id, amount, paid_amount, remaining_amount, due_date, status, created_at)
payments (id, invoice_id, amount, payment_date, method, notes, created_at)
reports (id, report_no, report_type, period_start, period_end, created_by, created_at)
```

## Tips Penggunaan

1. **Backup Data**: Data disimpan di IndexedDB browser Anda
   - Jangan clear browser cache jika ingin data tetap ada
   - Gunakan browser yang sama untuk akses konsisten

2. **Multiple Users**: Setiap login dengan akun berbeda membuka session terpisah

3. **Data Entry**: Semua field form harus diisi dengan lengkap

4. **Export PDF**: Fitur generate PDF mencatat laporan di database

## Security Notes

- Ini adalah aplikasi demo untuk pembelajaran
- Password disimpan di IndexedDB (tidak di-encrypt)
- Untuk production: implementasikan proper authentication & encryption
- Data hanya tersimpan lokal di browser Anda

## Installation (Local Development)

1. Clone repository:
   ```bash
   git clone https://github.com/angganurfirmansah3-dot/piutangku.git
   ```

2. Buka file `index.html` di browser atau gunakan local server:
   ```bash
   python -m http.server 8000
   # atau
   npx http-server
   ```

3. Akses di `http://localhost:8000`

## License

MIT

## Support

Jika ada pertanyaan atau saran, silakan buat issue di repository ini.
