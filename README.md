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

## Menambah File
Perlu diketahui pada git terdapat 3 stage:
1. Working Directory/Local Area
2. Staging Area/Staging Index
3. Repository

Untuk menambah kan file dari Working directory ke Staging Area menggunakan perintah `git add`, contoh kasus: 
1. Menyiapkan file untuk uji coba.
```sh
$ touch file1.txt
$ ls -l
total 8
-rw-rw-r-- 1 taufiq taufiq    0 Mei 20 13:03 file1.txt
-rw-rw-r-- 1 taufiq taufiq 1083 Mei 15 10:51 LICENSE
-rw-rw-r-- 1 taufiq taufiq 1961 Mei 15 11:57 README.md
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        file1.txt

nothing added to commit but untracked files present (use "git add" to track)
```
2. Menambahkan file dari Working Directory ke Staging Index.
```sh
$ git add file1.txt 
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   file1.txt
```
3. Melakukan commit ke Repository flag ```-m``` digunakan untuk memberikan pesan atau informasi terhadap perubahan yg terjadi.
```sh
$ git commit -m "Menambahkan file1.txt ke repository"
[main 8024d66] Menambahkan file1.txt ke repository
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 file1.txt
 $ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```