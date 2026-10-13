# Deteksi Covid-19 Fake News menggunakan PySpark MLlib

Repositori ini berisi kode eksperimen untuk Tugas Eksplorasi Mandiri Mahadata (IF25-40402). Eksperimen ini merupakan replikasi parsial dan simulasi dari artikel jurnal *"Using artificial intelligence techniques for detecting Covid-19 epidemic fake news in Moroccan tweets"* (2021).

## Tujuan Eksperimen
Menerapkan metode pemrosesan teks terdistribusi (NLP Pipeline) menggunakan Apache Spark dan mengevaluasi kinerja tiga algoritma *machine learning* (Random Forest, Decision Tree, dan Naive Bayes) dalam mendeteksi berita palsu terkait Covid-19. Karena keterbatasan akses API *real-time*, eksperimen ini menggunakan dataset substitusi dari Kaggle.

## Struktur Repositori
- `Eksplorasi_Mahadata_PySpark.ipynb` : File Jupyter Notebook (Google Colab) utama yang berisi seluruh alur kerja mulai dari pemuatan dataset, rekayasa fitur teks (TF-IDF), hingga pelatihan dan evaluasi model.
- `README.md` : Dokumentasi repositori.

## Persiapan Lingkungan
Eksperimen ini dirancang agar dapat dieksekusi secara cepat menggunakan lingkungan *cloud* Google Colab dengan spesifikasi *single-node cluster*.
library utama yang dibutuhkan:
- `pyspark` (Apache Spark MLlib)
- `kagglehub` (Untuk mengunduh dataset secara otomatis)

## Cara Menjalankan Kode
1. Buka file `Eksplorasi_Mahadata_PySpark.ipynb` di repositori ini.
2. Klik tombol **"Open in Colab"** (atau unduh dan unggah manual ke [Google Colab](https://colab.research.google.com/)).
3. Pastikan *environment runtime* di Colab sudah aktif (Python 3).
4. Jalankan sel (*cell*) pertama untuk mengunduh Apache Spark dan pustaka pendukung.
5. Jalankan sel-sel berikutnya secara berurutan dari atas ke bawah. Kode akan otomatis mengunduh dataset `elvinagammed/covid19-fake-news-dataset-nlp` langsung ke dalam memori Spark.
6. Hasil evaluasi metrik (Akurasi, Presisi, Recall, F1-Score, dan Waktu komputasi) untuk ketiga algoritma akan muncul pada *output* di sel terakhir.

## Ringkasan Hasil
<img width="441" height="448" alt="Screenshot 2026-10-14 004926" src="https://github.com/user-attachments/assets/37727af3-bba3-4f3c-aee4-3002b1a00558" />

Pada eksperimen simulasi ini, algoritma **Naive Bayes** menunjukkan performa komputasi paling cepat sekaligus menghasilkan akurasi tertinggi dibandingkan Random Forest dan Decision Tree.

