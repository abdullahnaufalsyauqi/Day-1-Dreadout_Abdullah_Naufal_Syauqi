# Rangkuman Materi Day 1

**Tanggal:** 9 November 2026

Materi Day 1 terdiri dari tiga bagian: pengenalan akademik, prompt engineering, dan Git serta GitHub, yang kemudian dipraktikkan lewat proyek Student Task Planner.

---

## Bagian 1: Pengenalan Akademik (Kurikulum Merdeka di Perguruan Tinggi)

### MBKM (Merdeka Belajar Kampus Merdeka)

- Kebijakan Kemendikbudristek sejak 2020 yang memberi mahasiswa kesempatan mengasah kemampuan sesuai bakat dan minat, termasuk terjun langsung ke dunia kerja.
- Mahasiswa memiliki hak belajar di luar program studi asal (menurut slide: hingga 2 semester).
- Kegiatan di luar program studi dapat diakui hingga 20 SKS per semester dan dikonversi oleh program studi.
- Tujuan utama: lulusan siap kerja dan relevan dengan kebutuhan industri, dengan pembelajaran yang fleksibel, tidak hanya di dalam kelas.

**8 bentuk kegiatan pembelajaran MBKM:**

1. Pertukaran Pelajar
2. Magang / Praktik Kerja
3. Asistensi Mengajar
4. Penelitian / Riset
5. Proyek Kemanusiaan
6. Kegiatan Wirausaha
7. Proyek Independen
8. Membangun Desa / KKN

### MSIB (Magang dan Studi Independen Bersertifikat)

- Program unggulan yang menjadi salah satu jalur pelaksanaan MBKM, dijalankan bersama mitra industri dan organisasi.
- Berdurasi 1 semester, dikonversi 20 SKS, peserta memperoleh sertifikat, dan ada peluang rekomendasi ke mitra.
- Dua jenis:
  - **Magang Bersertifikat:** belajar sambil bekerja di mitra, mengerjakan tugas dan proyek nyata, dibimbing mentor industri.
  - **Studi Independen Bersertifikat:** belajar kompetensi spesifik dari pakar lewat short course, bootcamp, atau kelas daring terbuka (MOOC), dilanjutkan proyek atau studi kasus.

### Metode Pembelajaran

| Metode | Inti | Hasil |
|---|---|---|
| **PjBL (Project-Based Learning)** | Belajar lewat karya nyata, umumnya dalam tim dan waktu tertentu | Produk, prototipe, aplikasi, atau laporan yang dipresentasikan |
| **PBL (Problem-Based Learning)** | Belajar lewat pemecahan masalah nyata yang tidak punya jawaban tunggal | Solusi hasil analisis; dosen berperan sebagai fasilitator |
| **CBL (Case-Based Learning)** | Menganalisis kasus nyata yang sudah tersedia | Rekomendasi solusi beserta alasan dan risikonya |

Persamaan ketiganya: mahasiswa aktif, kerja tim, berbasis masalah nyata, dan melatih berpikir kritis.

Alur CBL: pelajari kasus → identifikasi masalah → analisis dan diskusi → rumuskan solusi → presentasi dan refleksi.

### Alur Mengikuti Program Kampus Merdeka

1. Cek data PDDikti
2. Buat akun di portal Kampus Merdeka
3. Pilih program
4. Daftar dan ikuti seleksi
5. Jalani program, raih sertifikat, dan ajukan konversi SKS ke prodi

### Tips Sukses

Kenali minat dan arah karier, konsultasi dengan dosen, siapkan CV dan portofolio, rapikan data akademik, disiplin mendokumentasikan kegiatan, dan selalu cek informasi resmi.

---

## Bagian 2: Building with AI (Prompt Engineering)

**Pemateri:** Nugi Farhan, Senior Product Designer

- **Prompt** adalah instruksi atau masukan yang diberikan kepada model AI untuk mendapatkan hasil tertentu, bisa berupa pertanyaan, kata kunci, instruksi rumit, atau potongan kode.
- **Prompt engineering** adalah cara merancang instruksi agar AI memberi jawaban yang tepat, relevan, dan layak digunakan.
- **Context is key:** prompt tanpa konteks (misalnya "Create student task planner") menghasilkan jawaban yang umum, sedangkan prompt dengan konteks menghasilkan hasil yang jauh lebih sesuai kebutuhan.

