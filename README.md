# 🌍 ISPU Air Quality Clustering: Fuzzy C-Means (FCM) Analysis

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![Excel](https://img.shields.io/badge/Excel-Manual_Calculation-green.svg)
![Status](https://img.shields.io/badge/Status-Completed-success.svg)

Proyek ini bertujuan untuk mengelompokkan data Indeks Standar Pencemaran Udara (ISPU) Provinsi DKI Jakarta tahun 2022 menggunakan algoritma **Fuzzy C-Means (FCM)**. Proyek ini membandingkan akurasi dan efisiensi antara perhitungan manual (Excel) dengan otomatisasi menggunakan Python.

## 📌 Gambaran Proyek
* **Tujuan**: Mengklasifikasikan kualitas udara ke dalam kategori "Sedang" dan "Tidak Sehat".
* **Algoritma**: Fuzzy C-Means (Clustering).
* **Dataset**: 98 Baris data ISPU 2022 (Sumber: Jakarta Open Data).
* **Fokus Utama**: Perbandingan kecepatan eksekusi dan validasi akurasi antara metode manual vs program.

## 🛠️ Metodologi (Fuzzy C-Means)
Algoritma ini bekerja dengan mencari pusat klaster (centroid) yang optimal melalui proses iterasi. Setiap data memiliki derajat keanggotaan terhadap setiap klaster yang diperbarui di setiap langkah.



**Parameter yang digunakan:**
- Jumlah Klaster ($n$): 2
- Pangkat Fuzziness ($m$): 2
- Maksimal Iterasi: 5
- Kriteria Berhenti: $\epsilon < 1e-5$

## 📊 Hasil Perbandingan: Python vs Excel

Berikut adalah temuan utama dari proyek ini:

| Parameter | Perhitungan Manual (Excel) | Program (Python) |
| :--- | :--- | :--- |
| **Waktu Eksekusi** | ± 3 Minggu (Proses Belajar & Input) | **< 0.1 Detik** |
| **Akurasi Akhir** | 83.67% | 83.67% |
| **Risiko Error** | Tinggi (Human Error pada Rumus) | Sangat Rendah (Otomatis) |
| **Skalabilitas** | Sulit untuk data besar | Sangat Mudah |

### **Progress Akurasi Per Iterasi**
1. **Iterasi 1**: 30.61% (Inisialisasi Acak)
2. **Iterasi 2**: 42.86%
3. **Iterasi 4**: 75.51%
4. **Iterasi 5**: **83.67% (Optimal/Konvergen)**

## 🚀 Fitur Program Python
- **Normalisasi Data**: Menggunakan Min-Max Scaling (0-1).
- **Stopwatch Timer**: Menghitung kecepatan eksekusi secara *real-time*.
- **Visualisasi PCA**: Memproyeksikan data 6 dimensi polutan ke dalam grafik 2D.
- **Auto-Mapping**: Menghitung akurasi secara otomatis dengan mencocokkan hasil klaster dengan label asli.

## 📁 Struktur Repositori
- `FCM_Analysis.ipynb` : Script utama Jupyter Notebook.
- `Dataset_ISPU_2022.csv` : Data mentah yang digunakan.
- `Hasil_Perhitungan_Excel.xlsx` : Bukti perhitungan manual 5 iterasi.

## 🎓 Kontributor
**ALDI** Informatics Student - Universitas Muhammadiyah Makassar.

---
*"Program Python terbukti jutaan kali lebih cepat dibanding Excel, namun Excel membantu saya memahami logika matematika di balik algoritma secara mendalam."*
