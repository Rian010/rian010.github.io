---
layout: article
author: YAN
title: Tentang Blog ini
key: 10001
tags: blog
category: blog
date: 2024-02-05 23:15:00 +08:00
---

Saya selalu senang menggunakan Evernote. Saya akan membagi pengalaman belajar, halaman web favorit, pemikiran mendadak, pengingat dll.

<!--more-->

Suatu hari hujan, ketika saya sedang memilah catatan saya, saya menyesali bahwa sebagian besar catatan saya berada dalam siklus pembuatan, modifikasi, dan melupakan. Setelah suatu catatan ditulis dalam jangka waktu tertentu, lambat laun akan terlupakan di pojokan, kecuali kadang-kadang jika dilihat atau dicari secara tidak sengaja, di lain waktu catatan itu tergeletak diam di sana tanpa ada yang menghargainya.Inilah tragedi catatan yang sebenarnya. Tiba-tiba saya berpikir, jika saya menyusun catatan ini dan menaruhnya secara online, bukankah catatan tersebut dapat diperiksa dan dibaca oleh orang lain yang membutuhkannya? Jadi ide untuk menulis blog muncul saat itu, namun baru pada musim panas ini saya membuka blog saya sendiri.

Setelah mencoba beberapa host gratis dan menyerah karena terlalu lambat dan rumit, jadi saya berpikir Cobalah untuk membangun blog sendiri. 

## Blog statis

Blog yang dibangun di Halaman GitHub adalah [situs web statis](https://id.wikipedia.org/wiki/Situs_web#Situs_web_statis). Situs web semacam ini memiliki persyaratan server yang rendah dan merupakan situs web yang sangat ringan. Namun, operasi Ini rumit, dan file halaman web HTML lengkap harus ditulis untuk setiap halaman. Untungnya, sudah ada banyak sistem blog statis yang sangat baik, yang dapat dengan mudah menghasilkan file web yang sesuai berdasarkan konten yang Anda tulis. Yang perlu Anda lakukan hanyalah menulis postingan blog menggunakan [Markdown](https://id.wikipedia.org/wiki/Markdown), kemudian jalankan sistem blog untuk menghasilkan file halaman web, dan kemudian mengunggah file halaman web yang dihasilkan ke server. Sederhananya, alat blogging ini membuat situs web statis sedikit lebih dinamis, mirip dengan mekanisme cache halaman situs web dinamis.

Namun demikian, metode ini masih sangat rumit dan merepotkan.Jika Anda tidak terlalu merepotkan dan sangat tertarik, saya tetap menyarankan menggunakan situs web dinamis tradisional (Wordpress adalah pilihan yang bagus).

Termasuk sistem blog statis yang lebih populer saat ini

- [Jekyll](https://github.com/jekyll/)

- [Pelican](https://github.com/getpelican/pelican)

- [Octopress](https://github.com/imathis/octopress)

- [Hexo](https://github.com/hexojs/hexo/)

Blog ini menggunakan sistem blog Jekyll, karena lingkungan operasi Jekyll telah diatur di Halaman GitHub. Kita hanya perlu mengunggah kode sumbernya. GitHub secara otomatis akan menghasilkan file halaman web di latar belakang. Tidak perlu mengkompilasinya secara lokal atau kompilasi kode sumber. Cabang dibuat secara terpisah untuk file halaman web (gangguan obsesif-kompulsif berarti itu bagus), sementara sistem lain mengharuskan Anda mengunggah file halaman web yang dibuat secara lokal. Dengan cara ini kita bisa langsung mengedit file Markdown di GitHub versi web untuk mempublikasikan postingan blog secara langsung, apakah mirip dengan website dinamis?

## Proses pembangunan

Posting blog ini dimaksudkan untuk merekam proses terbentuknya blog ini. Jika Anda tertarik untuk membuat blog statis, ada banyak tutorial di Internet. Ini dia contoh proses pembuatan blog saya [rian010.github.io/jekyll-TeXt-theme](https://rian010.github.io/jekyll-TeXt-theme/).

Blog statis hanya menyediakan halaman statis seperti homepage, postingan blog, dll. Tidak dapat menyediakan fungsi interaktif dinamis seperti komentar. Di sini kita dapat menggunakan sistem komentar pihak ketiga untuk mencapai hal tersebut. Saat ini banyak sekali sistem komentar sosial, termasuk [Disqus](https://disqus.com/), saya pakai disini untuk bercerita lebih banyak.

Ada juga gambar blog, karena gambarnya relatif besar dan memakan banyak ruang, sehingga akan memakan banyak bandwidth server selama transmisi. **Di sini saya menyarankan untuk menempatkan sumber gambar di situs web lain untuk mengurangi beban pada server GitHub.**Situs web yang secara profesional menyediakan layanan penyimpanan tautan eksternal gambar disebut **Picture Bed**. Situs ini menyediakan ruang untuk menyimpan gambar dan memungkinkan Anda menghubungkan gambar ke dunia luar. Faktanya, album foto luar angkasa, disk jaringan, dll. dapat digunakan sebagai tempat tidur gambar / penyimpanan cloud. Cukup atur hak akses dari gambar yang dirujuk dalam posting blog ke publik (yaitu, dapat diakses oleh semua orang), sehingga siapa pun yang menelusuri Anda posting blog, mereka dapat melihatnya Gambar yang dikutip. Album foto mikro Sina Weibo adalah tempat tidur gambar / penyimpanan cloud yang bagus [contoh album foto mikro](http://photo.weibo.com/1941806611/albums).

## Alat yang digunakan di blog ini

- [GitHub Pages](https://pages.github.com/)

- [Jekyll](https://github.com/jekyll/) Sistem blog statis

- [Pygment](http://pygments.org/) penyorotan kode

- [Album mikro](http://photo.weibo.com/) tempat tidur bergambar / penyimpanan cloud

- [Emojify.js](https://github.com/Ranks/emojify.js) Tampilkan Emoji

- [DISQUS](https://disqus.com/) Sistem komentar

- [Google Analytics](https://www.google.com/analytics/) Alat analisis statistik situs web

## Catatan tambahan

[YAN Blog](https://rian010.github.io/blog) adalah blog teknologi komputer. Sebagai Pelajar ilmu komputer, sangatlah bermanfaat dan memuaskan untuk dapat berbagi ilmu sambil mempelajari ilmu profesional.
