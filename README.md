# Sistem Prediksi dan Pemetaan Daerah Rawan Banjir berbasis SIG dan Machine Learning

## 📌 Latar Belakang

Banjir merupakan salah satu bencana alam yang sering terjadi, terutama di wilayah dengan curah hujan tinggi dan kondisi geografis tertentu. Untuk meminimalisir dampak yang ditimbulkan, pemerintah daerah memerlukan sistem yang mampu memprediksi dan memetakan daerah rawan banjir secara akurat.

Menurut studi oleh Smith et al. (2020), **Sistem Informasi Geografis (SIG)** dapat digunakan secara efektif untuk pemetaan bencana dengan menggabungkan analisis spasial dan pemodelan prediksi berbasis AI. Penggunaan data historis seperti curah hujan, kemiringan lereng, dan penggunaan lahan memungkinkan sistem untuk memperkirakan daerah rentan banjir secara lebih tepat.

> 📚 **Referensi:**
>
> - Smith, J., & Patel, R. (2020). *Flood Risk Prediction Using GIS and Machine Learning: A Review.* *International Journal of Environmental Science & Technology*, 17(3), 145–160.  
> - Zhang, Y., & Lee, H. (2021). *Application of Machine Learning Algorithms in Flood Prediction.* *Journal of Hydrology and Meteorology*, 35(4), 234–249.

---

## 🤖 Model AI yang Digunakan

Model **Random Forest** dipilih sebagai algoritma utama karena keunggulannya dalam:

- Menangani berbagai tipe data (numerik & kategorikal).
- Menghindari overfitting.
- Memberikan akurasi tinggi pada dataset dengan banyak fitur.

Model ini memanfaatkan data historis seperti:
- Curah hujan
- Kemiringan lereng
- Penggunaan lahan
- Ketinggian wilayah

untuk memprediksi kemungkinan terjadinya banjir di suatu lokasi.

---

## 🗺️ Integrasi Data Spasial dan Non-Spasial

### Platform dan Tools:
- **GeoPandas**: Mengelola data spasial (shapefile, GeoJSON).
- **Matplotlib & Seaborn**: Visualisasi peta dan hasil prediksi.

### Proses Integrasi:
1. **Pengumpulan Data**
   - Data topografi, penggunaan lahan, curah hujan, dan kejadian banjir dikumpulkan dari instansi terkait.
2. **Preprocessing**
   - Membersihkan dan menyamakan format data spasial & non-spasial.
   - Menggabungkan data untuk membentuk satu dataset terpadu.
3. **Pelatihan Model**
   - Model Random Forest dilatih menggunakan data historis untuk mempelajari pola penyebab banjir.
4. **Prediksi & Visualisasi**
   - Model menghasilkan prediksi yang divisualisasikan dalam bentuk **peta interaktif**.

---

## 🔄 Alur Kerja Sistem

```text
1. Pengumpulan Data
   - Peta topografi & penggunaan lahan (data spasial)
   - Curah hujan & catatan banjir masa lalu (data non-spasial)

2. Preprocessing
   - Pembersihan data & penyatuan data spasial-nonspasial

3. Pelatihan Model
   - Model Random Forest dilatih untuk memetakan tingkat kerawanan banjir

4. Prediksi
   - Model memproses data terbaru dan memberikan hasil prediksi

5. Visualisasi
   - Peta interaktif ditampilkan dengan warna:
     - 🔴 Merah: Rawan banjir
     - 🟢 Hijau: Aman dari banjir