**Struktur prompt yang baik:**

| Unsur | Fungsi |
|---|---|
| **Role** | Peran yang diminta dari AI |
| **Task** | Tujuan atau tugas yang diminta |
| **Context** | Kebutuhan (requirements) dan batasan (constraints) |
| **Format** | Bentuk keluaran yang diinginkan |

**Taktik prompt yang efektif (contoh dari slide):** gunakan kata kerja aksi, tentukan panjang dan format keluaran, sebutkan target audiens, sertakan fakta dan data yang relevan, rujuk dokumen atau sumber tertentu, dan definisikan istilah kunci.

**Keuntungan prompt engineering:** meningkatkan performa model AI, mengurangi bias dan respons yang offensive, meningkatkan kontrol dan prediktabilitas, serta memberi pengalaman pengguna yang lebih baik.

---

## Bagian 3: Git dan GitHub

### Git vs GitHub

| | Git | GitHub |
|---|---|---|
| **Apa itu** | Sistem version control terdistribusi (DVCS) | Platform berbasis web untuk menyimpan repository Git secara online |
| **Fungsi** | Melacak dan mengelola perubahan kode secara lokal | Mendukung kolaborasi |

Git diciptakan oleh Linus Torvalds pada 2005 untuk mencatat siapa, kapan, dan apa saja yang berubah pada suatu file.

### Alur Kerja Git (Git Workflow)

- **Working directory:** salinan satu versi proyek yang sedang dikerjakan di komputer.
- **Staging area (index):** tempat menyimpan informasi perubahan yang akan masuk ke commit berikutnya.
- **Git directory (repository):** tempat Git menyimpan metadata dan object database proyek; bagian inilah yang disalin saat `clone`.

Alurnya: Working Directory → (stage) → Staging Area → (commit) → Repository.

### Setup

1. Install Git, lalu cek dengan `git --version`.
2. Set identitas: `git config --global user.name "..."` dan `git config --global user.email "..."`.
3. Cek konfigurasi: `git config --global --list`.
4. Install VS Code dan pasang perintah `code` ke PATH.
5. Buat SSH key (`ssh-keygen -t ed25519 -C "email"`), daftarkan public key ke GitHub, lalu verifikasi dengan `ssh -T git@github.com`. (Contoh di slide memakai macOS.)

### Perintah Dasar

| Perintah | Fungsi |
|---|---|
| `git init` | Memulai repository baru |
| `git clone "url"` | Menyalin repository dari GitHub |
| `git add .` / `git add -A` | Memindahkan perubahan ke staging area |
| `git commit -m 'message'` | Menyimpan perubahan ke repository |
| `git remote add <name> <url>` | Menghubungkan repository lokal dengan repository di GitHub |
| `git push origin main` | Mengirim commit ke GitHub |
| `git pull origin main` | Mengambil perubahan dari GitHub dan menggabungkannya |

---

## Bagian 4: Proyek Workshop Day 1, Student Task Planner

Proyek: membuat aplikasi web sederhana untuk membantu mahasiswa baru mencatat tugas dan deadline (daftar tugas, status selesai, dan filter all/pending/completed), dibuat dengan HTML, CSS, dan JavaScript.

Alur pengerjaan:

1. Pasang platform AI (Claude, Antigravity, ChatGPT).
2. Tulis prompt untuk membuat web/aplikasi.
3. Tambahkan ke Git dengan `git init`.
4. Commit dan push ke GitHub.
5. Lakukan perubahan.
6. Commit dan push lagi ke GitHub.

**Progres saya:** Pada Day 1 saya mengikuti alur pengerjaan di atas: memahami tujuan proyek, menyusun prompt terstruktur untuk AI, lalu mengelola hasilnya dengan Git (`git init`, `add`, `commit`) dan mengunggahnya ke GitHub (`push`). Repository dokumentasi ini sendiri adalah praktik langsung dari alur tersebut.
