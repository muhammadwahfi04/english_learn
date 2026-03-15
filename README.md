# LearnEnglish — Website Belajar Bahasa Inggris

Website belajar bahasa Inggris interaktif untuk pemula (Tahap 1 & 2), lengkap dengan materi dan latihan soal dari bank soal JSON.

## Struktur Folder

```
english-app/
├── index.html          ← Website utama
├── data/
│   ├── simple_present.json      ← 30 soal Simple Present Tense
│   ├── present_continuous.json  ← 30 soal Present Continuous
│   ├── simple_past.json         ← 30 soal Simple Past Tense
│   ├── question_words.json      ← 30 soal Question Words
│   ├── prepositions.json        ← 30 soal Prepositions
│   └── adjectives.json          ← 30 soal Adjectives
└── README.md
```

## Fitur

- **Tahap 1 (Absolute Beginner):** Materi Alphabet, Greetings, Numbers, Colors, Basic Vocabulary, To Be
- **Tahap 1 — Latihan To Be:** 10 soal isian ketik sendiri, diacak setiap ronde
- **Tahap 2 (Elementary A1-A2):** Materi 6 topik lengkap
- **Tahap 2 — Latihan per Topik:** Pilih topik, 10 soal diacak dari bank 30 soal per topik
- Semua soal dalam **Bahasa Indonesia** + penjelasan jawaban
- **100% gratis**, tidak butuh API key

## Cara Jalankan Lokal

Karena menggunakan `fetch()` untuk membaca file JSON, **tidak bisa dibuka langsung sebagai file HTML** — butuh server lokal.

### Opsi 1 — VS Code Live Server
1. Install ekstensi **Live Server** di VS Code
2. Klik kanan `index.html` → **Open with Live Server**

### Opsi 2 — Python
```bash
cd english-app
python -m http.server 8080
# Buka: http://localhost:8080
```

### Opsi 3 — Node.js
```bash
npx serve .
```

## Deploy ke Vercel

1. Push folder ini ke GitHub
2. Login ke [vercel.com](https://vercel.com)
3. Klik **Add New Project** → Import repo dari GitHub
4. Vercel otomatis detect sebagai Static Site
5. Klik **Deploy** — selesai!

> File JSON di folder `data/` akan otomatis tersedia sebagai static files di Vercel.

## Menambah Soal

Edit file JSON di folder `data/`. Format setiap soal:

```json
{
  "id": "sp031",
  "q": "Teks soal di sini.",
  "opts": ["Pilihan A", "Pilihan B", "Pilihan C", "Pilihan D"],
  "ans": 0,
  "exp": "Penjelasan kenapa jawaban ini benar."
}
```

- `ans` adalah index jawaban benar (0 = A, 1 = B, 2 = C, 3 = D)
- Tambahkan soal baru di array `questions` di file JSON yang sesuai
