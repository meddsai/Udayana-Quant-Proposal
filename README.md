# Udayana-Quant-Proposal

Template LaTeX untuk Usulan Penelitian Kuantitatif di Universitas Udayana.

## Persyaratan Sistem

Untuk menggunakan template ini, Anda memerlukan:

1. Distribusi TeX (pilih salah satu):
   - Windows: MiKTeX atau TeX Live
   - macOS: MacTeX
   - Linux: TeX Live

2. Editor LaTeX (opsional, pilih salah satu):
   - TeXstudio
   - TeXmaker
   - Visual Studio Code dengan ekstensi LaTeX Workshop
   - Overleaf (online)

## Instalasi di Ubuntu/Debian

```bash
# Install TeX Live lengkap dan Biber
sudo apt-get update
sudo apt-get install texlive-full biber
```

## Cara Kompilasi

1. Clone repositori ini:
   ```bash
   git clone [URL_REPOSITORI]
   cd Udayana-Quant-Proposal
   ```

2. Kompilasi dokumen dengan urutan berikut:
   ```bash
   pdflatex main.tex    # Langkah 1: Membuat file auxiliary
   biber main           # Langkah 2: Memproses bibliografi
   pdflatex main.tex    # Langkah 3: Memperbarui referensi
   pdflatex main.tex    # Langkah 4: Memastikan semua referensi terbarui
   ```

## Struktur File

- `main.tex`: File utama LaTeX
- `references.bib`: Database referensi dalam format BibTeX
- `logo.png`: Logo universitas
- `.gitignore`: File untuk mengabaikan file sementara LaTeX

## Menambahkan Referensi

1. Tambahkan entri bibliografi ke file `references.bib`
2. Kutip dalam teks menggunakan:
   - `\parencite{key}` untuk kutipan dalam kurung: (Penulis, Tahun)
   - `\textcite{key}` untuk kutipan naratif: Penulis (Tahun)

## Troubleshooting

Jika terjadi error saat kompilasi:

1. Hapus file sementara:
   ```bash
   rm -f main.aux main.bbl main.blg main.log main.lof main.lot main.toc main.pdf
   ```

2. Kompilasi ulang dengan urutan di atas

## Lisensi

[Sesuaikan dengan lisensi proyek]