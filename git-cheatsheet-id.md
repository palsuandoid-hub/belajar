# Cheatsheet Git – Bahasa Indonesia

> Panduan singkat untuk perintah Git yang paling umum, dalam bahasa Indonesia.

---

## 📚 Dasar-dasar

| Perintah | Deskripsi |
|---------|-------------|
| `git init <nama-repo>` | Membuat repositori Git baru (lokal) di folder saat ini. |
| `git clone <URL>` | Mengkloning repositori jarak jauh ke mesin lokal. |
| `git add <file>` | Menambahkan file ke area staging (indeks). |
| `git add .` | Menambahkan semua file yang diubah ke area staging. |
| `git commit -m "esan"` | Membuat commit dengan pesan yang diberikan. |
| `git status` | Menampilkan status kerja saat ini (tidak ada perubahan, perubahan yang dimodifikasi, file yang diabaikan, dll.). |
| `git log` | Menampilkan riwayat commit (grafik sederhana). |
| `git diff` | Menampilkan perubahan yang belum di‑commit (kerja yang dimodifikasi). |
| `git checkout <branch>` | Beralih ke branch lain. |
| `git merge <branch>` | Menggabungkan branch target ke branch saat ini. |

---

##  branch & Tag

| Perintah | Deskripsi |
|---------|-------------|
| `git branch` | Menampilkan daftar branch yang ada. |
| `git branch <nama-branch>` | Membuat branch baru. |
| `git branch -m <nama-branch>` | Mengganti nama branch. |
| `git branch -d <nama-branch>` | Menghapus branch (hanya jika sudah digabungkan). |
| `git tag <versi>` | Membuat tag anotasi untuk sebuah release. |
| `git show <tag>` | Menampilkan detail tag. |

---

## 🔄 Rebase & Reset

| Perintah | Deskripsi |
|---------|-------------|
| `git rebase <branch>` | Memindahkan branch saat ini ke atas commit dari branch target. |
| `git rebase --abort` | Membatalkan rebase yang sedang berjalan. |
| `git reset <commit>` | Mengembalikan HEAD (dan perubahan yang di‑staging) ke commit yang ditentukan. |
| `git reset --hard <commit>` | Mengembalikan HEAD, staging, dan kerja ke commit yang ditentukan (kehilangan perubahan yang tidak di‑commit). |
| `git reset HEAD <file>` | “Un‑stage” sebuah file. |

---

## 📦 Remote & Kolaborasi

| Perintah | Deskripsi |
|---------|-------------|
| `git remote add <nama>` `<URL>` | Menambahkan remote baru. |
| `git remote -v` | Menampilkan nama dan URL remote yang ada. |
| `git push <remote> <branch>` | Mengirimkan branch ke remote. |
| `git pull <remote> <branch>` | Mengambil dan menggabungkan branch remote. |
| `git fetch <remote>` | Mengambil objek dan referensi dari remote, tanpa menggabungkannya. |
| `git remote rename <lama> <baru>` | Mengganti nama remote. |
| `git remote remove <nama>` | Menghapus remote. |

---

## 🎒 Stash & Cherry‑Pick

| Perintah | Deskripsi |
|---------|-------------|
| `git stash` | Menyimpan perubahan yang belum di‑commit ke dalam stack stash. |
| `git stash pop` | Menerapkan stash terakhir (atau `git stash apply`). |
| `git stash list` | Menampilkan daftar stash yang tersimpan. |
| `git stash drop <indeks>` | Menghapus sebuah stash berdasarkan indeks. |
| `git cherry-pick <hash>` | Menerapkan commit tunggal dari branch lain ke branch saat ini. |

---

## 📊 Log & Inspeksi

| Perintah | Deskripsi |
|---------|-------------|
| `git log --oneline` | Menampilkan commit dalam format singkat (hash + pesan). |
| `git log --graph --oneline --all` | Menampilkan riwayat commit dalam bentuk grafik untuk semua branch. |
| `git log --stat` | Menampilkan statistik perubahan untuk setiap commit. |
| `git log --follow <file>` | Menampilkan riwayat untuk sebuah file, bahkan jika namanya berubah. |
| `git show <hash>` | Menampilkan detail commit (diff + metadata). |
| `git blame <file>` | Menampilkan siapa yang terakhir mengubah setiap baris dalam file. |

---

## 🛠️ Utilitas & Konfigurasi

| Perintah | Deskripsi |
|---------|-------------|
| `git config --global user.name "Nama Kamu"` | Mengatur nama pengguna global. |
| `git config --global user.email "kamu@contoh.com"` | Mengatur email pengguna global. |
| `git config --global core.editor "code --wait"` | Mengatur editor default (misalnya VS Code). |
| `git config --global alias.co checkout` | Membuat alias untuk perintah yang sering digunakan. |
| `git config --global alias.st status` | Contoh alias lain. |
| `git clean -fd` | Menghapus file yang tidak diawasi (berbahaya – gunakan dengan hati‑hati!). |
| `git rm --cached <file>` | Menghapus file dari indeks (staging) tetapi tetap menyimpannya di working tree. |

---

## 📌 Tips Singkat

- **Staging area** adalah “penampungan” untuk perubahan yang akan dimasukkan ke dalam commit berikutnya.
- **Commit** adalah snapshot yang tidak bisa diubah (kecuali dengan `amend` atau `reset`).
- Gunakan **branch** untuk fitur, perbaikan, atau eksperimen – gabungkan kembali ke `main` (atau `master`) saat sudah siap.
- **Rebase** membuat riwayat commit terlihat linear dan mudah dibaca, tetapi hindari rebase pada commit yang sudah dipublikasikan.
- **Stash** berguna saat kamu perlu beralih pekerjaan secara tiba‑tiba tanpa menyimpan perubahan.
- Selalu lakukan `git pull` (atau `git fetch` + `git merge`) sebelum melakukan push ke remote bersama untuk menghindari konflik.

---

## 🆘 Memecahkan Masalah Umum

| Masalah | Perintah / Solusi |
|---------|--------------------|
| Konflik penggabungan | Selesaikan konflik di editor, lalu `git add <file>` dan `git commit`. |
| Kehilangan perubahan lokal | Periksa `git reflog` untuk menemukan commit yang terhapus. |
| Remote tidak dikenal | Jalankan `git remote -v` dan pastikan URL benar; perbarui dengan `git remote set-url`. |
| “Sudah ada objek dengan nama yang sama” saat push | Pastikan kamu menggunakan branch yang benar, atau lakukan `git push --force` (hanya jika kamu yakin). |
| “Berada di luar tree kerja utama” | Gunakan `git worktree add <path>` untuk membuat tree kerja tambahan. |

---

*Cheatsheet ini bisa kamu simpan sebagai `git-cheatsheet-id.md` dan buka kapan saja saat kamu butuh pengingat cepat dalam bahasa Indonesia. Selamat bersenang-senang dengan Git!* 🚀
