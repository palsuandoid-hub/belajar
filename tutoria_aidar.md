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
