# bpom-sentiment
Analisis sentimen ulasan aplikasi **BPOM Mobile** pada platform Google Play Store menggunakan metode **Lexicon-Based** dan algoritma **Random Forest**.

## 📌 Latar Belakang
BPOM Mobile adalah aplikasi resmi dari **Badan Pengawas Obat dan Makanan (BPOM) RI** yang membantu masyarakat memverifikasi legalitas obat, makanan, dan kosmetik melalui pemindaian QR code serta pengecekan nomor registrasi.  

Walaupun telah diunduh lebih dari **1 juta kali** (April 2025), aplikasi ini hanya memperoleh **rating 2,1/5 bintang** dari sekitar 3.000 ulasan di Google Play Store.  

Penelitian ini bertujuan untuk **menganalisis sentimen ulasan pengguna** sehingga dapat memberikan masukan bagi pengembangan aplikasi.

## 📊 Dataset
- **Sumber**: Ulasan aplikasi BPOM Mobile di Google Play Store  
- **Jumlah data**: ±1744 ulasan berbahasa Indonesia  
- **Teknik pengambilan data**: *Web Scraping* dengan library `google-play-scraper`  
- **Distribusi kelas hasil pelabelan (Lexicon-Based dengan kamus Inset Lexicon):**  
  - 548 negatif  
  - 544 netral  
  - 498 positif  

## ⚙️ Metodologi
Proyek ini menggunakan pendekatan **CRISP-DM** dengan tahapan:  
1. **Business Understanding** – Analisis kebutuhan dan tujuan penelitian  
2. **Data Understanding** – Eksplorasi dataset hasil scraping  
3. **Data Preparation** – Preprocessing teks:  
   - Case Folding  
   - Normalisasi Kata  
   - Tokenizing  
   - Stopword Removal  
   - Stemming  
4. **Modeling** –  
   - Ekstraksi fitur dengan **CountVectorizer**  
   - Klasifikasi dengan algoritma **Random Forest (100 trees)**  
5. **Evaluation** – Menggunakan **Confusion Matrix, Accuracy, Precision, Recall, F1-score**

## 🏆 Hasil
- **Akurasi model**: 77%  
- **F1-score tertinggi**: kelas negatif  
- Mayoritas ulasan cenderung bernada **negatif**  

## 🛠️ Teknologi yang Digunakan
- **Python**  
- **Google Colab**  
- Library:  
  - `pandas`  
  - `numpy`  
  - `scikit-learn`  
  - `nltk`  
  - `google-play-scraper`  

## ✅ Kesimpulan
Model **Lexicon-Based + Random Forest** mampu mengklasifikasikan sentimen ulasan BPOM Mobile dengan cukup baik.  
Hasil penelitian menunjukkan kecenderungan sentimen **negatif** dari pengguna, yang dapat menjadi bahan evaluasi bagi pengembang aplikasi.  
