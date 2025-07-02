# Proyek-Analisis-Sentimen
Submission kelas Belajar Fundamental Deep Learning (Laskar AI &amp; Dicoding)
🚖 Analisis Sentimen Review Gojek
Proyek ini berfokus pada scraping, preprocessing, pelabelan sentimen berbasis lexicon, visualisasi, serta klasifikasi menggunakan model MLP terhadap review aplikasi Gojek dari Google Play Store.

📌 Tujuan
Mengambil data review aplikasi Gojek.

Membersihkan dan memproses teks review.

Melakukan pelabelan sentimen menggunakan pendekatan lexicon-based.

Menampilkan visualisasi distribusi sentimen dan WordCloud.

Melatih model klasifikasi sentimen menggunakan MLPClassifier.

🔍 1. Scraping Data
Menggunakan google-play-scraper.

Aplikasi: com.gojek.app.

Bahasa: Indonesia (id).

Total ulasan diambil: 10.000.

Hanya review dengan sort MOST_RELEVANT.

Data disimpan dalam DataFrame dan dibersihkan dari nilai NaN.

🧹 2. Preprocessing Teks
Tahapan pembersihan dan pemrosesan teks meliputi:

Cleaning: Hapus mention, hashtag, angka, tanda baca, newline, dan link.

Case Folding: Konversi ke huruf kecil.

Slang Correction: Mengubah kata informal ke bentuk baku (contoh: "abis" → "habis").

Tokenization: Pecah kalimat menjadi token.

Stopword Removal: Menghapus kata umum Bahasa Indonesia dan Inggris.

Stemming: Menggunakan Sastrawi untuk kata dasar.

Rekonstruksi: Token bersih dijadikan kembali sebagai kalimat utuh.

🏷️ 3. Labeling Sentimen (Lexicon-Based)
Menggunakan dua kamus:

lexicon_positive.csv

lexicon_negative.csv

Proses:

Skor sentimen dihitung dari jumlah kata positif dan negatif.

Label ditentukan:

positive jika skor ≥ 0

negative jika skor < 0

Hasil disimpan pada kolom polarity_score dan sentiment.

📊 4. Visualisasi
Pie Chart untuk distribusi sentimen positif dan negatif.

WordCloud untuk:

Seluruh review

Review positif

Review negatif

🤖 5. Modeling: Klasifikasi dengan MLP
Ekstraksi Fitur:
Menggunakan TF-IDF dengan:

min_df=5

max_df=0.8

sublinear_tf=True

Pembagian Data:
80% training, 20% testing.

Model:
Menggunakan MLPClassifier dari scikit-learn.

Konfigurasi:

python
Salin
Edit
hidden_layer_sizes=(512, 256, 128)
activation='relu'
solver='adam'
alpha=1.0
learning_rate='adaptive'
max_iter=1000
early_stopping=True
Hasil Evaluasi:
Akurasi Training: 98.11%

Akurasi Testing: 92.14%

Classification Report dicetak di output notebook.

💡 Insight
Dataset berhasil disiapkan melalui preprocessing teks dan labeling berbasis lexicon.

WordCloud berhasil menunjukkan kata-kata dominan berdasarkan sentimen.

Model MLP menunjukkan performa tinggi dengan akurasi testing 92.14%, menandakan kemampuan klasifikasi yang kuat terhadap review positif dan negatif aplikasi Gojek.

💾 Output
data_scraping_gojek.csv: Dataset final setelah preprocessing dan pelabelan.

Visualisasi Pie Chart dan WordCloud tersedia di dalam notebook.
