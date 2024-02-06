---
layout: article
title: Menerapkan subtitle pembuka Star Wars menggunakan HTML5
key: 10007
tags: FrontEnd
category: blog
date: 2016-02-17 21:30:00 +08:00
---

![the-force-awake](https://wx3.sinaimg.cn/large/73bd9e13ly1fjldo8obm7j21kw16oaj8.jpg)

Tahun lalu saya pergi ke bioskop untuk menonton film Star Wars terbaru ["The Force Awakens"](https://movie.douban.com/subject/20326665/)。Ceritanya sederhana, tapi adegan dan karakternya (saya sangat suka Han Solo, sayang sekali) sangat menarik. Suara mencicit lightsaber, kostum para prajurit, para murid di pulau (Luke akhirnya muncul)...berbeda dari Middle Earth (Kamu berjalan di jalan yang sepi, Oh! Seberapa jauh kamu dari rumah...), Star Wars Dunia menunjukkan filosofi Timur yang misterius di mana-mana.

Setelah menonton filmnya, saya menonton keseluruhan serial Star Wars. Di Star Wars, terdapat animasi subtitle klasik di awal setiap film. Teks kuning mengalir ke depan dalam bentuk trapesium dan berangsur-angsur menghilang. Latar belakangnya adalah langit berbintang yang gelap. Sederhana, namun mengesankan.

<!--more-->

Saat saya sedang mencari informasi kemarin sore, saya tidak sengaja melihat artikel [Pengantar Transformasi 3D CSS3](http://www.w3school.com.cn/css3/css3_3dtransform.asp), dan secara acak saya melihat gambar ini:

![css3_3dtransform](https://wx1.sinaimg.cn/large/73bd9e13ly1fjldo82ostj207c06wglf.jpg)

Tunggu, bukankah ini subtitle Star Wars? Jadi dengan sikap main-main, saya menulis [animasi H5 ini](/blog/projects/star-war.html)。

## Persiapan

- editor teks
- Browser yang mendukung H5
-JQuery
-Taruh Keripik Kentang

Pertama, mari kita buat kanvas hitam dengan ukuran yang sama dengan jendela browser `div.paper`。

{% highlight html %}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title></title>
    <script src="https://cdn.bootcss.com/jquery/2.1.4/jquery.min.js"></script>
</head>
<body>
    <div class="paper">
    </div>
</body>
</html>
{% endhighlight %}

Isi seluruh jendela...

{% highlight css %}
.paper {
    height: 100%;
    width: 100%;
    background-color: black;
}
{% endhighlight %}

Periksa efeknya, seluruh antarmuka pucat...

![Antarmuka pucat](https://wx3.sinaimg.cn/large/73bd9e13ly1fjldo7inddj20l10hp74p.jpg)

![AreYouKiddingMe](https://wx3.sinaimg.cn/large/73bd9e13ly1fjldgnth3cj206404ja9y.jpg)

Melihat elemen antarmuka, Anda dapat menemukannya saat ini `div.paper` dari hight untuk 0, dan tidak seperti yang kami tulis `height: 100%` Itu sama dengan tinggi jendela. Mengapa?

Kita tahu bahwa 100% di sini mengacu pada tinggi relatif terhadap elemen induk 100%，`div.paper` Orang tua dari adalah `body`, dan saat ini `body` Tingginya juga 0, jadi kami menambahkan

{% highlight css %}
body {
    height: 100%;
}
{% endhighlight %}

Periksa efeknya, seluruh antarmuka masih pucat...

![fuuuuuuuu](https://wx1.sinaimg.cn/large/73bd9e13ly1fjldgotoe6j208706oglt.jpg)

Melihat elemen antarmuka, Anda dapat menemukannya saat ini`body` Tingginya masih 0，Dilihat lagi kode HTML diatas, ternyata begitu `body` ada juga `html` elemen, jadi kami menambahkan：

{% highlight html %}
html {
   height: 100%;
}
{% endhighlight %}

Ck ck, pekerjaan besar telah dilakukan. lalu hapus `body` Margin bagian dalam (padding), mari kita lihat efeknya.

![kanvas sempurna](https://wx3.sinaimg.cn/large/73bd9e13ly1fjldo77qxgj20ki0e2q37.jpg)

PERFECT

![Sempurna](https://wx3.sinaimg.cn/large/73bd9e13ly1fjldgn3ycej208y08cwez.jpg)

## Elemen teks seperti konten

Mari tambahkan satu `div#content` elemen sebagai lapisan teks.

{% highlight html %}
<body>
    <div class="paper">
        <div id="content">
            <p>A long time ago, in a galaxy far, far away...</p>
            <br><br>
            <p>Episode IV</p>
            <p>A NEW HOPE</p>
            <p>It is a period of civil war. Rebel spaceships, striking from a hidden base, have won their first victory against the evil Galactic Empire.</p>
            <p>During the battle, Rebel spies managed to steal secret plans to the Empire's ultimate weapon,the DEATH STAR,an armored space station with enough power to destroy an entire planet.</p>
            <p>Pursued by the Empire's sinister agents,Princess Leia races home aboard her starship,custodian of the stolen plans that can save her people and restore freedom galaxy...</p>
        </div>
    </div>
</body>
{% endhighlight %}

Atur font, ukuran font, warna dan pemusatan teks.

{% highlight css %}
body {
    height: 100%;
    padding: 0;
    margin: 0;
    font-family: "lucida grande", "lucida sans unicode", lucida, helvetica, "Hiragino Sans GB", "Microsoft YaHei", "WenQuanYi Micro Hei", sans-serif;
    color: #ffda00;
    font-size: 4em;
    text-align: center;
}
{% endhighlight %}

Mari kita lihat efeknya.

![teks dengan bingkai putih](https://wx2.sinaimg.cn/large/73bd9e13ly1fjldo6rdlwj20ki0e2q3h.jpg)

Pfft...kenapa ada bingkai putih di situ?

![Saya perlu tenang](https://wx1.sinaimg.cn/large/73bd9e13ly1fjldgmnkamj20c809574j.jpg)

Tenang saja lihat elemennya, ternyata penyebab ada kotak putih di atasnya adalah karena margin paragraf `p` pada "Dahulu kala" sudah melewatinya. `div.paper`,tiba `div.paper` di atas, aturan ini disebut**[hamparan margin](http://www.cnblogs.com/snowinmay/archive/2013/04/28/3048997.html)**，Karena marginnya transparan, maka elemen induk dirender `body` putih.

Solusinya sederhana.

1. mempersiapkan `div.paper` Batas bagian dalam, sehingga menjadi margin elemen turunan（margin）Tidak bisa ditembus.

2. Atur warna latar belakang `body`.

Di sini, saya menggunakan metode 2。

### Tambahkan bilah gulir

Atur gaya `content`, tinggi, lebar, posisi tengah, dan tentu saja bilah gulir.

{% highlight css %}
#content {
    box-sizing: border-box;
    margin: 0 auto;
    width: 80%;
    height: 100%;
    overflow: scroll;
}
{% endhighlight %}

Lihatlah efeknya.

![Efek awal pesawat](https://wx4.sinaimg.cn/large/73bd9e13ly1fjldo64ekqj211y0ijjrn.jpg)

Wah, lumayan.

![good](https://wx4.sinaimg.cn/large/73bd9e13ly1fjldvedp06j207p0693zd.jpg)

## Transformasi 3D dengan CSS3

Bagian paling penting ada di sini. Menurut [contoh ini] w3school (http://www.w3school.com.cn/tiy/t.asp?f=css3_perspective1), mewujudkan subtitle 3D seperti Star Wars melibatkan atribut perspektif dan rotasiX。

Mengikuti contoh yang sama, kami menambahkan transformasi 3D ke `body` dan `div.paper`:

{% highlight css %}
body {
    /*Menghilangkan*/
    perspective: 500;
    -webkit-perspective: 500;
}
{% endhighlight %}

{% highlight css %}
.paper {
    /*Menghilangkan*/
    transform: rotateX(60deg);
    -webkit-transform: rotateX(60deg);
}
{% endhighlight %}

Lihatlah efeknya.

![Transformasi 3D 1](https://wx4.sinaimg.cn/large/73bd9e13ly1fjldo5mkrsj20kv0e3wf3.jpg)

good。

## animasi jQuery

Mari tambahkan animasi bersama-sama untuk membuat subtitle bergulir dari awal hingga akhir.

Meskipun CSS3 memiliki kemampuan animasi, saya tetap memilih menggunakan jQuery untuk animasi. (malas……)

Animasi jQuery dilakukan menggunakan fungsi `animate`. Anda hanya perlu memberikan parameter seperti nilai atribut tertentu setelah animasi berakhir dan waktu animasi (tidak wajib), dan Anda dapat membuat animasi untuk parameter ini, silakan merujuk ke [pengantar animasi JQuery w3school] (http: //www.w3school.com.cn/jquery/jquery_animate.asp).

Ada dua properti yang terlibat di sini, [scrollTop](https://developer.mozilla.org/en-US/docs/Web/API/Element/scrollTop) dan [scrollHeight](https://developer.mozilla.org/ id-US/docs/Web/API/Element/scrollHeight).

scrollTop dapat mengontrol tinggi gulir bilah gulir, dan scrollHeight dapat memperoleh tinggi sebenarnya dari konten gulir. Untuk lebih jelasnya anda bisa merujuk ke link diatas yang sangat detail.

Setelah mengetahui fungsi dan atribut `animate` bila diperlukan, saya segera menulis kodenya. Properti `scrollTop` dimulai dari 0 dan berubah menjadi `scrollHeight` dengan kecepatan konstan setelah `scrollHeight * 20` milidetik.

{% highlight js %}
$(function(){
    var scrollHeight = $("#content")[0].scrollHeight;
    var scrollTop = $("#content")[0].scrollTop;
    $("#content").animate({scrollTop: scrollHeight}, scrollHeight * 20, "linear");
};
{% endhighlight %}

Terakhir, sembunyikan bilah gulir。

{% highlight css %}
#content {
    /*Menghilangkan*/
    overflow: hidden;
}
{% endhighlight %}

![Transformasi 3D 2](https://wx3.sinaimg.cn/large/73bd9e13ly1fjldo56n7jj211y0ijtc8.jpg)

Nah, Anda sudah selesai. Namun masih ada beberapa kendala, seharusnya tidak ada teks di awal. Kita dapat menambahkan spasi di awal `div#content`.

{% highlight html %}
<div class="content">
    <div class="empty-content top"></div>
    <p>A long time ago, in a galaxy far, far away...</p>
    ...
{% endhighlight %}

{% highlight css %}
.empty-content {
    box-sizing: border-box;
    width: 100%;
    height: 100%;
}
{% endhighlight %}

Cukup banyak. Tentu saja kita juga bisa menambahkan background gambar dan musik latar. Saya tidak akan melakukannya di sini…

[Demo animasi](/projects/demo/star-wars-opening-crawl/) |
[Kode sumber](https://github.com/rian010/kitian616.github.io/blob/master/projects/demo/star-wars-opening-crawl/index.html)

![Yoda](https://wx1.sinaimg.cn/large/73bd9e13ly1fjldo4fv1nj20b404qglq.jpg)