# Tutorial Aider.Chat

## Pengenalan
Aider.Chat adalah alat bantu berbasis AI untuk pengembangan perangkat lunak yang terintegrasi dengan Git. Panduan ini akan membantu Anda memulai dan menggunakan fitur-fiturnya secara efektif.

## Instalasi
1. Pastikan Python terinstal di sistem Anda.
2. Jalankan perintah berikut di terminal:
   ```
   pip install aider-chat
   ```
3. Setelah instalasi selesai, Anda dapat menjalankan Aider dengan mengetik `aider` di terminal.

## Perintah Dasar
- `/help` – Menampilkan daftar semua perintah yang tersedia.
- `/help <perintah>` – Menampilkan detail bantuan untuk perintah tertentu.
- `/model <nama_model>` – Mengatur model AI yang akan digunakan (misalnya, `gpt-4`, `claude-3`).
- `/temperature <nilai>` – Mengatur tingkat kreativitas model (0.0 = jawaban deterministik, 1.0 = lebih kreatif).
- `/prompt <teks>` – Mengatur prompt sistem yang akan digunakan oleh model.
- `/reset` – Menghapus riwayat percakapan saat ini dan memulai yang baru.
- `/clear` – Membersihkan layar konsol.
- `/exit` atau `/quit` – Keluar dari Aider.Chat.

## Interaksi dengan Git
- `/git status` – Memeriksa status repository Git saat ini.
- `/git diff` – Menampilkan perubahan yang belum di-commit.
- `/git commit` – Membuat commit baru dengan pesan yang Anda tentukan.
- `/git push` – Push commit ke remote repository.
- `/git pull` – Pull perubahan terbaru dari remote repository.
- `/git apply` – Menerapkan patch Git ke codebase.

## Manajemen Percakapan
- `/history` – Menampilkan riwayat percakapan terbaru.
- `/save <nama_file>` – Menyimpan percakapan saat ini ke file.
- `/load <nama_file>` – Memuat percakapan yang telah disimpan.
- `/undo` – Membatalkan perubahan terakhir yang diterapkan.
- `/redo` – Mengulangi perubahan yang telah dibatalkan.

## Tips Praktis
1. Gunakan perintah singkat – Aider.Chat mendukung penyelesaian otomatis (tab) untuk sebagian besar perintah.
2. Manfaatkan prompt sistem – Sesuaikan prompt sistem untuk mengarahkan perilaku model sesuai kebutuhan Anda.
3. Atur temperature dengan bijak – Nilai temperature yang lebih rendah menghasilkan jawaban yang lebih konsisten; gunakan nilai yang lebih tinggi untuk tugas kreatif.
4. Pantau penggunaan token – Gunakan perintah `/tokens` (jika tersedia) untuk melacak konsumsi token dan menghindari biaya berlebihan.
5. Dokumentasikan sesi Anda – Simpan percakapan penting (`/save`) untuk referensi di masa depan atau untuk berbagi dengan anggota tim.
6. Integrasikan dengan Git – Menggunakan perintah Git yang terintegrasi memungkinkan Anda untuk meninjau, menerapkan, dan melakukan commit perubahan langsung dari antarmuka Aider.
7. Perbarui secara berkala – Periksa pembaruan dengan `/update` untuk mendapatkan fitur terbaru dan perbaikan bug.

## Memulai
1. Instal Aider.Chat dengan menjalankan `pip install aider-chat` (atau ikuti instruksi di situs resmi).
2. Jalankan `aider` di terminal Anda.
3. Gunakan `/help` untuk melihat daftar perintah yang tersedia.
4. Atur model dan prompt sistem sesuai kebutuhan Anda.
5. Mulailah berinteraksi—Ajukan pertanyaan, berikan instruksi, dan gunakan perintah Git untuk mengelola repository Anda.

Dengan mengikuti tutorial ini, Anda akan dapat memanfaatkan Aider.Chat secara maksimal untuk meningkatkan produktivitas pengembangan perangkat lunak Anda.

# Perintah Dalam Chat

## Perintah Slash

Aider mendukung perintah yang dapat dijalankan dari dalam chat, semuanya diawali dengan `/`.

