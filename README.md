<div align="center">

# 📊 Global Sales and Profitability Dashboard
### Tugas Mata Kuliah Business Intelligence

![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi&logoColor=black)
![Excel](https://img.shields.io/badge/Data-Excel-217346?logo=microsoftexcel&logoColor=white)
![Rows](https://img.shields.io/badge/Data-700%20baris-blue)
![Periode](https://img.shields.io/badge/Periode-2013--2014-orange)
![Status](https://img.shields.io/badge/Status-Selesai-success)

</div>

---

## 📌 Ringkasan

Proyek ini adalah tugas mata kuliah **Business Intelligence** yang diusulkan oleh **Bp. Agus Nugraha, S.T., M.Kom.**

Tujuannya adalah membangun dashboard **Power BI** yang menjawab pertanyaan dasar bisnis: **berapa penjualan dan keuntungan perusahaan, dari mana asalnya, dan seberapa besar diskon menggerus profit?**

![Dashboard Preview](assets/dashboard-preview.png)

---

## 🎯 Tujuan

1. Menampilkan indikator kinerja utama (KPI): total penjualan, total profit, dan profit margin.
2. Melihat tren penjualan dan profit dari bulan ke bulan.
3. Memetakan penjualan berdasarkan negara.
4. Membandingkan profitabilitas pada tiap tingkat diskon.
5. Menyediakan filter interaktif berdasarkan produk dan segmen.

---

## 📈 Hasil Utama

| Indikator | Nilai |
|---|---:|
| **Total Sales** | **118,73 juta** |
| **Total Profit** | **16,89 juta** |
| **Profit Margin** | **14,23%** |

### Profitabilitas per Tingkat Diskon

| Discount Band | Total Sales | Total Profit | Profit Margin |
|---|---:|---:|---:|
| None | 7.943.654 | 1.736.455 | **21,86%** |
| Low | 34.629.779 | 6.188.858 | 17,87% |
| Medium | 38.780.431 | 5.579.523 | 14,39% |
| High | 37.372.487 | 3.388.867 | **9,07%** |
| **Total** | **118.726.350** | **16.893.702** | **14,23%** |

### Temuan

**1. Makin besar diskon, makin tipis margin.** Margin turun dari 21,86% (tanpa diskon) menjadi 9,07% (diskon tinggi). Band diskon High menyumbang penjualan hampir setara Medium, tetapi profitnya hampir 40% lebih rendah.

**2. Penjualan merata di lima negara.** Amerika Serikat, Kanada, Prancis, Jerman, dan Meksiko berada di kisaran 21–25 juta. Amerika Serikat paling tinggi dalam penjualan (25,03 juta), tetapi margin-nya paling rendah (12,0%). Jerman dan Prancis memiliki margin tertinggi (sekitar 15,5–15,7%).

**3. Segmen Government paling dominan.** Segmen ini menyumbang 52,5 juta penjualan dengan margin 21,7%. Sebaliknya, segmen **Enterprise mencatat kerugian** (profit −0,61 juta, margin −3,1%).

**4. Paseo adalah produk terlaris** dengan penjualan 33,0 juta, lebih dari dua kali lipat Carretera yang terendah (13,8 juta).

**5. Tren bulanan fluktuatif** dengan puncak di akhir 2014. Penjualan dan profit bergerak searah, tetapi profit selalu jauh di bawah penjualan.

> Temuan nomor 2 sampai 4 berasal dari analisis data Excel, bukan dari visual di dashboard. Kalau ingin ditampilkan, tambahkan visual per segmen dan produk.

### 💡 Saran

- Evaluasi kebijakan **diskon tinggi**, karena memangkas margin lebih dari separuh dibanding penjualan tanpa diskon.
- Telusuri penyebab **kerugian segmen Enterprise**, misalnya harga, diskon, atau biaya produksi.
- Pertahankan segmen **Government** sebagai penopang profit.

---

## 🗂️ Dataset

**File:** `Sample data praktikum 1.xlsx` (sampel data praktikum)

| Atribut | Keterangan |
|---|---|
| Jumlah baris | 700 transaksi |
| Jumlah kolom | 16 |
| Periode | September 2013 – Desember 2014 |
| Segmen | Government, Midmarket, Channel Partners, Enterprise, Small Business |
| Negara | Canada, France, Germany, Mexico, United States of America |
| Produk | Carretera, Montana, Paseo, Velo, VTT, Amarilla |
| Discount Band | None, Low, Medium, High |

**Kolom:** `Segment`, `Country`, `Product`, `Discount Band`, `Units Sold`, `Manufacturing Price`, `Sale Price`, `Gross Sales`, `Discounts`, `Sales`, `COGS`, `Profit`, `Date`, `Month Number`, `Month Name`, `Year`.

> **Catatan:** nilai `None` pada kolom `Discount Band` adalah kategori sah (tanpa diskon), bukan data kosong. Beberapa aplikasi, termasuk pandas, membacanya sebagai nilai kosong secara tidak sengaja.

---

## 🧮 Ukuran (Measure) di Power BI

| Measure | Fungsi |
|---|---|
| `Total Sales` | Jumlah penjualan |
| `Total Profit` | Jumlah keuntungan |
| `Profit Margin (%)` | Total Profit dibagi Total Sales |

Model data juga memakai tabel **Calendar Table** untuk analisis waktu.

---

## 📊 Komponen Dashboard

| Visual | Fungsi |
|---|---|
| Slicer **Product** dan **Segment** | Filter interaktif |
| Kartu **Total Sales**, **Total Profit**, **Profit Margin** | Ringkasan KPI |
| Line chart **By Year and Month** | Tren penjualan dan profit bulanan |
| Peta **Total Sales by Country** | Sebaran penjualan per negara |
| Tabel **Discount Band** | Penjualan, profit, dan margin per tingkat diskon |

---

## 🧰 Teknologi

- **Microsoft Power BI Desktop** untuk pemodelan dan visualisasi
- **DAX** untuk measure dan tabel kalender
- **Microsoft Excel** sebagai sumber data

---

## 📁 Struktur Repositori

```
Tugas-Business-Intelligence/
├── assets/
│   └── dashboard-preview.png          # Pratinjau dashboard untuk README
├── Sample data praktikum 1.xlsx       # Dataset
├── Tugas Bussines Intelegence.pbix    # File dashboard Power BI
├── Tugas Bussines Intelegence.pdf     # Hasil dashboard (PDF)
└── README.md
```

---

## 🚀 Cara Menjalankan

1. **Clone repositori**
   ```bash
   git clone https://github.com/ashafamultazam/Tugas-Business-Intelligence.git
   cd Tugas-Business-Intelligence
   ```
2. **Install Power BI Desktop** (gratis, hanya untuk Windows).
3. **Buka** `Tugas Bussines Intelegence.pbix`.
4. Jika sumber data tidak ditemukan, arahkan ke file Excel di folder ini lewat **Transform data → Data source settings**.
5. Gunakan slicer **Product** dan **Segment** untuk menjelajahi data.

Tanpa Power BI, lihat hasilnya di `Tugas Bussines Intelegence.pdf`.

---

## ⚠️ Keterbatasan

- Data hanya **700 baris** dalam **16 bulan**, sehingga tren jangka panjang tidak dapat disimpulkan.
- Dataset berupa **data latihan**, bukan data bisnis riil.
- Hubungan diskon dan margin adalah **korelasi**, bukan bukti sebab-akibat.
- Satuan mata uang tidak disebutkan pada data.

---

## 👤 Penulis

**Asha Fa Multazam** — [GitHub](https://github.com/ashafamultazam)

Dosen pengampu: **Bp. Agus Nugraha, S.T., M.Kom.**

---

<div align="center">

⭐ Jika proyek ini bermanfaat, beri bintang pada repositori ini.

</div>
