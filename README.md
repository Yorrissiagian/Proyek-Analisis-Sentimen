# Proyek-Analisis-Sentimen
Submission kelas Belajar Fundamental Deep Learning (Laskar AI &amp; Dicoding)
🚖 Analisis Sentimen Review Gojek
Proyek ini bertujuan untuk melakukan scraping data ulasan aplikasi Gojek dari Google Play Store dan melakukan klasifikasi sentimen (positif vs negatif) berdasarkan teks ulasan pengguna.

Terdiri dari dua bagian utama:

📥 Web Scraping — Mengambil data ulasan dari Google Play Store.

🧠 Klasifikasi Sentimen — Memprediksi sentimen dari teks ulasan menggunakan Machine Learning.

📥 1. Scraping Ulasan Gojek
Deskripsi
Notebook ini mengambil review aplikasi Gojek dari Google Play Store menggunakan pustaka google-play-scraper.

Langkah-langkah
Menentukan parameter scraping (jumlah ulasan, bahasa, negara).

Menyimpan hasil scraping ke dalam DataFrame.

Mengekspor data ke file CSV untuk digunakan dalam proses selanjutnya.

Output
gojek_reviews.csv — Dataset berisi teks ulasan dan rating dari pengguna.

🧠 2. Klasifikasi Sentimen
Deskripsi
Notebook ini membangun model Machine Learning untuk memprediksi sentimen (positif/negatif) dari ulasan pengguna terhadap aplikasi Gojek.

Alur Pengerjaan
Data Preparation

Labeling otomatis berdasarkan rating: >=4 dianggap positif, sisanya negatif.

Text preprocessing: lowercasing, penghapusan tanda baca, stopwords removal, stemming.

Feature Extraction

Menggunakan TF-IDF Vectorizer.

Modeling

Algoritma: Logistic Regression (baseline), Naive Bayes, dan SVM.

Evaluasi menggunakan accuracy, precision, recall, F1-score.

Eksperimen

Perbandingan performa antar model.

Confusion matrix dan classification report.

Output
Model klasifikasi terlatih.

Visualisasi performa model.