::: {}
  Perintah                 Keterangan
  ----------------------- -----------------------------------------------------------------------------------------------------------------
  **/add**                Tambahkan file ke dalam chat sehingga aider dapat mengeditnya atau meninjau secara detail
  **/architect**          Masuk ke mode arsitek/editor menggunakan 2 model yang berbeda. Jika tidak ada prompt yang diberikan, beralih ke mode arsitek/editor.
  **/ask**                Ajukan pertanyaan tentang basis kode tanpa mengedit file apa pun. Jika tidak ada prompt yang diberikan, beralih ke mode tanya.
  **/chat-mode**          Beralih ke mode chat baru
  **/clear**              Hapus riwayat chat
  **/code**               Minta perubahan pada kode Anda. Jika tidak ada prompt yang diberikan, beralih ke mode kode.
  **/commit**             Commit perubahan pada repo yang dilakukan di luar chat (pesan commit opsional)
  **/context**            Masuk ke mode konteks untuk melihat kode di sekitarnya. Jika tidak ada prompt yang diberikan, beralih ke mode konteks.
  **/copy**               Salin pesan asisten terakhir ke clipboard
  **/copy-context**       Salin konteks chat saat ini sebagai markdown, cocok untuk ditempelkan ke antarmuka web
  **/diff**               Tampilkan diff perubahan sejak pesan terakhir
  **/drop**               Hapus file dari sesi chat untuk membebaskan ruang konteks
  **/edit**               Alias untuk /editor: Buka editor untuk menulis prompt
  **/editor**             Buka editor untuk menulis prompt
  **/editor-model**       Beralih ke model Editor LLM baru
  **/exit**               Keluar dari aplikasi
  **/git**                Jalankan perintah git (output dikecualikan dari chat)
  **/help**               Ajukan pertanyaan tentang aider
  **/lint**               Lint dan perbaiki file dalam chat atau semua file yang kotor jika tidak ada dalam chat
  **/load**               Muat dan jalankan perintah dari file
  **/ls**                 Daftar semua file yang diketahui dan tunjukkan mana yang termasuk dalam sesi chat
  **/map**                Cetak peta repository saat ini
  **/map-refresh**        Paksa penyegaran peta repository
  **/model**              Beralih ke Model Utama LLM baru
  **/models**             Cari daftar model yang tersedia
  **/multiline-mode**     Alihkan mode multi-baris (menukar fungsi Meta+Enter dan Enter)
  **/ok**                 Alias untuk `/code Ok, silakan lanjutkan dan lakukan perubahan tersebut.` (argumen apa pun akan ditambahkan)
  **/paste**              Tempel gambar/teks dari clipboard ke dalam chat. Opsional berikan nama untuk gambar.
  **/quit**               Keluar dari aplikasi
  **/read-only**          Tambahkan file ke dalam chat yang hanya untuk referensi, atau ubah file yang ditambahkan menjadi read-only
  **/reasoning-effort**   Atur tingkat upaya penalaran (nilai: angka atau low/medium/high tergantung pada model)
  **/report**             Laporkan masalah dengan membuka Issue GitHub
  **/reset**              Hapus semua file dan bersihkan riwayat chat
  **/run**                Jalankan perintah shell dan opsional tambahkan output ke chat (alias: !)
  **/save**               Simpan perintah ke file yang dapat merekonstruksi file sesi chat saat ini
  **/settings**           Cetak pengaturan saat ini
  **/test**               Jalankan perintah shell dan tambahkan output ke chat pada kode keluar non-nol
  **/think-tokens**       Atur anggaran token berpikir, misal: 8096, 8k, 10.5k, 0.5M, atau 0 untuk menonaktifkan.
  **/tokens**             Laporkan jumlah token yang digunakan oleh konteks chat saat ini
  **/undo**               Batalkan commit git terakhir jika dilakukan oleh aider
  **/voice**              Rekam dan transkripsi input suara
  **/weak-model**         Beralih ke Model Lemah LLM baru
  **/web**                Scrape halaman web, konversi ke markdown dan kirim dalam pesan
:::

Anda dapat dengan mudah mengirim ulang perintah atau pesan. Gunakan panah atas ⬆ untuk menggulir kembali atau CONTROL-R untuk mencari riwayat pesan Anda.

## Memasukkan Pesan Multi-baris dalam Chat

Anda dapat mengirim pesan multi-baris yang panjang dalam chat dengan beberapa cara:

- Tempelkan pesan multi-baris langsung ke dalam chat.
- Ketik `{` sendiri pada baris pertama untuk memulai pesan multi-baris dan `}` sendiri pada baris terakhir untuk mengakhiri pesan.
  - Atau, mulai dengan `{tag` (di mana "tag" adalah urutan huruf/angka apa pun) dan akhiri dengan `tag}`. Ini berguna ketika Anda perlu menyertakan kurung tutup `}` dalam pesan Anda.
