# 🛠️ Tugas Membuat Aplikasi Kalkulator BBM (Bahan Bakar Minyak)

## 📚 Tujuan

Membuat aplikasi sederhana menggunakan **PHP** yang berjalan di **console/terminal**, untuk menghitung **berapa liter BBM yang bisa dibeli** berdasarkan **jumlah uang** dan **jenis BBM** yang dipilih.

---

## 🔰 Part 1: Basic

### ✅ Fitur Wajib

1. Aplikasi dijalankan di **console/terminal**.
2. **Tampilkan daftar harga BBM** saat aplikasi dimulai.
3. Input dilakukan secara **berurutan**:
   - **Nominal pembelian** (berapa uang yang ingin dibelikan BBM)
   - **Jenis BBM** (dipilih dari daftar)
   - **Jumlah uang yang dibayar**
4. Setelah input selesai, tampilkan hasil perhitungan:
   - Jenis BBM
   - Harga per liter
   - Nominal beli
   - Jumlah liter BBM yang didapat
   - Uang dibayar
   - Kembalian (jika ada)

---

### 🛢️ Daftar Harga BBM

| Jenis BBM  | Harga/Liter (Rp) |
| ---------- | ---------------- |
| Pertamax   | 12.500           |
| Pertalite  | 10.000           |
| Dexlite    | 13.000           |
| Solar      | 6.000            |

---

### 🧮 Contoh Kasus

Fazl ingin membeli **Pertamax** sebanyak **Rp 20.000**, dan ia membayar dengan **Rp 50.000**.

**Perhitungan:**

- Harga Pertamax: Rp 12.500/liter  
- Jumlah liter: `20.000 ÷ 12.500 = 1,6 liter`  
- Kembalian: `50.000 - 20.000 = Rp 30.000`

---

### 🧩 Contoh Output Console

```bash
=== Daftar Harga BBM ===
1. Pertamax - Rp 12.500
2. Pertalite - Rp 10.000
3. Dexlite - Rp 13.000
4. Solar - Rp 6.000

Masukkan nominal pembelian BBM: 20000
Pilih jenis BBM (misal: Pertamax): Pertamax
Masukkan jumlah uang yang dibayar: 50000

=== Hasil Transaksi ===
Jenis BBM     : Pertamax
Harga/liter   : Rp 12.500
Nominal beli  : Rp 20.000
Liter dapat   : 1,6 liter
Uang dibayar  : Rp 50.000
Kembalian     : Rp 30.000

```
---

### ⚠️ Validasi Wajib
- Nominal pembelian dan uang dibayar harus angka (tidak boleh huruf).
- Tidak boleh membeli lebih dari uang yang dibayar.
- Output angka gunakan format Rp dan pemisah ribuan (contoh: Rp 12.500).

---

## 🚀 Part 2: Advance
Tambahkan dua fitur baru:
### 1️⃣ Fitur Diskon (Opsional)

- Pengguna boleh memasukkan diskon dalam persen (%)
- Diskon maksimal 100%, tidak boleh negatif.
- Jika ada diskon, harga BBM dikurangi diskon sebelum dihitung liter.

### 🧮 Contoh:

Harga Pertamax: Rp 12.500
Diskon: 20%
Harga setelah diskon = 12.500 - (20% x 12.500) = Rp 10.000
### 2️⃣ Tambahkan PPN (Pajak Pertambahan Nilai)

   - Besarnya PPN = 11%

   - PPN dihitung setelah diskon

   - PPN wajib ditambahkan ke total pembelian

### 🧮 Contoh:
   Harga BBM setelah diskon: Rp 20.000
   PPN 11% = 11% × 20.000 = Rp 2.200
   Total yang harus dibayar = Rp 22.200

### 📝 Contoh Output Advance
```bash
=== Hasil Transaksi ===
Jenis BBM        : Pertamax
Harga/liter      : Rp 12.500
Diskon           : 20%
Harga diskon     : Rp 10.000
Nominal beli     : Rp 20.000
PPN (11%)        : Rp 2.200
Total dibayar    : Rp 22.200
Liter didapat    : 2 liter
Uang dibayar     : Rp 25.000
Kembalian        : Rp 2.800
```

💡 Tips Tambahan
   - Gunakan fungsi number_format() di PHP untuk memformat angka dengan ribuan.
   - Gunakan array untuk menyimpan daftar BBM dan harganya.
   - Validasi input dengan is_numeric().
