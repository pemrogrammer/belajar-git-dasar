# belajar-git-dasar
Perintah-perintah dasar git dipelajari pada repositori ini dimana sumber materinya diambil dari [sini](https://docs.google.com/presentation/d/1ZzM1xYw1YoaDOTqK7ziVrkgOQh3T8mqodGzEKYFnsfY/edit#slide=id.p) dan untuk mendownload git melalui [sini](https://git-scm.com/downloads) kemudian lakukan installasi.

## Cek Versi
Setelah berhasil menginstall langkah pertama yang dilakukan adalah mencoba perintah dibawah.
```sh 
$ git --version

git version 2.25.1
```
## Konfigurasi Username dan E-mail
Langkah awal anda diharuskan untuk membuat akun github terlebih dahulu, untuk membuat akun dapat dilakukan [disini](https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home) alternatif silahkan kunjungi [https://github.com](https://github.com) kemudian cari menu signup. Jika selesai melakukan registrasi akun github anda dapat melakukan konfigurasi username dan E-mail melalui terminal dengan menggunakan perintah dibawah. **Sesuaikan username dan email anda.**
```sh
$ git config --global user.name "taufiqsumadi"
$ git config --global user.email "taufiqsumadi@email.com"
```
Melihat konfigurasi dengan menggunakan perintah
```sh
$ git config --list --show-origin

file:/home/taufiq/.gitconfig    user.name=taufiqsumadi
file:/home/taufiq/.gitconfig    user.email=taufiqsumadi@email.com
```

## Membuat Repository
Sebagai contoh saya akan bekerja pada directory ~/Documents/belajar-git-dasar kemudian jalankan perintah 
```sh 
$ git init

Initialized empty Git repository in /home/taufiq/Documents/belajar-git-dasar/.git/
```

## Melihat Status Perubahan
Kita dapat melihat status adanya perubahan, penambahan dan/atau penghapusan file yang terjadi pada working directory, staging area, repository dengan menggunakan perintah
```sh
$ git status

On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```