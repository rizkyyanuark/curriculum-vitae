# AGENT.MD: Operating Guidelines for AI Assistants

Dokumen ini adalah pedoman dan regulasi baku untuk setiap AI Assistant yang memodifikasi atau mengelola repositori **`curriculum-vitae`**.

---

## 1. Standar Format Deskripsi Release Tag (WAJIB)

Setiap kali membuat atau memperbarui GitHub Release / Git Tag versi CV baru di repositori ini, deskripsi rilis (Release Notes) **WAJIB** mengikuti format baku 3 seksi di bawah ini:

```markdown
## Profil & Orientasi Peran
- **Target Track:** <Nama Track, misal: Data Scientist / AI Data Engineer>
- **Recommended Apply:** <posisi yang direkomendasikan>
- **Fokus Pembaruan:** <penjelasan singkat fokus atau perubahan pada varian ini>

## Fitur Unggulan
- **Riset & Publikasi:** <ringkasan riset / paper jika ada>
- **Pengalaman Industri & Magang:**
  - *<Nama Instansi 1>:* <highlight pengalaman dan hasil STAR>
  - *<Nama Instansi 2>:* <highlight pengalaman dan hasil STAR>
- **Proyek Teknis:** <ringkasan proyek teknis utama>
- **Pendidikan & Sertifikasi:** <ringkasan gelar, sertifikasi, dan bahasa>

## Keywords
<Daftar kata kunci teknis/domain yang relevan dipisahkan dengan koma>
```

### Aturan Ketat untuk Field `Recommended Apply`:
Nilai pada baris `- **Recommended Apply:**` **HANYA BOLEH** dipilih dari 5 posisi berikut:
1. `ai engineer`
2. `ai data engineer`
3. `data engineer`
4. `ml engineer`
5. `data scientist`

*Catatan:* Pilih 1 sampai 3 posisi yang paling cocok dari daftar di atas sesuai orientasi varian CV. **Dilarang keras** menambahkan posisi di luar 5 opsi resmi ini.

### Larangan Format Rilis:
* **DILARANG** menambahkan seksi `Panduan Memilih Varian CV di Masa Depan:`.
* **DILARANG** menambahkan seksi `Aset Terlampir:`.
* Seksi `Fitur Unggulan` harus informatif dan merangkum outline isi CV sehingga pengguna dapat memahami keunggulan dan isinya tanpa perlu membuka file PDF.

---

## 2. Prinsip Copywriting & Tone (Antislop)

1. **Metode STAR (Situation, Task, Action, Result):**
   * Setiap *bullet point* pengalaman kerja dan proyek harus menyertakan konteks masalah nyata, tindakan teknis yang diambil, dan hasil terukur.
   * Hindari deskripsi pasif yang hanya menyebutkan jobdesc tanpa hasil nyata.
2. **Diksi Realistis Fresh Graduate (Anti-Inflation):**
   * Gunakan kata kerja aksi konkret: `Built`, `Wrote`, `Set up`, `Trained`, `Structured`, `Planned`, `Collected`.
   * **HINDARI** kata-kata yang terlalu *fancy* atau terkesan *too good to be true* untuk level fresh graduate: `Engineered`, `Architected`, `Integrated`, `Established`, `Orchestrated`.
3. **Larangan Buzzword AI:**
   * Dilarang menggunakan diksi klise: `seamless`, `cutting-edge`, `next-level`, `elevate`, `unlock`, `delve`, `game-changer`, `actionable insights`.
4. **Larangan Karakter Em Dash:**
   * Dilarang menggunakan tanda baca em dash (`—`). Gunakan tanda koma, titik dua, tanda kurung, atau en dash (`–` / `--`) untuk rentang tanggal/angka.

---

## 3. Standar Layout & Aksesibilitas

1. **Format Dokumen LaTeX (`cv.tex`):**
   * Ditargetkan untuk **2 halaman seimbang** tanpa ada entri pekerjaan yang terbelah canggung di tengah jalan.
   * Halaman 1 memuat: Header, Summary, Education, dan seluruh Work Experience.
   * Halaman 2 memuat: Technical Projects, Organizational Experience, Technical Skills, Certifications, dan Languages.
2. **Web CV (`index.html`):**
   * Memenuhi standar aksesibilitas WCAG AA (rasio kontras teks > 4.5:1 untuk teks normal, > 3.0:1 untuk teks besar dan kontrol interaktif).
   * Mendukung navigasi keyboard (`:focus-visible`), zoom 200% tanpa teks terpotong, dan mode gelap/terang.

---

## 4. Alur Kerja CI/CD (GitHub Actions)

* **Push ke `main`:** Otomatis mengompilasi `cv.tex` dan men-*deploy* hasil `cv.pdf` serta `index.html` ke branch `build` untuk hosting GitHub Pages.
* **Push tag `v*`:** Otomatis membuat GitHub Release resmi dan melampirkan file `cv.pdf` sebagai aset unduhan dengan format release notes di atas.
