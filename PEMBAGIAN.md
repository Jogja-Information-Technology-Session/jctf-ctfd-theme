# Pembagian Tugas

**Deskripsi pekerjaan:**

1.  Memastikan bahwa tampilan (termasuk tata letak/penggunaan komponen) sudah
    sesuai desain UI (Mas Handy?).
2.  Melakukan perubahan yang perlu agar template sesuai.
3.  Memastikan UI berfungsi semestinya.

## Detail

Fleksibel aja. Tidak perlu mengacu 100% ke pembagian di bawah. BTW, ini
kupilihnya pakai feeling aja. Jadi, kalau ada yang terasa kurang sesuai, mohon
info biar bisa direvisi.

Keterangan:

-   `@nama`, artinya `nama` **bertanggung jawab** atas perilaku file-file yang
    ditunjuk termasuk direktori di dalamnya (kecuali dituliskan secara
    eksplisit)

-   `x`, artinya tidak usah dikerjakan (biasanya karena kurang relevan atau
    interface setup/admin)

        SCOPE                           ASSIGNEE
        ------------------------------- -----------------
        templates/
        ├── base.html                   @yoga
        ├── challenge.html              @ihsan
        ├── challenges.html             @ihsan
        ├── components                  @yoga
        │   ├── errors.html
        │   ├── navbar.html
        │   └── notifications.html
        ├── config.html                 x
        ├── confirm.html                @yoga
        ├── errors                      @lois
        │   ├── 403.html
        │   ├── 404.html
        │   ├── 429.html
        │   ├── 500.html
        │   └── 502.html
        ├── login.html                  @lois
        ├── macros                      @ihsan
        │   └── forms.html
        ├── notifications.html          @lois
        ├── page.html                   @none
        ├── register.html               @ihsan
        ├── reset_password.html         @lois
        ├── scoreboard.html             @lois
        ├── settings.html               @lois
        ├── setup.html                  x
        ├── teams                       @ihsan && @yoga
        │   ├── invite.html             @ihsan
        │   ├── join_team.html          @ihsan
        │   ├── new_team.html           @ihsan
        │   ├── private.html            @yoga
        │   ├── public.html             @yoga
        │   ├── team_enrollment.html    @yoga
        │   └── teams.html              @ihsan
        └── users                       @yoga
        ├── private.html                @yoga
        ├── public.html                 @ihsan
        └── users.html                  @ihsan
