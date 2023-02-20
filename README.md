![random xkcd](https://imgs.xkcd.com/comics/borders.png)

# jctf-ctfd-theme

Repositori ini berisi tema (custom) CTFd yang di-*fork* dari tema
[core-beta](https://github.com/CTFd/core-beta).

## Konteks

Untuk mempermudah teman-teman yang mungkin masih *no context*, mungkin bisa
baca-baca ini dulu.

### Apa itu CTF?

Capture-the-flag (CTF) adalah perlombaan yang goal-nya adalah meng-capture flag
sebanyak-banyaknya. Sebenarnya, ada beberapa format permainan CTF, tapi yang
paling sering dan yang dipakai di CTF JOINTS 2023 adalah format Jeopardy.

#### Jeopardy by ChatGPT

"Gaya Jeopardy" atau "Jeopardy-style" adalah salah satu jenis format yang umum
digunakan dalam kompetisi Capture the Flag (CTF). Dalam format ini, setiap tim
atau peserta akan diberikan serangkaian tantangan atau "soal" yang harus
diselesaikan untuk mencetak poin.

Setiap tantangan biasanya memiliki kategori, seperti "reversing" (membalikkan
kode), "exploitation" (mengambil keuntungan dari kerentanan), "crypto"
(kriptografi), "web" (pemrograman web), atau "forensik" (analisis forensik), dan
setiap tantangan memiliki nilai poin tertentu tergantung pada tingkat
kesulitannya.

Peserta akan diberikan waktu terbatas untuk menyelesaikan setiap tantangan dan
masing-masing tantangan dapat memiliki beberapa tingkat kesulitan, dari yang
mudah hingga yang sangat sulit. Setelah selesai menyelesaikan setiap tantangan,
peserta akan memberikan jawaban untuk membuktikan bahwa mereka telah
menyelesaikan tantangan tersebut, dan jika jawaban mereka benar, mereka akan
menerima poin sesuai dengan nilai tantangan.

Pada akhir kompetisi, peserta atau tim dengan poin tertinggi akan dinyatakan
sebagai pemenang.

### Apa itu CTFd?

CTFd adalah platform berbasis web yang sering digunakan untuk meng-host dan
berpartisipasi dalam kompetisi Capture the Flag (CTF). CTFd menyediakan
fitur-fitur yang memungkinkan pengguna untuk membuat tantangan, mengelola
peserta, mengatur skor, dan menganalisis statistik kompetisi. Platform ini juga
memiliki fitur keamanan yang kuat untuk melindungi tantangan dari serangan dan
menjaga integritas kompetisi. Selain itu, CTFd adalah platform open source dan
mudah diatur, sehingga cocok untuk digunakan oleh individu, kelompok, atau
organisasi yang ingin mengadakan kompetisi CTF.

### Kita ngapain?

Supaya semakin khas, kita perlu mendesain tema custom untuk CTFd hehe. Karena
menggunakan Flask, mungkin agak trivial dalam mendesain temanya.

### Tl;dr

Intinya, CTF itu permainan mengumpulkan flag, yang paling banyak mengumpulkan
flag adalah yang menang. Di JCTF23, format permainannya adalah Jeopardy,
artinya, flag diperoleh dengan menyelesaikan soal-soal. CTFd adalah platform
berbasis Flask (Python) untuk mengadakan event CTF. Yang ingin kita lakukan di
sini adalah mendesain tema custom untuk CTFd.

## CTFd Theming System

Teman-teman diharuskan untuk membaca dan mempelajari CTFd (terutama sistem
temanya) di halaman-halaman ini.

1.  <https://docs.ctfd.io/docs/themes/overview>
2.  <https://docs.ctfd.io/docs/themes/structure>
3.  <https://docs.ctfd.io/docs/themes/build-system>
4.  <https://docs.ctfd.io/docs/themes/templates>
5.  <https://docs.ctfd.io/docs/themes/css>
6.  <https://docs.ctfd.io/docs/themes/javascript>
7.  <https://docs.ctfd.io/docs/themes/ctfd-js>
8.  <https://docs.ctfd.io/docs/themes/alpine-js>

Jika ada yang dibingungkan, silahkan ditanyakan.

## Development Environment Setup

Tema CTFd tidak bisa dikembangkan secara independen, tapi harus menginstall CTFd
juga. Berikut adalah cara untuk menyiapkan lingkungan untuk pengembangan tema
CTFd. Tidak harus persis, tapi kurang lebih seperti berikut.

### Requirements

-   Python 3.9 (belum coba di versi lain)
-   Git
-   npm

### Steps

1.  Clone repository CTFd

        git clone https://github.com/CTFd/CTFd
        cd CTFd

2.  Buat virtual environment

        python -m venv .venv

3.  Aktifkan virtual environment (sesuaikan dengan OS dan shell yang digunakan)

    -   Windows (coba cari di Google kalau error)

            .venv\Scripts\activate

    -   Unix-like (Bash)

            . .venv/bin/activate

4.  Install development requirements dengan pip

        pip install -r development.txt

5.  Jalankan `populate.py` untuk mengisi database CTFd dengan dummy data

        python populate.py

6.  Jalankan development server CTFd

        python serve.py

7.  Verifikasi bahwa server telah berjalan normal dengan membuka
    "http://localhost:4000" di browser. Selesaikan juga tahapan setup yang
    diminta (ngasal aja, tapi harus pilih Team Mode, karena JCTF nanti mode
    team).

8.  Harusnya setup CTFd sudah selesai. Sekarang, repository ini di folder
    `CTFd/themes`

        cd CTFd/themes
        git clone git@github.com:Jogja-Information-Technology-Session/jctf-ctfd-theme.git
        cd jctf-ctfd-theme

9.  Install dependensi dengan npm

        npm install .

10. Jalankan ini (gatau namanya, jarang main js wkwk, please refer to CTFd theme
    docs, intinya untuk auto build file-file yang di `assets/` ke `templates/`).

        npm run dev

11. Yeay! Sekarang coba modifikasi file di `templates/` atau di `assets/`,
    harusnya langsung rebuild (meskipun tidak hot reload). Semangat semua!

## Lisensi

-   `core-beta`: Apache License, Version 2.0
