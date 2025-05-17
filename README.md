# 🎓 Deploy Chatbot Kampus dengan Flask dan JavaScript

Program ini menjelaskan tentang chatbot kampus yang dibuat menggunakan Python, Flask, dan JavaScript. Chatbot ini dapat digunakan untuk menjawab pertanyaan seputar kampus seperti:

- Program studi
- Fasilitas
- Biaya kuliah
- Alur pendaftaran
- Kegiatan mahasiswa, dan lainnya

## 🚀 Opsi Deployment:

1. Menjalankan chatbot di dalam aplikasi Flask menggunakan template Jinja2.
2. Menyediakan API Flask saja, dan frontend (HTML, CSS & JavaScript).

---

## 📦 Persiapan Awal

Clone repositori dan buat virtual environment:

```
$ git clone https://github.com/Pindosaputra123/Marooners-Chatbot.git
$ cd Marooners-Chatbot
$ python -m venv venv
$ .\venv\Scripts\Activate
```

### Install dependencies:

```
$ (venv) pip install Flask torch torchvision nltk
```

### Download dataset dari NLTK:

```
$ (venv) python
>>> import nltk
>>> nltk.download('punkt')
```

---

## ✏️ Edit intents.json

Edit file `intents.json` untuk menyesuaikan dengan kebutuhan chatbot kampus. Contoh:

```
{
  "intents": [
    {
      "tag": "pengertian",
      "patterns": [
        "Apa itu Universitas Singaperbangsa Karawang?",
        "Apa itu UNSIKA?",
        "UNSIKA itu apa?",
        "Singaperbangsa Karawang itu universitas apa?",
        "Bisa jelaskan tentang UNSIKA?",
        "Apa kepanjangan dari UNSIKA?",
        "UNSIKA singkatan dari apa?",
        "Ceritakan tentang Universitas Singaperbangsa Karawang.",
        "UNSIKA itu PTN atau PTS?",
        "Kapan UNSIKA menjadi PTN?"
      ],
      "responses": [
        "UNSIKA merupakan singkatan dari Universitas Singaperbangsa Karawang.",
        "Universitas ini didirikan pada tanggal 2 Februari 1982 dan menjadi PTN pada 6 Oktober 2014.",
        "Nama 'Singaperbangsa' berasal dari tokoh sejarah Karawang, yaitu Raden Adipati Singaperbangsa.",
        ]
    },
    {
      "tag": "lokasi",
      "patterns": [
        "Dimana lokasi Universitas Singaperbangsa Karawang?",
        "UNSIKA ada di mana?",
        "Lokasi kampus UNSIKA dimana?",
        "Alamat UNSIKA dimana ya?",
        "UNSIKA berlokasi di mana?",
        "Dimana letak Universitas Singaperbangsa Karawang?",
        "Kampus UNSIKA ada di daerah mana?",
        "Universitas Singaperbangsa Karawang terletak di mana?",
        "Dimana saya bisa menemukan kampus UNSIKA?",
        "Letak geografis UNSIKA ada di mana?"
      ],
      "responses": [
        "Universitas Singaperbangsa Karawang terletak di Kabupaten Karawang, Jawa Barat, Indonesia.",
        "Lokasi UNSIKA berada di Jl. HS. Ronggowaluyo, Puseurjaya, Kecamatan Telukjambe Timur, Karawang.",
        "UNSIKA berlokasi di Karawang Timur, Provinsi Jawa Barat.",
        "Kampus UNSIKA berada di wilayah industri Karawang, tepatnya di Telukjambe Timur.",
      ]
    }
  ]
}
```

---

## 🧠 Latih Model

```
$ (venv) python train.py
```

Model akan menghasilkan file `data.pth`.

Untuk menguji chatbot di terminal:

```
$ (venv) python chat.py
```

Untuk menguji chatbot di web:

```
$ (venv) python app.py
```

