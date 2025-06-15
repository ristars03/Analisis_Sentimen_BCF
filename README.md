# 🧠 ANALISIS SENTIMEN PENILAIAN PARTNERSHIP AWARDS DENGAN METODE NATURAL LANGUAGE PROCESSING (NLP): STUDI KASUS BAKRIE CENTER FOUNDATION

Sistem ini dikembangkan untuk mengklasifikasikan sentimen dari penilaian stakeholder terhadap mitra yang aktif berkontribusi dalam program - program di **Bakrie Center Foundation (BCF)**. Dengan menggunakan model **Bidirectional LSTM (BiLSTM)** dan **FastText pretrained Bahasa Indonesia**, sistem ini mampu secara otomatis mengidentifikasi apakah suatu pernyataan bersifat *positif*, *netral*, atau *negatif*.

---

## 🚀 Fitur Utama

- Klasifikasi otomatis teks penilaian menjadi: `positif`, `netral`, atau `negatif`
- Menampilkan confidence score (%) untuk setiap hasil prediksi
- Evaluasi dan visualisasi performa model
- Mendukung penentuan pemenang kategori Partnership Awards

---

## 📂 Struktur Repositori

```
📦 Analisis_Sentimen_BCF
├── Analisis_Sentimen_BCF.ipynb     # Notebook utama (training, evaluasi, demo)
├── README.md                       # Dokumentasi proyek
├── requirements.txt               # Daftar dependensi
├── model/
│   ├── model_sentimen_bilstm.h5   # (opsional) file model terlatih
│   └── tokenizer.pickle           # (opsional) tokenizer hasil training
├── data/
│   └── example_input.csv          # (opsional) contoh input untuk demo
├── fasttext/
│   └── cc.id.300.vec              # (disarankan, tidak disertakan karena besar)
```

---

## ▶️ Cara Menjalankan Proyek Ini

1. **Clone repo ini** atau buka `Analisis_Sentimen_BCF.ipynb` di Google Colab
2. **Jalankan sel satu per satu** dari atas ke bawah
3. Pada bagian demo, edit list `penilaian_baru` untuk memasukkan kalimat stakeholder
4. Sistem akan menampilkan:
   - Hasil klasifikasi (label + confidence %)
   - Distribusi total sentimen
     
---

## 📊 Contoh Output Demo

```
1. "Mitra sangat aktif mendampingi mahasiswa." → positif 87.25%
2. "Tidak ada komunikasi sama sekali dari pihak mitra." → negatif 91.42%
3. "Kinerja cukup baik namun bisa ditingkatkan." → netral 78.16%

Distribusi Sentimen:
positif: 60.00% | netral: 20.00% | negatif: 20.00%

✅ Rekomendasi: Layak menjadi pemenang (positif ≥ 60%)
```

---

## 📦 Instalasi Dependencies (Opsional jika dijalankan lokal)

Pastikan Python 3.8+ terpasang. Install dependensi:

```bash
pip install -r requirements.txt
```

---

## 📚 Sumber Daya Tambahan

- Pretrained FastText Bahasa Indonesia:  
  [Download `cc.id.300.vec`](https://fasttext.cc/docs/en/crawl-vectors.html)
- Dataset internal: 1000 penilaian stakeholder dari BCF (tidak disertakan demi kerahasiaan)

---

## ✅ Untuk Apa Sistem Ini Digunakan?

Sistem ini mendukung:
- Automasi proses evaluasi Partnership Awards
- Pengambilan keputusan berbasis data
- Transparansi dalam proses pemilihan mitra terbaik

---

## 👨‍💻 Developer
Dibuat oleh Rista Bella, mahasiswa Politeknik Negeri Bali untuk keperluan skripsi dan implementasi sistem internal di Bakrie Center Foundation.


---
