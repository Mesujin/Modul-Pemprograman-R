<div align="center">
<h1> Modul Pemprograman Bahasa R </h2>
Di translate oleh Ilman M a.k.a. Mesujin
</div>

## Bab 1 - Pengenalan R
#### 1. Penginstallasian Dasar Untuk R
Hal pertama yang harus dilakukan ialah menginstall bahasa pemprograman yakni "R". R adalah bahasa pemprograman yang tersedia secara gratis untuk OS Windows, Mac, dan juga Linux yang disediakan oleh situs [Comprehensive R Archive Network (CRAN)](https://cloud.r-project.org/). Untuk pengguna Windows dan Mac, kami menyarankan untuk mengunduh dan menginstal versi "pre-compiled binary" nya.

#### 1.1 Untuk pengguna Windows
Untuk pengguna Windows, pilih "Download R for Windows" pada situs yang telah dijelaskan, selanjutnya pilih "base" kemudian pilih "Download R-4.3.2 for Windows" untuk link pengunduhannya. Sebuah file yang ber-extensi ".exe" seharusnya akan mulai terunduh. Setelah pengunduhannya selesai, jalankan atau buka file tersebut dan ikuti perintah yang akan muncul. Instruksi lengkap terkait instalasi dapat di jumpai di situs CRAN.

Atau dapat menggunakan link berikut ;
> https://cloud.r-project.org/bin/windows/base/R-4.3.2-win.exe

#### 1.2 Pengetesan R
Terlepas dari OS apa yang sedang kamu gunakan, setelah R terinstal, pastikan untuk mengeceknya apakah aplikasinya bekerja dengan baik. Cara yang paling sederhana ialah dengan menjalankan aplikasi R tersebut (untuk Windows atau Mac) atau dengan mengetik R ke konsol yang ada (untuk Linux). "R Console" seharusnya akan muncul dan kamu bisa memasukan komando-komando R ke konsol tersebut setelah huruf ">". Coba masukan kode R berikut kemudian tekan Enter (jangan khawatir jika kamu tidak mengerti kode berikut - ini hanya untuk memastikan saja).

R Script :
```R
plot(1:10)
```
Result :<br>
<div align="center"><img src="/Assets/plot(1-10).png" alt="Result for the code." style="height:400px; width:400px;"/></div>
<br>
Sebuah "plot" dengan nilai dari 1 hingga 10 pada kedua x dan y seharusnya muncul. Jika "window" tersebut muncul, maka aplikasi R tersebut berjalan dengan baik, jika tidak, kami menyarankan untuk mencari catatan hasil dari "error" yang muncul di Google untuk menindaklanjuti masalah yang ada.

#### 2. Menginstal RStudio

Walaupun hanya dengan menggunakan installasi dasar saja sebenarnya cukup, kita akan menggunakan sebuah Integrated Development Envoriment (IDE) yang cukup terkenal yakni RStudio. Kamu bisa anggap RStudio sebagai tambahan karena memiliki tampilan yang lebih mudah dipahami, penggabunggan konsol R, "script editor", dan fungsi berguna lainnya (seperti R Markdown dan penghubungan ke GitHub).

RStudio tersedia gratis untuk OS Windows, Mac, dan Linux yang dapat diunduh dari situs [RStudio](https://posit.co/download/rstudio-desktop/). Pilihlah versi "RStudio Desktop". Perlu dicatat bahwa R harus diinstal sebelumnya (lihat bagian sebelumnya untuk detailnya).

#### 2.1 Untuk Pengguna Windows
Untuk Windows, kamu seharusnya akan melihat link yang jelas untuk pengunduhan. Atau gunakan link berikut untuk pengunduhannya ;

> https://download1.rstudio.org/electron/windows/RStudio-2023.12.1-402.exe

Jika pada situs RStudio tidak muncul versi "RStudio Desktop", scroll ke bawah pada bagian "All Installers".

#### 2.2 Pengetesan RStudio
Setelah terinstall, kamu bisa mengecek apakah semuanya berjalan lancar atau tidak dengan menjalankan RStudio (tidak perlu menjalankan R juga, cukup RStudio). Kamu seharusnya dapat melihat tampilan seperti gambar dibawah (akan ada sedikit perbedaan jika kamu menggunakan OS Linux atau Mac.).
<br>
<div align="center"><img src="/Assets/RStudio.png" alt="RStudio's main interface." style="height:400px; width:600px;"/></div>

#### 3. Pengelnalan RStudio
Ketika kamu membuka RStudio untuk pertama kalinya, kamu seharusnya dapat melihat tampilan seperti gambar dibawah (akan sedikit berbeda untuk pengguna OS Mac dan Linux).
<br>
<div align="center"><img src="/Assets/RStudio.png" alt="RStudio's main interface." style="height:400px; width:600px;"/></div><br>

Window yang besar (atau dikenal "pane") pada bagian kiri adalah Konsol. "Pane" pada bagian kanan atas adalah untuk "Environment" / "History" / "Connection" dan dibagian bawahnya adalah untuk "Files" / "Plots" / "Packages" / "Help" / "Help". Setiap "pane" atau window-nya akan dibahas secara bertahap dibawah. Letak posisi setiap "pane"-nya dapat kamu kostumisasi semaumu dengan mengklik pada menu "Tools" kemudian "Global Options" -> "Pane Layout". Kamu juga bisa mengatur ukurannya dengan mengklik bagian ujung "pane"-nya kemudian menggesernya kearah yang kamu mau. Masih ada banyak cara lain untuk mengkostumisasi tampilan RStudio.

#### 3.1 R Konsol
Konsol adalah bagian untukmu melakukan pekerjaan atau menjalan perintah/komando yang ada di R. Dibagian ini R akan mengevaluasi/membaca semua kode yang kamu tulis. Kamu bisa menuliskan secara langsung kode R didepan "command line prompt" yang disimbolkan dengan `>`. Sebagai contoh, jika kamu mengetik `2 + 2` kedalam konsol tersebut kemudian Enter atau jalankan kodenya, akan muncul jawaban `4`. Jangan khawatir tentang `[1]` yang akan muncul, itu hanya penanda awal barisan.
<br>
<div align="center"><img src="/Assets/2+2.png" alt="RStudio's main interface." style="height:200px; width:350px;"/></div><br>


## Bab 2 - Dasar-dasar Bahasa Pemprograman R
Pada bab ini, akan dikenalkan bagaimana menggunakan R dan RStudio untuk menjalankan hal-hal mendasar dari R seperti membuat "Object" dan memberi nilai kepada "Object", mengekplorasi jenis-jenis "Object" dan menjalankan beberapa operasi dasar pada "Object". Kita juga akan belajar bagaimana bertanya perihal R dan mendapatkan beberapa sumber yang mampu membantumu dalam mempelajari R. Tidak lupa, cara bagaimana menyimpan hasil kerja mu.

Sebelum kita melanjutkan ke materi, ada beberapa hal yang harus kamu perhatikan di bab ini :
> R merupakan bahasa pemerograman yang memperhatikan huruf-hurufnya, dengan kata lain `A` tidak sama dengan `a` yang mana `anova` tidak sama dengan `Anova`.

Apapun yang ada setelah simbol `#` tidak akan dianggap oleh R atau disebut sebagai komentar di dalam kode. Sebuah komentar seharusnya berfungsi sebagai bahan untuk mengungkapkan pendapat atau sebagai informasi baik untuk dirimu sendiri atau orang lain. Menulis komentar merupakan sebuah `art` dan sesuatu yang seharusnya menjadi kebiasaan kedepannya.

>Dalam R, pada dasarnya setiap perintah atau komando akan dipisah oleh barisan baru. Tetapi titik koma `;` juga bisa berfungsi untuk memisahkan setiap perintah atau komando mu, walaupun jarang digunakan.

Jika ada "continuation prompt" yang disimbolkan dengan `+` pada konsol mu, itu berarti kamu belum menyelesaikan kode mu dengan benar. Hal ini biasanya terjadi jika kamu lupa mengakhiri buka kurung `{` dengan tutup kurung `}` akibat menumpuk tanda tersebut seperti `{{{{beberapa kode}}}}`. cukup selesaikan perintah atau komando nya pada baris baru dan perbaiki "typo" mu atau tekan "Esc" pada keyboard mu (perhatikan kalimat dibawah) lalu perbaiki.

>Pada dasarnya, R cukup mentolelir spasi-spasi berlebihan yang ada pada kode mu, pada kenyataanya menggunakan spasi yang banyak adalah hal yang baik. Meskipun begitu, spasi tersebut tidak boleh dimasukkan kedalam operator, dengan kata lain "` <-`" tidak boleh dibaca seperti "`<-`" (perhatikan spasinya). Silakan cari di Google terkait "style guide" untuk bantuan mengenai peletakan spasi pada kode mu sehingga kode mu mudah dibaca.

Jika konsol mu "hangs" dan menjadi "unresponsive" setelah atau ketika menjalankan beberapa kode, tekan "Esc" pada keyboard mu untuk menghindari masalah tersebut, atau bisa juga dengan menekan ikon "Stop" yang ada pada bagian atas konsol. Hal ini akan men-"Terminate" operasi-operasi yang sedang berjalan.

#### 1. Cara Kerja
Pada bagian "Editor"

<br>
<br>