- Gunakan Meta-ENTER untuk memulai baris baru tanpa mengirim pesan (Esc+ENTER di beberapa lingkungan).
- Gunakan perintah `/paste` untuk menempelkan teks dari clipboard ke dalam chat.
- Gunakan perintah `/editor` (atau tekan `Ctrl-X Ctrl-E` jika terminal Anda mengizinkannya) untuk membuka editor eksternal guna membuat pesan chat berikutnya. Lihat [dokumentasi konfigurasi editor](/docs/config/editor.html) untuk informasi lebih lanjut.
- Gunakan mode multi-baris, yang menukar fungsi Meta-Enter dan Enter, sehingga Enter menyisipkan baris baru dan Meta-Enter mengirimkan perintah Anda. Untuk mengaktifkan mode multi-baris:
  - Gunakan perintah `/multiline-mode` untuk mengaktifkannya selama sesi.
  - Gunakan opsi `--multiline`.

Contoh dengan tag:

:::: {}
::: {}
    {python
    def hello():
        print("Hello}")  # Note: contains a brace
    python}
:::
::::

Banyak orang meminta agar SHIFT-ENTER menjadi soft-newline. Sayangnya tidak ada cara portabel untuk mendeteksi ketukan tombol tersebut di terminal.

## Menginterupsi dengan CONTROL-C

Selalu aman menggunakan Control-C untuk menginterupsi aider jika ia tidak memberikan respons yang berguna. Respons parsial tetap ada dalam percakapan, sehingga Anda dapat merujuknya ketika Anda membalas LLM dengan informasi atau arahan lebih lanjut.

## Peta Tombol

Prompt interaktif dibangun dengan
[prompt-toolkit](https://github.com/prompt-toolkit/python-prompt-toolkit) yang menyediakan peta tombol emacs dan vi.

### Emacs

- `Panah Atas` : Pindah satu baris ke atas dalam pesan saat ini.
- `Panah Bawah` : Pindah satu baris ke bawah dalam pesan saat ini.
- `Ctrl-Up` : Gulir kembali melalui pesan sebelumnya.
- `Ctrl-Down` : Gulir maju melalui pesan sebelumnya.
- `Ctrl-A` : Pindahkan kursor ke awal baris.
- `Ctrl-B` : Pindahkan kursor satu karakter ke belakang.
- `Ctrl-D` : Hapus karakter di bawah kursor.
- `Ctrl-E` : Pindahkan kursor ke akhir baris.
- `Ctrl-F` : Pindahkan kursor satu karakter ke depan.
- `Ctrl-K` : Hapus dari kursor ke akhir baris.
- `Ctrl-L` : Bersihkan layar.
- `Ctrl-N` : Pindah ke entri riwayat berikutnya.
- `Ctrl-P` : Pindah ke entri riwayat sebelumnya.
- `Ctrl-R` : Pencarian terbalik dalam riwayat perintah.
- `Ctrl-X Ctrl-E` : Buka input saat ini di editor eksternal
- `Ctrl-Y` : Tempel (yank) teks yang sebelumnya dipotong.

### Vi

Untuk menggunakan peta tombol vi/vim, jalankan aider dengan opsi `--vim`.

- `Panah Atas` : Pindah satu baris ke atas dalam pesan saat ini.
- `Panah Bawah` : Pindah satu baris ke bawah dalam pesan saat ini.
- `Ctrl-Up` : Gulir kembali melalui pesan sebelumnya.
- `Ctrl-Down` : Gulir maju melalui pesan sebelumnya.
- `Esc` : Beralih ke mode perintah.
- `i` : Beralih ke mode insert.
- `a` : Pindahkan kursor satu karakter ke kanan dan beralih ke mode insert.
- `A` : Pindahkan kursor ke akhir baris dan beralih ke mode insert.
- `I` : Pindahkan kursor ke awal baris dan beralih ke mode insert.
- `h` : Pindahkan kursor satu karakter ke kiri.
- `j` : Pindahkan kursor ke bawah satu baris.
- `k` : Pindahkan kursor ke atas satu baris.
- `l` : Pindahkan kursor satu karakter ke kanan.
- `w` : Pindahkan kursor maju satu kata.
- `b` : Pindahkan kursor mundur satu kata.
- `0` : Pindahkan kursor ke awal baris.
- `$` : Pindahkan kursor ke akhir baris.
- `x` : Hapus karakter di bawah kursor.
- `dd` : Hapus baris saat ini.
- `u` : Batalkan perubahan terakhir.
- `Ctrl-R` : Ulangi perubahan yang dibatalkan terakhir.
