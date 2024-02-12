---
title: Cara Memasukkan Project Lokal ke Repo Github
tags: Github
date: 2024-02-12 07:58:00 +08:00
---
![g](https://www.earthdatascience.org/images/earth-analytics/git-version-control/git-fork-emphasis.png)

Berikut adalah langkah-langkah untuk memasukkan project lokal ke repo Github:




## **1. Buat Repo Baru di Github:**

- Buka website Github dan masuk ke akun Anda.
- Klik tombol "New repository".
- Berikan nama repo dan deskripsi singkat (opsional).
- Pilih "Public" atau "Private" untuk visibility repo.
- Klik tombol "Create repository".
<!--more-->
## **2. Inisialisasi Git di Project Lokal:**

- Buka terminal/command prompt di folder project lokal Anda.
- Jalankan perintah berikut:

```
git init
```

- Perintah ini akan membuat folder `.git` di project lokal Anda.

## **3. Tambahkan File ke Staging Area:**

- Gunakan perintah `git add` untuk menambahkan file-file project Anda ke staging area.

```
git add .
```

- Perintah ini akan menambahkan semua file di folder project Anda ke staging area.

**4. Commit File ke Local Repository:**

- Gunakan perintah `git commit` untuk commit file-file yang ada di staging area ke local repository.

```
git commit -m "Pesan commit"
```

- Ganti "Pesan commit" dengan pesan yang menjelaskan perubahan yang Anda lakukan.

## **5. Hubungkan Repo Lokal ke Repo Github:**

- Jalankan perintah berikut untuk menghubungkan repo lokal Anda ke repo Github yang Anda buat di langkah 1:

```
git remote add origin https://github.com/<username>/<nama-repo>.git
```

- Ganti `<username>` dengan username Github Anda dan `<nama-repo>` dengan nama repo Github Anda.

## **6. Push Local Changes ke Github:**

- Jalankan perintah berikut untuk push perubahan lokal Anda ke repo Github:

```
git push origin main
```

- Perintah ini akan push semua perubahan di local repository Anda ke branch "main" di repo Github Anda.

## **7. Verifikasi di Github:**

- Buka website Github dan masuk ke akun Anda.
- Buka repo yang Anda buat di langkah 1.
- Anda akan melihat perubahan yang Anda push dari local repository Anda.

## **Tips:**

* Anda dapat menggunakan flag `-a` dengan perintah `git add` untuk menambahkan semua file yang baru dan yang sudah diubah ke staging area.
* Anda dapat menggunakan flag `-m` dengan perintah `git commit` untuk menambahkan pesan commit.
* Anda dapat menggunakan flag `-u` dengan perintah `git push` untuk push perubahan ke branch lain di repo Github Anda.

**Sumber Informasi:**

* **Dokumentasi Git:** [https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository](https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository)

**Semoga informasi ini bermanfaat!**
