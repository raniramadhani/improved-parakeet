﻿# EMT untuk Perhitungan Aljabar
Pada notebook ini Anda belajar menggunakan EMT untuk melakukan
berbagai perhitungan terkait dengan materi atau topik dalam Aljabar.
Kegiatan yang harus Anda lakukan adalah sebagai berikut:


* 
Membaca secara cermat dan teliti notebook ini;

* 
Menerjemahkan teks bahasa Inggris ke bahasa Indonesia;

* 
Mencoba contoh-contoh perhitungan (perintah EMT) dengan cara
* meng-ENTER setiap perintah EMT yang ada (pindahkan kursor ke baris
* perintah)

* 
Jika perlu Anda dapat memodifikasi perintah yang ada dan memberikan
* keterangan/penjelasan tambahan terkait hasilnya.

* 
Menyisipkan baris-baris perintah baru untuk mengerjakan soal-soal
* Aljabar dari file PDF yang saya berikan;

* 
Memberi catatan hasilnya.

* 
Jika perlu tuliskan soalnya pada teks notebook (menggunakan format
* LaTeX).

* 
Gunakan tampilan hasil semua perhitungan yang eksak atau simbolik
* dengan format LaTeX. (Seperti contoh-contoh pada notebook ini.)


## Contoh pertama

Menyederhanakan bentuk aljabar:


\>$&6\*x^(-3)\*y^5\*-7\*x^2\*y^(-9)


Menjabarkan:


\>$&showev('expand((6\*x^(-3)+y^5)\*(-7\*x^2-y^(-9))))


## Baris Perintah

Baris perintah Euler terdiri dari satu atau beberapa perintah Euler
yang diikuti dengan titik koma ";" atau koma ",". Titik koma mencegah
pencetakan hasil. Koma setelah perintah terakhir dapat dihilangkan.


Baris perintah berikut ini hanya akan mencetak hasil dari ekspresi,
bukan penugasan atau perintah fotmat.


\>r:=2; h:=4; pi\*r^2\*h/3


    16.7551608191

Perintah harus dipisahkan dengan spasi. Baris perintah berikut ini
mencetak dua hasilnya.


\>pi\*2\*r\*h, %+2\*pi\*r\*h // Ingat tanda % menyatakan hasil perhitungan terakhir sebelumnya


    50.2654824574
    100.530964915

Baris perintah dieksekusi sesuai urutan pengguna menekan tombol
return. Jadi, anda mendapatkan nilai baru setiap kali mengeksekusi
baris kedua.


\>x := 1;

\>x := cos(x) // nilai cosinus (x dalam radian)


    0.540302305868

\>x := cos(x)


    0.857553215846

Jika dua baris dihubungkan dengan "...", kedua baris tersebut akan
selalu dieksekusi secara bersamaan.


\>x := 1.5; ...  
\>   x := (x+2/x)/2, x := (x+2/x)/2, x := (x+2/x)/2, 


    1.41666666667
    1.41421568627
    1.41421356237

Ini juga merupakan cara yang baik untuk membagi perintah yang panjang
menjadi dua baris atau lebih. Anda dapat menekan Ctrl+Return untuk
membagi baris menjadi dua pada posisi kursor saat ini, atau Ctlr+Back
untuk menggabungkan baris-baris tersebut.


Untuk melipat semua garis yang ada tekan Ctrl+L. Maka garis-garis
berikutnya hanya akan terlihat jika salah satu dari garis-garis
tersebut menjadi fokus. Untuk melipat satu baris ganda, mulailah baris
pertama dengan "%+".


\>%+ x=4+5; ...  
\>    // garis ini tidak akan terlihat setelah kursor keluar dari garisThis line will not be visible once the cursor is off the line


Baris yang dimulai dengan %% tidak akan terlihat sama sekali.


    81

Euler mendukung perulangan dalam baris perintah, asalkan dapat
dimasukkan ke dalam satu baris atau beberapa baris. Dalam program,
pembatasan ini tentu saja tidak berlaku. Untuk informasi lebih lanjut,
lihat pengantar berikut.


\>x=1; for i=1 to 5; x := (x+2/x)/2, end; // menghitung akar 2


    1.5
    1.41666666667
    1.41421568627
    1.41421356237
    1.41421356237

Tidak apa-apa menggunakan beberapa baris. Pastikan baris diakhiri
dengan "...".


\>x := 1.5; // komentar pergi ke sini sebelum ...  
\>   repeat xnew:=(x+2/x)/2; until xnew~=x; ...  
\>      x := xnew; ...  
\>   end; ...  
\>   x,


    1.41421356237

Struktur kondisional juga berfungsi.


\>if E^pi\>pi^E; then "Thought so!", endif;


    Thought so!

Saat menjalankan perintah,kursor dapat berada di posisi mana pun di
baris perintah. Anda dapat kembali ke perintah sebelumnya atau
melompat ke perintah berikutnya dengan tombol panah. Atau Anda dapat
mengeklik bagian komentar di atas perintah untuk membuka perintah
tersebut.


Saat menggerakkan kursor di sepanjang baris, pasangan tanda kurung
buka dan tutup akan disorot. Perhatikan juga baris status. Setelah
tanda kurung buka fungsi sqrt(), baris status akan menampilkan teks
bantuan untuk fungsi tersebut. Jalankan perintah dengan tombol return.


\>sqrt(sin(10°)/cos(20°))


    0.429875017772

Untuk melihat bantuan untuk perintah terbaru, buka jendela bantuan
dengan F1. Di sana, Anda dapat memasukkan teks yang ingin dicari. Pada
baris kosong, bantuan untuk jendela bantuan akan ditampilkan. Anda
dapat menekan escape untuk menghapus baris, atau untuk menutup jendela
bantuan.


Anda dapat mengklik dua kali pada perintah apa pun untuk membuka
bantuan untuk perintah ini. Coba klik dua kali perintah expand di
bawah pada baris perintah.


\>exp(log(2.5))


    2.5

Anda juga dapat menyalin dan menempel di Euler. Gunakan Ctrl-C dan
Ctrl-V untuk ini. Untuk menandai teks, seret mouse atau gunakan shift
bersamaan dengan tombol kursor apa pun. Selain itu, Anda dapat
menyalin tanda kurung yang disorot.


## Sintaksis Dasar

Euler mengetahui fungsi matematika yang umum. Seperti yang telah Anda
lihat di atas, fungsi trigonometri bekerja dalam radian atau derajat.
Untuk mengonversi ke derajat, tambahkan simbol derajat (dengan tombol
F7) ke nilai, atau gunakan fungsi rad(x). Fungsi akar kuadrat disebut
sqrt dalam Euler. Tentu saja, x^(1/2) juga memungkinkan.


Untuk mengatur variabel, gunakan "=" atau ":=". Demi kejelasan,
pengantar ini menggunakan bentuk yang terakhir. Spasi tidak menjadi
masalah. Namun, spasi di antara perintah diharapkan.


Beberapa perintah dalam satu baris dipisahkan dengan "," atau ";".
Tanda titik koma menghilangkan keluaran perintah. Di akhir baris
perintah, tanda "," diasumsikan, jika ";" tidak ada.


\>g:=9.81; t:=2.5; 1/2\*g\*t^2


    30.65625

EMT menggunakan sintaks pemrograman untuk ekspresi. Untuk  memasukkan


Anda harus menetapkan tanda kurung yang benar dan menggunakan / untuk
pecahan. Perhatikan tanda kurung yang disorot untuk mendapatkan
bantuan. Perhatikan bahwa konstanta Euler e diberi nama E dalam EMT.


\>E^2\*(1/(3+4\*log(0.6))+1/7)


    8.77908249441

Untuk menghitung ekspresi rumit seperti


Anda perlu memasukkannya dalam formulir baris.


\>((1/7 + 1/8 + 2) / (1/3 + 1/2))^2 \* pi


    23.2671801626

Letakkan tanda kurung di sekitar sub-ekspresi yang perlu dihitung
terlebih dahulu dengan hati-hati. EMT membantu Anda dengan menyorot
ekspresi yang diakhiri tanda kurung tutup. Anda juga harus memasukkan
nama "pi" untuk huruf Yunani pi.




Hasil perhitungan ini adalah angka floating point. Angka ini dicetak
dengan akurasi sekitar 12 digit secara default.


Pada baris perintah berikut, kita juga mempelajari cara merujuk ke
hasil sebelumnya dalam baris yang sama.


\>1/3+1/7, fraction %


    0.47619047619
    10/21

Perintah Euler dapat berupa ekspresi atau perintah primitif. Ekspresi
terdiri dari operator dan fungsi. Jika perlu, ekspresi harus berisi
tanda kurung untuk memaksakan urutan eksekusi yang benar. Jika ragu,
sebaiknya gunakan tanda kurung. Perhatikan bahwa EMT menampilkan tanda
kurung buka dan tutup saat mengedit baris perintah


\>(cos(pi/4)+1)^3\*(sin(pi/4)+1)^2


    14.4978445072

Operator numerik Euler meliputi


 + unary or operator plus  
 - unary or operator minus  
 *, /  
 . the matrix product  
 a^b power for positive a or integer b (a**b works too)  
 n! the factorial operator  

dan masih banyak lagi.


Berikut ini beberapa fungsi yang mungkin Anda perlukan. Masih banyak
lagi.


 sin,cos,tan,atan,asin,acos,rad,deg  
 log,exp,log10,sqrt,logbase  
 bin,logbin,logfac,mod,floor,ceil,round,abs,sign  
 conj,re,im,arg,conj,real,complex  
 beta,betai,gamma,complexgamma,ellrf,ellf,ellrd,elle  
 bitand,bitor,bitxor,bitnot  

Beberapa perintah memiliki aliasi, misalnya ln untuk log.


\>ln(E^2), arctan(tan(0.5))


    2
    0.5

\>sin(30°)


    0.5

Pastikan untuk menggunakan tanda kurung (kurung bundar), jika ada
keraguan tentang urutan eksekusi! Berikut ini tidak sama dengan
(2^3)^4, yang merupakan default untuk 2^3^4 dalam EMT (beberapa sistem
numerik melakukannya dengan cara lain).


\>2^3^4, (2^3)^4, 2^(3^4)


    2.41785163923e+24
    4096
    2.41785163923e+24

## Bilangan Riil

Tipe data utama dalam Euler adalah bilangan riil. Bilangan riil
direpresentasikan dalam format IEEE dengan akurasi sekitar 16 digit
desimal.


\>longest 1/3


         0.3333333333333333 

Representasi ganda internal membutuhkan 8 byte.


\>printdual(1/3)


    1.0101010101010101010101010101010101010101010101010101*2^-2

\>printhex(1/3)


    5.5555555555554*16^-1

## String

Suatu string dalam Euler didefinisikan dengan "...".


\>"Suatu string dapat berisi apa saja."


    Suatu string dapat berisi apa saja.

String dapat dirangkai dengan | atau dengan +. Ini juga berlaku untuk
angka, yang dalam kasus tersebut diubah menjadi string.


\>"The area of the circle with radius " + 2 + " cm is " + pi\*4 + " cm^2."


    The area of the circle with radius 2 cm is 12.5663706144 cm^2.

Fungsi cetak juga mengonversi angka menjadi string. Fungsi ini dapat
memuat sejumlah digit dan sejumlah tempat (0 untuk keluaran padat),
dan optimalnya satu unit.


\>"Golden Ratio : " + print((1+sqrt(5))/2,5,0)


    Golden Ratio : 1.61803

Ada string khusus none, yang tidak dicetak. String ini dikembalikan
oleh beberapa fungsi, ketika hasilnya tidak penting. (Dikembalikan
secara otomatis, jika fungsi tersebut tidak memiliki pernyataan
return.)


\>none


Untuk mengubah string menjadi angka, cukup evaluasi string tersebut.
Ini juga berlaku untuk ekspresi (lihat di bawah).


\>"1234.5"()


    1234.5

Untuk mendefinisikan vektor string, gunakan notasi vektor [...]


\>v:=["affe","charlie","bravo"]


    affe
    charlie
    bravo

Vektor string kosong dilambangkan dengan [none]. Vektor string dapat
dirangkai.


\>w:=[none]; w|v|v


    affe
    charlie
    bravo
    affe
    charlie
    bravo

String dapat berisi karakter Unicode. Secara internal, string ini
berisi kode UTF-8. Untuk membuat string seperti itu, gunakan u"..."
dan salah satu entitas HTML.


String Unicode dapat dirangkai seperti string lainnya.


\>u"&alpha; = " + 45 + u"&deg;" // pdfLaTeX mungkin gagal menampilkan secara benar


    α = 45°

I


Dalam komentar, entitas yang sama seperti alpha, beta, dll. dapat
digunakan. Ini mungkin merupakan alternatif cepat untuk Lateks.
(Rincian lebih lanjut pada komentar di bawah).


Ada beberapa fungsi untuk membuat atau menganalisis string unicode.
Fungsi strtochar() akan mengenali string Unicode dan  menerjemahkannya
dengan benar.


\>v=strtochar(u"&Auml; is a German letter")


    [196,  32,  105,  115,  32,  97,  32,  71,  101,  114,  109,  97,  110,
    32,  108,  101,  116,  116,  101,  114]

Hasilnya adalah vektor angka Unicode. Fungsi kebalikannya adalah
chartoutf().


\>v[1]=strtochar(u"&Uuml;")[1]; chartoutf(v)


    Ü is a German letter

Fungsi utf() dapat menerjemahkan string dengan entitas dalam variabel
menjadi string Unicode.


\>s="We have &alpha;=&beta;."; utf(s) // pdfLaTeX mungkin gagal menampilkan secara benar


    We have α=β.

Dimungkinkan juga untuk menggunakan entitas numerik.


\>u"&#196;hnliches"


    Ähnliches

## Nilai Boolean 

Nilai Boolean direpresentasikan dengan 1=benar atau 0=salah dalam
Euler. String dapat dibandingkan, seperti halnya angka.


\>2<1, "apel"<"banana"


    0
    1

"and" adalah operator "&amp;&amp;" dan "or" adalah operator "||", seperti
dalam bahasa C. (Kata "and" dan "or" hanya dapat digunakan dalam
kondisi "if".)


\>2<E && E<3


    1

Operator Boolean mematuhi aturan bahasa matriks.


\>(1:10)\>5, nonzeros(%)


    [0,  0,  0,  0,  0,  1,  1,  1,  1,  1]
    [6,  7,  8,  9,  10]

Anda dapat menggunakan fungsi nonzeros() untuk mengekstrak elemen
tertentu dari sebuah vektor. Dalam contoh ini, kami  menggunakan
kondisional isprime(n).


\>N=2|3:2:99 // N berisi elemen 2 dan bilangan2 ganjil dari 3 s.d. 99


    [2,  3,  5,  7,  9,  11,  13,  15,  17,  19,  21,  23,  25,  27,  29,
    31,  33,  35,  37,  39,  41,  43,  45,  47,  49,  51,  53,  55,  57,
    59,  61,  63,  65,  67,  69,  71,  73,  75,  77,  79,  81,  83,  85,
    87,  89,  91,  93,  95,  97,  99]

\>N[nonzeros(isprime(N))] //pilih anggota2 N yang prima


    [2,  3,  5,  7,  11,  13,  17,  19,  23,  29,  31,  37,  41,  43,  47,
    53,  59,  61,  67,  71,  73,  79,  83,  89,  97]

## Format Keluaran

Format keluaran default EMT mencetak 12 digit. Untuk memastikan bahwa
kita melihat default, kita mengatur ulang formatnya.


\>defformat; pi


    3.14159265359

Secara internal, EMT menggunakan standar IEEE untuk angka ganda dengan
sekitar 16 digit desimal. Untuk melihat jumlah digit lengkap, gunakan
perintah "longestformat", atau kami menggunakan operator "longest"
untuk menampilkan hasil dalam format terpanjang.


\>longest pi


          3.141592653589793 

Berikut adalah representasi heksadesimal internal dari angka ganda.


\>printhex(pi)


    3.243F6A8885A30*16^0

Format keluaran dapat diubah secara permanen dengan perintah format.


\>format(12,5); 1/3, pi, sin(1)


        0.33333 
        3.14159 
        0.84147 

Format defaulnya adalah (12).


\>format(12); 1/3


    0.333333333333

Fungsi seperti "shortestformat", "shortformat", "longformat" bekerja
untuk vektor dengan cara berikut.


\>shortestformat; random(3,8)


      0.66    0.2   0.89   0.28   0.53   0.31   0.44    0.3 
      0.28   0.88   0.27    0.7   0.22   0.45   0.31   0.91 
      0.19   0.46  0.095    0.6   0.43   0.73   0.47   0.32 

Format default untuk skalar adalah format(12). Namun, ini dapat
diubah.


\>setscalarformat(5); pi


    3.1416

Fungsi "longestformat" juga mengatur format skalar.


\>longestformat; pi


    3.141592653589793

Sebagai referensi, berikut adalah daftar format keluaran yang paling
penting.


shortestformat  shortformat longformat, longestformat 


format(length,digits) goodformat(length)


fracformat(length)


defformat 


Akurasi internal EMT adalah sekitar 16 tempat desimal, yang merupakan
standar IEEE. Angka-angka disimpan dalam format internal ini.


Namun format keluaran EMT dapat diatur secara fleksibel.


\>longestformat; pi,


    3.141592653589793

\>format(10,5); pi


      3.14159 

Standarnya adalah defformat().


\>defformat; // default


Ada operator pendek yang hanya mencetak satu nilai. Operator
"terpanjang" akan mencetak semua digit angka yang valid.


\>longest pi^2/2


          4.934802200544679 

Ada juga operator pendek untuk mencetak hasil dalam format pecahan.
Kami telah menggunakannya di atas.


\>fraction 1+1/2+1/3+1/4


    25/12

Karena format internal menggunakan cara biner untuk menyimpan angka,
nilai 0,1 tidak akan terwakili secara tepat. Kesalahannya bertambah
sedikit, seperti yang Anda lihat dalam perhitungan berikut.


\>longest 0.1+0.1+0.1+0.1+0.1+0.1+0.1+0.1+0.1+0.1-1


     -1.110223024625157e-16 

Namun dengan "longformat" default, Anda tidak akan melihat hal ini.
Demi kenyamanan, output angka yang sangat kecil adalah 0.


\>0.1+0.1+0.1+0.1+0.1+0.1+0.1+0.1+0.1+0.1-1


    0

# Ekspresi

String atau nama dapat digunakan untuk menyimpan ekspresi matematika,
yang dapat dievaluasi oleh EMT. Untuk ini, gunakan tanda kurung
setelah ekspresi. Jika Anda ingin menggunakan string sebagai ekspresi,
gunakan konvensi untuk menamainya "fx" atau "fxy", dst. Ekspresi lebih
diutamakan daripada fungsi.


Variabel global dapat digunakan dalam evaluasi.


\>r:=2; fx:="pi\*r^2"; longest fx()


          12.56637061435917 

Parameter ditetapkan ke x, y, dan z dalam urutan tersebut. Parameter
tambahan dapat ditambahkan menggunakan parameter yang ditetapkan.


\>fx:="a\*sin(x)^2"; fx(5,a=-1)


    -0.919535764538

Perhatikan bahwa ekspresi akan selalu menggunakan variabel global,
bahkan jika ada variabel dalam suatu fungsi dengan nama yang sama.
(Jika tidak, evaluasi ekspresi dalam fungsi dapat memberikan hasil
yang sangat membingungkan bagi pengguna yang memanggil fungsi
tersebut.)


\>at:=4; function f(expr,x,at) := expr(x); ...  
\>   f("at\*x^2",3,5) // computes 4\*3^2 not 5\*3^2


    36

Jika Anda ingin menggunakan nilai lain untuk "at" selain nilai global,
Anda perlu menambahkan "at=value".


\>at:=4; function f(expr,x,a) := expr(x,at=a); ...  
\>   f("at\*x^2",3,5)


    45

Sebagai referensi, kami mencatat bahwa koleksi panggilan (dibahas di
tempat lain) dapat berisi ekspresi. Jadi, kita dapat membuat contoh di
atas sebagai berikut.


\>at:=4; function f(expr,x) := expr(x); ...  
\>   f({{"at\*x^2",at=5}},3)


    45

Ekspresi dalam x sering digunakan seperti fungsi.


Perhatikan bahwa mendefinisikan fungsi dengan nama yang sama seperti
ekspresi simbolik global akan menghapus variabel ini untuk menghindari
kebingungan antara ekspresi simbolik dan fungsi.


\>f &= 5\*x;

\>function f(x) := 6\*x;

\>f(2)


    12

Berdasarkan konvensi, ekspresi simbolik atau numerik harus diberi nama
fx, fxy, dst. Skema penamaan ini tidak boleh digunakan untuk fungsi.


\>fx &= diff(x^x,x); $&fx


Bentuk khusus dari suatu ekspresi memperbolehkan variabel apa pun
sebagai parameter tanpa nama untuk evaluasi ekspresi, bukan  hanya
"x", "y", dst. Untuk ini, awali ekspresi dengan "@(variabel)...".


\>"@(a,b) a^2+b^2", %(4,5)


    @(a,b) a^2+b^2
    41

Hal ini memungkinkan untuk memanipulasi ekspresi dalam variabel lain
untuk fungsi EMT yang memerlukan ekspresi dalam "x".


Cara paling mendasar untuk mendefinisikan fungsi sederhana adalah
dengan menyimpan rumusnya dalam ekspresi simbolik atau  numerik. Jika
variabel utamanya adalah x, ekspresi tersebut dapat dievaluasi seperti
halnya fungsi.


Seperti yang Anda lihat dalam contoh berikut, variabel global terlihat
selama evaluasi.


\>fx &= x^3-a\*x;  ...  
\>   a=1.2; fx(0.5)


    -0.475

Semua variabel lain dalam ekspresi dapat ditentukan dalam evaluasi
menggunakan parameter yang ditetapkan.


\>fx(0.5,a=1.1)


    -0.425

Suatu ekspresi tidak harus bersifat simbolis. Hal ini diperlukan jika
ekspresi tersebut mengandung fungsi-fungsi yang hanya diketahui dalam
kernel numerik, bukan dalam Maxima.


# Matematika Simbolik

EMT mengerjakan matematika simbolik dengan bantuan Maxima. Untuk
detailnya, mulailah dengan tutorial berikut, atau telusuri referensi
untuk Maxima. Para ahli di Maxima harus memperhatikan bahwa ada
perbedaan dalam sintaksis antara sintaksis asli Maxima dan  sintaksis
default ekspresi simbolik di EMT.


Matematika simbolik terintegrasi dengan lancar ke dalam Euler dengan
&amp;. Ekspresi apa pun yang dimulai dengan &amp; adalah ekspresi simbolik.
Ekspresi ini dievaluasi dan dicetak oleh Maxima.


Pertama-tama, Maxima memiliki aritmatika "tak terbatas" yang dapat
menangani angka yang sangat besar.


\>$&44!


Dengan cara ini, Anda dapat menghitung hasil yang besar secara tepat.
Mari kita hitung


\>$& 44!/(34!\*10!) // nilai C(44,10)


Tentu saja, Maxima memiliki fungsi yang lebih efisien untuk ini
(seperti halnya bagian numerik EMT).


\>$binomial(44,10) //menghitung C(44,10) menggunakan fungsi binomial()


Untuk mempelajari lebih lanjut tentang fungsi tertentu, klik dua kali
pada fungsi tersebut. Misalnya, coba klik dua kali pada "&amp;binomial"
pada baris perintah sebelumnya. Ini akan membuka dokumentasi Maxima
sebagaimana disediakan oleh penulis program tersebut.


Anda akan mempelajari bahwa hal berikut juga berfungsi


\>$binomial(x,3) // C(x,3)


Jika Anda ingin mengganti x dengan nilai tertentu gunakan "with".


\>$&binomial(x,3) with x=10 // substitusi x=10 ke C(x,3)


Dengan cara itu Anda dapat menggunakan solusi suatu persamaan dalam
persamaan lainnya.


Ekspresi simbolik dicetak oleh Maxima dalam bentuk 2D. Alasannya
adalah adanya bendera simbolik khusus dalam string.


Seperti yang telah Anda lihat pada contoh sebelumnya dan berikut, jika
Anda telah menginstal LaTeX, Anda dapat mencetak ekspresi simbolik
dengan Latex. Jika tidak, perintah berikut akan menampilkan pesan
kesalahan.


Untuk mencetak ekspresi simbolik dengan LaTeX, gunakan $ di depan &amp;
(atau Anda dapat menghilangkan &amp;) sebelum perintah. Jangan jalankan
perintah Maxima dengan $, jika Anda tidak menginstal LaTeX.


\>$(3+x)/(x^2+1)


Ekspresi simbolik diurai oleh Euler. Jika Anda memerlukan sintaksis
yang kompleks dalam satu ekspresi, Anda dapat melampirkan ekspresi
tersebut dalam "...". Menggunakan lebih dari satu ekspresi sederhana
dimungkinkan, tetapi sangat tidak disarankan.


\>&"v := 5; v^2"


    
                                      25
    

Untuk kelengkapan, kami mencatat bahwa ekspresi simbolik dapat
digunakan dalam program, tetapi harus disertakan dalam tanda  kutip.
Selain itu, akan jauh lebih efektif untuk memanggil Maxima pada waktu
kompilasi jika memungkinkan.


\>$&expand((1+x)^4), $&factor(diff(%,x)) // diff: turunan, factor: faktor


Sekali lagi, % mengacu pada hasil sebelumnya.


Untuk mempermudah, kami menyimpan solusi ke variabel simbolik.
Variabel simbolik didefinisikan dengan "&amp;=".


\>fx &= (x+1)/(x^4+1); $&fx


Ekspresi simbolik dapat digunakan dalam ekspresi simbolik lainnya.


\>$&factor(diff(fx,x))


Input langsung perintah Maxima juga tersedia. Awali baris perintah
dengan "::". Sintaks Maxima disesuaikan dengan sintaks EMT (disebut
"mode kompatibilitas").


\>&factor(20!)


    
                             2432902008176640000
    

\>::: factor(10!)


    
                                   8  4  2
                                  2  3  5  7
    

\>:: factor(20!)


    
                            18  8  4  2
                           2   3  5  7  11 13 17 19
    

Jika Anda ahli dalam Maxima, Anda mungkin ingin menggunakan sintaksis
asli Maxima. Anda dapat melakukannya dengan ":::".


\>::: av:g$ av^2;


    
                                       2
                                      g
    

\>fx &= x^3\*exp(x), $fx


    
                                     3  x
                                    x  E
    

Variabel tersebut dapat digunakan dalam ekspresi simbolik lainnya.
Perhatikan bahwa dalam perintah berikut sisi kanan &amp;= dievaluasi
sebelum penugasan ke Fx.


\>&(fx with x=5), $%, &float(%)


    
                                         5
                                    125 E
    
    
                              18551.64488782208
    

\>fx(5)


    18551.6448878

Untuk mengevaluasi suatu ekspresi dengan nilai variabel tertentu, Anda
dapat menggunakan operator "with".


Baris perintah berikut juga menunjukkan bahwa Maxima dapat
mengevaluasi ekspresi secara numerik dengan float().


\>&(fx with x=10)-(fx with x=5), &float(%)


    
                                    10        5
                              1000 E   - 125 E
    
    
                             2.20079141499189e+7
    

\>$factor(diff(fx,x,2))


Untuk mendapatkan kode Latex untuk suatu ekspresi, Anda dapat
menggunakan perintah tex.


\>tex(fx)


    x^3\,e^{x}

Ekspresi simbolik dapat dievaluasi seperti halnya ekspresi numerik.


\>fx(0.5)


    0.206090158838

Dalam ekspresi simbolik, ini tidak berfungsi, karena Maxima tidak
mendukungnya. Sebagai gantinya, gunakan sintaks "with" (bentuk yang
lebih baik dari perintah at(...) dari Maxima).


\>$&fx with x=1/2


Penugasan tersebut juga dapat bersifat simbolis.


\>$&fx with x=1+t


Perintah solve memecahkan ekspresi simbolik untuk variabel dalam
Maxima. Hasilnya adalah vektor solusi.


\>$&solve(x^2+x=4,x)


Bandingkan dengan perintah numerik "solve" di Euler, yang memerlukan
nilai awal, dan secara opsional nilai target.


\>solve("x^2+x",1,y=4)


    1.56155281281

Nilai numerik dari solusi simbolik dapat dihitung dengan mengevaluasi
hasil simbolik. Euler akan membaca ulang penugasan x= dst. Jika Anda
tidak memerlukan hasil numerik untuk perhitungan lebih lanjut, Anda
juga dapat membiarkan Maxima menemukan nilai numeriknya.


\>sol &= solve(x^2+2\*x=4,x); $&sol, sol(), $&float(sol)


    [-3.23607,  1.23607]

Untuk mendapatkan solusi simbolis yang spesifik, seseorang dapat
menggunakan "with" dan indeks.


\>$&solve(x^2+x=1,x), x2 &= x with %[2]; $&x2


Untuk menyelesaikan sistem persamaan, gunakan vektor persamaan.
Hasilnya adalah vektor solusi.


\>sol &= solve([x+y=3,x^2+y^2=5],[x,y]); $&sol, $&x\*y with sol[1]


Ekspresi simbolik dapat memiliki tanda, yang menunjukkan perlakuan
khusus di Maxima. Beberapa tanda dapat digunakan sebagai perintah
juga, yang lainnya tidak. Tanda ditambahkan dengan "|" (bentuk yang
lebih baik dari "ev(...,flags)")


\>$& diff((x^3-1)/(x+1),x) //turunan bentuk pecahan

\>$& diff((x^3-1)/(x+1),x) | ratsimp //menyederhanakan pecahan

\>$&factor(%)


# Fungsi

Dalam EMT, fungsi adalah program yang ditentukan dengan perintah
“function”. Fungsi dapat berupa fungsi satu baris atau fungsi
multibaris.


ungsi satu baris dapat berupa numerik atau simbolik. Fungsi satu baris
numerik didefinisikan dengan “:=”.


\>function f(x) := x\*sqrt(x^2+1)


Sebagai gambaran umum, kami menunjukkan semua definisi yang mungkin
untuk fungsi satu baris. Sebuah fungsi dapat dievaluasi seperti halnya
fungsi Euler bawaan.


\>f(2)


    4.472135955

Fungsi ini juga dapat digunakan untuk vektor, mengikuti bahasa matriks
Euler, karena ekspresi yang digunakan dalam fungsi ini adalah vektor.


\>f(0:0.1:1)


    [0,  0.100499,  0.203961,  0.313209,  0.430813,  0.559017,  0.699714,
    0.854459,  1.0245,  1.21083,  1.41421]

Fungsi dapat diplot. Alih-alih ekspresi, kita hanya perlu memberikan
nama fungsi.


Berbeda dengan ekspresi simbolik atau numerik, nama fungsi harus
disediakan dalam bentuk string.


\>solve("f",1,y=1)


    0.786151377757

Secara default, jika Anda perlu menimpa fungsi built-in, Anda harus
menambahkan kata kunci “overwrite”. Menimpa fungsi bawaan berbahaya
dan dapat menyebabkan masalah bagi fungsi lain yang bergantung pada
fungsi tersebut.


Anda masih dapat memanggil fungsi bawaan sebagai “_...”, jika fungsi
tersebut merupakan fungsi dalam inti Euler.


\>function overwrite sin (x) := \_sin(x°) // redine sine in degrees

\>sin(45)


    0.707106781187

Sebaiknya kita hilangkan definisi ulang tentang dosa ini.


\>forget sin; sin(pi/4)


    0.707106781187

## Parameter Default



Fungsi numerik dapat memiliki parameter default.


\>function f(x,a=1) := a\*x^2


Menghilangkan parameter ini menggunakan nilai default.


\>f(4)


    16

Menetapkannya akan menimpa nilai default.


\>f(4,5)


    80

Parameter yang ditetapkan juga menimpanya. Ini digunakan oleh banyak
fungsi Euler seperti plot2d, plot3d.


\>f(4,a=1)


    16

Jika sebuah variabel bukan parameter, maka variabel tersebut harus
bersifat global. Fungsi satu baris dapat melihat variabel global.


\>function f(x) := a\*x^2

\>a=6; f(2)


    24

Tetapi parameter yang ditetapkan akan menggantikan nilai global.


Jika argumen tidak ada dalam daftar parameter yang telah ditetapkan
sebelumnya, argumen tersebut harus dideklarasikan dengan “:=”!


\>f(2,a:=5)


    20

Fungsi simbolik didefinisikan dengan “&amp;=”. Fungsi-fungsi ini
didefinisikan dalam Euler dan Maxima, dan dapat digunakan di kedua
bahasa tersebut. Ekspresi pendefinisian dijalankan melalui Maxima
sebelum definisi.


\>function g(x) &= x^3-x\*exp(-x); $&g(x)


Fungsi simbolis dapat digunakan dalam ekspresi simbolis.


\>$&diff(g(x),x), $&% with x=4/3


Fungsi ini juga dapat digunakan dalam ekspresi numerik. Tentu saja,
ini hanya akan berfungsi jika EMT dapat menginterpretasikan semua yang
ada di dalam fungsi.


\>g(5+g(1))


    178.635099908

Mereka dapat digunakan untuk mendefinisikan fungsi atau ekspresi
simbolis lainnya.


\>function G(x) &= factor(integrate(g(x),x)); $&G(c) // integrate: mengintegralkan


\>solve(&g(x),0.5)


    0.703467422498

Hal berikut ini juga dapat digunakan, karena Euler menggunakan
ekspresi simbolik dalam fungsi g, jika tidak menemukan variabel
simbolik g, dan jika ada fungsi simbolik g.


\>solve(&g,0.5)


    0.703467422498

\>function P(x,n) &= (2\*x-1)^n; $&P(x,n)

\>function Q(x,n) &= (x+2)^n; $&Q(x,n)

\>$&P(x,4), $&expand(%)

\>P(3,4)


    625

\>$&P(x,4)+ Q(x,3), $&expand(%)

\>$&P(x,4)-Q(x,3), $&expand(%), $&factor(%)

\>$&P(x,4)\*Q(x,3), $&expand(%), $&factor(%)

\>$&P(x,4)/Q(x,1), $&expand(%), $&factor(%)

\>function f(x) &= x^3-x; $&f(x)


Dengan &amp;=, fungsi ini bersifat simbolis, dan dapat digunakan dalam
ekspresi simbolis lainnya.


\>$&integrate(f(x),x)


Dengan := fungsi tersebut berupa angka. Contoh yang baik adalah
integral pasti seperti


yang tidak dapat dievaluasi secara simbolik.


Jika kita mendefinisikan ulang fungsi tersebut dengan kata kunci
“map”, maka fungsi tersebut dapat digunakan untuk vektor x.


Secara internal, fungsi tersebut dipanggil untuk semua nilai x satu
kali, dan hasilnya disimpan dalam sebuah vektor.


\>function map f(x) := integrate("x^x",1,x)

\>f(0:0.5:2)


    [-0.783431,  -0.410816,  0,  0.676863,  2.05045]

Fungsi dapat memiliki nilai default untuk parameter.


\>function mylog (x,base=10) := ln(x)/ln(base);


Sekarang, fungsi ini dapat dipanggil dengan atau tanpa parameter
“base”.


\>mylog(100), mylog(2^6.7,2)


    2
    6.7

Selain itu, dimungkinkan untuk menggunakan parameter yang ditetapkan.


\>mylog(E^2,base=E)


    2

Sering kali, kita ingin menggunakan fungsi untuk vektor di satu
tempat, dan untuk masing-masing elemen di tempat lain. Hal ini
dimungkinkan dengan parameter vektor.


\>function f([a,b]) &= a^2+b^2-a\*b+b; $&f(a,b), $&f(x,y)


Fungsi simbolik seperti itu dapat digunakan untuk variabel simbolik.


Tetapi fungsi ini juga dapat digunakan untuk vektor numerik.


\>v=[3,4]; f(v)


    17

Ada juga fungsi yang murni simbolis, yang tidak dapat digunakan secara
numerik.


\>function lapl(expr,x,y) &&= diff(expr,x,2)+diff(expr,y,2)//turunan parsial kedua


    
                     diff(expr, y, 2) + diff(expr, x, 2)
    

\>$&realpart((x+I\*y)^4), $&lapl(%,x,y)


Tetapi tentu saja, semua itu bisa digunakan dalam ekspresi simbolis
atau dalam definisi fungsi simbolis.


\>function f(x,y) &= factor(lapl((x+y^2)^5,x,y)); $&f(x,y)


Untuk meringkas


* 
&amp;= mendefinisikan fungsi simbolik,


* 
:= mendefinisikan fungsi numerik,


* 
&amp;&amp;= mendefinisikan fungsi simbolik murni.


# Memecahkan Ekspresi 

Ekspresi dapat diselesaikan secara numerik dan simbolik.


Untuk menyelesaikan ekspresi sederhana dari satu variabel, kita dapat
menggunakan fungsi solve(). Fungsi ini membutuhkan nilai awal untuk
memulai pencarian. Secara internal, solve() menggunakan metode secant.


\>solve("x^2-2",1)


    1.41421356237

Hal ini juga bisa digunakan untuk ekspresi simbolis. Perhatikan fungsi
berikut ini.


\>$&solve(x^2=2,x)

\>$&solve(x^2-2,x)

\>$&solve(a\*x^2+b\*x+c=0,x)

\>$&solve([a\*x+b\*y=c,d\*x+e\*y=f],[x,y])


\>px &= 4\*x^8+x^7-x^4-x; $&px


Sekarang kita mencari titik, di mana polinomialnya adalah 2. Dalam
solve(), nilai target default y=0 dapat diubah dengan variabel yang
ditetapkan.


ami menggunakan y=2 dan mengeceknya dengan mengevaluasi polinomial
pada hasil sebelumnya.


\>solve(px,1,y=2), px(%)


    0.966715594851
    2

Memecahkan sebuah ekspresi simbolik dalam bentuk simbolik
mengembalikan sebuah daftar solusi. 


Kami menggunakan pemecah simbolik solve() yang disediakan oleh Maxima.


\>sol &= solve(x^2-x-1,x); $&sol


Cara termudah untuk mendapatkan nilai numerik adalah dengan
mengevaluasi solusi secara numerik seperti sebuah ekspresi.


\>longest sol()


        -0.6180339887498949       1.618033988749895 

Untuk menggunakan solusi secara simbolis dalam ekspresi lain, cara
termudah adalah “with”.


\>$&x^2 with sol[1], $&expand(x^2-x-1 with sol[2])


Menyelesaikan sistem persamaan secara simbolik dapat dilakukan dengan
vektor persamaan dan pemecah simbolik solve(). Jawabannya adalah
sebuah daftar daftar persamaan.


\>$&solve([x+y=2,x^3+2\*y+x=4],[x,y])


Fungsi f() dapat melihat variabel global. Tetapi seringkali kita ingin
menggunakan parameter lokal.


dengan a = 3.


\>function f(x,a) := x^a-a^x;


Salah satu cara untuk mengoper parameter tambahan ke f() adalah dengan
menggunakan sebuah daftar yang berisi nama fungsi dan parameternya
(cara lainnya adalah dengan menggunakan parameter titik koma).


\>solve({{"f",3}},2,y=0.1)


    2.54116291558

Hal ini juga dapat dilakukan dengan ekspresi. Namun, elemen daftar
bernama harus digunakan. (Lebih lanjut tentang daftar dalam tutorial
tentang sintaks EMT).


\>solve({{"x^a-a^x",a=3}},2,y=0.1)


    2.54116291558

# Menyelesaikan Pertidaksamaan

Untuk menyelesaikan pertidaksamaan, EMT tidak akan dapat melakukannya,
melainkan dengan bantuan Maxima, artinya secara eksak (simbolik).
Perintah Maxima yang digunakan adalah fourier_elim(), yang harus
dipanggil dengan perintah "load(fourier_elim)" terlebih dahulu.


\>&load(fourier\_elim)


    
            C:/Program Files/Euler x64/maxima/share/maxima/5.35.1/share/f\
    ourier_elim/fourier_elim.lisp
    

\>$&fourier\_elim([x^2 - 1\>0],[x]) // x^2-1 \> 0

\>$&fourier\_elim([x^2 - 1<0],[x]) // x^2-1 < 0

\>$&fourier\_elim([x^2 - 1 # 0],[x]) // x^-1 <\> 0

\>$&fourier\_elim([x # 6],[x])

\>$&fourier\_elim([x < 1, x \> 1],[x]) // tidak memiliki penyelesaian

\>$&fourier\_elim([minf < x, x < inf],[x]) // solusinya R

\>$&fourier\_elim([x^3 - 1 \> 0],[x])

\>$&fourier\_elim([cos(x) < 1/2],[x]) // ??? gagal


\>$&fourier\_elim([y-x < 5, x - y < 7, 10 < y],[x,y]) // sistem pertidaksamaan

\>$&fourier\_elim([y-x < 5, x - y < 7, 10 < y],[y,x])

\>$&fourier\_elim((x + y < 5) and (x - y \>8),[x,y])

\>$&fourier\_elim(((x + y < 5) and x < 1) or  (x - y \>8),[x,y])

\>&fourier\_elim([max(x,y) \> 6, x # 8, abs(y-1) \> 12],[x,y])


    
            [6 &lt; x, x &lt; 8, y &lt; - 11] or [8 &lt; x, y &lt; - 11]
     or [x &lt; 8, 13 &lt; y] or [x = y, 13 &lt; y] or [8 &lt; x, x &lt; y, 13 &lt; y]
     or [y &lt; x, 13 &lt; y]
    

\>$&fourier\_elim([(x+6)/(x-9) <= 6],[x])


# Bahasa Matriks

Dokumentasi inti EMT berisi diskusi terperinci tentang bahasa matriks
Euler.


Vektor dan matriks dimasukkan dengan tanda kurung siku, elemen
dipisahkan dengan koma, baris dipisahkan dengan titik koma.


\>A=[1,2;3,4]


                1             2 
                3             4 

Hasil kali matriks dilambangkan dengan sebuah titik.


\>b=[3;4]


                3 
                4 

\>b' // transpose b


    [3,  4]

\>inv(A) //inverse A


               -2             1 
              1.5          -0.5 

\>A.b //perkalian matriks


               11 
               25 

\>A.inv(A)


                1             0 
                0             1 

Poin utama dari bahasa matriks adalah bahwa semua fungsi dan operator
bekerja elemen demi elemen.


\>A.A


                7            10 
               15            22 

\>A^2 //perpangkatan elemen2 A


                1             4 
                9            16 

\>A.A.A


               37            54 
               81           118 

\>power(A,3) //perpangkatan matriks


               37            54 
               81           118 

\>A/A //pembagian elemen-elemen matriks yang seletak


                1             1 
                1             1 

\>A/b //pembagian elemen2 A oleh elemen2 b kolom demi kolom (karena b vektor kolom)


         0.333333      0.666667 
             0.75             1 

\>A\\b // hasilkali invers A dan b, A^(-1)b 


               -2 
              2.5 

\>inv(A).b


               -2 
              2.5 

\>A\\A   //A^(-1)A


                1             0 
                0             1 

\>inv(A).A


                1             0 
                0             1 

\>A\*A //perkalin elemen-elemen matriks seletak


                1             4 
                9            16 

Ini bukan hasil kali matriks, tetapi perkalian elemen demi elemen. Hal
yang sama berlaku untuk vektor.


\>b^2 // perpangkatan elemen-elemen matriks/vektor


                9 
               16 

ika salah satu operan adalah vektor atau skalar, maka operan tersebut
akan diperluas dengan cara alami.


\>2\*A


                2             4 
                6             8 

Misalnya, jika operan adalah vektor kolom, elemen-elemennya diterapkan
ke semua baris A.


\>[1,2]\*A


                1             4 
                3             8 

Jika ini adalah vektor baris, vektor ini diterapkan ke semua kolom A.


\>A\*[2,3]


                2             6 
                6            12 

Kita dapat membayangkan perkalian ini seolah-olah vektor baris v telah
diduplikasi untuk membentuk matriks dengan ukuran yang sama dengan A.


\>dup([1,2],2) // dup: menduplikasi/menggandakan vektor [1,2] sebanyak 2 kali (baris)


                1             2 
                1             2 

\>A\*dup([1,2],2) 


                1             4 
                3             8 

Hal ini juga berlaku untuk dua vektor di mana satu vektor adalah
vektor baris dan yang lainnya adalah vektor kolom. Kami menghitung i*j
untuk i, j dari 1 sampai 5. Caranya adalah dengan mengalikan 1:5
dengan transposenya. Bahasa matriks Euler secara otomatis menghasilkan
sebuah tabel nilai.


\>(1:5)\*(1:5)' // hasilkali elemen-elemen vektor baris dan vektor kolom


                1             2             3             4             5 
                2             4             6             8            10 
                3             6             9            12            15 
                4             8            12            16            20 
                5            10            15            20            25 

Sekali lagi, ingatlah bahwa ini bukan produk matriks!


\>(1:5).(1:5)' // hasilkali vektor baris dan vektor kolom


    55

\>sum((1:5)\*(1:5)) // sama hasilnya


    55

Bahkan operator seperti &lt; atau == bekerja dengan cara yang sama.


\>(1:10)<6 // menguji elemen-elemen yang kurang dari 6


    [1,  1,  1,  1,  1,  0,  0,  0,  0,  0]

Sebagai contoh, kita dapat menghitung jumlah elemen yang memenuhi
kondisi tertentu dengan fungsi sum().


\>sum((1:10)<6) // banyak elemen yang kurang dari 6


    5

Euler memiliki operator perbandingan, seperti “==”, yang memeriksa
kesetaraan.


Kita mendapatkan vektor 0 dan 1, di mana 1 berarti benar.


\>t=(1:10)^2; t==25 //menguji elemen2 t yang sama dengan 25 (hanya ada 1)


    [0,  0,  0,  0,  1,  0,  0,  0,  0,  0]

Dari vektor seperti itu, “nonzeros” memilih elemen bukan nol.


Dalam hal ini, kita mendapatkan indeks semua elemen yang lebih besar
dari 50.


\>nonzeros(t\>50) //indeks elemen2 t yang lebih besar daripada 50


    [8,  9,  10]

Tentu saja, kita dapat menggunakan vektor indeks ini untuk mendapatkan
nilai yang sesuai dalam t.


\>t[nonzeros(t\>50)] //elemen2 t yang lebih besar daripada 50


    [64,  81,  100]

Sebagai contoh, mari kita cari semua kuadrat dari angka 1 sampai 1000,
yaitu 5 modulo 11 dan 3 modulo 13.


\>t=1:1000; nonzeros(mod(t^2,11)==5 && mod(t^2,13)==3)


    [4,  48,  95,  139,  147,  191,  238,  282,  290,  334,  381,  425,
    433,  477,  524,  568,  576,  620,  667,  711,  719,  763,  810,  854,
    862,  906,  953,  997]

EMT tidak sepenuhnya efektif untuk komputasi bilangan bulat. EMT
menggunakan floating point presisi ganda secara internal. Akan tetapi,
hal ini sering kali sangat berguna.


Kita dapat memeriksa bilangan prima. Mari kita cari tahu, berapa
banyak kuadrat ditambah 1 yang merupakan bilangan prima.


\>t=1:1000; length(nonzeros(isprime(t^2+1)))


    112

Fungsi nonzeros() hanya bekerja untuk vektor. Untuk matriks, ada
mnonzeros().


\>seed(2); A=random(3,4)


         0.765761      0.401188      0.406347      0.267829 
          0.13673      0.390567      0.495975      0.952814 
         0.548138      0.006085      0.444255      0.539246 

Ini mengembalikan indeks elemen, yang bukan nol.


\>k=mnonzeros(A<0.4) //indeks elemen2 A yang kurang dari 0,4


                1             4 
                2             1 
                2             2 
                3             2 

Indeks ini dapat digunakan untuk menetapkan elemen ke suatu nilai.


\>mset(A,k,0) //mengganti elemen2 suatu matriks pada indeks tertentu


         0.765761      0.401188      0.406347             0 
                0             0      0.495975      0.952814 
         0.548138             0      0.444255      0.539246 

Fungsi mset() juga dapat mengatur elemen-elemen pada indeks ke
entri-entri matriks lain.


\>mset(A,k,-random(size(A)))


         0.765761      0.401188      0.406347     -0.126917 
        -0.122404     -0.691673      0.495975      0.952814 
         0.548138     -0.483902      0.444255      0.539246 

Dan dimungkinkan untuk mendapatkan elemen-elemen dalam vektor.


\>mget(A,k)


    [0.267829,  0.13673,  0.390567,  0.006085]

Fungsi lain yang berguna adalah extrema, yang mengembalikan nilai
minimal dan maksimal di setiap baris matriks dan posisinya.


\>ex=extrema(A)


         0.267829             4      0.765761             1 
          0.13673             1      0.952814             4 
         0.006085             2      0.548138             1 

Kita bisa menggunakan ini untuk mengekstrak nilai maksimal dalam
setiap baris.


\>ex[,3]'


    [0.765761,  0.952814,  0.548138]

Ini, tentu saja, sama dengan fungsi max().


\>max(A)'


    [0.765761,  0.952814,  0.548138]

Tetapi dengan mget(), kita dapat mengekstrak indeks dan menggunakan
informasi ini untuk mengekstrak elemen-elemen pada posisi yang sama
dari matriks yang lain.


\>j=(1:rows(A))'|ex[,4], mget(-A,j)


                1             1 
                2             4 
                3             1 
    [-0.765761,  -0.952814,  -0.548138]

# Fungsi Matriks Lainnya (Membangun Matriks)

Untuk membangun sebuah matriks, kita dapat menumpuk satu matriks di
atas matriks lainnya. Jika keduanya tidak memiliki jumlah kolom yang
sama, kolom yang lebih pendek akan diisi dengan 0.


\>v=1:3; v\_v


                1             2             3 
                1             2             3 

Demikian juga, kita dapat melampirkan matriks ke matriks lain secara
berdampingan, jika keduanya memiliki jumlah baris yang sama.


\>A=random(3,4); A|v'


         0.032444     0.0534171      0.595713      0.564454             1 
          0.83916      0.175552      0.396988       0.83514             2 
        0.0257573      0.658585      0.629832      0.770895             3 

Jika keduanya tidak memiliki jumlah baris yang sama, matriks yang
lebih pendek diisi dengan 0.


Ada pengecualian untuk aturan ini. Bilangan real yang dilampirkan pada
sebuah matriks akan digunakan sebagai kolom yang diisi dengan bilangan
real tersebut.


\>A|1


         0.032444     0.0534171      0.595713      0.564454             1 
          0.83916      0.175552      0.396988       0.83514             1 
        0.0257573      0.658585      0.629832      0.770895             1 

Dimungkinkan untuk membuat matriks vektor baris dan kolom.


\>[v;v]


                1             2             3 
                1             2             3 

\>[v',v']


                1             1 
                2             2 
                3             3 

Tujuan utama dari hal ini adalah untuk menginterpretasikan vektor
ekspresi untuk vektor kolom.


\>"[x,x^2]"(v')


                1             1 
                2             4 
                3             9 

Untuk mendapatkan ukuran A, kita dapat menggunakan fungsi berikut ini.


\>C=zeros(2,4); rows(C), cols(C), size(C), length(C)


    2
    4
    [2,  4]
    4

Untuk vektor, ada length().


\>length(2:10)


    9

Ada banyak fungsi lain yang menghasilkan matriks.


\>ones(2,2)


                1             1 
                1             1 

Ini juga dapat digunakan dengan satu parameter. Untuk mendapatkan
vektor dengan angka selain 1, gunakan yang berikut ini.


\>ones(5)\*6


    [6,  6,  6,  6,  6]

Matriks angka acak juga dapat dibuat dengan acak (distribusi seragam)
atau normal (distribusi Gauß).


\>random(2,2)


          0.66566      0.831835 
            0.977      0.544258 

Berikut ini adalah fungsi lain yang berguna, yang merestrukturisasi
elemen-elemen matriks menjadi matriks lain.


\>redim(1:9,3,3) // menyusun elemen2 1, 2, 3, ..., 9 ke bentuk matriks 3x3


                1             2             3 
                4             5             6 
                7             8             9 

Dengan fungsi berikut, kita dapat menggunakan fungsi ini dan fungsi
dup untuk menulis fungsi rep(), yang mengulang sebuah vektor sebanyak
n kali.


\>function rep(v,n) := redim(dup(v,n),1,n\*cols(v))


Mari kita uji.


\>rep(1:3,5)


    [1,  2,  3,  1,  2,  3,  1,  2,  3,  1,  2,  3,  1,  2,  3]

Fungsi multdup() menduplikasi elemen-elemen sebuah vektor.


\>multdup(1:3,5), multdup(1:3,[2,3,2])


    [1,  1,  1,  1,  1,  2,  2,  2,  2,  2,  3,  3,  3,  3,  3]
    [1,  1,  2,  2,  2,  3,  3]

Fungsi flipx() dan flipy() membalik urutan baris atau kolom dari
sebuah matriks. Misalnya, fungsi flipx() membalik secara horizontal.


\>flipx(1:5) //membalik elemen2 vektor baris


    [5,  4,  3,  2,  1]

Untuk rotasi, Euler memiliki rotleft() dan rotright().


\>rotleft(1:5) // memutar elemen2 vektor baris


    [2,  3,  4,  5,  1]

Fungsi khusus adalah drop(v,i), yang menghapus elemen dengan indeks di
i dari vektor v.


\>drop(10:20,3)


    [10,  11,  13,  14,  15,  16,  17,  18,  19,  20]

Perhatikan bahwa vektor i dalam drop(v,i) merujuk pada indeks elemen
dalam v, bukan nilai elemen. Jika Anda ingin menghapus elemen, Anda
harus menemukan elemen-elemen tersebut terlebih dahulu. Fungsi
indexof(v,x) dapat digunakan untuk menemukan elemen x dalam vektor
terurut v.


\>v=primes(50), i=indexof(v,10:20), drop(v,i)


    [2,  3,  5,  7,  11,  13,  17,  19,  23,  29,  31,  37,  41,  43,  47]
    [0,  5,  0,  6,  0,  0,  0,  7,  0,  8,  0]
    [2,  3,  5,  7,  23,  29,  31,  37,  41,  43,  47]

Seperti yang Anda lihat, tidak ada salahnya menyertakan indeks di luar
jangkauan (seperti 0), indeks ganda, atau indeks yang tidak diurutkan.


\>drop(1:10,shuffle([0,0,5,5,7,12,12]))


    [1,  2,  3,  4,  6,  8,  9,  10]

Ada beberapa fungsi khusus untuk mengatur diagonal atau menghasilkan
matriks diagonal.


Kita mulai dengan matriks identitas.


\>A=id(5) // matriks identitas 5x5


                1             0             0             0             0 
                0             1             0             0             0 
                0             0             1             0             0 
                0             0             0             1             0 
                0             0             0             0             1 

Kemudian, kami menetapkan diagonal bawah (-1) ke 1:4.


\>setdiag(A,-1,1:4) //mengganti diagonal di bawah diagonal utama


                1             0             0             0             0 
                1             1             0             0             0 
                0             2             1             0             0 
                0             0             3             1             0 
                0             0             0             4             1 

Perhatikan bahwa kita tidak mengubah matriks A. Kita mendapatkan
sebuah matriks baru sebagai hasil dari setdiag().


Berikut adalah sebuah fungsi yang mengembalikan sebuah matriks
tri-diagonal.


\>function tridiag (n,a,b,c) := setdiag(setdiag(b\*id(n),1,c),-1,a); ...  
\>   tridiag(5,1,2,3)


                2             3             0             0             0 
                1             2             3             0             0 
                0             1             2             3             0 
                0             0             1             2             3 
                0             0             0             1             2 

Diagonal sebuah matriks juga dapat diekstrak dari matriks. Untuk
mendemonstrasikan hal ini, kami merestrukturisasi vektor 1:9 menjadi
matriks 3x3.


\>A=redim(1:9,3,3)


                1             2             3 
                4             5             6 
                7             8             9 

Sekarang kita bisa mengekstrak diagonal.


\>d=getdiag(A,0)


    [1,  5,  9]

Contoh: Kita dapat membagi matriks dengan diagonalnya. Bahasa matriks
memperhatikan bahwa vektor kolom d diterapkan ke matriks baris demi
baris.


\>fraction A/d'


            1         2         3 
          4/5         1       6/5 
          7/9       8/9         1 

# Vektorisasi

Hampir semua fungsi di Euler juga dapat digunakan untuk input matriks
dan vektor, jika hal ini masuk akal.


Sebagai contoh, fungsi sqrt() menghitung akar kuadrat dari semua
elemen vektor atau matriks.


\>sqrt(1:3)


    [1,  1.41421,  1.73205]

Jadi, Anda dapat dengan mudah membuat tabel nilai. Ini adalah salah
satu cara untuk memplot sebuah fungsi (alternatif lainnya menggunakan
ekspresi).


\>x=1:0.01:5; y=log(x)/x^2; // terlalu panjang untuk ditampikan


Dengan ini dan operator titik dua a:delta:b, vektor nilai fungsi dapat
dihasilkan dengan mudah.


Pada contoh berikut, kita membuat vektor nilai t[i] dengan jarak 0.1
dari -1 hingga 1. Kemudian kita membuat vektor nilai dari fungsi 


lateks:


 s = t^3-t  

\>t=-1:0.1:1; s=t^3-t


    [0,  0.171,  0.288,  0.357,  0.384,  0.375,  0.336,  0.273,  0.192,
    0.099,  0,  -0.099,  -0.192,  -0.273,  -0.336,  -0.375,  -0.384,
    -0.357,  -0.288,  -0.171,  0]

EMT memperluas operator untuk skalar, vektor, dan matriks dengan cara
yang jelas.


Misalnya, vektor kolom dikalikan vektor baris diperluas menjadi
matriks, jika operator diterapkan. Berikut ini, v' adalah vektor yang
ditransposisikan (vektor kolom).


\>shortest (1:5)\*(1:5)'


         1      2      3      4      5 
         2      4      6      8     10 
         3      6      9     12     15 
         4      8     12     16     20 
         5     10     15     20     25 

Perhatikan, bahwa ini sangat berbeda dengan hasil kali matriks. Hasil
kali matriks dilambangkan dengan sebuah titik “.” dalam EMT.


\>(1:5).(1:5)'


    55

Secara default, vektor baris dicetak dalam format ringkas.


\>[1,2,3,4]


    [1,  2,  3,  4]

Untuk matriks, operator khusus . menyatakan perkalian matriks, dan A'
menyatakan transposisi. Matriks 1x1 dapat digunakan seperti halnya
bilangan real.


\>v:=[1,2]; v.v', %^2


    5
    25

Untuk mentransposisikan matriks, kita menggunakan apostrof.


\>v=1:4; v'


                1 
                2 
                3 
                4 

Jadi kita dapat menghitung matriks A dikali vektor b.


\>A=[1,2,3,4;5,6,7,8]; A.v'


               30 
               70 

Perhatikan bahwa v masih merupakan vektor baris. Jadi v'.v berbeda
dengan v.v'.


\>v'.v


                1             2             3             4 
                2             4             6             8 
                3             6             9            12 
                4             8            12            16 

v.v' menghitung norma v kuadrat untuk vektor baris v. Hasilnya adalah
vektor 1x1, yang berfungsi seperti bilangan real.


\>v.v'


    30

Ada juga norma fungsi (bersama dengan banyak fungsi Aljabar Linier
lainnya).


\>norm(v)^2


    30

Operator dan fungsi mematuhi bahasa matriks Euler.


Berikut ini adalah ringkasan aturannya.


* 
Sebuah fungsi yang diterapkan pada vektor atau matriks diterapkan
* pada setiap elemen.


* 
Operator yang beroperasi pada dua matriks dengan ukuran yang sama
* diterapkan secara berpasangan pada elemen-elemen matriks.


* 
Jika dua matriks memiliki dimensi yang berbeda, keduanya diperluas
* dengan cara yang masuk akal, sehingga memiliki ukuran yang sama.


Misalnya, nilai skalar dikalikan vektor mengalikan nilai tersebut
dengan setiap elemen vektor. Atau matriks dikali vektor (dengan *,
bukan .) memperluas vektor ke ukuran matriks dengan menduplikasinya.


Berikut ini adalah kasus sederhana dengan operator ^.


\>[1,2,3]^2


    [1,  4,  9]

Ini adalah kasus yang lebih rumit. Vektor baris dikalikan vektor kolom
memperluas keduanya dengan menduplikasi.


\>v:=[1,2,3]; v\*v'


                1             2             3 
                2             4             6 
                3             6             9 

Perhatikan bahwa hasil kali skalar menggunakan hasil kali matriks,
bukan tanda *!


\>v.v'


    14

Ada banyak fungsi untuk matriks. Kami memberikan daftar singkat. Anda
harus membaca dokumentasi untuk informasi lebih lanjut mengenai
perintah-perintah ini.


sum,prod menghitung jumlah dan hasil kali dari baris-baris


 cumsum,cumprod melakukan hal yang sama secara kumulatif


 menghitung nilai ekstrem dari setiap baris


 extrema mengembalikan vektor dengan informasi ekstrem


 diag(A,i) mengembalikan diagonal ke-i


 setdiag(A,i,v) menetapkan diagonal ke-i


 id(n) matriks identitas


 det(A) determinan


 charpoly(A) polinomial karakteristik


 eigenvalues(A) nilai eigen


\>v\*v, sum(v\*v), cumsum(v\*v)


    [1,  4,  9]
    14
    [1,  5,  14]

Operator : menghasilkan vektor baris dengan spasi yang sama, opsional
dengan ukuran langkah.


\>1:4, 1:2:10


    [1,  2,  3,  4]
    [1,  3,  5,  7,  9]

Untuk menggabungkan matriks dan vektor, terdapat operator “|” dan “_”.


\>[1,2,3]|[4,5], [1,2,3]\_1


    [1,  2,  3,  4,  5]
                1             2             3 
                1             1             1 

Elemen-elemen dari sebuah matriks disebut dengan “A[i,j]”.


\>A:=[1,2,3;4,5,6;7,8,9]; A[2,3]


    6

Untuk vektor baris atau kolom, v[i] adalah elemen ke-i dari vektor
tersebut. Untuk matriks, ini mengembalikan baris ke-i dari matriks.


\>v:=[2,4,6,8]; v[3], A[3]


    6
    [7,  8,  9]

Indeks juga dapat berupa vektor baris dari indeks. : menunjukkan semua
indeks.


\>v[1:2], A[:,2]


    [2,  4]
                2 
                5 
                8 

Bentuk singkat untuk : adalah menghilangkan indeks sepenuhnya.


\>A[,2:3]


                2             3 
                5             6 
                8             9 

Untuk tujuan vektorisasi, elemen-elemen matriks dapat diakses
seolah-olah mereka adalah vektor.


\>A{4}


    4

Sebuah matriks juga dapat diratakan, dengan menggunakan fungsi
redim(). Hal ini diimplementasikan dalam fungsi flatten().


\>redim(A,1,prod(size(A))), flatten(A)


    [1,  2,  3,  4,  5,  6,  7,  8,  9]
    [1,  2,  3,  4,  5,  6,  7,  8,  9]

Untuk menggunakan matriks untuk tabel, mari kita atur ulang ke format
default, dan menghitung tabel nilai sinus dan kosinus. Perhatikan
bahwa sudut dalam radian secara default.


\>defformat; w=0°:45°:360°; w=w'; deg(w)


                0 
               45 
               90 
              135 
              180 
              225 
              270 
              315 
              360 

Sekarang kita menambahkan kolom ke matriks.


\>M = deg(w)|w|cos(w)|sin(w)


                0             0             1             0 
               45      0.785398      0.707107      0.707107 
               90        1.5708             0             1 
              135       2.35619     -0.707107      0.707107 
              180       3.14159            -1             0 
              225       3.92699     -0.707107     -0.707107 
              270       4.71239             0            -1 
              315       5.49779      0.707107     -0.707107 
              360       6.28319             1             0 

Dengan menggunakan bahasa matriks, kita dapat membuat beberapa tabel
dari beberapa fungsi sekaligus.


Pada contoh berikut, kita menghitung t[j]^i untuk i dari 1 hingga n.
Kita mendapatkan sebuah matriks, di mana setiap baris adalah tabel t^i
untuk satu i. Dengan kata lain, matriks tersebut memiliki
elemen-elemen lateks: a_{i, j} = t_j^i, \qad 1 \le j \le 101, \qad 1
\le i \le n


Sebuah fungsi yang tidak bekerja untuk input vektor harus
“divektorkan”. Hal ini dapat dicapai dengan kata kunci “map” dalam
definisi fungsi. Kemudian fungsi akan dievaluasi untuk setiap elemen
parameter vektor.


Integrasi numerik integrate() hanya bekerja untuk batas interval
skalar. Jadi kita perlu membuat vektornya.


\>function map f(x) := integrate("x^x",1,x)


Kata kunci “map” membuat vektor fungsi. Fungsi ini sekarang akan
bekerja


ntuk vektor angka.


\>f([1:5])


    [0,  2.05045,  13.7251,  113.336,  1241.03]

# Sub-Matriks dan Elemen Matriks

Untuk mengakses elemen mmatriks, gunakan notasi kurung. 


\>A=[1,2,3;4,5,6;7,8,9], A[2,2]


                1             2             3 
                4             5             6 
                7             8             9 
    5

Kita dapat mengakses baris lengkap dari sebuah matriks.


\>A[2]


    [4,  5,  6]

Dalam kasus vektor baris atau kolom, ini mengembalikan elemen vektor.


\>v=1:3; v[2]


    2

Untuk memastikan, Anda mendapatkan baris pertama untuk matriks 1xn dan
mxn, tentukan semua kolom menggunakan indeks kedua yang kosong.


\>A[2,]


    [4,  5,  6]

Jika indeks adalah vektor indeks, Euler akan memgembalikan baris-baris
yang sesuai dari matriks.


Di sini kita menginginkan baris pertama dan kedua dari A.


\>A[[1,2]]


                1             2             3 
                4             5             6 

Kita bahkan dapat menyusun ulang A menggunakan vektor indeks.
Tepatnya, kita tidak menubah A di sini tetapi menghitung versi susunan
ulng dari A.


\>A[[3,2,1]]


                7             8             9 
                4             5             6 
                1             2             3 

Trik indeks juga dapat digunakan pada kolom.


Contoh ini memilih semua baris A dan kolom kedua dan ketiga.


\>A[1:3,2:3]


                2             3 
                5             6 
                8             9 

Untuk singkatan ":" menunjukkan semua indeks baris atau kolom.


\>A[:,3]


                3 
                6 
                9 

Sebagai artenatif, biarkan indeks pertama kosong.


\>A[,2:3]


                2             3 
                5             6 
                8             9 

Kita juga bisa mendapatkan baris terakhir A.


\>A[-1]


    [7,  8,  9]

Sekarang mari kita ubah elemen-elemen dari A dengan memberikan sebuah
submatriks dari A kesuatu nilai.


Hal ini sebenarnya mengubah matriks A yang tersimpan.


\>A[1,1]=4


                4             2             3 
                4             5             6 
                7             8             9 

Kita juga dapat menetapkan nilai pada deretan A.


\>A[1]=[-1,-1,-1]


               -1            -1            -1 
                4             5             6 
                7             8             9 

Kami bahkan dapat menetapkan ke sub-matriks juka memiliki ukuran yang
tepat.


\>A[1:2,1:2]=[5,6;7,8]


                5             6            -1 
                7             8             6 
                7             8             9 

Selain itu, bebrapa jalan pintas diperbolehkan.


\>A[1:2,1:2]=0


                0             0            -1 
                0             0             6 
                7             8             9 

Peringatan : Indeks diluar batas akan mengembalikan matriks kosong,
atau pesan kesalahan, tergantung pada pengaturan sistem. Standarnya
adalah pesan kesalahan. Namun, ingatlah bahwa indeks negatif dapat
diginakan untuk mengakses elemen-elemen matriks yang dihitung dari
akhir.


\>A[4]


    Row index 4 out of bounds!
    Error in:
    A[4] ...
        ^

# Menyortir dan Mengacak

Fungsi mengurutkan () mengurutkan vektor baris.


\>sort([5,6,4,8,1,9])


    [1,  4,  5,  6,  8,  9]

Sering kali diperlukan untuk mengetahui indeks vektor yang diurutkan
dalam vektor aslinya. Hal ini dapat digunakan untuk menyusun ulang
vektor lain dengan cara yang sama.


Mari kita acak sebuah vektor.


\>v=shuffle(1:10)


    [4,  5,  10,  6,  8,  9,  1,  7,  2,  3]

Indeks berisi urutan v yang tepat.


\>{vs,ind}=sort(v); v[ind]


    [1,  2,  3,  4,  5,  6,  7,  8,  9,  10]

Hal ini juga berlaku untuk vektor string.


\>s=["a","d","e","a","aa","e"]


    a
    d
    e
    a
    aa
    e

\>{ss,ind}=sort(s); ss


    a
    a
    aa
    d
    e
    e

Seperti yang anda lihat, posisi entri ganda agak acak.


\>ind


    [4,  1,  5,  2,  6,  3]

Fungsi unique mengembalikan daftar terurut dari elemen unik vektor.


\>intrandom(1,10,10), unique(%)


    [4,  4,  9,  2,  6,  5,  10,  6,  5,  1]
    [1,  2,  4,  5,  6,  9,  10]

Hal ini juga berlaku untuk vektor string.


\>unique(s)


    a
    aa
    d
    e

# Aljabar Linier

EMT memiiki banyak fungsi untuk menyelesaikan sistem linier, sistem
jarang, atau masalah regresi. 


Untuk sistem linier Ax=b, anda dapat menggunakan algoritma Gauss,
matriks invers, atau kecocokan linier. Operator A/b menggunakan versi
algoritma Gauss.


\>A=[1,2;3,4]; b=[5;6]; A\\b


               -4 
              4.5 

Sebagai contoh lain, kita membuat matriks 200x200 dan jumlah barisnya.
Kemudian kita selesaikan Ax=b dengan menggunakan matriks kebalikannya.
Kita mengukur kesalahan sebagai deviasi maksimal dari semua elemen
dari 1, yang tentu saja merupakan solusi yang benar. 


\>A=normal(200,200); b=sum(A); longest totalmax(abs(inv(A).b-1))


      8.790745908981989e-13 

Jika sistem tidak memiliki solusi, pencocokan linier meminimalkan
norma kesalahan Ax-b.


\>A=[1,2,3;4,5,6;7,8,9]


                1             2             3 
                4             5             6 
                7             8             9 

Determinan dari matris ini adalah 0.


\>det(A)


    0

# Matriks Simbolik

Maxima memiliki matriks simbolik. Tentu saja, Maxima dapat digunakan
untuk masalah aljabar linier sederhana. Kita bisa mendefinisikan
matriks untuk Euler dan Maxima dengan &amp;:=, lalu menggunakannya dalam
ekspresi simbolik. Bentuk [...] yang biasa untuk mendefinisikan
matriks dapat digunakan dalam Euler untuk mendefinisikan matriks
simbolik.


\>A &= [a,1,1;1,a,1;1,1,a]; $A

\>$&det(A), $&factor(%)

\>$&invert(A) with a=0

\>A &= [1,a;b,2]; $A


Seperti semua variabel simbolik, matriks ini dapat digunakan dalam
ekspresi simbolik lainnya.


\>$&det(A-x\*ident(2)), $&solve(%,x)


Nilai eigen juga dapat dihitung secara otomatis. Hasilnya adalah
sebuah vektor dengan dua vektor nilai eigen dan kelipatannya.


\>$&eigenvalues([a,1;1,a])


Untuk mengekstrak vektor eigen tertentu, diperlukan pengindeksan yang
cermat.


\>$&eigenvectors([a,1;1,a]), &%[2][1][1]


    
                                   [1, - 1]
    

Matriks simbolik dapat dievaluasi dalam Euler secara numerik seperti
halnya ekspresi simbolik lainnya.


\>A(a=4,b=5)


                1             4 
                5             2 

Dalam ekspresi simbolik, gunakan dengan.


\>$&A with [a=4,b=5]


Akses ke baris matriks simbolik bekerja seperti halnya matriks
numerik.


\>$&A[1]


Ekspresi simbolik dapat berisi sebuah penugasan. Dana itu mengubah
matriks A.


\>&A[1,1]:=t+1; $&A


Terdapat fungsi-fungsi simbolik dalam Maxima untuk membuat vektor dan
matriks. Untuk hal ini, lihat dokumentasi Maxima atau tutorial tentang
Maxima di EMT.


\>v &= makelist(1/(i+j),i,1,3); $v


\>B &:= [1,2;3,4]; $B, $&invert(B)


Hasilnya dapat dievaluasi secara numerik dalam Euler. Untuk informasi
lebih lanjut tentang Maxima, lihat pengantar Maxima.


\>$&invert(B)()


               -2             1 
              1.5          -0.5 

Euler juga memiliki fungsi yang kuat xinv(), yang membuat usaha yang
lebih besar dan mendapatkan hasil yang tepat.


Perhatikan, bahwa dengan &amp;:= matriks B telah didefinisikan sebagai
simbolik dalam ekspresi numerik. Jadi kita dapat menggunakannya
disini.


\>longest B.xinv(B)


                          1                       0 
                          0                       1 

Misalnya, nilai eigen dari A dapat dihitung secara numerik.


\>A=[1,2,3;4,5,6;7,8,9]; real(eigenvalues(A))


    [16.1168,  -1.11684,  0]

Atau secara simbolik. Lihat tutorial tentang Maxima untuk mengetahui
detailnya.


\>$&eigenvalues(@A)


# Nilai Numerik dalam Ekspresi simbolik

Ekspresi simbolik hanyalah sebuah string yang berisi ekspresi. Jika
kita ingin mendefinisikan nilai untuk ekspresi simbolik dan ekspresi
numerik, kita haris menggunkan "&amp;:=".


\>A &:= [1,pi;4,5]


                1       3.14159 
                4             5 

Masih ada perbedaan antara bentuk numerik dan bentuk simbolik. Ketika
mentransfer matriks ke bentuk simbolik, perkiraan pecahan untuk
bilangan real akan digunakan.


\>$&A


Untuk menghindari hal ini, ada fungsi "mxmset(variabel)".


\>mxmset(A); $&A


Maxima juga dapat menghitung dengan angka floating point, dan bahkan
dengan angka mengambang yang besar dengan 32 digit. Namun, evaluasinya
jauh lebih lambat.


\>$&bfloat(sqrt(2)), $&float(sqrt(2))


Ketepatan angka floating point yang besar dapat diubah.


\>&fpprec:=100; &bfloat(pi)


    
            3.14159265358979323846264338327950288419716939937510582097494\
    4592307816406286208998628034825342117068b0
    

Variabel numerik dapat digunakan dalam ekspresi simbolik apapun dengan
menggunakan "@var".


Perhatikan bahwa hal ini hanya diperlukan, jika variabel telh
didefinisikan dengan ":=" atau "=" sebuah variabel numerik.


\>B:=[1,pi;3,4]; $&det(@B)


# Demo - Suku Bunga

Di bawah ini, kami menggunakan Eular Mtah Toolbox (EMT) untuk
menghitung suku bunga. Kami melakukan secara numerik dan simbolik
untuk menunjukkan kepada anda bagaimana euler dapat digunakan untuk
memecahkan masalah dikehidupan nyata.


Asumsikan anda memiliki modal awal sebesar modal awal sebesar
5000(katakan dalama dolar).


\>K=5000


    5000

Sekarang kita asumsikan suku bunga 3% per tahun. Maka kita tambahkan
satu suku bunga sederhana dan hitung hasilnya. 


\>K\*1.03


    5150

Euler juga akan memahami sintaks berikut ini.


\>K+K\*3%


    5150

Tetapi akan lebih mudah untuk menggunakan faktor.


\>q=1+3%, K\*q


    1.03
    5150

Untuk 10 tahun, kita cukup mengalihkan faktor-faktor tersebut dan
mendapatkan nilai akhir dengan suku bunga majemuk. 


\>K\*q^10


    6719.58189672

Untuk tujuan kita, kita bisa menetapkan format ke 2 digit setelah
titik desimal.


\>format(12,2); K\*q^10


        6719.58 

Mari kita cetak angka yang dibulatkan menjadi 2 digit dalam kalimat
lengkap.


\>"Starting from " + K + "$ you get " + round(K\*q^10,2) + "$."


    Starting from 5000$ you get 6719.58$.

Bagaimana jika kita ingin mengetahui hasil antara dari tahun ke-1
hingga tahun ke-9? Untuk hal ini, bahasa matriks euler sangat
membantu. Anda tidak perlu menulis perulangan, tetapi cukup
memasukkan.


\>K\*q^(0:10)


    Real 1 x 11 matrix
    
        5000.00     5150.00     5304.50     5463.64     ...

Bagaimana keajaiban ini bekerja? Pertama, ekspresi 0:10 mengembalikan
sebuah vektor bilangan bulat


\>short 0:10


    [0,  1,  2,  3,  4,  5,  6,  7,  8,  9,  10]

Kemudian semua operator dan fungsi dalam Euler dapat diterapkan pada
vektor elemen demi elemen. Jadi


\>short q^(0:10)


    [1,  1.03,  1.0609,  1.0927,  1.1255,  1.1593,  1.1941,  1.2299,
    1.2668,  1.3048,  1.3439]

adalah vektor faktor q^0 hingga q^10. Ini dikalikan dengan K, dan kita
mendapatkan vektor nilai.


\>VK=K\*q^(0:10);


Tentu saja, cara yang realistis untuk menghitung suku bunga ini adalah
dengan membulatkan ke sen terdekat setelah setiap tahun. Mari kita
tambahkan fungsi untuk ini.


\>function oneyear (K) := round(K\*q,2)


Mari kita bandingkan kedua hasil tersebut, dengan dan tanpa
pembulatan.


\>longest oneyear(1234.57), longest 1234.57\*q


                    1271.61 
                  1271.6071 

Sekarang tidak ada rumus sederhana untuk tahun ke-n, dan kita harus
mengulang selama bertahun-tahun. Euler menyediakan banyak solusi untuk
ini.


Cara termudah adalah iterasi fungsi, yang mengulang fungsi yang
diberikan beberapa kali.


\>VKr=iterate("oneyear",5000,10)


    Real 1 x 11 matrix
    
        5000.00     5150.00     5304.50     5463.64     ...

Kita bisa mencetaknya dengan cara yang bersahabat, menggunakan format
kita dengan angka desimal yang tetap.


\>VKr'


        5000.00 
        5150.00 
        5304.50 
        5463.64 
        5627.55 
        5796.38 
        5970.27 
        6149.38 
        6333.86 
        6523.88 
        6719.60 

Untuk mendapatkan elemen tertentu dari vektor, kita menggunakan indeks
dalam tanda kurung siku.


\>VKr[2], VKr[1:3]


        5150.00 
        5000.00     5150.00     5304.50 

Yang mengejutkan, kita juga dapat menggunakan vektor indeks. Ingatlah
bahwa 1:3 menghasilkan vektor [1,2,3].


Mari kita bandingkan elemen terakhir dari nilai yang dibulatkan dengan
nilai penuh.


\>VKr[-1], VK[-1]


        6719.60 
        6719.58 

Perbedaannya sangat kecil.


# Menyelesaikan Persamaan

Sekarang kita ambil fungsi yang lebih maju, yang menambahkan tingkat
uang tertentu setiap tahun.


\>function onepay (K) := K\*q+R


Kita tidak perlu menentukan q atau R untuk definisi fungsi. Hanya jika
kita menjalankan perintah, kita harus mendefinisikan nilai-nilai ini.
Kami memilih R = 200.


\>R=200; iterate("onepay",5000,10)


    Real 1 x 11 matrix
    
        5000.00     5350.00     5710.50     6081.82     ...

Bagaimana jika kita menghapus jumlah yang sama setiap tahun?


\>R=-200; iterate("onepay",5000,10)


    Real 1 x 11 matrix
    
        5000.00     4950.00     4898.50     4845.45     ...

Kami melihat bahwa uangnya berkurang. Jelas, jika kita hanya
mendapatkan 150 bunga di tahun pertama, tetapi menghapus 200, kita
kehilangan uang setiap tahun.


Bagaimana kita dapat menentukan berapa tahun uang itu akan bertahan?
Kita harus menulis perulangan untuk ini. Cara termudah adalah dengan
melakukan perulangan yang cukup lama.


\>VKR=iterate("onepay",5000,50)


    Real 1 x 51 matrix
    
        5000.00     4950.00     4898.50     4845.45     ...

Dengan menggunakan bahasa matriks, kita dapat menentukan nilai negatif
pertama dengan cara berikut.


\>min(nonzeros(VKR<0))


          48.00 

Alasannya adalah karena nonzeros(VKR&lt;0) mengembalikan vektor dengan
indeks i, di mana VKR[i]&lt;0, dan min menghitung indeks minimal.


Karena vektor selalu dimulai dengan indeks 1, maka jawabannya adalah
47 tahun.


Fungsi iterate() memiliki satu trik lagi. Fungsi ini dapat menerima
kondisi akhir sebagai argumen. Kemudian fungsi ini akan mengembalikan
nilai dan jumlah iterasi.


\>{x,n}=iterate("onepay",5000,till="x<0"); x, n,


         -19.83 
          47.00 

Mari kita coba menjawab pertanyaan yang lebih ambigu. Anggaplah kita
tahu bahwa nilainya adalah 0 setelah 50 tahun. Berapakah tingkat suku
bunganya?


Ini adalah pertanyaan yang hanya bisa dijawab secara numerik. Di bawah
ini, kami akan menurunkan rumus yang diperlukan. Kemudian Anda akan
melihat bahwa tidak ada rumus yang mudah untuk suku bunga. Namun untuk
saat ini, kita akan mencari solusi numerik.


Langkah pertama adalah mendefinisikan sebuah fungsi yang melakukan
iterasi sebanyak n kali. Kita tambahkan semua parameter ke fungsi ini.


\>function f(K,R,P,n) := iterate("x\*(1+P/100)+R",K,n;P,R)[-1]


Perulangannya sama seperti di atas


Tetapi kita tidak lagi menggunakan nilai global R dalam ekspresi kita.
Fungsi-fungsi seperti iterate() memiliki trik khusus dalam Euler. Anda
bisa mengoper nilai variabel dalam ekspresi sebagai parameter titik
koma. Dalam hal ini P dan R.


Selain itu, kita hanya tertarik pada nilai terakhir. Jadi kita
mengambil indeks [-1].


Mari kita coba sebuah tes.


\>f(5000,-200,3,47)


         -19.83 

Sekarang kita bisa menyelesaikan masalah kita.


\>solve("f(5000,-200,x,50)",3)


           3.15 

Rutin penyelesaian menyelesaikan ekspresi = 0 untuk variabel x.
Jawabannya adalah 3,15% per tahun. Kita mengambil nilai awal 3% untuk
algoritma ini. Fungsi solve() selalu membutuhkan nilai awal.


Kita dapat menggunakan fungsi yang sama untuk menyelesaikan pertanyaan
berikut: Berapa banyak yang dapat kita hapus per tahun sehingga modal
awal habis setelah 20 tahun dengan asumsi tingkat bunga 3% per tahun.


\>solve("f(5000,x,3,20)",-200)


        -336.08 

Perhatikan bahwa Anda tidak dapat menyelesaikan jumlah tahun, karena
fungsi kita mengasumsikan n sebagai nilai bilangan bulat.


## Solusi Simbolik untuk Masalah Suku Bunga

Kita dapat menggunakan bagian simbolik dari Euler untuk mempelajari
masalah ini. Pertama, kita mendefinisikan fungsi onepay() secara
simbolik.


\>function op(K) &= K\*q+R; $&op(K)


Sekarang kita bisa mengulangi hal ini.


\>$&op(op(op(op(K)))), $&expand(%)


Kita melihat sebuah pola. Setelah n periode, kita memiliki


Rumus tersebut adalah rumus untuk jumlah geometris, yang dikenal
dengan Maxima.


\>&sum(q^k,k,0,n-1); $& % = ev(%,simpsum)


Ini sedikit rumit. Penjumlahan dievaluasi dengan flag “simpsum” untuk
menguranginya menjadi hasil bagi.


Mari kita buat sebuah fungsi untuk ini.


\>function fs(K,R,P,n) &= (1+P/100)^n\*K + ((1+P/100)^n-1)/(P/100)\*R; $&fs(K,R,P,n)


Fungsi ini melakukan hal yang sama seperti fungsi f kita sebelumnya.
Tetapi fungsi ini lebih efektif.


\>longest f(5000,-200,3,47), longest fs(5000,-200,3,47)


         -19.82504734650985 
         -19.82504734652684 

Sekarang kita dapat menggunakannya untuk menanyakan waktu n. Kapan
modal kita habis? 


Perkiraan awal kita adalah 30 tahun.


\>solve("fs(5000,-330,3,x)",30)


          20.51 

Jawaban ini mengatakan bahwa nilai tersebut akan menjadi negatif
setelah 21 tahun.


Kita juga bisa menggunakan sisi simbolis dari Euler untuk menghitung
rumus pembayaran.


Asumsikan kita mendapatkan pinjaman sebesar K, dan membayar n kali
pembayaran sebesar R (dimulai setelah tahun pertama) sehingga
menyisakan sisa utang sebesar Kn (pada saat pembayaran terakhir).
Rumus untuk hal ini adalah sebagai berikut


\>equ &= fs(K,R,P,n)=Kn; $&equ


Biasanya rumus ini diberikan dalam bentuk


\>equ &= (equ with P=100\*i); $&equ


Kita dapat menyelesaikan laju R secara simbolis.


\>$&solve(equ,R)


Seperti yang dapat Anda lihat dari rumusnya, fungsi ini mengembalikan
kesalahan floating point untuk i = 0. Euler tetap memplotnya.


Tentu saja, kita memiliki batas berikut.


\>$&limit(R(5000,0,x,10),x,0)


Jelasnya, tanpa bunga kita harus membayar kembali 10 suku bunga 500.


Persamaan ini juga dapat diselesaikan untuk n. Akan terlihat lebih
baik jika kita menerapkan beberapa penyederhanaan.


\>fn &= solve(equ,n) | ratsimp; $&fn


# Contoh Penyelesaian Soal-Soal Aljabar

## R.2 Exercise Set



Write an equvalent expression without negative exponents


\>$&((24\*a^10\*b^(-8)\*c^7)/(12\*a^6\*b^(-3)\*c^5))^(-5)


$$\frac{b^{25}}{32\,a^{20}\,c^{10}}$$Calculate.


\>$&(2^6\*2^(-3)/2^(10)/2^(-8))


$$2$$Syntesis


Saving plan. The formula


gives the amount S accumulated in a savings plan when a deposit of P
dollars is made each month for t years in an account with interest
rate r, compounded monthly.


\>function savingPlan(deposit, years, interestRate) ...


    return deposit * ((1 + (years / 12) ^ (12 * years)) - 1 / (interestRate / 12))
    endfunction
</pre>
97. James deposits $250 in a retirement account each month beginning
at age 40. If the investment earns 5% interest, compounded monthly,
how much will have accumulated in the account when he retires 27 years
later?


\>result := savingPlan(250, 27, 0.05)


    3.19945404606e+116

\>&round(result)


    
                                round(result)
    

98. Kayla deposits $100 in a retirement account each month beginning
at age 25. If the investment earns 4% interest, compounded monthly,
how much will have accumulated in the account when she retires at age
65?


\>savingPlan(100, 65-25, 0.04)


    9.58953910649e+252

100. Lamont wants to have $200,000 accumulated in a retirement account
by age 70. If he starts making monthly deposits to the plan at age 30
and can count on an interest rate of 4.5%, compounded monthly, how
much should he deposit each month in order to accomplish this?


\>savingPlan(200000, 70 - 30, 0.045)


    1.9179078213e+256

Simplify. Assume that all exponents are integers, all denominators are
nonzero, and zero is not raised to a nonpositive power


\>$&((m^(x-b)\*n^(x+b))^(x)\*(m^(b)\*n^(-b))^(x))


$$\left(\frac{m^{b}}{n^{b}}\right)^{x}\,\left(m^{x-b}\,n^{x+b}\right)
 ^{x}$$## R.3 Exercise Set



Determine the terms and the degree of the polynomials


\>$&factor((2\*x + 3\*y + x - 7) + (4\*x - 2\*y - z + 8) + (-3\*x + y - 2\*z -4))


$$-3\,z+2\,y+4\,x-3$$\>$&factor((2\*x^2 + 12\*x\*y - 11) + (6\*x^2 - 2\*x + 4) + (-x^2 - y - 2))


$$12\,x\,y-y+7\,x^2-2\,x-9$$\> 


\>$&factor((3\*x^2 - 2\*x - x^3 + 2) - (5\*x^2 - 8\*x - x^3 + 4))


$$-2\,\left(x^2-3\,x+1\right)$$\> 


\>$&expand((5\*x - 3)^2)


$$25\,x^2-30\,x+9$$\> 


Systhesis


Multiply. Assume that all exponents are natural numbers.


\>$&expand((a + b + c)^2)


$$c^2+2\,b\,c+2\,a\,c+b^2+2\,a\,b+a^2$$## R.4 Exercise Set

Factor the difference of squares


\>$&factor(z^2 - 81)


$$\left(z-9\right)\,\left(z+9\right)$$Factor the square of a binomial.


\>$&factor(5\*a^2 - 10\*a\*b + 5\*b^2)


$$5\,\left(b-a\right)^2$$Factor the sum or difference of cubes.


\>$&factor(t^6 + 1)


$$\left(t^2+1\right)\,\left(t^4-t^2+1\right)$$Factor completely.


\>$&factor(4\*x^2 + 12\*x\*y^2)


$$4\,x\,\left(3\,y^2+x\right)$$Synthesis


Factor.


\>$&factor((x + 0.01)^2 - x^2)


$$\frac{200\,x+1}{10000}$$Factor. Assume that variables in exponents represent


natural numbers.


\>$&factor((y - 1)^4 - (y - 1)^2)


$$\left(y-2\right)\,\left(y-1\right)^2\,y$$## R.5 Exercise Set

\>$&solve(7\*(3\*x + 6) = 11 - (x + 2), x)


$$\left[ x=-\frac{3}{2} \right] $$\>$&solve(y^2 - 4\*y - 45 = 0, y)


$$\left[ y=9 , y=-5 \right] $$

for: h (Area of a trapezoid)


\>$&(solve(A = (1/2)\* h \* (b1 + b2), h))


$$\left[ h=\frac{2\,A}{{\it b_2}+{\it b_1}} \right] $$

for A


\>$&solve(A\*x + By = C, A)


$$\left[ A=\frac{C-{\it By}}{x} \right] $$Synthesis


Solve


\>$&solve(3\*(5 - 3\*(4 - t)) - 2 = 5\*(3\*(5 \* t - 4) + 8) - 26, t)


$$\left[ t=\frac{23}{66} \right] $$\>$&solve(3\*x^3 + 6\*x^2 - 27\*x - 54 = 0, x)


$$\left[ x=-3 , x=-2 , x=3 \right] $$<pre class="udf">    
</pre>
    

## R.6 Exercise Set



Penyelesaian :


mencari faktor pembilang


\>$&factor(x^3-6\*x^2+9\*x)


$$\left(x-3\right)^2\,x$$mencari faktor penyebut


\>$&factor(x^3-3\*x^2)


$$\left(x-3\right)\,x^2$$jadi tugas kita menyelesaikan :


\>$&((x-3)^2 \* x)/((x-3) \* x^2)


$$\frac{x-3}{x}$$atau dengan perintah EMT untuk menyelesaikan soal ini adalah


\>$&ratsimp((x^3-6\*x^2+9\*x)/(x^3-3\*x^2)) ...  
\>   //menyederhanakan pecahan dengan perintah ratsimp


$$\frac{x-3}{x}$$17. Multiply or divide and, if possible, simplify




Penyelesaian:


\>$&ratsimp((r-s)/(r+s))\*((r^2-s^2)/((r-s)^2)) ...  
\>   //menyederhanakan pecahan


$$\frac{r^2-s^2}{\left(r-s\right)\,\left(s+r\right)}$$\>$&(r^2-s^2)/(r-s)\*(s+r), $&ratsimp(%) ...  
\>   //menyederhanakan pecahan lalu hasilnya disederhanakan lagi pakai %


$$\frac{\left(s+r\right)\,\left(r^2-s^2\right)}{r-s}$$$$s^2+2\,r\,s+r^2$$

Penyelesaian:


\>$&ratsimp((c^3+8)/(c^2-4))/((c^2-2\*c+4)/(c^2-4\*c+4)), $&ratsimp(%) ...  
\>   //menyederhanakan pecahan lalu hasilnya disederhanakan lagi pakai %


$$\frac{c^2-4\,c+4}{c-2}$$$$c-2$$40. add or subtract and, if possible, simplify




Penyelesaian:


\>$&expand(6/y^2+6\*y+9)-(5/y-3), $&ratsimp(%) ...  
\>   //menyederhanakan pecahan lalu melakukan operasi pada hasilnya


$$6\,y-\frac{5}{y}+\frac{6}{y^2}+12$$$$\frac{6\,y^3+12\,y^2-5\,y+6}{y^2}$$62. Simplify




Penyelesaian:


\>$&factor((a^2/b)+(b^2/a))/(a^2-a\*b+b^2) ...  
\>   //menyederhanakan bentuk paling sederhana dengan perintah factor


$$\frac{b+a}{a\,b}$$## R.7 Exercise Set



53. Simplify. Assume that no radicands were formed by raising negative
quantities to even powers.




Penyelesaian:


\>$&expand(2\*(3)^1/2 + (5)^1/2)\*((3)^1/2 - 3\*(5)^1/2)


$$-33$$## Review Exercise

66. the cost of a house is $98,000. The down payment is %16,000, the
interest rate is 6 1/2%, and the loan period is 25 years. What is the
monthly mortgage payment?


Penyelesaian :


Rumus angsuran per bulan:


dengan M : angsuran per bulan


P : jumlah pinjaman


r : suku bunga bulanan


n : jumlah total pembayaran (dalam bulan)


diketahui:


Harga rumah : $98,000


Uang muka : $16,000


suku bunga tahunan: 6 1/2%


6 1/2% diubah menjadi 6.5%


lama angsur : 25 tahun


ditanya: angsuran per bulan berapa


Variabel yang dibutuhkan pada rumus adalah :


\>P = 98000-16000


    82000

\>r = 6.5/100


    0.065

\>n = 25\*12


    300

Substitusi semua variabel yang telah diperoleh ke rumus M


\>M = P \* (r/12 \* (1 + r/12)^n)/((1+r/12)^n -1 )


    553.669872305

Jadi, biaya angsuran per bulan selama 25 tahun dengan suku bunga
sebesar 6.5% persen per tahun adalah $553,669872305




Penyelesaian:


\>$&expand((x^n + 10)\*(x^n - 4)) ...  
\>   //menjabarkan fungsi


$$x^{2\,n}+6\,x^{n}-40$$

Penyelesaian:


\>$&expand((t^a + t^(-a))^2) ...  
\>   //menjabarkan fungsi


$$t^{2\,a}+\frac{1}{t^{2\,a}}+2$$\>$&showev('expand((a^n - b^n)^3)), $&expand((a^n - b^n)^3) ...  
\>   //menjabarkan fungsi dengan showev


$${\it expand}\left(\left(a^{n}-b^{n}\right)^3\right)=-b^{3\,n}+3\,a
 ^{n}\,b^{2\,n}-3\,a^{2\,n}\,b^{n}+a^{3\,n}$$$$-b^{3\,n}+3\,a^{n}\,b^{2\,n}-3\,a^{2\,n}\,b^{n}+a^{3\,n}$$## 2.3 Exercise Set

Given that




Find each of the following


Menyimpan semua nilai fx, gx, dan hx.


\>fx &= 3\*x + 1; gx &= x^2 - 2\*x - 6; hx &= x^3;


1. Mencari nilai




Penyelesaian:


fungsi komposisi di atas juga dapat ditulis sebagai :


Mencari nilai g(-1)


\>gx(-1) //cara manual


    -3

Lalu mencari nilai f(-3)


\>fx(-3)


    -8

Perintah fungsi komposisi di EMT


Akan menghasilkan hasil yang sama dengan cara manual di atas. Cara ini
lebih efisien.


\>fx(gx(-1)) //cara cepat


    -8

4. Mencari nilai




Penyelesaian:


Fungsi komposisi di atas juga dapat ditulis


\>gx(hx(1/2))


    -6.234375

7. Mencari nilai




Penyelesaian:


Fungsi komposisi di atas bisa ditulis


\>fx(gx(-3))


    28

11. Mencari nilai




Penyelesaian


Fungsi komposisi di atas dapat ditulis


\>hx(hx(2))


    512

13. Mencari nilai




Penyelesaian:


Fungsi komposisi di atas dapat ditulis


\>fx(fx(-4))


    -32

## 3.1 Exercise Set

11. Simplify. Where answer in the form a + bi, where a and b are real
numbers.




Penyelesaian:


\>bilangan1 = -5 + 3\*I, bilangan2 = 7 + 8\*I, bilangan1 + bilangan2


    -5+3i
    7+8i
    2+11i



Penyelesaian:


\>bilangan1 = 10 + 7\*I, bilangan2 = 5 + 3\*I, bilangan1 - bilangan2


    10+7i
    5+3i
    5+4i



Penyelesaian:


\>bilangan1 = 7\*I, bilangan2 = 2-5\*I, bilangan1\*bilangan2


    0+7i
    2-5i
    35+14i



Penyelesaian:


\>bilangan1 = 3\*I, bilangan2 = 6 + 4\*I, bilangan1\*bilangan2


    0+3i
    6+4i
    -12+18i



Penyelesaian:


\>bilangan1 = -2\*I, bilangan2 = -8 + 3\*I, bilangan1\*bilangan2


    0-2i
    -8+3i
    6+16i

## 3.4 Exercise Set

\>$&solve((1/4)+(1/5)=(1/t))


$$\left[ t=\frac{20}{9} \right] $$\>$&solve(((x+2)/4)-((x-1)/5)=15)


$$\left[ x=286 \right] $$\>$&solve(((t+1)/3)-((t-1)/2))


$$\left[ t=5 \right] $$\>$&solve((5/(3\*x+2))=(3/2\*x))


$$\left[ x=\frac{-\sqrt{11}-1}{3} , x=\frac{\sqrt{11}-1}{3} \right] $$\>$&solve((3\*x-4)^1/2 = 1)


$$\left[ x=2 \right] $$## 3.5 Exercise Set

\>$&solve(abs(x+3)-2=8, x)


$$\left[ \left| x+3\right| =10 \right] $$\>$&solve(abs(x+3))


$$\left[ x=-3 \right] $$\>$&solve(abs(x+3)-2=8)


$$\left[ \left| x+3\right| =10 \right] $$\>$&solve((abs(x+3))=10)


$$\left[ \left| x+3\right| =10 \right] $$\>$&expand(abs(x+3)=10)


$$\left| x+3\right| =10$$\>$&solve((x+3)=10)


$$\left[ x=7 \right] $$\>$&solve((x+3)=-10)


$$\left[ x=-13 \right] $$\>$&solve(abs(5\*x+4)+2=5, x)


$$\left[ \left| 5\,x+4\right| =3 \right] $$\>$&solve((5\*x+4)=3)


$$\left[ x=-\frac{1}{5} \right] $$\>$&solve((5\*x+4)=-3)


$$\left[ x=-\frac{7}{5} \right] $$\>$&solve(5-(abs(4\*x+3)=2))


$$\left[ \left| 4\,x+3\right| =2 \right] $$\>$&solve((4\*x+3)=2)


$$\left[ x=-\frac{1}{4} \right] $$\>$&solve((4\*x+3)=-2)


$$\left[ x=-\frac{5}{4} \right] $$\>&load(fourier\_elim)


    
            C:/Program Files/Euler x64/maxima/share/maxima/5.35.1/share/f\
    ourier_elim/fourier_elim.lisp
    

\>$&fourier\_elim([abs(2\*x)] \>= 6, [x])


$$\left[ \left[ 2\,\left(\left| x\right| -3\right) \right] =0
  \right] \lor \left[ \left[ 2\,\left(\left| x\right| -3\right)
  \right] >0 \right] $$\>$&fourier\_elim([abs(2\*x)] \>= 6, [x])


$$\left[ \left[ 2\,\left(\left| x\right| -3\right) \right] =0
  \right] \lor \left[ \left[ 2\,\left(\left| x\right| -3\right)
  \right] >0 \right] $$## Chapter 3 test

\>$&solve(x+5\*(x)^1/2-36=0)


$$\left[ x=\frac{72}{7} \right] $$\>$&solve(((x+4)^1/2)-((x-4)^1/2=2))


$$\left[ x=8 \right] $$\>$&solve(((x+4)^1/2)-2=1)


$$\left[ x=2 \right] $$\>$&fourier\_elim([abs(x+3)<=4], [x])


$$\left[ x=1 \right] \lor \left[ x=-7 \right] \lor \left[ -7<x , x<1
  \right] $$\>$&fourier\_elim([abs(2\*x-1)<5],[x])


$$\left[ -2<x , x<3 \right] $$## 4.1 Exercise Set

\>$&solve((x^2-5\*x+6)^2)


$$\left[ x=3 , x=2 \right] $$\>$&solve(x^4-4\*x^2+3)


$$\left[ x=-1 , x=1 , x=-\sqrt{3} , x=\sqrt{3} \right] $$\>$&solve(x^3-x^2-2\*x+2)


$$\left[ x=-\sqrt{2} , x=\sqrt{2} , x=1 \right] $$\>$&fourier\_elim([2\*y-3\>=1-y+5],[x])


$$\left[ y-3 \right] \lor \left[ y-3>0 \right] $$\>$&fourier\_elim([x+(1/4)<=(2/3)],[x])


$$\left[ x=\frac{5}{12} \right] \lor \left[ x<\frac{5}{12} \right] $$## Mid-Chapter Mixed Review



find g(-5)


\>function g(x) := (x^3-9x^2+4x-10)

\>g(-5)


    -380



find


\>a = - sqrt(2)


    -1.41421356237

\>fx &= 5\*x^4 + x^3 - x; fx(a)


    18.5857864376

\>$&expand((x^5-5)/(x+1))


$$\frac{x^5}{x+1}-\frac{5}{x+1}$$

find


\>function f(x) :=(20\*x^2-40\*x)

\>f(1/2)


    -15



Penyelesaian :


\>$&factor(x^3-2\*x^2-55\*x+56)


$$\left(x-8\right)\,\left(x-1\right)\,\left(x+7\right)$$\>$&solve(x^3-2\*x^2-55\*x+56)


$$\left[ x=-7 , x=8 , x=1 \right] $$

Penyelesaian :


\>$&factor(x^4-2\*x^3-13\*x^2+14\*x+24)


$$\left(x-4\right)\,\left(x-2\right)\,\left(x+1\right)\,\left(x+3
 \right)$$\>$&solve(x^4-2\*x^3-13\*x^2+14\*x+24)


$$\left[ x=-3 , x=-1 , x=2 , x=4 \right] $$## 4.3 Exercise Set

penyelesaian :


\>$&solve(x^3+4\*x^2+x-6)


$$\left[ x=-3 , x=-2 , x=1 \right] $$Penyelesaian


\>$&solve(x^4+x^3-3\*x^2-5\*x-2)


$$\left[ x=2 , x=-1 \right] $$

Penyelesaian


\>$&solve(x^3-7\*x+6)


$$\left[ x=1 , x=2 , x=-3 \right] $$

Penyelesaian :


\>$&solve(x^3-12\*x+16)


$$\left[ x=-4 , x=2 \right] $$\>$&solve(-x^3+3\*x^2+6\*x-8)


$$\left[ x=-2 , x=4 , x=1 \right] $$# Menggambar Grafik 2D dengan EMT

Notebook ini menjelaskan tentang cara menggambar berbagaikurva dan
grafik 2D dengan software EMT. EMT menyediakan fungsi plot2d() untuk
menggambar berbagai kurva dan grafik dua dimensi (2D).


## Plot Dasar

Ada beberapa fungsi dasar plot. Ada koordinat layar, yang selalu
berkisar dari 0 hingga 1024 di setiap sumbu, tidak peduli apakah
layarnya persegi atau tidak. Selain itu ada koordinat plot, yang dapat
diatur dengan setplot().Pemetaan antara koordinat bergantung pada
jendela plot saat ini. Misalnya, shrinkwindow() default menyisakan
ruang untuk  label sumbu dan judul plot.


Dalam contoh ini, kita hanya menggambar beberapa garis acak dengan
berbagai warna. Untuk detail tentang fungsi-fungsi ini, pelajari
fungsi-fungsi inti EMT.


\>clg; // clear screen

\>window(0,0,1024,1024); // use all of the window

\>setplot(0,1,0,1); // set plot coordinates

\>hold on; // start overwrite mode

\>n=100; X=random(n,2); Y=random(n,2);  // get random points

\>colors=rgb(random(n),random(n),random(n)); // get random colors

\>loop 1 to n; color(colors[#]); plot(X[#],Y[#]); end; // plot

\>hold off; // end overwrite mode

\>insimg; // insert to notebook


![images/Final%20Project%20Aplikom%20Semester%203-078.png](images/Final%20Project%20Aplikom%20Semester%203-078.png)

\>reset;


Perlu untuk menahan grafik, karena perintah plot() akan menghapus
jendela plot.


Untuk menghapus semua yang telah kita lakukan, kita gunakan reset().


Untuk menampilkan gambar hasil plot di layar notebook, perintah
plot2d() dapat diakhiri dengan titik dua (:). Cara lain adalah
perintah plot2d() diakhiri dengan titik koma (;), kemudian menggunakan
perintah insimg() untuk menampilkan gambar hasil plot.


Untuk contoh lain, kita menggambar plot sebagai inset di plot lain.
Ini dilakukan dengan menentukan jendela plot yang lebih kecil.
Perhatikan bahwa jendela ini tidak menyediakan ruang untuk label sumbu
di luar jendela plot. Kita harus menambahkan beberapa margin untuk ini
sesuai kebutuhan. Perhatikan bahwa kita menyimpan dan memulihkan
jendela penuh, dan menahan plot saat ini saat kita memplot inset.


\>plot2d("x^3-x");

\>xw=200; yw=100; ww=300; hw=300;

\>ow=window();

\>window(xw,yw,xw+ww,yw+hw);

\>hold on;

\>barclear(xw-50,yw-10,ww+60,ww+60);

\>plot2d("x^4-x",grid=6):


![images/Final%20Project%20Aplikom%20Semester%203-079.png](images/Final%20Project%20Aplikom%20Semester%203-079.png)

\>hold off;

\>window(ow);


Plot dengan beberapa gambar dibuat dengan cara yang sama. Ada fungsi
utilitas figure() untuk ini.


## Aspek Plot

Plot default menggunakan jendela plot persegi. Anda dapat mengubahnya
dengan fungsi aspect(). Jangan lupa untuk mengatur  ulang aspect
nanti. Anda juga dapat mengubah default ini di menu dengan "Set
Aspect" ke rasio aspek tertentu atau ke ukuran jendela grafik saat
ini.


Namun, Anda juga dapat mengubahnya untuk satu plot. Untuk ini, ukuran
area plot saat ini diubah, dan jendela diatur sehingga  label memiliki
cukup ruang.


\>aspect(2); // rasio panjang dan lebar 2:1

\>plot2d(["sin(x)","cos(x)"],0,2pi):


![images/Final%20Project%20Aplikom%20Semester%203-080.png](images/Final%20Project%20Aplikom%20Semester%203-080.png)

\>aspect();

\>reset;


Fungsi reset() mengembalikan pengaturan plot default termasuk rasio
aspek.


Plot 2D dalam Euler


EMT Math Toolbox memiliki plot dalam 2D, baik untuk data maupun
fungsi. EMT menggunakan fungsi plot2d. Fungsi ini dapat  memplot
fungsi dan data.


Dimungkinkan untuk membuat plot di Maxima menggunakan Gnuplot atau di
Python menggunakan Math Plot Lib.


Euler dapat memplot plot 2D dari 


- ekspresi


- fungsi, variabel, atau kurva berparameter,


- vektor nilai xy,


- titik-titik pada bidang,


- kurva implisit dengan level atau daerah level.


- Fungsi kompleks


Gaya plot mencakup berbagai gaya untuk garis dan titik, plot batang,
dan plot berbayang.


# Plot Ekspresi atau Variabel

Ekspresi tunggal dalam "x" (misalnya "4*x^2") atau nama suatu fungsi
(misalnya "f") menghasilkan grafik fungsi tersebut.


Berikut adalah contoh paling dasar, yang menggunakan rentang default
dan menetapkan rentang y yang tepat agar sesuai dengan plot fungsi.


Catatan: Jika Anda mengakhiri baris perintah dengan titik dua ":",
plot akan dimasukkan ke dalam jendela teks. Jika tidak, tekan TAB
untuk melihat plot jika jendela plot tertutup.


\>plot2d("x^2"):


![images/Final%20Project%20Aplikom%20Semester%203-081.png](images/Final%20Project%20Aplikom%20Semester%203-081.png)

\>aspect(1.5); plot2d("x^3-x"):


![images/Final%20Project%20Aplikom%20Semester%203-082.png](images/Final%20Project%20Aplikom%20Semester%203-082.png)

\>a:=5.6; plot2d("exp(-a\*x^2)/a"); insimg(30); // menampilkan gambar hasil plot setinggi 25 baris


![images/Final%20Project%20Aplikom%20Semester%203-083.png](images/Final%20Project%20Aplikom%20Semester%203-083.png)

Dari beberapa contoh sebelumnya Anda dapat melihat bahwa aslinya
gambar plot menggunakan sumbu X dengan rentang nilai dari -2 sampai
dengan 2. Untuk mengubah rentang nilai X dan Y, Anda dapat menambahkan
nilai-nilai batas X (dan Y) di belakang ekspresi yang digambar.


Rentang plot ditetapkan dengan parameter yang ditetapkan berikut


* 
a,b: rentang-x (default -2,2)

* 
c,d: rentang-y (default: skala dengan nilai)

* 
r: alternatifnya radius di sekitar pusat plot

* 
cx,cy: koordinat pusat plot (default 0,0)


\>plot2d("x^3-x",-1,2):


![images/Final%20Project%20Aplikom%20Semester%203-084.png](images/Final%20Project%20Aplikom%20Semester%203-084.png)

\>plot2d("sin(x)",-2\*pi,2\*pi): // plot sin(x) pada interval [-2pi, 2pi]


![images/Final%20Project%20Aplikom%20Semester%203-085.png](images/Final%20Project%20Aplikom%20Semester%203-085.png)

\>plot2d("cos(x)","sin(3\*x)",xmin=0,xmax=2pi):


![images/Final%20Project%20Aplikom%20Semester%203-086.png](images/Final%20Project%20Aplikom%20Semester%203-086.png)

Alternatif untuk titik dua adalah perintah insimg(baris), yang
menyisipkan plot yang menempati sejumlah baris teks tertentu.


Dalam opsi, plot dapat diatur agar muncul


* 
di jendela terpisah yang dapat diubah ukurannya,

* 
di jendela catatan.


Lebih banyak gaya dapat dicapai dengan perintah plot yang spesifik.


Bagaimanapun, tekan tombol tabulator untuk melihat plot, jika
tersembunyi.


Untuk membagi jendela menjadi beberapa plot, gunakan perintah
figure(). Dalam contoh ini, kita memplot x^1 hingga x^4 ke dalam 4
bagian jendela. figure(0) akan mengatur ulang jendela default.


\>reset;

\>figure(2,2); ...  
\>   for n=1 to 4; figure(n); plot2d("x^"+n); end; ...  
\>   figure(0):


![images/Final%20Project%20Aplikom%20Semester%203-087.png](images/Final%20Project%20Aplikom%20Semester%203-087.png)

Dalam plot2d(), tersedia gaya alternatif dengan grid=x. Sebagai
gambaran umum, kami menampilkan berbagai gaya grid dalam satu gambar
(lihat di bawah untuk perintah figure()). Gaya grid=0 tidak
disertakan. Gaya ini tidak menampilkan grid dan bingkai.


\>figure(3,3); ...  
\>   for k=1:9; figure(k); plot2d("x^3-x",-2,1,grid=k); end; ...  
\>   figure(0):


![images/Final%20Project%20Aplikom%20Semester%203-088.png](images/Final%20Project%20Aplikom%20Semester%203-088.png)

Jika argumen untuk plot2d() adalah ekspresi yang diikuti oleh empat
angka, angka-angka ini adalah rentang x dan y untuk plot.


Sebagai alternatif, a, b, c, d dapat ditetapkan sebagai parameter yang
ditetapkan sebagai a=... dst.


Dalam contoh berikut, kami mengubah gaya kisi, menambahkan label, dan
menggunakan label vertikal untuk sumbu y.


\>aspect(1.5); plot2d("sin(x)",0,2pi,-1.2,1.2,grid=3,xl="x",yl="sin(x)"):


![images/Final%20Project%20Aplikom%20Semester%203-089.png](images/Final%20Project%20Aplikom%20Semester%203-089.png)

\>plot2d("sin(x)+cos(2\*x)",0,4pi):


![images/Final%20Project%20Aplikom%20Semester%203-090.png](images/Final%20Project%20Aplikom%20Semester%203-090.png)

Gambar yang dihasilkan dengan memasukkan plot ke dalam jendela teks
disimpan dalam direktori yang sama dengan buku catatan, secara default
dalam subdirektori bernama "images". Gambar tersebut juga digunakan
oleh ekspor HTML.


Anda cukup menandai gambar apa saja dan menyalinnya ke clipboard
dengan Ctrl-C. Tentu saja, Anda juga dapat mengekspor  grafik saat ini
dengan fungsi-fungsi di menu File.


Fungsi atau ekspresi dalam plot2d dievaluasi secara adaptif. Untuk
kecepatan lebih tinggi, matikan plot adaptif dengan &lt;adaptive dan
tentukan jumlah subinterval dengan n=... Ini hanya diperlukan dalam
kasus yang jarang terjadi.


\>plot2d("sign(x)\*exp(-x^2)",-1,1,<adaptive,n=10000):


![images/Final%20Project%20Aplikom%20Semester%203-091.png](images/Final%20Project%20Aplikom%20Semester%203-091.png)

\>plot2d("x^x",r=1.2,cx=1,cy=1):


![images/Final%20Project%20Aplikom%20Semester%203-092.png](images/Final%20Project%20Aplikom%20Semester%203-092.png)

Perhatikan bahwa x^x tidak didefinisikan untuk x&lt;=0. Fungsi plot2d
menangkap kesalahan ini, dan mulai memplot segera setelah fungsi
didefinisikan. Ini berfungsi untuk semua fungsi yang mengembalikan NAN
di luar rentang definisinya.


\>plot2d("log(x)",-0.1,2):


![images/Final%20Project%20Aplikom%20Semester%203-093.png](images/Final%20Project%20Aplikom%20Semester%203-093.png)

Parameter square=true (atau &gt;square) memilih rentang y secara otomatis
sehingga hasilnya adalah jendela plot persegi.  Perhatikan bahwa
secara default, Euler menggunakan ruang persegi di dalam jendela plot.


\>plot2d("x^3-x",\>square):


![images/Final%20Project%20Aplikom%20Semester%203-094.png](images/Final%20Project%20Aplikom%20Semester%203-094.png)

\>plot2d(''integrate("sin(x)\*exp(-x^2)",0,x)'',0,2): // plot integral


![images/Final%20Project%20Aplikom%20Semester%203-095.png](images/Final%20Project%20Aplikom%20Semester%203-095.png)

Jika Anda memerlukan lebih banyak ruang untuk label-y, panggil
shrinkwindow() dengan parameter yang lebih kecil, atau tetapkan nilai
positif untuk "lebih kecil" di plot2d().


\>plot2d("gamma(x)",1,10,yl="y-values",smaller=6,<vertical):


![images/Final%20Project%20Aplikom%20Semester%203-096.png](images/Final%20Project%20Aplikom%20Semester%203-096.png)

Ekspresi simbolik juga dapat digunakan, karena disimpan sebagai
ekspresi string sederhana.


\>x=linspace(0,2pi,1000); plot2d(sin(5x),cos(7x)):


![images/Final%20Project%20Aplikom%20Semester%203-097.png](images/Final%20Project%20Aplikom%20Semester%203-097.png)

\>a:=5.6; expr &= exp(-a\*x^2)/a; // define expression

\>plot2d(expr,-2,2): // plot from -2 to 2


![images/Final%20Project%20Aplikom%20Semester%203-098.png](images/Final%20Project%20Aplikom%20Semester%203-098.png)

\>plot2d(expr,r=1,thickness=2): // plot in a square around (0,0)


![images/Final%20Project%20Aplikom%20Semester%203-099.png](images/Final%20Project%20Aplikom%20Semester%203-099.png)

\>plot2d(&diff(expr,x),\>add,style="--",color=red): // add another plot


![images/Final%20Project%20Aplikom%20Semester%203-100.png](images/Final%20Project%20Aplikom%20Semester%203-100.png)

\>plot2d(&diff(expr,x,2),a=-2,b=2,c=-2,d=1): // plot in rectangle


![images/Final%20Project%20Aplikom%20Semester%203-101.png](images/Final%20Project%20Aplikom%20Semester%203-101.png)

\>plot2d(&diff(expr,x),a=-2,b=2,\>square): // keep plot square


![images/Final%20Project%20Aplikom%20Semester%203-102.png](images/Final%20Project%20Aplikom%20Semester%203-102.png)

\>plot2d("x^2",0,1,steps=1,color=red,n=10):


![images/Final%20Project%20Aplikom%20Semester%203-103.png](images/Final%20Project%20Aplikom%20Semester%203-103.png)

\>plot2d("x^2",\>add,steps=2,color=blue,n=10):


![images/Final%20Project%20Aplikom%20Semester%203-104.png](images/Final%20Project%20Aplikom%20Semester%203-104.png)

# Fungsi dalam Satu Parameter

Fungsi plotting yang paling penting untuk plot planar adalah plot2d().
Fungsi ini diimplementasikan dalam bahasa Euler dalam  file "plot.e",
yang dimuat di awal program.


Berikut ini beberapa contoh penggunaan fungsi. Seperti biasa dalam
EMT, fungsi yang berfungsi untuk fungsi atau ekspresi  lain, Anda
dapat meneruskan parameter tambahan (selain x) yang bukan variabel
global ke fungsi dengan parameter titik koma  atau dengan kumpulan
panggilan.


\>function f(x,a) := x^2/a+a\*x^2-x; // define a function

\>a=0.3; plot2d("f",0,1;a): // plot with a=0.3


![images/Final%20Project%20Aplikom%20Semester%203-105.png](images/Final%20Project%20Aplikom%20Semester%203-105.png)

\>plot2d("f",0,1;0.4): // plot with a=0.4


![images/Final%20Project%20Aplikom%20Semester%203-106.png](images/Final%20Project%20Aplikom%20Semester%203-106.png)

\>plot2d({{"f",0.2}},0,1): // plot with a=0.2


![images/Final%20Project%20Aplikom%20Semester%203-107.png](images/Final%20Project%20Aplikom%20Semester%203-107.png)

\>plot2d({{"f(x,b)",b=0.1}},0,1): // plot with 0.1


![images/Final%20Project%20Aplikom%20Semester%203-108.png](images/Final%20Project%20Aplikom%20Semester%203-108.png)

\>function f(x) := x^3-x; ...  
\>   plot2d("f",r=1):


![images/Final%20Project%20Aplikom%20Semester%203-109.png](images/Final%20Project%20Aplikom%20Semester%203-109.png)

Berikut ini adalah ringkasan fungsi yang diterima


* 
ekspresi atau ekspresi simbolik dalam x

* 
fungsi atau fungsi simbolik berdasarkan nama seperti "f"

* 
fungsi simbolik hanya berdasarkan nama f


Fungsi plot2d() juga menerima fungsi simbolik. Untuk fungsi simbolik,
hanya nama yang berfungsi.


\>function f(x) &= diff(x^x,x)


    
                                x
                               x  (log(x) + 1)
    

\>plot2d(f,0,2):


![images/Final%20Project%20Aplikom%20Semester%203-110.png](images/Final%20Project%20Aplikom%20Semester%203-110.png)

Tentu saja, untuk ekspresi atau ungkapan simbolik, nama variabel sudah
cukup untuk memplotnya.


\>expr &= sin(x)\*exp(-x)


    
                                  - x
                                 E    sin(x)
    

\>plot2d(expr,0,3pi):


![images/Final%20Project%20Aplikom%20Semester%203-111.png](images/Final%20Project%20Aplikom%20Semester%203-111.png)

\>function f(x) &= x^x;

\>plot2d(f,r=1,cx=1,cy=1,color=blue,thickness=2);

\>plot2d(&diff(f(x),x),\>add,color=red,style="-.-"):


![images/Final%20Project%20Aplikom%20Semester%203-112.png](images/Final%20Project%20Aplikom%20Semester%203-112.png)

Untuk garis gaya, ada berbagai pilihan.


* 
style="...". Pilih dari "-", "--", "-.", ".", ".-.", "-.-".

* 
warna: Lihat dibawah untuk warna.

* 
ketebalan: Defaultnya adalah 1.


Warna dapat dipilih sebagai salah satu warna default, atau sebagai
warna RGB.


* 
0..15: indeks warna default.

* 
warna konstan: putih, hitam, merah, hijau, biru, biru kehijauan,
* hijau kekuningan, abu-abu muda, abu-abu tua, oranye, hijau muda,
* toska, biru muda, oranye muda, kuning 

* 
rgb(merah,hijau,biru): parameternya adalah bilangan riil dalam
* [0,1].


\>plot2d("exp(-x^2)",r=2,color=red,thickness=3,style="--"):


![images/Final%20Project%20Aplikom%20Semester%203-113.png](images/Final%20Project%20Aplikom%20Semester%203-113.png)

Berikut ini tampilan warna EMT yang telah ditetapkan sebelumnya.


\>aspect(2); columnsplot(ones(1,16),lab=0:15,grid=0,color=0:15):


![images/Final%20Project%20Aplikom%20Semester%203-114.png](images/Final%20Project%20Aplikom%20Semester%203-114.png)

Namun anda dapat menggunakan warna apapun.


\>columnsplot(ones(1,16),grid=0,color=rgb(0,0,linspace(0,1,15))):


![images/Final%20Project%20Aplikom%20Semester%203-115.png](images/Final%20Project%20Aplikom%20Semester%203-115.png)

# Menggambar Beberapa Kurva pada bidang koordinat yang sama

Plotting lebih dari satu fungsi (multifungsi) ke dalam satu jendela
dapat dilakukan dengan berbagai cara. Salah satu metodenya adalah
menggunakan &gt;add untuk beberapa panggilan ke plot2d secara
keseluruhan, kecuali panggilan pertama. Kami telah  menggunakan fitur
ini pada contoh di atas.


\>aspect(); plot2d("cos(x)",r=2,grid=6); plot2d("x",style=".",\>add):


![images/Final%20Project%20Aplikom%20Semester%203-116.png](images/Final%20Project%20Aplikom%20Semester%203-116.png)

\>aspect(1.5); plot2d("sin(x)",0,2pi); plot2d("cos(x)",color=blue,style="--",\>add):


![images/Final%20Project%20Aplikom%20Semester%203-117.png](images/Final%20Project%20Aplikom%20Semester%203-117.png)

Salah satu kegunaan &gt;add adalah untuk menambahkan titik pada kurva.


\>plot2d("sin(x)",0,pi); plot2d(2,sin(2),\>points,\>add):


![images/Final%20Project%20Aplikom%20Semester%203-118.png](images/Final%20Project%20Aplikom%20Semester%203-118.png)

Kami menambahkan titik persimpangan dengan label (pada posisi "cl"
untuk tengah kiri), dan memasukkan hasilnya ke dalam buku catatan.
Kami juga menambahkan judul pada plot.


\>plot2d(["cos(x)","x"],r=1.1,cx=0.5,cy=0.5, ...  
\>     color=[black,blue],style=["-","."], ...  
\>     grid=1);

\>x0=solve("cos(x)-x",1);  ...  
\>     plot2d(x0,x0,\>points,\>add,title="Intersection Demo");  ...  
\>     label("cos(x) = x",x0,x0,pos="cl",offset=20):


![images/Final%20Project%20Aplikom%20Semester%203-119.png](images/Final%20Project%20Aplikom%20Semester%203-119.png)

Dalam demo berikut, kami memplot fungsi sinc(x)=sin(x)/x dan ekspansi
Taylor ke-8 dan ke-16. Kami menghitung ekspansi ini  menggunakan
Maxima melalui ekspresi simbolik.


Plot ini dilakukan dalam perintah multi-baris berikut dengan tiga
panggilan ke plot2d(). Yang kedua dan ketiga memiliki tanda &gt;add yang
ditetapkan, yang membuat plot menggunakan rentang sebelumnya.


Kami menambahkan kotak label yang menjelaskan fungsinya.


\>$taylor(sin(x)/x,x,0,4)


$$\frac{x^4}{120}-\frac{x^2}{6}+1$$\>plot2d("sinc(x)",0,4pi,color=green,thickness=2); ...  
\>     plot2d(&taylor(sin(x)/x,x,0,8),\>add,color=blue,style="--"); ...  
\>     plot2d(&taylor(sin(x)/x,x,0,16),\>add,color=red,style="-.-"); ...  
\>     labelbox(["sinc","T8","T16"],styles=["-","--","-.-"], ...  
\>       colors=[black,blue,red]):


![images/Final%20Project%20Aplikom%20Semester%203-121.png](images/Final%20Project%20Aplikom%20Semester%203-121.png)

Dalam contoh berikut, kami menghasilkan Polinomial Bernstein.


\>plot2d("(1-x)^10",0,1); // plot first function

\>for i=1 to 10; plot2d("bin(10,i)\*x^i\*(1-x)^(10-i)",\>add); end;

\>insimg;


![images/Final%20Project%20Aplikom%20Semester%203-122.png](images/Final%20Project%20Aplikom%20Semester%203-122.png)

Metode kedua menggunakan sepasang matriks nilai-x dan matriks nilai-y
yang berukuran sama.


Kami membuat matriks nilai dengan satu Bernstein-Polinomial di setiap
baris. Untuk ini, kami cukup menggunakan vektor kolom i. Lihat
pengantar tentang bahasa matriks untuk mempelajari lebih detail.


\>x=linspace(0,1,500);

\>n=10; k=(0:n)'; // n is row vector, k is column vector

\>y=bin(n,k)\*x^k\*(1-x)^(n-k); // y is a matrix then

\>plot2d(x,y):


![images/Final%20Project%20Aplikom%20Semester%203-123.png](images/Final%20Project%20Aplikom%20Semester%203-123.png)

Perhatikan bahwa parameter warna dapat berupa vektor. Maka setiap
warna digunakan untuk setiap baris matriks.


\>x=linspace(0,1,200); y=x^(1:10)'; plot2d(x,y,color=1:10):


![images/Final%20Project%20Aplikom%20Semester%203-124.png](images/Final%20Project%20Aplikom%20Semester%203-124.png)

Metode lain adalah menggunakan vektor ekspresi (string). Anda kemudian
dapat menggunakan array warna, array gaya, dan array ketebalan dengan
panjang yang sama.


\>plot2d(["sin(x)","cos(x)"],0,2pi,color=4:5): 


![images/Final%20Project%20Aplikom%20Semester%203-125.png](images/Final%20Project%20Aplikom%20Semester%203-125.png)

\>plot2d(["sin(x)","cos(x)"],0,2pi): // plot vector of expressions


![images/Final%20Project%20Aplikom%20Semester%203-126.png](images/Final%20Project%20Aplikom%20Semester%203-126.png)

Kita bisa mendapatkan vektor tersebut dari Maxima menggunakan
makelist() dan mxm2str().


\>v &= makelist(binomial(10,i)\*x^i\*(1-x)^(10-i),i,0,10) // make list


    
                    10            9              8  2             7  3
            [(1 - x)  , 10 (1 - x)  x, 45 (1 - x)  x , 120 (1 - x)  x , 
               6  4             5  5             4  6             3  7
    210 (1 - x)  x , 252 (1 - x)  x , 210 (1 - x)  x , 120 (1 - x)  x , 
              2  8              9   10
    45 (1 - x)  x , 10 (1 - x) x , x  ]
    

\>mxm2str(v) // get a vector of strings from the symbolic vector


    (1-x)^10
    10*(1-x)^9*x
    45*(1-x)^8*x^2
    120*(1-x)^7*x^3
    210*(1-x)^6*x^4
    252*(1-x)^5*x^5
    210*(1-x)^4*x^6
    120*(1-x)^3*x^7
    45*(1-x)^2*x^8
    10*(1-x)*x^9
    x^10

\>plot2d(mxm2str(v),0,1): // plot functions


![images/Final%20Project%20Aplikom%20Semester%203-127.png](images/Final%20Project%20Aplikom%20Semester%203-127.png)

Alternatif lain adalah menggunakan bahasa matriks Euler.


Jika suatu ekspresi menghasilkan matriks fungsi, dengan satu fungsi
pada setiap baris, semua fungsi ini akan diplot menjadi satu plot.


Untuk ini, gunakan vektor parameter dalam bentuk vektor kolom. Jika
array warna ditambahkan, array tersebut akan digunakan  untuk setiap
baris plot.


\>n=(1:10)'; plot2d("x^n",0,1,color=1:10):


![images/Final%20Project%20Aplikom%20Semester%203-128.png](images/Final%20Project%20Aplikom%20Semester%203-128.png)

Ekspresi dan fungsi satu baris dapat melihat variabel global.


Jika Anda tidak dapat menggunakan variabel global, Anda perlu
menggunakan fungsi dengan parameter tambahan, dan meneruskan parameter
ini sebagai parameter titik koma.


Berhati-hatilah untuk meletakkan semua parameter yang ditetapkan di
akhir perintah plot2d. Dalam contoh ini, kita meneruskan  a=5 ke
fungsi f, yang kita plot dari -10 hingga 10.


\>function f(x,a) := 1/a\*exp(-x^2/a); ...  
\>   plot2d("f",-10,10;5,thickness=2,title="a=5"):


![images/Final%20Project%20Aplikom%20Semester%203-129.png](images/Final%20Project%20Aplikom%20Semester%203-129.png)

Atau, gunakan koleksi dengan nama fungsi dan semua parameter tambahan.
Daftar khusus ini disebut koleksi panggilan, dan itu  adalah cara yang
lebih disukai untuk meneruskan argumen ke suatu fungsi yang diteruskan
sebagai argumen ke fungsi lain.


Dalam contoh berikut, kami menggunakan loop untuk memplot beberapa
fungsi (lihat tutorial tentang pemrograman untuk loop).


\>plot2d({{"f",1}},-10,10); ...  
\>   for a=2:10; plot2d({{"f",a}},\>add); end:


![images/Final%20Project%20Aplikom%20Semester%203-130.png](images/Final%20Project%20Aplikom%20Semester%203-130.png)

Kita dapat memperoleh hasil yang sama dengan cara berikut menggunakan
bahasa matriks EMT. Setiap baris matriks f(x,a) adalah satu fungsi.


Selain itu, kita dapat mengatur warna untuk setiap baris matriks. Klik
dua kali pada fungsi getspectral() untuk penjelasannya.


\>x=-10:0.01:10; a=(1:10)'; plot2d(x,f(x,a),color=getspectral(a/10)):


![images/Final%20Project%20Aplikom%20Semester%203-131.png](images/Final%20Project%20Aplikom%20Semester%203-131.png)

## Label Teks

Dekorasi sederhana bisa berupa


* 
judul dengan title="..."

* 
label x dan y dengan xl="...", yl="..."

* 
label teks dengan label("...",x,y)


Perintah label akan memplot ke dalam plot saat ini pada koordinat plot
(x,y). Perintah ini dapat mengambil argumen posisi.


\>plot2d("x^3-x",-1,2,title="y=x^3-x",yl="y",xl="x"):


![images/Final%20Project%20Aplikom%20Semester%203-132.png](images/Final%20Project%20Aplikom%20Semester%203-132.png)

\>expr := "log(x)/x"; ...  
\>     plot2d(expr,0.5,5,title="y="+expr,xl="x",yl="y"); ...  
\>     label("(1,0)",1,0); label("Max",E,expr(E),pos="lc"):


![images/Final%20Project%20Aplikom%20Semester%203-133.png](images/Final%20Project%20Aplikom%20Semester%203-133.png)

Ada juga fungsi labelbox(), yang dapat menampilkan fungsi dan teks.
Fungsi ini mengambil vektor string dan warna, satu item untuk setiap
fungsi.


\>function f(x) &= x^2\*exp(-x^2);  ...  
\>   plot2d(&f(x),a=-3,b=3,c=-1,d=1);  ...  
\>   plot2d(&diff(f(x),x),\>add,color=blue,style="--"); ...  
\>   labelbox(["function","derivative"],styles=["-","--"], ...  
\>      colors=[black,blue],w=0.4):


![images/Final%20Project%20Aplikom%20Semester%203-134.png](images/Final%20Project%20Aplikom%20Semester%203-134.png)

Kotak tersebut ditambatkan di kanan atas secara default, tetapi &gt;left
menambatkannya di kiri atas. Anda dapat memindahkannya ke  tempat mana
pun yang Anda suka. Posisi jangkar adalah sudut kanan atas kotak, dan
angka-angkanya adalah pecahan dari ukuran  jendela grafis. Lebarnya
otomatis.


Untuk plot titik, kotak label juga berfungsi. Tambahkan parameter
&gt;points, atau vektor bendera, satu untuk setiap label.


Dalam contoh berikut, hanya ada satu fungsi. Jadi, kita dapat
menggunakan string, bukan vektor string. Kita tetapkan warna teks
menjadi hitam untuk contoh ini. 


\>n=10; plot2d(0:n,bin(n,0:n),\>addpoints); ...  
\>   labelbox("Binomials",styles="[]",\>points,x=0.1,y=0.1, ...  
\>   tcolor=black,\>left):


![images/Final%20Project%20Aplikom%20Semester%203-135.png](images/Final%20Project%20Aplikom%20Semester%203-135.png)

Gaya plot ini juga tersedia di statplot(). Seperti di plot2d(), warna
dapat diatur untuk setiap baris plot. Ada plot yang lebih khusus untuk
keperluan statistik (lihat tutorial tentang statistik).


\>statplot(1:10,random(2,10),color=[red,blue]):


![images/Final%20Project%20Aplikom%20Semester%203-136.png](images/Final%20Project%20Aplikom%20Semester%203-136.png)

Fitur serupa adalah fungsi textbox().


Lebarnya secara default adalah lebar maksimal baris teks. Namun,
lebarnya juga dapat diatur oleh pengguna.


\>function f(x) &= exp(-x)\*sin(2\*pi\*x); ...  
\>   plot2d("f(x)",0,2pi); ...  
\>   textbox(latex("\\text{Example of a damped oscillation}\\ f(x)=e^{-x}sin(2\\pi x)"),w=0.85):


![images/Final%20Project%20Aplikom%20Semester%203-137.png](images/Final%20Project%20Aplikom%20Semester%203-137.png)

Label teks, judul, kotak label, dan teks lainnya dapat berisi string
Unicode (lihat sintaksis EMT untuk informasi lebih lanjut tentang
string Unicode).


\>plot2d("x^3-x",title=u"x &rarr; x&sup3; - x"):


![images/Final%20Project%20Aplikom%20Semester%203-138.png](images/Final%20Project%20Aplikom%20Semester%203-138.png)

Label pada sumbu x dan y dapat vertikal, begitu pula sumbunya. 


\>plot2d("sinc(x)",0,2pi,xl="x",yl=u"x &rarr; sinc(x)",\>vertical):


![images/Final%20Project%20Aplikom%20Semester%203-139.png](images/Final%20Project%20Aplikom%20Semester%203-139.png)

## LaTeX

Anda juga dapat memplot rumus LaTeX jika Anda telah menginstal sistem
LaTeX. Saya merekomendasikan MiKTeX. Jalur ke biner "latex" dan
"dvipng" harus berada di jalur sistem, atau Anda harus mengatur LaTeX
di opsi menu.


Perlu dicatat, bahwa penguraian LaTeX berlangsung lambat. Jika Anda
ingin menggunakan LaTeX dalam plot animasi, Anda harus memanggil
latex() sebelum loop sekali dan menggunakan hasilnya (gambar dalam
matriks RGB).


Pada plot berikut, kami menggunakan LaTeX untuk label x dan y, label,
kotak label, dan judul plot.


\>plot2d("exp(-x)\*sin(x)/x",a=0,b=2pi,c=0,d=1,grid=6,color=blue, ...  
\>     title=latex("\\text{Function $\\Phi$}"), ...  
\>     xl=latex("\\phi"),yl=latex("\\Phi(\\phi)")); ...  
\>   textbox( ...  
\>     latex("\\Phi(\\phi) = e^{-\\phi} \\frac{\\sin(\\phi)}{\\phi}"),x=0.8,y=0.5); ...  
\>   label(latex("\\Phi",color=blue),1,0.4):


![images/Final%20Project%20Aplikom%20Semester%203-140.png](images/Final%20Project%20Aplikom%20Semester%203-140.png)

Seringkali, kita menginginkan spasi nonkonformal dan label teks pada
sumbu x. Kita dapat menggunakan xaxis() dan yaxis() seperti yang akan
kita tunjukkan nanti.


Cara termudah adalah dengan membuat plot kosong dengan bingkai
menggunakan grid=4, lalu menambahkan grid dengan ygrid() dan xgrid().
Dalam contoh berikut, kami menggunakan tiga string LaTeX untuk label
pada sumbu x dengan xtick().


\>plot2d("sinc(x)",0,2pi,grid=4,<ticks); ...  
\>   ygrid(-2:0.5:2,grid=6); ...  
\>   xgrid([0:2]\*pi,<ticks,grid=6);  ...  
\>   xtick([0,pi,2pi],["0","\\pi","2\\pi"],\>latex):


![images/Final%20Project%20Aplikom%20Semester%203-141.png](images/Final%20Project%20Aplikom%20Semester%203-141.png)

Tentu saja, fungsi juga dapat digunakan. 


\>function map f(x) ...


    if x>0 then return x^4
    else return x^2
    endif
    endfunction
</pre>
Parameter "map" membantu penggunaan fungsi untuk vektor. Untuk plot,
parameter ini tidak diperlukan. Namun, untuk menunjukkan bahwa
vektorisasi berguna, kami menambahkan beberapa poin penting ke plot
pada x=-1, x=0, dan x=1.


Pada plot berikut, kami juga memasukkan beberapa kode LaTeX. Kami
menggunakannya untuk dua label dan satu kotak teks. Tentu saja, Anda
hanya dapat menggunakan LaTeX jika Anda telah menginstal LaTeX dengan
benar.


\>plot2d("f",-1,1,xl="x",yl="f(x)",grid=6);  ...  
\>   plot2d([-1,0,1],f([-1,0,1]),\>points,\>add); ...  
\>   label(latex("x^3"),0.72,f(0.72)); ...  
\>   label(latex("x^2"),-0.52,f(-0.52),pos="ll"); ...  
\>   textbox( ...  
\>     latex("f(x)=\\begin{cases} x^3 & x\>0 \\\\ x^2 & x \\le 0\\end{cases}"), ...  
\>     x=0.7,y=0.2):


![images/Final%20Project%20Aplikom%20Semester%203-142.png](images/Final%20Project%20Aplikom%20Semester%203-142.png)

## Interaksi User

Saat memplot fungsi atau ekspresi, parameter &gt;user memungkinkan
pengguna untuk memperbesar dan menggeser plot dengan tombol kursor
atau mouse. Pengguna dapat


* 
zoom dengan + or -

* 
memindahkan plot dengan tombol kursor

* 
memilih jendela plot dengan mouse

* 
mengatur ulang tampilan dengan spasi

* 
keluar dengan return


Tombol spasi akan mengatur ulang plot ke jendela plot asli.


Saat memetakan data, tanda &gt;user akan menunggu penekanan tombol.


\>plot2d({{"x^3-a\*x",a=1}},\>user,title="Press any key!"):


![images/Final%20Project%20Aplikom%20Semester%203-143.png](images/Final%20Project%20Aplikom%20Semester%203-143.png)

\>plot2d("exp(x)\*sin(x)",user=true, ...  
\>     title="+/- or cursor keys (return to exit)"):


![images/Final%20Project%20Aplikom%20Semester%203-144.png](images/Final%20Project%20Aplikom%20Semester%203-144.png)

Berikut ini menunjukkan cara interaksi pengguna yang canggih (lihat
tutorial tentang pemrograman untuk detailnya).


Fungsi bawaan mousedrag() menungggu kejadian mouse atau keyboard.
Fungsi ini melaporkan gerakan mouse ke atas dan penekanan tombol.
Fungsi dragpoints() memanfaatkan fungsi ini, dan memungkinkan pengguna
menyeret titik m pun dalam plot.


Pertama-tama, kita perlu fungsi plot. Misalnya, kita melakukan
interpolasi pada 5 titik dengan polinomial. Fungsi tersebutharus
diplot ke dalam area plot yang tetap.


\>function plotf(xp,yp,select) ...


      d=interp(xp,yp);
      plot2d("interpval(xp,d,x)";d,xp,r=2);
      plot2d(xp,yp,>points,>add);
      if select>0 then
        plot2d(xp[select],yp[select],color=red,>points,>add);
      endif;
      title("Drag one point, or press space or return!");
    endfunction
</pre>
Perhatikan parameter titik koma di plot2d (d dan xp), yang diteruskan
ke evaluasi fungsi interp(). Tanpa ini, kita harus menulis fungsi
plotinterp() terlebih dahulu, yang mengakses nilai secara global.


Sekarang kita buat beberapa nilai acak dan biarkan pengguna menyeret
titik-titiknya.


\>t=-1:0.5:1; dragpoints("plotf",t,random(size(t))-0.5):


![images/Final%20Project%20Aplikom%20Semester%203-145.png](images/Final%20Project%20Aplikom%20Semester%203-145.png)

Ada juga fungsi yang memplot fungsi lain tergantung pada vektor
parameter, dan memungkinkan pengguna menyesuaikan parameter ini.


Pertama kita butuh fungsi plot.


\>function plotf([a,b]) := plot2d("exp(a\*x)\*cos(2pi\*b\*x)",0,2pi;a,b);


Kemudian kita perlu nama untuk parameter, nilai awal dan matriks
rentang nx2, secara opsional baris judul.


Terdapat slider interaktif, yang dapat mengatur nilai oleh pengguna.
Fungsi dragvalues() menyediakannya.


\>dragvalues("plotf",["a","b"],[-1,2],[[-2,2];[1,10]], ...  
\>     heading="Drag these values:",hcolor=black):


![images/Final%20Project%20Aplikom%20Semester%203-146.png](images/Final%20Project%20Aplikom%20Semester%203-146.png)

Dimungkinkan untuk membatasi nilai yang diseret ke bilangan bulat.
Misalnya, kita menulis fungsi plot, yang memplot polinomial Taylor
berderajat n ke fungsi kosinus.


\>function plotf(n) ...


    plot2d("cos(x)",0,2pi,>square,grid=6);
    plot2d(&"taylor(cos(x),x,0,@n)",color=blue,>add);
    textbox("Taylor polynomial of degree "+n,0.1,0.02,style="t",>left);
    endfunction
</pre>
Sekarang kita mengizinkan derajat n bervariasi dari 0 hingga 20 dalam
20 stop. Hasil dragvalues() digunakan untuk memplot sketsa dengan n
ini, dan untuk memasukkan plot ke dalam buku catatan.


\>nd=dragvalues("plotf","degree",2,[0,20],20,y=0.8, ...  
\>      heading="Drag the value:"); ...  
\>   plotf(nd):


![images/Final%20Project%20Aplikom%20Semester%203-147.png](images/Final%20Project%20Aplikom%20Semester%203-147.png)

Berikut ini adalah demonstrasi sederhana dari fungsi tersebut.
Pengguna dapat menggambar di atas jendela plot, meninggalkan jejak
titik-titik.


\>function dragtest ...


      plot2d(none,r=1,title="Drag with the mouse, or press any key!");
      start=0;
      repeat
        {flag,m,time}=mousedrag();
        if flag==0 then return; endif;
        if flag==2 then
          hold on; mark(m[1],m[2]); hold off;
        endif;
      end
    endfunction
</pre>
\>dragtest // lihat hasilnya dan cobalah lakukan!


## Gaya Plot 2D

Secara default, EMT menghitung tanda centang sumbu otomatis dan
menambahkan label ke setiap tanda centang. Ini dapat diubah dengan
parameter grid. Gaya default sumbu dan label dapat dimodifikasi.
Selain itu, label dan judul dapat ditambahkan secara manual. Untuk
mengatur ulang ke gaya default, gunakan reset().


\>aspect();

\>figure(3,4); ...  
\>    figure(1); plot2d("x^3-x",grid=0); ... // no grid, frame or axis

\> figure(2); plot2d("x^3-x",grid=1); ... // x-y-axis

\> figure(3); plot2d("x^3-x",grid=2); ... // default ticks

\> figure(4); plot2d("x^3-x",grid=3); ... // x-y- axis with labels inside

\> figure(5); plot2d("x^3-x",grid=4); ... // no ticks, only labels

\> figure(6); plot2d("x^3-x",grid=5); ... // default, but no margin

\> figure(7); plot2d("x^3-x",grid=6); ... // axes only

\> figure(8); plot2d("x^3-x",grid=7); ... // axes only, ticks at axis

\> figure(9); plot2d("x^3-x",grid=8); ... // axes only, finer ticks at axis

\> figure(10); plot2d("x^3-x",grid=9); ... // default, small ticks inside

\> figure(11); plot2d("x^3-x",grid=10); ...// no ticks, axes only

\> figure(0):


![images/Final%20Project%20Aplikom%20Semester%203-148.png](images/Final%20Project%20Aplikom%20Semester%203-148.png)

Parameter &lt;frame mematikan frame, dan framecolor=blue mengatur frame
menjadi warna biru.


Jika Anda menginginkan tanda centang Anda sendiri, Anda dapat
menggunakan style=0, dan menambahkan semuanya nanti. 


\>aspect(1.5); 

\>plot2d("x^3-x",grid=0); // plot

\>frame; xgrid([-1,0,1]); ygrid(0): // add frame and grid


![images/Final%20Project%20Aplikom%20Semester%203-149.png](images/Final%20Project%20Aplikom%20Semester%203-149.png)

Untuk judul plot dan label sumbu, lihat contoh berikut.


\>plot2d("exp(x)",-1,1);

\>textcolor(black); // set the text color to black

\>title(latex("y=e^x")); // title above the plot

\>xlabel(latex("x")); // "x" for x-axis

\>ylabel(latex("y"),\>vertical); // vertical "y" for y-axis

\>label(latex("(0,1)"),0,1,color=blue): // label a point


![images/Final%20Project%20Aplikom%20Semester%203-150.png](images/Final%20Project%20Aplikom%20Semester%203-150.png)

Sumbu dapat digambar secara terpisah dengan xaxis() dan yaxis().


\>plot2d("x^3-x",<grid,<frame);

\>xaxis(0,xx=-2:1,style="-\>"); yaxis(0,yy=-5:5,style="-\>"):


![images/Final%20Project%20Aplikom%20Semester%203-151.png](images/Final%20Project%20Aplikom%20Semester%203-151.png)

Teks pada plot dapat diatur dengan label(). Dalam contoh berikut, "lc"
berarti tengah bawah. Ini mengatur posisi label relatif terhadap
koordinat plot.


\>function f(x) &= x^3-x


    
                                     3
                                    x  - x
    

\>plot2d(f,-1,1,\>square);

\>x0=fmin(f,0,1); // compute point of minimum

\>label("Rel. Min.",x0,f(x0),pos="lc"): // add a label there


![images/Final%20Project%20Aplikom%20Semester%203-152.png](images/Final%20Project%20Aplikom%20Semester%203-152.png)

Ada juga kotak teks.


\>plot2d(&f(x),-1,1,-2,2); // function

\>plot2d(&diff(f(x),x),\>add,style="--",color=red); // derivative

\>labelbox(["f","f'"],["-","--"],[black,red]): // label box


![images/Final%20Project%20Aplikom%20Semester%203-153.png](images/Final%20Project%20Aplikom%20Semester%203-153.png)

\>plot2d(["exp(x)","1+x"],color=[black,blue],style=["-","-.-"]):


![images/Final%20Project%20Aplikom%20Semester%203-154.png](images/Final%20Project%20Aplikom%20Semester%203-154.png)

\>gridstyle("-\>",color=gray,textcolor=gray,framecolor=gray);  ...  
\>    plot2d("x^3-x",grid=1);   ...  
\>    settitle("y=x^3-x",color=black); ...  
\>    label("x",2,0,pos="bc",color=gray);  ...  
\>    label("y",0,6,pos="cl",color=gray); ...  
\>    reset():


![images/Final%20Project%20Aplikom%20Semester%203-155.png](images/Final%20Project%20Aplikom%20Semester%203-155.png)

Untuk kontrol lebih, sumbu x dan sumbu y dapat dilakukan secara
manual.


Perintah fullwindow() memperluas jendela plot karena kita tidak lagi
memerlukan tempat untuk label di luar jendela plot. Gunakan
shrinkwindow() atau reset() untuk mengatur ulang ke default.


\>fullwindow; ...  
\>    gridstyle(color=darkgray,textcolor=darkgray); ...  
\>    plot2d(["2^x","1","2^(-x)"],a=-2,b=2,c=0,d=4,<grid,color=4:6,<frame); ...  
\>    xaxis(0,-2:1,style="-\>"); xaxis(0,2,"x",<axis); ...  
\>    yaxis(0,4,"y",style="-\>"); ...  
\>    yaxis(-2,1:4,\>left); ...  
\>    yaxis(2,2^(-2:2),style=".",<left); ...  
\>    labelbox(["2^x","1","2^-x"],colors=4:6,x=0.8,y=0.2); ...  
\>    reset:


![images/Final%20Project%20Aplikom%20Semester%203-156.png](images/Final%20Project%20Aplikom%20Semester%203-156.png)

Berikut contoh lain, dimana string Unicode digunakan dan sumbu berada
di luar area plot.


\>aspect(1.5); 

\>plot2d(["sin(x)","cos(x)"],0,2pi,color=[red,green],<grid,<frame); ...  
\>    xaxis(-1.1,(0:2)\*pi,xt=["0",u"&pi;",u"2&pi;"],style="-",\>ticks,\>zero);  ...  
\>    xgrid((0:0.5:2)\*pi,<ticks); ...  
\>    yaxis(-0.1\*pi,-1:0.2:1,style="-",\>zero,\>grid); ...  
\>    labelbox(["sin","cos"],colors=[red,green],x=0.5,y=0.2,\>left); ...  
\>    xlabel(u"&phi;"); ylabel(u"f(&phi;)"):


![images/Final%20Project%20Aplikom%20Semester%203-157.png](images/Final%20Project%20Aplikom%20Semester%203-157.png)

# Memplot Data 2D 

Jika x dan y adalah vektor data, data ini akan digunakan sebagai
koordinat x dan y dari sebuah kurva. Dalam kasus ini, a, b, c, dan d,
atau radius r dapat ditentukan, atau jendela plot akan menyesuaikan
secara otomatis dengan data. Atau, &gt;square dapat diatur untuk
mempertahankan rasio aspek persegi.


Memplot ekspresi hanyalah singkatan dari plot data. Untuk plot data,
Anda memerlukan satu atau beberapa baris nilai-x, dan satu atau
beberapa baris nilai-y. Dari rentang dan nilai-x, fungsi plot2d akan
menghitung data yang akan diplot, secara default dengan evaluasi
adaptif fungsi tersebut. Untuk plot titik gunakan "&gt;points", untuk
garis dan titik campuran gunakan "&gt;addpoints".


Namun Anda dapat memasukkan data secara langsung.


* 
Gunakan vektor baris untuk x dan y untuk satu fungsi.

* 
Matriks untuk x dan y diplot baris demi baris.


Berikut adalah contoh dengan satu baris untuk x dan y.


\>x=-10:0.1:10; y=exp(-x^2)\*x; plot2d(x,y):


![images/Final%20Project%20Aplikom%20Semester%203-158.png](images/Final%20Project%20Aplikom%20Semester%203-158.png)

Data juga dapat diplot sebagai titik. Gunakan points=true untuk ini.
Plot bekerja seperti poligon, tetapi hanya menggambar sudut.


* 
style="...": Pilih dari "[]", "&lt;&gt;", "o", ".", "..", "+", "*", "[]#",
* "&lt;&gt;#", "o#", "..#", "#", "|".


Untuk memplot kumpulan titik, gunakan &gt;points. Jika warnanya adalah
vektor warna, setiap titik akan mendapatkan warna yang berbeda. Untuk
matriks koordinat dan vektor kolom, warna berlaku untuk baris matriks.


Parameter &gt;addpoints menambahkan titik ke segmen garis untuk plot
data.


\>xdata=[1,1.5,2.5,3,4]; ydata=[3,3.1,2.8,2.9,2.7]; // data

\>plot2d(xdata,ydata,a=0.5,b=4.5,c=2.5,d=3.5,style="."); // lines

\>plot2d(xdata,ydata,\>points,\>add,style="o"): // add points


![images/Final%20Project%20Aplikom%20Semester%203-159.png](images/Final%20Project%20Aplikom%20Semester%203-159.png)

\>p=polyfit(xdata,ydata,1); // get regression line

\>plot2d("polyval(p,x)",\>add,color=red): // add plot of line


![images/Final%20Project%20Aplikom%20Semester%203-160.png](images/Final%20Project%20Aplikom%20Semester%203-160.png)

# Menggambar Daerah Yang Dibatasi Kurva

Plot data sebenarnya adalah poligon. Kita juga dapat memplot kurva
atau kurva terisi.


* 
filled=true mengisi plot.

* 
style="...": Pilih dari "#", "/", "\", "\/".

* 
fillcolor: Lihat di atas untuk warna yang tersedia.


Warna isian ditentukan oleh argumen "fillcolor", dan pada &lt;outline
opsional mencegah penggambaran batas untuk semua gaya kecuali yang
default. 


\>t=linspace(0,2pi,1000); // parameter for curve

\>x=sin(t)\*exp(t/pi); y=cos(t)\*exp(t/pi); // x(t) and y(t)

\>figure(1,2); aspect(16/9)

\>figure(1); plot2d(x,y,r=10); // plot curve

\>figure(2); plot2d(x,y,r=10,\>filled,style="/",fillcolor=red); // fill curve

\>figure(0):


![images/Final%20Project%20Aplikom%20Semester%203-161.png](images/Final%20Project%20Aplikom%20Semester%203-161.png)

Pada contoh berikut ini kami memplot elips yang terisi dan dua segi
enam yang terisi menggunakan kurva tertutup dengan 6 titik dengan gaya
isian yang berbeda.


\>x=linspace(0,2pi,1000); plot2d(sin(x),cos(x)\*0.5,r=1,\>filled,style="/"):


![images/Final%20Project%20Aplikom%20Semester%203-162.png](images/Final%20Project%20Aplikom%20Semester%203-162.png)

\>t=linspace(0,2pi,6); ...  
\>   plot2d(cos(t),sin(t),\>filled,style="/",fillcolor=red,r=1.2):


![images/Final%20Project%20Aplikom%20Semester%203-163.png](images/Final%20Project%20Aplikom%20Semester%203-163.png)

\>t=linspace(0,2pi,6); plot2d(cos(t),sin(t),\>filled,style="#"):


![images/Final%20Project%20Aplikom%20Semester%203-164.png](images/Final%20Project%20Aplikom%20Semester%203-164.png)

Contoh lain adalah septagon, yang kita buat dengan 7 titik pada
lingkaran satuan.


\>t=linspace(0,2pi,7);  ...  
\>    plot2d(cos(t),sin(t),r=1,\>filled,style="/",fillcolor=red):


![images/Final%20Project%20Aplikom%20Semester%203-165.png](images/Final%20Project%20Aplikom%20Semester%203-165.png)

Berikut ini adalah himpunan nilai maksimal dari empat kondisi linier
yang kurang dari atau sama dengan 3. Ini adalah A[k].v&lt;=3 untuk semua
baris A. Untuk mendapatkan sudut yang bagus, kita menggunakan n yang
relatif besar.


\>A=[2,1;1,2;-1,0;0,-1];

\>function f(x,y) := max([x,y].A');

\>plot2d("f",r=4,level=[0;3],color=green,n=111):


![images/Final%20Project%20Aplikom%20Semester%203-166.png](images/Final%20Project%20Aplikom%20Semester%203-166.png)

Poin utama dari bahasa matriks adalah memungkinkan pembuatan tabel
fungsi dengan mudah.


\>t=linspace(0,2pi,1000); x=cos(3\*t); y=sin(4\*t);


Sekarang kita memiliki vektor nilai x dan y. plot2d() dapat memplot
nilai-nilai ini sebagai kurva yang menghubungkan titik-titik. Plot
dapat diisi. Dalam kasus ini, hasilnya akan bagus karena aturan
lilitan, yang digunakan untuk mengisi.


\>plot2d(x,y,<grid,<frame,\>filled):


![images/Final%20Project%20Aplikom%20Semester%203-167.png](images/Final%20Project%20Aplikom%20Semester%203-167.png)

Vektor interval diplot terhadap nilai x sebagai daerah terisi antara
nilai interval bawah dan atas.


Hal ini dapat berguna untuk memetakan kesalahan perhitungan. Namun,
hal ini juga dapat digunakan untuk memetakan kesalahan statistik.


\>t=0:0.1:1; ...  
\>    plot2d(t,interval(t-random(size(t)),t+random(size(t))),style="|");  ...  
\>    plot2d(t,t,add=true):


![images/Final%20Project%20Aplikom%20Semester%203-168.png](images/Final%20Project%20Aplikom%20Semester%203-168.png)

Jika x adalah vektor yang diurutkan, dan y adalah vektor interval,
maka plot2d akan memplot rentang interval yang terisi pada bidang,
gaya isian sama dengan gaya poligon.


\>t=-1:0.01:1; x=~t-0.01,t+0.01~; y=x^3-x;

\>plot2d(t,y):


![images/Final%20Project%20Aplikom%20Semester%203-169.png](images/Final%20Project%20Aplikom%20Semester%203-169.png)

Dimungkinkan untuk mengisi wilayah nilai untuk fungsi tertentu. Untuk


ini, level harus berupa matriks 2xn. Baris pertama adalah batas bawah


dan baris kedua berisi batas atas.


\>expr := "2\*x^2+x\*y+3\*y^4+y"; // define an expression f(x,y)

\>plot2d(expr,level=[0;1],style="-",color=blue): // 0 <= f(x,y) <= 1


![images/Final%20Project%20Aplikom%20Semester%203-170.png](images/Final%20Project%20Aplikom%20Semester%203-170.png)

Kita juga dapat mengisi rentang nilai seperti


\>plot2d("(x^2+y^2)^2-x^2+y^2",r=1.2,level=[-1;0],style="/"):


![images/Final%20Project%20Aplikom%20Semester%203-171.png](images/Final%20Project%20Aplikom%20Semester%203-171.png)

\>plot2d("cos(x)","sin(x)^3",xmin=0,xmax=2pi,\>filled,style="/"):


![images/Final%20Project%20Aplikom%20Semester%203-172.png](images/Final%20Project%20Aplikom%20Semester%203-172.png)

# Grafik Fungsi Parametrik

Nilai x tidak perlu diurutkan. (x,y) hanya menggambarkan sebuah kurva.
Jika x diurutkan, kurva tersebut adalah grafik fungsi.


Pada contoh berikut, kita memplot spiral


lateks: \gamma(t) = t \cdot (\cos(2\pi t),\sin(2\pi t))


Kita mungkin perlu menggunakan sangat banyak titik untuk tampilan yang
halus atau fungsi adaptive() untuk mengevaluasi ekspresi (lihat fungsi
adaptive() untuk lebih jelasnya).


\>t=linspace(0,1,1000); ...  
\>   plot2d(t\*cos(2\*pi\*t),t\*sin(2\*pi\*t),r=1):


![images/Final%20Project%20Aplikom%20Semester%203-173.png](images/Final%20Project%20Aplikom%20Semester%203-173.png)

Sebagai alternatif, Anda dapat menggunakan dua ekspresi untuk kurva.
Berikut ini memplot kurva yang sama seperti di atas.


\>plot2d("x\*cos(2\*pi\*x)","x\*sin(2\*pi\*x)",xmin=0,xmax=1,r=1):


![images/Final%20Project%20Aplikom%20Semester%203-174.png](images/Final%20Project%20Aplikom%20Semester%203-174.png)

\>t=linspace(0,1,1000); r=exp(-t); x=r\*cos(2pi\*t); y=r\*sin(2pi\*t);

\>plot2d(x,y,r=1):


![images/Final%20Project%20Aplikom%20Semester%203-175.png](images/Final%20Project%20Aplikom%20Semester%203-175.png)

Pada contoh berikutnya, kita memplot kurva


dengan


\>t=linspace(0,2pi,1000); r=1+sin(3\*t)/2; x=r\*cos(t); y=r\*sin(t); ...  
\>   plot2d(x,y,\>filled,fillcolor=red,style="/",r=1.5):


![images/Final%20Project%20Aplikom%20Semester%203-176.png](images/Final%20Project%20Aplikom%20Semester%203-176.png)

# Menggambar Grafik Bilangan Kompleks

Sebuah deretan bilangan kompleks juga dapat diplot. Kemudian
titik-titik kisi akan dihubungkan. Jika sejumlah garis kisi ditentukan
(atau vektor 1x2 garis kisi) pada argumen cgrid, hanya garis-garis
kisi tersebut yang akan terlihat.


Matriks bilangan kompleks akan secara otomatis diplot sebagai sebuah
grid pada bidang kompleks.


Pada contoh berikut, kita memplot gambar lingkaran satuan di bawah
fungsi eksponensial. Parameter cgrid menyembunyikan beberapa kurva
grid.


\>aspect(); r=linspace(0,1,50); a=linspace(0,2pi,80)'; z=r\*exp(I\*a);...  
\>   plot2d(z,a=-1.25,b=1.25,c=-1.25,d=1.25,cgrid=10):


![images/Final%20Project%20Aplikom%20Semester%203-177.png](images/Final%20Project%20Aplikom%20Semester%203-177.png)

\>aspect(1.25); r=linspace(0,1,50); a=linspace(0,2pi,200)'; z=r\*exp(I\*a);

\>plot2d(exp(z),cgrid=[40,10]):


![images/Final%20Project%20Aplikom%20Semester%203-178.png](images/Final%20Project%20Aplikom%20Semester%203-178.png)

\>r=linspace(0,1,10); a=linspace(0,2pi,40)'; z=r\*exp(I\*a);

\>plot2d(exp(z),\>points,\>add):


![images/Final%20Project%20Aplikom%20Semester%203-179.png](images/Final%20Project%20Aplikom%20Semester%203-179.png)

Vektor bilangan kompleks secara otomatis diplot sebagai kurva pada
bidang kompleks dengan bagian nyata dan bagian imajiner.


Pada contoh, kami memplot lingkaran satuan dengan


atex: \gamma(t) = e^{it}


\>t=linspace(0,2pi,1000); ...  
\>   plot2d(exp(I\*t)+exp(4\*I\*t),r=2):


![images/Final%20Project%20Aplikom%20Semester%203-180.png](images/Final%20Project%20Aplikom%20Semester%203-180.png)

# Plot Statistik

Terdapat banyak fungsi yang dikhususkan untuk plot statistik. Salah
satu plot yang sering digunakan adalah plot kolom.


Jumlah kumulatif dari nilai berdistribusi normal 0-1 menghasilkan
jalan acak.


\>plot2d(cumsum(randnormal(1,1000))):


![images/Final%20Project%20Aplikom%20Semester%203-181.png](images/Final%20Project%20Aplikom%20Semester%203-181.png)

Menggunakan dua baris menunjukkan jalan dalam dua dimensi.


\>X=cumsum(randnormal(2,1000)); plot2d(X[1],X[2]):


![images/Final%20Project%20Aplikom%20Semester%203-182.png](images/Final%20Project%20Aplikom%20Semester%203-182.png)

\>columnsplot(cumsum(random(10)),style="/",color=blue):


![images/Final%20Project%20Aplikom%20Semester%203-183.png](images/Final%20Project%20Aplikom%20Semester%203-183.png)

Ini juga dapat menampilkan string sebagai label.


\>months=["Jan","Feb","Mar","Apr","May","Jun", ...  
\>     "Jul","Aug","Sep","Oct","Nov","Dec"];


    Variable months not found!
    Error in:
    ... nths=["Jan","Feb","Mar","Apr","May","Jun", months=["Jan","Feb" ...
                                                         ^

\>values=[10,12,12,18,22,28,30,26,22,18,12,8];

\>columnsplot(values,lab=months,color=red,style="-");


    Variable months not found!
    Error in:
    columnsplot(values,lab=months,color=red,style="-"); ...
                                 ^

\>title("Temperature"):


![images/Final%20Project%20Aplikom%20Semester%203-184.png](images/Final%20Project%20Aplikom%20Semester%203-184.png)

\>k=0:10;

\>plot2d(k,bin(10,k),\>bar):


![images/Final%20Project%20Aplikom%20Semester%203-185.png](images/Final%20Project%20Aplikom%20Semester%203-185.png)

\>plot2d(k,bin(10,k)); plot2d(k,bin(10,k),\>points,\>add):


![images/Final%20Project%20Aplikom%20Semester%203-186.png](images/Final%20Project%20Aplikom%20Semester%203-186.png)

\>plot2d(normal(1000),normal(1000),\>points,grid=6,style=".."):


![images/Final%20Project%20Aplikom%20Semester%203-187.png](images/Final%20Project%20Aplikom%20Semester%203-187.png)

\>plot2d(normal(1,1000),\>distribution,style="O"):


![images/Final%20Project%20Aplikom%20Semester%203-188.png](images/Final%20Project%20Aplikom%20Semester%203-188.png)

\>plot2d("qnormal",0,5;2.5,0.5,\>filled):


![images/Final%20Project%20Aplikom%20Semester%203-189.png](images/Final%20Project%20Aplikom%20Semester%203-189.png)

Untuk memplot distribusi statistik eksperimental, Anda dapat
menggunakan distribution=n dengan plot2d.


\>w=randexponential(1,1000); // exponential distribution

\>plot2d(w,\>distribution): // or distribution=n with n intervals


![images/Final%20Project%20Aplikom%20Semester%203-190.png](images/Final%20Project%20Aplikom%20Semester%203-190.png)

Atau Anda dapat menghitung distribusi dari data dan memplot hasilnya
dengan &gt;bar di plot3d, atau dengan plot kolom.


\>w=normal(1000); // 0-1-normal distribution

\>{x,y}=histo(w,10,v=[-6,-4,-2,-1,0,1,2,4,6]); // interval bounds v

\>plot2d(x,y,\>bar):


![images/Final%20Project%20Aplikom%20Semester%203-191.png](images/Final%20Project%20Aplikom%20Semester%203-191.png)

Fungsi statplot() mengatur gaya dengan string sederhana.


\>statplot(1:10,cumsum(random(10)),"b"):


![images/Final%20Project%20Aplikom%20Semester%203-192.png](images/Final%20Project%20Aplikom%20Semester%203-192.png)

\>n=10; i=0:n; ...  
\>   plot2d(i,bin(n,i)/2^n,a=0,b=10,c=0,d=0.3); ...  
\>   plot2d(i,bin(n,i)/2^n,points=true,style="ow",add=true,color=blue):


![images/Final%20Project%20Aplikom%20Semester%203-193.png](images/Final%20Project%20Aplikom%20Semester%203-193.png)

Selain itu, data dapat diplot sebagai batang. Dalam hal ini, x harus
diurutkan dan satu elemen lebih panjang dari y. Batang akan memanjang
dari x[i] ke x[i+1] dengan nilai y[i]. Jika x memiliki ukuran yang
sama dengan y, maka x akan diperpanjang satu elemen dengan jarak
terakhir.


Gaya isian dapat digunakan seperti di atas.


\>n=10; k=bin(n,0:n); ...  
\>   plot2d(-0.5:n+0.5,k,bar=true,fillcolor=lightgray):


![images/Final%20Project%20Aplikom%20Semester%203-194.png](images/Final%20Project%20Aplikom%20Semester%203-194.png)

Data untuk plot batang (bar=1) dan histogram (histogram = 1) dapat
diberikan secara eksplisit dalam xv dan yv, atau dapat dihitung dari
distribusi empiris dalam xv dengan &gt;distribusi (atau distribusi = n).
Histogram dari nilai xv akan dihitung secara otomatis dengan
&gt;histogram. Jika &gt;even ditentukan, nilai xv akan dihitung dalam
interval bilangan bulat.


\>plot2d(normal(10000),distribution=50):


![images/Final%20Project%20Aplikom%20Semester%203-195.png](images/Final%20Project%20Aplikom%20Semester%203-195.png)

\>k=0:10; m=bin(10,k); x=(0:11)-0.5; plot2d(x,m,\>bar):


![images/Final%20Project%20Aplikom%20Semester%203-196.png](images/Final%20Project%20Aplikom%20Semester%203-196.png)

\>columnsplot(m,k):


![images/Final%20Project%20Aplikom%20Semester%203-197.png](images/Final%20Project%20Aplikom%20Semester%203-197.png)

\>plot2d(random(600)\*6,histogram=6):


![images/Final%20Project%20Aplikom%20Semester%203-198.png](images/Final%20Project%20Aplikom%20Semester%203-198.png)

Untuk distribusi, ada parameter distribution=n, yang menghitung nilai
secara otomatis dan mencetak distribusi relatif dengan n sub-interval.


\>plot2d(normal(1,1000),distribution=10,style="\\/"):


![images/Final%20Project%20Aplikom%20Semester%203-199.png](images/Final%20Project%20Aplikom%20Semester%203-199.png)

Dengan parameter even=true, ini akan menggunakan interval integer.


\>plot2d(intrandom(1,1000,10),distribution=10,even=true):


![images/Final%20Project%20Aplikom%20Semester%203-200.png](images/Final%20Project%20Aplikom%20Semester%203-200.png)

Perhatikan bahwa ada banyak plot statistik yang mungkin berguna.
Lihatlah tutorial tentang statistik.


\>columnsplot(getmultiplicities(1:6,intrandom(1,6000,6))):


![images/Final%20Project%20Aplikom%20Semester%203-201.png](images/Final%20Project%20Aplikom%20Semester%203-201.png)

\>plot2d(normal(1,1000),\>distribution); ...  
\>     plot2d("qnormal(x)",color=red,thickness=2,\>add):


![images/Final%20Project%20Aplikom%20Semester%203-202.png](images/Final%20Project%20Aplikom%20Semester%203-202.png)

Ada juga banyak plot khusus untuk statistik. Boxplot menunjukkan
kuartil dari distribusi ini dan banyak pencilan. Menurut definisi,
pencilan dalam boxplot adalah data yang melebihi 1,5 kali kisaran 50%
tengah plot.


\>M=normal(5,1000); boxplot(quartiles(M)):


![images/Final%20Project%20Aplikom%20Semester%203-203.png](images/Final%20Project%20Aplikom%20Semester%203-203.png)

# Fungsi Implisit

Plot implisit menunjukkan garis level yang menyelesaikan f(x,y)=level,
di mana “level” dapat berupa nilai tunggal atau vektor nilai. Jika
level = “auto”, akan ada nc garis level, yang akan menyebar di antara
nilai minimum dan maksimum fungsi secara merata. Warna yang lebih
gelap atau lebih terang dapat ditambahkan dengan &gt;hue untuk
mengindikasikan nilai fungsi. Untuk fungsi implisit, xv haruslah
sebuah fungsi atau ekspresi dari parameter x dan y, atau, sebagai
alternatif, xv dapat berupa sebuah matriks nilai.


Euler dapat menandai garis level


dari fungsi apa pun.


Untuk menggambar himpunan f(x,y)=c untuk satu atau lebih konstanta c,
Anda dapat menggunakan plot2d() dengan plot implisitnya pada bidang.
Parameter untuk c adalah level = c, di mana c dapat berupa vektor
garis level. Sebagai tambahan, sebuah skema warna dapat digambar pada
latar belakang untuk mengindikasikan nilai fungsi untuk setiap titik
pada plot. Parameter “n” menentukan kehalusan plot.


\>aspect(1.5); 

\>plot2d("x^2+y^2-x\*y-x",r=1.5,level=0,contourcolor=red):


![images/Final%20Project%20Aplikom%20Semester%203-204.png](images/Final%20Project%20Aplikom%20Semester%203-204.png)

\>expr := "2\*x^2+x\*y+3\*y^4+y"; // define an expression f(x,y)

\>plot2d(expr,level=0): // Solutions of f(x,y)=0


![images/Final%20Project%20Aplikom%20Semester%203-205.png](images/Final%20Project%20Aplikom%20Semester%203-205.png)

\>plot2d(expr,level=0:0.5:20,\>hue,contourcolor=white,n=200): // nice


![images/Final%20Project%20Aplikom%20Semester%203-206.png](images/Final%20Project%20Aplikom%20Semester%203-206.png)

\>plot2d(expr,level=0:0.5:20,\>hue,\>spectral,n=200,grid=4): // nicer


![images/Final%20Project%20Aplikom%20Semester%203-207.png](images/Final%20Project%20Aplikom%20Semester%203-207.png)

Hal ini juga berlaku untuk plot data. Tetapi Anda harus menentukan
rentang untuk label sumbu.


\>x=-2:0.05:1; y=x'; z=expr(x,y);

\>plot2d(z,level=0,a=-1,b=2,c=-2,d=1,\>hue):


![images/Final%20Project%20Aplikom%20Semester%203-208.png](images/Final%20Project%20Aplikom%20Semester%203-208.png)

\>plot2d("x^3-y^2",\>contour,\>hue,\>spectral):


![images/Final%20Project%20Aplikom%20Semester%203-209.png](images/Final%20Project%20Aplikom%20Semester%203-209.png)

\>plot2d("x^3-y^2",level=0,contourwidth=3,\>add,contourcolor=red):


![images/Final%20Project%20Aplikom%20Semester%203-210.png](images/Final%20Project%20Aplikom%20Semester%203-210.png)

\>z=z+normal(size(z))\*0.2;

\>plot2d(z,level=0.5,a=-1,b=2,c=-2,d=1):


![images/Final%20Project%20Aplikom%20Semester%203-211.png](images/Final%20Project%20Aplikom%20Semester%203-211.png)

\>plot2d(expr,level=[0:0.2:5;0.05:0.2:5.05],color=lightgray):


![images/Final%20Project%20Aplikom%20Semester%203-212.png](images/Final%20Project%20Aplikom%20Semester%203-212.png)

\>plot2d("x^2+y^3+x\*y",level=1,r=4,n=100):


![images/Final%20Project%20Aplikom%20Semester%203-213.png](images/Final%20Project%20Aplikom%20Semester%203-213.png)

\>plot2d("x^2+2\*y^2-x\*y",level=0:0.1:10,n=100,contourcolor=white,\>hue):


![images/Final%20Project%20Aplikom%20Semester%203-214.png](images/Final%20Project%20Aplikom%20Semester%203-214.png)

Dimungkinkan juga untuk mengisi set


lateks: a \le f(x,y) \le b


dengan rentang level.


Dimungkinkan untuk mengisi wilayah nilai untuk fungsi tertentu. Untuk
ini, level harus berupa matriks 2xn. Baris pertama adalah batas bawah
dan baris kedua berisi batas atas.


\>plot2d(expr,level=[0;1],style="-",color=blue): // 0 <= f(x,y) <= 1


![images/Final%20Project%20Aplikom%20Semester%203-215.png](images/Final%20Project%20Aplikom%20Semester%203-215.png)

Plot implisit juga dapat menunjukkan rentang level. Maka level harus
berupa matriks 2xn interval level, di mana baris pertama berisi awal
dan baris kedua adalah akhir dari setiap interval. Sebagai alternatif,
vektor baris sederhana dapat digunakan untuk level, dan parameter dl
memperluas nilai level ke interval.


\>plot2d("x^4+y^4",r=1.5,level=[0;1],color=blue,style="/"):


![images/Final%20Project%20Aplikom%20Semester%203-216.png](images/Final%20Project%20Aplikom%20Semester%203-216.png)

\>plot2d("x^2+y^3+x\*y",level=[0,2,4;1,3,5],style="/",r=2,n=100):


![images/Final%20Project%20Aplikom%20Semester%203-217.png](images/Final%20Project%20Aplikom%20Semester%203-217.png)

\>plot2d("x^2+y^3+x\*y",level=-10:20,r=2,style="-",dl=0.1,n=100):


![images/Final%20Project%20Aplikom%20Semester%203-218.png](images/Final%20Project%20Aplikom%20Semester%203-218.png)

\>plot2d("sin(x)\*cos(y)",r=pi,\>hue,\>levels,n=100):


![images/Final%20Project%20Aplikom%20Semester%203-219.png](images/Final%20Project%20Aplikom%20Semester%203-219.png)

Anda juga dapat menandai suatu wilayah


lateks: a \le f(x,y) \le b.


Hal ini dilakukan dengan menambahkan level dengan dua baris.


\>plot2d("(x^2+y^2-1)^3-x^2\*y^3",r=1.3, ...  
\>     style="#",color=red,<outline, ...  
\>     level=[-2;0],n=100):


![images/Final%20Project%20Aplikom%20Semester%203-220.png](images/Final%20Project%20Aplikom%20Semester%203-220.png)

Dimungkinkan untuk menentukan level tertentu. Sebagai contoh, kita
dapat memplot solusi dari persamaan seperti


lateks: x^3-xy+x^2y^2=6


\>plot2d("x^3-x\*y+x^2\*y^2",r=6,level=1,n=100):


![images/Final%20Project%20Aplikom%20Semester%203-221.png](images/Final%20Project%20Aplikom%20Semester%203-221.png)

\>function starplot1 (v, style="/", color=green, lab=none) ...


      if !holding() then clg; endif;
      w=window(); window(0,0,1024,1024);
      h=holding(1);
      r=max(abs(v))*1.2;
      setplot(-r,r,-r,r);
      n=cols(v); t=linspace(0,2pi,n);
      v=v|v[1]; c=v*cos(t); s=v*sin(t);
      cl=barcolor(color); st=barstyle(style);
      loop 1 to n
        polygon([0,c[#],c[#+1]],[0,s[#],s[#+1]],1);
        if lab!=none then
          rlab=v[#]+r*0.1;
          {col,row}=toscreen(cos(t[#])*rlab,sin(t[#])*rlab);
          ctext(""+lab[#],col,row-textheight()/2);
        endif;
      end;
      barcolor(cl); barstyle(st);
      holding(h);
      window(w);
    endfunction
</pre>
Tidak ada kisi-kisi atau kutu sumbu di sini. Selain itu, kami
menggunakan jendela penuh untuk plot.


Kami memanggil reset sebelum kami menguji plot ini untuk mengembalikan
default grafis. Hal ini tidak perlu dilakukan, jika Anda yakin bahwa
plot Anda berfungsi.


\>reset; starplot1(normal(1,10)+5,color=red,lab=1:10):


![images/Final%20Project%20Aplikom%20Semester%203-222.png](images/Final%20Project%20Aplikom%20Semester%203-222.png)

Terkadang, Anda mungkin ingin memplot sesuatu yang tidak dapat
dilakukan oleh plot2d, tetapi hampir.


Pada fungsi berikut ini, kita akan membuat plot impuls logaritmik.
plot2d dapat membuat plot logaritmik, tetapi tidak untuk batang
impuls.


\>function logimpulseplot1 (x,y) ...


      {x0,y0}=makeimpulse(x,log(y)/log(10));
      plot2d(x0,y0,>bar,grid=0);
      h=holding(1);
      frame();
      xgrid(ticks(x));
      p=plot();
      for i=-10 to 10;
        if i<=p[4] and i>=p[3] then
           ygrid(i,yt="10^"+i);
        endif;
      end;
      holding(h);
    endfunction
</pre>
Let us test it with exponentially distributed values.


\>aspect(1.5); x=1:10; y=-log(random(size(x)))\*200; ...  
\>   logimpulseplot1(x,y):


![images/Final%20Project%20Aplikom%20Semester%203-223.png](images/Final%20Project%20Aplikom%20Semester%203-223.png)

Mari kita menghidupkan kurva 2D dengan menggunakan plot langsung.
Perintah plot(x,y) hanya memplot kurva ke dalam jendela plot.
setplot(a,b,c,d) mengatur jendela ini.


Fungsi wait(0) memaksa plot untuk muncul pada jendela grafik. Jika
tidak, penggambaran ulang akan dilakukan dalam interval waktu yang
jarang.


\>function animliss (n,m) ...


    t=linspace(0,2pi,500);
    f=0;
    c=framecolor(0);
    l=linewidth(2);
    setplot(-1,1,-1,1);
    repeat
      clg;
      plot(sin(n*t),cos(m*t+f));
      wait(0);
      if testkey() then break; endif;
      f=f+0.02;
    end;
    framecolor(c);
    linewidth(l);
    endfunction
</pre>
Tekan sembarang tombol untuk menghentikan animasi ini.


\>animliss(2,3); // lihat hasilnya, jika sudah puas, tekan ENTER


# Logarithmic Plots

EMT menggunakan parameter “logplot” untuk skala logaritmik.


Plot logaritmik dapat diplot menggunakan skala logaritmik dalam y
dengan logplot = 1, atau menggunakan skala logaritmik dalam x dan y
dengan logplot = 2, atau dalam x dengan logplot = 3.


 - logplot=1: y-logarithmic  
 - logplot=2: x-y-logarithmic  
 - logplot=3: x-logarithmic  

\>plot2d("exp(x^3-x)\*x^2",1,5,logplot=1):


![images/Final%20Project%20Aplikom%20Semester%203-224.png](images/Final%20Project%20Aplikom%20Semester%203-224.png)

\>plot2d("exp(x+sin(x))",0,100,logplot=1):


![images/Final%20Project%20Aplikom%20Semester%203-225.png](images/Final%20Project%20Aplikom%20Semester%203-225.png)

\>plot2d("exp(x+sin(x))",10,100,logplot=2):


![images/Final%20Project%20Aplikom%20Semester%203-226.png](images/Final%20Project%20Aplikom%20Semester%203-226.png)

\>plot2d("gamma(x)",1,10,logplot=1):


![images/Final%20Project%20Aplikom%20Semester%203-227.png](images/Final%20Project%20Aplikom%20Semester%203-227.png)

\>plot2d("log(x\*(2+sin(x/100)))",10,1000,logplot=3):


![images/Final%20Project%20Aplikom%20Semester%203-228.png](images/Final%20Project%20Aplikom%20Semester%203-228.png)

Hal ini juga bisa dilakukan dengan plot data.


\>x=10^(1:20); y=x^2-x;

\>plot2d(x,y,logplot=2):


![images/Final%20Project%20Aplikom%20Semester%203-229.png](images/Final%20Project%20Aplikom%20Semester%203-229.png)

## SOAL DAN PEMBAHASAN

1. Gambarkan plot fungsi berikut


\>reset;

\>figure(2,2);...  
\>   for n=1 to 4; figure(n); plot2d("2\*x^2"+n); end;...  
\>   figure(0):


![images/Final%20Project%20Aplikom%20Semester%203-230.png](images/Final%20Project%20Aplikom%20Semester%203-230.png)

2. Gambarkan grafik fungsi berikut : 


\>reset;...  
\>   aspect(3,1); ...  
\>   figure(1,3); ...  
\>   figure(1); plot2d("2\*x^4+2\*x+4", grid=2); ...  
\>   figure(2); plot2d("6\*x^3+4\*x^2+4", grid=5); ...  
\>   figure(3); plot2d("2\*x^2+20\*x", grid=6); ...  
\>   figure(0):


![images/Final%20Project%20Aplikom%20Semester%203-231.png](images/Final%20Project%20Aplikom%20Semester%203-231.png)

3. Gambarkan grafik berikut


\>reset;...  
\>   aspect(7,7);...  
\>   figure(4,1);...  
\>   figure(1); plot2d("2\*tan(x)", 0, 5pi);...  
\>   figure(2); plot2d("2\*tan(x)", 1, 6pi);...  
\>   figure(3); plot2d("2\*tan(x)", 2, 7pi);...  
\>   figure(4); plot2d("2\*tan(x)", 3, 8pi);...  
\>   figure(0):


![images/Final%20Project%20Aplikom%20Semester%203-232.png](images/Final%20Project%20Aplikom%20Semester%203-232.png)

4. Buatlah grafik fungsi dari 


\>reset;...  
\>   plot2d("2\*x^2", a=-1, b=1.5, c=-1, d=2, grid=7, style="--");...  
\>   insimg(10):


![images/Final%20Project%20Aplikom%20Semester%203-233.png](images/Final%20Project%20Aplikom%20Semester%203-233.png)

![images/Final%20Project%20Aplikom%20Semester%203-234.png](images/Final%20Project%20Aplikom%20Semester%203-234.png)

\>plot2d("x", \>add, color=orange, thickness=2, style=".")

\>&$solve(2\*x^2=x)


    
                                     1
                                [x = -, x = 0]
                                     2
    

5. Buatkan beberapa contoh plot statistik !


\>reset;

\>plot2d(cumsum(randnormal(5,5000))):


![images/Final%20Project%20Aplikom%20Semester%203-235.png](images/Final%20Project%20Aplikom%20Semester%203-235.png)

\>reset;

\>plot2d(cumsum(randnormal(10,40000))):


![images/Final%20Project%20Aplikom%20Semester%203-236.png](images/Final%20Project%20Aplikom%20Semester%203-236.png)

\>reset;

\>X=cumsum(randnormal(5,2000)); plot2d(X[1],X[2]):


![images/Final%20Project%20Aplikom%20Semester%203-237.png](images/Final%20Project%20Aplikom%20Semester%203-237.png)

\>reset;

\>columnsplot(cumsum(random(20)),style="/",color=orange):


![images/Final%20Project%20Aplikom%20Semester%203-238.png](images/Final%20Project%20Aplikom%20Semester%203-238.png)

\>reset;


# Rujukan Lengkap Fungsi plot2d()

  function plot2d (xv, yv, btest, a, b, c, d, xmin, xmax, r, n,  ..  
  logplot, grid, frame, framecolor, square, color, thickness, style, ..  
  auto, add, user, delta, points, addpoints, pointstyle, bar, histogram,  ..  
  distribution, even, steps, own, adaptive, hue, level, contour,  ..  
  nc, filled, fillcolor, outline, title, xl, yl, maps, contourcolor, ..  
  contourwidth, ticks, margin, clipping, cx, cy, insimg, spectral,  ..  
  cgrid, vertical, smaller, dl, niveau, levels)  

Multipurpose plot function for plots in the plane (2D plots). This function can do
plots of functions of one variables, data plots, curves in the plane, bar plots, grids
of complex numbers, and implicit plots of functions of two variables.


Parameters




x,y       : equations, functions or data vectors


a,b,c,d   : Plot area (default a=-2,b=2)


r         : if r is set, then a=cx-r, b=cx+r, c=cy-r, d=cy+r


            r can be a vector [rx,ry] or a vector [rx1,rx2,ry1,ry2].


xmin,xmax : range of the parameter for curves


auto      : Determine y-range automatically (default)


square    : if true, try to keep square x-y-ranges


n         : number of intervals (default is adaptive)


grid      : 0 = no grid and labels,


            1 = axis only,


            2 = normal grid (see below for the number of grid lines)


            3 = inside axis


            4 = no grid


            5 = full grid including margin


            6 = ticks at the frame


            7 = axis only


            8 = axis only, sub-ticks


frame     : 0 = no frame


framecolor: color of the frame and the grid


margin    : number between 0 and 0.4 for the margin around the plot


color     : Color of curves. If this is a vector of colors,


            it will be used for each row of a matrix of plots. In the case of


            point plots, it should be a column vector. If a row vector or a


            full matrix of colors is used for point plots, it will be used for


            each data point.


thickness : line thickness for curves


            This value can be smaller than 1 for very thin lines.


style     : Plot style for lines, markers, and fills.


            For points use


            "[]", "&lt;&gt;", ".", "..", "...",


            "*", "+", "|", "-", "o"


            "[]#", "&lt;&gt;#", "o#" (filled shapes)


            "[]w", "&lt;&gt;w", "ow" (non-transparent)


            For lines use


            "-", "--", "-.", ".", ".-.", "-.-", "-&gt;"


            For filled polygons or bar plots use


            "#", "#O", "O", "/", "\", "\/",


            "+", "|", "-", "t"


points    : plot single points instead of line segments


addpoints : if true, plots line segments and points


add       : add the plot to the existing plot


user      : enable user interaction for functions


delta     : step size for user interaction


bar       : bar plot (x are the interval bounds, y the interval values)


histogram : plots the frequencies of x in n subintervals


distribution=n : plots the distribution of x with n subintervals


even      : use inter values for automatic histograms.


steps     : plots the function as a step function (steps=1,2)


adaptive  : use adaptive plots (n is the minimal number of steps)


level     : plot level lines of an implicit function of two variables


outline   : draws boundary of level ranges.




If the level value is a 2xn matrix, ranges of levels will be drawn


in the color using the given fill style. If outline is true, it


will be drawn in the contour color. Using this feature, regions of


f(x,y) between limits can be marked.




hue       : add hue color to the level plot to indicate the function


            value


contour   : Use level plot with automatic levels


nc        : number of automatic level lines


title     : plot title (default "")


xl, yl    : labels for the x- and y-axis


smaller   : if &gt;0, there will be more space to the left for labels.


vertical  :


  Turns vertical labels on or off. This changes the global variable


  verticallabels locally for one plot. The value 1 sets only vertical


  text, the value 2 uses vertical numerical labels on the y axis.


filled    : fill the plot of a curve


fillcolor : fill color for bar and filled curves


outline   : boundary for filled polygons


logplot   : set logarithmic plots


            1 = logplot in y,


            2 = logplot in xy,


            3 = logplot in x


own       :


  A string, which points to an own plot routine. With &gt;user, you get


  the same user interaction as in plot2d. The range will be set


  before each call to your function.


maps      : map expressions (0 is faster), functions are always mapped.


contourcolor : color of contour lines


contourwidth : width of contour lines


clipping  : toggles the clipping (default is true)


title     :


  This can be used to describe the plot. The title will appear above


  the plot. Moreover, a label for the x and y axis can be added with


  xl="string" or yl="string". Other labels can be added with the


  functions label() or labelbox(). The title can be a unicode


  string or an image of a Latex formula.


cgrid     :


  Determines the number of grid lines for plots of complex grids.


  Should be a divisor of the the matrix size minus 1 (number of


  subintervals). cgrid can be a vector [cx,cy].


Overview


The function can plot


* 
expressions, call collections or functions of one variable,

* 
parametric curves,

* 
x data against y data,

* 
implicit functions,

* 
bar plots,

* 
complex grids,

* 
polygons.


If a function or expression for xv is given, plot2d() will compute


values in the given range using the function or expression. The


expression must be an expression in the variable x. The range must


be defined in the parameters a and b unless the default range


[-2,2] should be used. The y-range will be computed automatically,


unless c and d are specified, or a radius r, which yields the range


[-r,r] for x and y. For plots of functions, plot2d will use an


adaptive evaluation of the function by default. To speed up the


plot for complicated functions, switch this off with &lt;adaptive, and


optionally decrease the number of intervals n. Moreover, plot2d()


will by default use mapping. I.e., it will compute the plot element


for element. If your expression or your functions can handle a


vector x, you can switch that off with &lt;maps for faster evaluation.


Note that adaptive plots are always computed element for element. 


If functions or expressions for both xv and for yv are specified,


plot2d() will compute a curve with the xv values as x-coordinates


and the yv values as y-coordinates. In this case, a range should be


defined for the parameter using xmin, xmax. Expressions contained


# Menggambar Plot 3D dengan EMT

Ini adalah pengenalan terhadap plot 3D di Euler. Kita memerlukan plot
3D untuk memvisualisasikan fungsi dari dua variabel.


Euler menggambar fungsi tersebut menggunakan algoritma pengurutan
untuk menyembunyikan bagian-bagian di latar belakang. Secara umum,
Euler menggunakan proyeksi pusat. Standarnya adalah dari kuadran x-y
positif ke arah titik asal x=y=z=0, tetapi sudut=0° terlihat dari arah
sumbu y. Sudut pandang dan ketinggian dapat diubah.


Euler dapat memetakan


* 
permukaan dengan bayangan dan garis level atau rentang level,

* 
awan titik-titik,

* 
kurva parametrik,

* 
permukaan implisit.


Plot 3D dari sebuah fungsi menggunakan plot3d. Cara termudah adalah
memplot ekspresi dalam x dan y. Parameter r mengatur rentang plot di
sekitar (0,0).


\>aspect(1.5); plot3d("x^2+sin(y)",-5,5,0,6\*pi):


![images/Final%20Project%20Aplikom%20Semester%203-239.png](images/Final%20Project%20Aplikom%20Semester%203-239.png)

\>plot3d("x^2+x\*sin(y)",-5,5,0,6\*pi):


![images/Final%20Project%20Aplikom%20Semester%203-240.png](images/Final%20Project%20Aplikom%20Semester%203-240.png)

Silakan lakukan modifikasi agar gambar "talang bergelombang" tersebut tidak lurus melainkan melengkung/melingkar, baik
melingkar secara mendatar maupun melingkar turun/naik (seperti papan peluncur pada kolam renang. Temukan rumusnya.


\>aspect(1.5); plot3d("3\*x^2+4\*y+20",-5,5,0):


![images/Final%20Project%20Aplikom%20Semester%203-241.png](images/Final%20Project%20Aplikom%20Semester%203-241.png)

# Fungsi dari dua Variabel

Untuk grafik sebuah fungsi, gunakan


* 
ekspresi sederhana dalam x dan y,

* 
nama fungsi dari dua variabell

* 
atau matriks data.


Standarnya adalah kisi-kisi kawat yang terisi dengan warna yang
berbeda di kedua sisi. Perhatikan bahwa jumlah default interval grid
adalah 10, namun plot menggunakan jumlah default 40x40 persegi panjang
untuk membangun permukaan. Hal ini dapat diubah.


* 
n=40, n=[40,40]: jumlah garis kisi di setiap arah

* 
grid=10, grid=[10,10]: jumlah garis grid di setiap arah.


Kami menggunakan default n=40 dan grid=10.


\>plot3d("x^2+y^2"):


![images/Final%20Project%20Aplikom%20Semester%203-242.png](images/Final%20Project%20Aplikom%20Semester%203-242.png)

Interaksi pengguna dapat dilakukan dengan parameter &gt;user. Pengguna
dapat menekan tombol berikut ini.


* 
kiri, kanan, atas, bawah: memutar sudut pandang

* 
+,-: memperbesar atau memperkecil

* 
a: menghasilkan anaglyph (lihat di bawah)

* 
l: beralih memutar sumber cahaya (lihat di bawah)

* 
spasi: mengatur ulang ke default

* 
kembali: mengakhiri interaksi


\>plot3d("exp(-x^2+y^2)",\>user, ...  
\>     title="Turn with the vector keys (press return to finish)"):


![images/Final%20Project%20Aplikom%20Semester%203-243.png](images/Final%20Project%20Aplikom%20Semester%203-243.png)

Rentang plot untuk fungsi dapat ditentukan dengan


* 
a, b: rentang x

* 
c, d: rentang y

* 
r: bujur sangkar simetris di sekitar (0,0).

* 
n: jumlah subinterval untuk plot.


Terdapat beberapa parameter untuk menskalakan fungsi atau mengubah
tampilan grafik.


fscale: skala untuk nilai fungsi (standarnya adalah &lt;fscale).


scale: angka atau vektor 1x2 untuk menskalakan ke arah x dan y.


frame: jenis bingkai (default 1).


\>plot3d("exp(-(x^2+y^2)/5)",r=10,n=80,fscale=4,scale=1.2,frame=3,\>user):


![images/Final%20Project%20Aplikom%20Semester%203-244.png](images/Final%20Project%20Aplikom%20Semester%203-244.png)

Tampilan dapat diubah dengan berbagai cara.


* 
jarak: jarak pandang ke plot.

* 
zoom: nilai zoom.

* 
angle: sudut ke sumbu y negatif dalam radian.

* 
height: ketinggian tampilan dalam radian.


Nilai default dapat diperiksa atau diubah dengan fungsi view(). Fungsi
ini mengembalikan parameter dalam urutan di atas.


\>view


    [5,  2.6,  2,  0.4]

Jarak yang lebih dekat membutuhkan zoom yang lebih sedikit. Efeknya
lebih seperti lensa sudut lebar.


Dalam contoh berikut ini, sudut = 0 dan tinggi = 0 terlihat dari sumbu
y negatif. Label sumbu untuk y disembunyikan dalam kasus ini.


\>plot3d("x^2+y",distance=3,zoom=1,angle=pi/2,height=0):


![images/Final%20Project%20Aplikom%20Semester%203-245.png](images/Final%20Project%20Aplikom%20Semester%203-245.png)

Plot terlihat selalu ke bagian tengah kubus plot. Anda dapat
memindahkan bagian tengah dengan parameter center.


\>plot3d("x^4+y^2",a=0,b=1,c=-1,d=1,angle=-20°,height=20°, ...  
\>     center=[0.4,0,0],zoom=5):


![images/Final%20Project%20Aplikom%20Semester%203-246.png](images/Final%20Project%20Aplikom%20Semester%203-246.png)

Plot diskalakan agar sesuai dengan kubus satuan untuk dilihat. Jadi,
tidak perlu mengubah jarak atau melakukan zoom, tergantung pada ukuran
plot. Namun demikian, label mengacu ke ukuran yang sesungguhnya.


Jika Anda menonaktifkannya dengan scale=false, Anda harus berhati-hati
agar plot tetap muat di dalam jendela plotting, dengan mengubah jarak
tampilan atau zoom, dan memindahkan bagian tengahnya.


\>plot3d("5\*exp(-x^2-y^2)",r=2,<fscale,<scale,distance=13,height=50°, ...  
\>     center=[0,0,-2],frame=3):


![images/Final%20Project%20Aplikom%20Semester%203-247.png](images/Final%20Project%20Aplikom%20Semester%203-247.png)

Plot polar juga tersedia. Parameter polar=true menggambar plot polar.
Fungsi harus tetap merupakan fungsi dari x dan y. Parameter “fscale”
menskalakan fungsi dengan skala sendiri. Jika tidak, fungsi akan
diskalakan agar sesuai dengan kubus.


\>plot3d("1/(x^2+y^2+1)",r=5,\>polar, ...  
\>   fscale=2,\>hue,n=100,zoom=4,\>contour,color=blue):


![images/Final%20Project%20Aplikom%20Semester%203-248.png](images/Final%20Project%20Aplikom%20Semester%203-248.png)

\>function f(r) := exp(-r/2)\*cos(r); ...  
\>   plot3d("f(x^2+y^2)",\>polar,scale=[1,1,0.4],r=pi,frame=3,zoom=4):


![images/Final%20Project%20Aplikom%20Semester%203-249.png](images/Final%20Project%20Aplikom%20Semester%203-249.png)

Parameter rotate memutar fungsi dalam x di sekitar sumbu x.


* 
rotate = 1: Menggunakan sumbu x

* 
rotate=2: Menggunakan sumbu z


\>plot3d("x^2+1",a=-1,b=1,rotate=true,grid=5):


![images/Final%20Project%20Aplikom%20Semester%203-250.png](images/Final%20Project%20Aplikom%20Semester%203-250.png)

\>plot3d("x^2+1",a=-1,b=1,rotate=2,grid=5):


![images/Final%20Project%20Aplikom%20Semester%203-251.png](images/Final%20Project%20Aplikom%20Semester%203-251.png)

\>plot3d("sqrt(25-x^2)",a=0,b=5,rotate=1):


![images/Final%20Project%20Aplikom%20Semester%203-252.png](images/Final%20Project%20Aplikom%20Semester%203-252.png)

\>plot3d("x\*sin(x)",a=0,b=6pi,rotate=2):


![images/Final%20Project%20Aplikom%20Semester%203-253.png](images/Final%20Project%20Aplikom%20Semester%203-253.png)

Berikut ini adalah plot dengan tiga fungsi.


\>plot3d("x","x^2+y^2","y",r=2,zoom=3.5,frame=3):


![images/Final%20Project%20Aplikom%20Semester%203-254.png](images/Final%20Project%20Aplikom%20Semester%203-254.png)

# Plot Kontur

Untuk plot, Euler menambahkan garis kisi-kisi. Sebagai gantinya,
dimungkinkan untuk menggunakan garis level dan rona satu warna atau
rona berwarna spektral. Euler dapat menggambar ketinggian fungsi pada
plot dengan bayangan. Pada semua plot 3D, Euler dapat menghasilkan
anaglyph merah/cyan.


* 
Rona: Mengaktifkan bayangan cahaya, bukan kabel.

* 
&gt;contour: Memplot garis kontur otomatis pada plot.

* 
level=... (atau level): Vektor nilai untuk garis kontur.


Defaultnya adalah level=“auto”, yang menghitung beberapa garis level
secara otomatis. Seperti yang Anda lihat di plot, level sebenarnya
adalah rentang level.


Gaya default dapat diubah. Untuk plot kontur berikut ini, kami
menggunakan grid yang lebih halus untuk titik 100x100, skala fungsi
dan plot, dan menggunakan sudut pandang yang berbeda.


\>plot3d("exp(-x^2-y^2)",r=2,n=100,level="thin", ...  
\>    \>contour,\>spectral,fscale=1,scale=1.1,angle=45°,height=20°):


![images/Final%20Project%20Aplikom%20Semester%203-255.png](images/Final%20Project%20Aplikom%20Semester%203-255.png)

\>plot3d("exp(x\*y)",angle=100°,\>contour,color=green):


![images/Final%20Project%20Aplikom%20Semester%203-256.png](images/Final%20Project%20Aplikom%20Semester%203-256.png)

Bayangan default menggunakan warna abu-abu. Tetapi, kisaran warna
spektral juga tersedia.


* 
&gt;spektral: Menggunakan skema spektral default

* 
color =...: Menggunakan warna khusus atau skema spektral


Untuk plot berikut ini, kami menggunakan skema spektral default dan
menambah jumlah titik untuk mendapatkan tampilan yang sangat mulus.


\>plot3d("x^2+y^2",\>spectral,\>contour,n=100):


![images/Final%20Project%20Aplikom%20Semester%203-257.png](images/Final%20Project%20Aplikom%20Semester%203-257.png)

Alih-alih garis level otomatis, kita juga dapat menetapkan nilai garis
level. Hal ini akan menghasilkan garis level yang tipis, alih-alih
rentang level.


\>plot3d("x^2-y^2",0,5,0,5,level=-1:0.1:1,color=redgreen):


![images/Final%20Project%20Aplikom%20Semester%203-258.png](images/Final%20Project%20Aplikom%20Semester%203-258.png)

Pada plot berikut ini, kami menggunakan dua pita level yang sangat
luas dari -0,1 hingga 1, dan dari 0,9 hingga 1. Ini dimasukkan sebagai
matriks dengan batas-batas level sebagai kolom.


Selain itu, kami menghamparkan grid dengan 10 interval di setiap arah.


\>plot3d("x^2+y^3",level=[-0.1,0.9;0,1], ...  
\>     \>spectral,angle=30°,grid=10,contourcolor=gray):


![images/Final%20Project%20Aplikom%20Semester%203-259.png](images/Final%20Project%20Aplikom%20Semester%203-259.png)

Pada contoh berikut, kami memplot himpunan, di mana


Kita menggunakan satu garis tipis untuk garis level.


\>plot3d("x^y-y^x",level=0,a=0,b=6,c=0,d=6,contourcolor=red,n=100):


![images/Final%20Project%20Aplikom%20Semester%203-260.png](images/Final%20Project%20Aplikom%20Semester%203-260.png)

Dimungkinkan untuk menampilkan bidang kontur di bawah plot. Warna dan
jarak ke plot dapat ditentukan.


\>plot3d("x^2+y^4",\>cp,cpcolor=green,cpdelta=0.2):


![images/Final%20Project%20Aplikom%20Semester%203-261.png](images/Final%20Project%20Aplikom%20Semester%203-261.png)

Berikut ini beberapa gaya lainnya. Kami selalu mematikan bingkai, dan
menggunakan berbagai skema warna untuk plot dan kisi-kisi.


\>figure(2,2); ...  
\>   expr="y^3-x^2"; ...  
\>   figure(1);  ...  
\>     plot3d(expr,<frame,\>cp,cpcolor=spectral); ...  
\>   figure(2);  ...  
\>     plot3d(expr,<frame,\>spectral,grid=10,cp=2); ...  
\>   figure(3);  ...  
\>     plot3d(expr,<frame,\>contour,color=gray,nc=5,cp=3,cpcolor=greenred); ...  
\>   figure(4);  ...  
\>     plot3d(expr,<frame,\>hue,grid=10,\>transparent,\>cp,cpcolor=gray); ...  
\>   figure(0):


![images/Final%20Project%20Aplikom%20Semester%203-262.png](images/Final%20Project%20Aplikom%20Semester%203-262.png)

Ada beberapa skema spektral lainnya, yang diberi nomor dari 1 hingga
9. Tetapi Anda juga dapat menggunakan color=value, di mana value


* 
spektral: untuk rentang dari biru ke merah

* 
putih: untuk rentang yang lebih redup

* 
kuningbiru, ungu-hijau, biru-kuning, hijau-merah

* 
biru-kuning, hijau-ungu, kuning-biru, merah-hijau


\>figure(3,3); ...  
\>   for i=1:9;  ...  
\>     figure(i); plot3d("x^2+y^2",spectral=i,\>contour,\>cp,<frame,zoom=4);  ...  
\>   end; ...  
\>   figure(0):


![images/Final%20Project%20Aplikom%20Semester%203-263.png](images/Final%20Project%20Aplikom%20Semester%203-263.png)

Sumber cahaya dapat diubah dengan l dan tombol kursor selama interaksi
pengguna. Ini juga dapat ditetapkan dengan parameter.


* 
light: arah cahaya

* 
amb: cahaya sekitar antara 0 dan 1


Perhatikan, bahwa program ini tidak membuat perbedaan di antara
sisi-sisi plot. Tidak ada bayangan. Untuk ini Anda akan membutuhkan
Povray.


\>plot3d("-x^2-y^2", ...  
\>     hue=true,light=[0,1,1],amb=0,user=true, ...  
\>     title="Press l and cursor keys (return to exit)"):


![images/Final%20Project%20Aplikom%20Semester%203-264.png](images/Final%20Project%20Aplikom%20Semester%203-264.png)

Parameter warna mengubah warna permukaan. Warna garis level juga dapat
diubah.


\>plot3d("-x^2-y^2",color=rgb(0.2,0.2,0),hue=true,frame=false, ...  
\>     zoom=3,contourcolor=red,level=-2:0.1:1,dl=0.01):


![images/Final%20Project%20Aplikom%20Semester%203-265.png](images/Final%20Project%20Aplikom%20Semester%203-265.png)

Warna 0 memberikan efek pelangi yang istimewa.


\>plot3d("x^2/(x^2+y^2+1)",color=0,hue=true,grid=10):


![images/Final%20Project%20Aplikom%20Semester%203-266.png](images/Final%20Project%20Aplikom%20Semester%203-266.png)

Permukaannya juga bisa transparan.


\>plot3d("x^2+y^2",\>transparent,grid=10,wirecolor=red):


![images/Final%20Project%20Aplikom%20Semester%203-267.png](images/Final%20Project%20Aplikom%20Semester%203-267.png)

# Plot Implisit

Ada juga plot implisit dalam tiga dimensi. Euler menghasilkan potongan
melalui objek. Fitur plot3d termasuk plot implisit. Plot-plot ini
menunjukkan himpunan nol dari sebuah fungsi dalam tiga variabel.


Solusi dari


dapat divisualisasikan dalam potongan yang sejajar dengan bidang x-y,
bidang x-z, dan bidang y-z.


* 
implisit = 1: potong sejajar dengan bidang y-z

* 
implicit = 2: memotong sejajar dengan bidang x-z

* 
implicit=4: memotong sejajar dengan bidang x-y


Tambahkan nilai-nilai ini, jika Anda suka. Pada contoh, kami memplot


\>plot3d("x^2+y^3+z\*y-1",r=5,implicit=3):


![images/Final%20Project%20Aplikom%20Semester%203-268.png](images/Final%20Project%20Aplikom%20Semester%203-268.png)

\>c=1; d=1;

\>plot3d("((x^2+y^2-c^2)^2+(z^2-1)^2)\*((y^2+z^2-c^2)^2+(x^2-1)^2)\*((z^2+x^2-c^2)^2+(y^2-1)^2)-d",r=2,<frame,\>implicit,\>user): 


![images/Final%20Project%20Aplikom%20Semester%203-269.png](images/Final%20Project%20Aplikom%20Semester%203-269.png)

\>plot3d("x^2+y^2+4\*x\*z+z^3",\>implicit,r=2,zoom=2.5):


![images/Final%20Project%20Aplikom%20Semester%203-270.png](images/Final%20Project%20Aplikom%20Semester%203-270.png)

\>plot3d("x^2+y^2+4\*x\*z+z^3",\>implicit,r=2,zoom=2.5):


![images/Final%20Project%20Aplikom%20Semester%203-271.png](images/Final%20Project%20Aplikom%20Semester%203-271.png)

# Memplot Data 3D

Sama seperti plot2d, plot3d menerima data. Untuk objek 3D, Anda perlu
menyediakan matriks nilai x, y, dan z, atau tiga fungsi atau ekspresi
fx(x,y), fy(x,y), fz(x,y).


Karena x,y,z adalah matriks, kita mengasumsikan bahwa (t,s) berjalan
melalui kotak persegi. Hasilnya, Anda dapat memplot gambar persegi
panjang dalam ruang.


Anda dapat menggunakan bahasa matriks Euler untuk menghasilkan
koordinat secara efektif.


Pada contoh berikut, kita menggunakan vektor nilai t dan vektor kolom
nilai s untuk memparameterkan permukaan bola. Pada gambar kita dapat
menandai daerah, dalam kasus kita daerah kutub.


\>t=linspace(0,2pi,180); s=linspace(-pi/2,pi/2,90)'; ...  
\>   x=cos(s)\*cos(t); y=cos(s)\*sin(t); z=sin(s); ...  
\>   plot3d(x,y,z,\>hue, ...  
\>   color=blue,<frame,grid=[10,20], ...  
\>   values=s,contourcolor=red,level=[90°-24°;90°-22°], ...  
\>   scale=1.4,height=50°):


![images/Final%20Project%20Aplikom%20Semester%203-272.png](images/Final%20Project%20Aplikom%20Semester%203-272.png)

Berikut ini adalah contoh, yang merupakan grafik suatu fungsi.


\>t=-1:0.1:1; s=(-1:0.1:1)'; plot3d(t,s,t\*s,grid=10):


![images/Final%20Project%20Aplikom%20Semester%203-273.png](images/Final%20Project%20Aplikom%20Semester%203-273.png)

Namun demikian, kita bisa membuat segala macam permukaan. Berikut ini
adalah permukaan yang sama dengan fungsi


\>plot3d(t\*s,t,s,angle=180°,grid=10):


![images/Final%20Project%20Aplikom%20Semester%203-274.png](images/Final%20Project%20Aplikom%20Semester%203-274.png)

Dengan lebih banyak upaya, kita bisa menghasilkan banyak permukaan.


Dalam contoh berikut ini, kami membuat tampilan berbayang dari bola
yang terdistorsi. Koordinat yang biasa digunakan untuk bola adalah


dengan


Kami mengubahnya dengan sebuah faktor


\>t=linspace(0,2pi,320); s=linspace(-pi/2,pi/2,160)'; ...  
\>   d=1+0.2\*(cos(4\*t)+cos(8\*s)); ...  
\>   plot3d(cos(t)\*cos(s)\*d,sin(t)\*cos(s)\*d,sin(s)\*d,hue=1, ...  
\>     light=[1,0,1],frame=0,zoom=5):


![images/Final%20Project%20Aplikom%20Semester%203-275.png](images/Final%20Project%20Aplikom%20Semester%203-275.png)

Tentu saja, awan titik juga dimungkinkan. Untuk memplot data titik
dalam ruang, kita membutuhkan tiga vektor untuk koordinat titik.


Gaya-gayanya sama seperti pada plot2d dengan points=true;


\>n=500;  ...  
\>     plot3d(normal(1,n),normal(1,n),normal(1,n),points=true,style="."):


![images/Final%20Project%20Aplikom%20Semester%203-276.png](images/Final%20Project%20Aplikom%20Semester%203-276.png)

Anda juga dapat memplot kurva dalam bentuk 3D. Dalam hal ini, akan
lebih mudah untuk menghitung titik-titik kurva. Untuk kurva pada
bidang, kami menggunakan urutan koordinat dan parameter wire = true.


\>t=linspace(0,8pi,500); ...  
\>   plot3d(sin(t),cos(t),t/10,\>wire,zoom=3):


![images/Final%20Project%20Aplikom%20Semester%203-277.png](images/Final%20Project%20Aplikom%20Semester%203-277.png)

\>t=linspace(0,4pi,1000); plot3d(cos(t),sin(t),t/2pi,\>wire, ...  
\>   linewidth=3,wirecolor=blue):


![images/Final%20Project%20Aplikom%20Semester%203-278.png](images/Final%20Project%20Aplikom%20Semester%203-278.png)

\>X=cumsum(normal(3,100)); ...  
\>    plot3d(X[1],X[2],X[3],\>anaglyph,\>wire):


![images/Final%20Project%20Aplikom%20Semester%203-279.png](images/Final%20Project%20Aplikom%20Semester%203-279.png)

EMT juga dapat membuat plot dalam mode anaglyph. Untuk melihat plot
semacam itu, Anda memerlukan kacamata merah/cyan.


\> plot3d("x^2+y^3",\>anaglyph,\>contour,angle=30°):


![images/Final%20Project%20Aplikom%20Semester%203-280.png](images/Final%20Project%20Aplikom%20Semester%203-280.png)

Sering kali, skema warna spektral digunakan untuk plot. Hal ini
menekankan ketinggian fungsi.


\>plot3d("x^2\*y^3-y",\>spectral,\>contour,zoom=3.2):


![images/Final%20Project%20Aplikom%20Semester%203-281.png](images/Final%20Project%20Aplikom%20Semester%203-281.png)

Euler juga dapat memplot permukaan yang diparameterkan, ketika
parameternya adalah nilai x, y, dan z dari gambar kisi-kisi persegi
panjang di dalam ruang.


Untuk demo berikut ini, kami menyiapkan parameter u dan v, dan
menghasilkan koordinat ruang dari parameter ini.


\>u=linspace(-1,1,10); v=linspace(0,2\*pi,50)'; ...  
\>   X=(3+u\*cos(v/2))\*cos(v); Y=(3+u\*cos(v/2))\*sin(v); Z=u\*sin(v/2); ...  
\>   plot3d(X,Y,Z,\>anaglyph,<frame,\>wire,scale=2.3):


![images/Final%20Project%20Aplikom%20Semester%203-282.png](images/Final%20Project%20Aplikom%20Semester%203-282.png)

Berikut ini contoh yang lebih rumit, yang tampak megah dengan kacamata
merah/cyan.


\>u:=linspace(-pi,pi,160); v:=linspace(-pi,pi,400)';  ...  
\>   x:=(4\*(1+.25\*sin(3\*v))+cos(u))\*cos(2\*v); ...  
\>   y:=(4\*(1+.25\*sin(3\*v))+cos(u))\*sin(2\*v); ...  
\>    z=sin(u)+2\*cos(3\*v); ...  
\>   plot3d(x,y,z,frame=0,scale=1.5,hue=1,light=[1,0,-1],zoom=2.8,\>anaglyph):


![images/Final%20Project%20Aplikom%20Semester%203-283.png](images/Final%20Project%20Aplikom%20Semester%203-283.png)

# Plot Statistik

Plot batang juga dapat digunakan. Untuk ini, kita harus menyediakan


* 
x: vektor baris dengan n+1 elemen

* 
y: vektor kolom dengan n+1 elemen

* 
z: matriks nilai berukuran nxn.


z dapat lebih besar, tetapi hanya nilai nxn yang akan digunakan.


Pada contoh, pertama-tama kita menghitung nilainya. Kemudian kita
sesuaikan x dan y, sehingga vektor berada di tengah-tengah nilai yang
digunakan.


\>x=-1:0.1:1; y=x'; z=x^2+y^2; ...  
\>   xa=(x|1.1)-0.05; ya=(y\_1.1)-0.05; ...  
\>   plot3d(xa,ya,z,bar=true):


![images/Final%20Project%20Aplikom%20Semester%203-284.png](images/Final%20Project%20Aplikom%20Semester%203-284.png)

Dimungkinkan untuk membagi plot permukaan menjadi dua bagian atau
lebih.


\>x=-1:0.1:1; y=x'; z=x+y; d=zeros(size(x)); ...  
\>   plot3d(x,y,z,disconnect=2:2:20):


![images/Final%20Project%20Aplikom%20Semester%203-285.png](images/Final%20Project%20Aplikom%20Semester%203-285.png)

Jika memuat atau menghasilkan matriks data M dari file dan perlu
memplotnya dalam 3D, Anda dapat menskalakan matriks ke [-1,1] dengan
scale(M), atau menskalakan matriks dengan &gt;zscale. Hal ini dapat
dikombinasikan dengan faktor penskalaan individual yang diterapkan
sebagai tambahan.


\>i=1:20; j=i'; ...  
\>   plot3d(i\*j^2+100\*normal(20,20),\>zscale,scale=[1,1,1.5],angle=-40°,zoom=1.8):


![images/Final%20Project%20Aplikom%20Semester%203-286.png](images/Final%20Project%20Aplikom%20Semester%203-286.png)

\>Z=intrandom(5,100,6); v=zeros(5,6); ...  
\>   loop 1 to 5; v[#]=getmultiplicities(1:6,Z[#]); end; ...  
\>   columnsplot3d(v',scols=1:5,ccols=[1:5]):


![images/Final%20Project%20Aplikom%20Semester%203-287.png](images/Final%20Project%20Aplikom%20Semester%203-287.png)

# Permukaan Benda Putar

\>plot2d("(x^2+y^2-1)^3-x^2\*y^3",r=1.3, ...  
\>   style="#",color=red,<outline, ...  
\>   level=[-2;0],n=100):


![images/Final%20Project%20Aplikom%20Semester%203-288.png](images/Final%20Project%20Aplikom%20Semester%203-288.png)

\>ekspresi &= (x^2+y^2-1)^3-x^2\*y^3; $ekspresi


$$\left(y^2+x^2-1\right)^3-x^2\,y^3$$Kami ingin memutar kurva jantung di sekitar sumbu y. Berikut ini
adalah ekspresi yang mendefinisikan jantung:


Selanjutnya kita atur


\>function fr(r,a) &= ekspresi with [x=r\*cos(a),y=r\*sin(a)] | trigreduce; $fr(r,a)


$$\left(r^2-1\right)^3+\frac{\left(\sin \left(5\,a\right)-\sin \left(
 3\,a\right)-2\,\sin a\right)\,r^5}{16}$$Hal ini memungkinkan untuk mendefinisikan fungsi numerik, yang
menyelesaikan untuk r, jika a diberikan. Dengan fungsi tersebut kita
dapat memplotkan jantung yang diputar sebagai permukaan parametrik.


\>function map f(a) := bisect("fr",0,2;a); ...  
\>   t=linspace(-pi/2,pi/2,100); r=f(t);  ...  
\>   s=linspace(pi,2pi,100)'; ...  
\>   plot3d(r\*cos(t)\*sin(s),r\*cos(t)\*cos(s),r\*sin(t), ...  
\>   \>hue,<frame,color=red,zoom=4,amb=0,max=0.7,grid=12,height=50°):


![images/Final%20Project%20Aplikom%20Semester%203-291.png](images/Final%20Project%20Aplikom%20Semester%203-291.png)

Berikut ini adalah plot 3D dari gambar di atas yang diputar
mengelilingi sumbu-z. Kami mendefinisikan fungsi, yang menggambarkan
objek.


\>function f(x,y,z) ...


    r=x^2+y^2;
    return (r+z^2-1)^3-r*z^3;
     endfunction
</pre>
\>plot3d("f(x,y,z)", ...  
\>   xmin=0,xmax=1.2,ymin=-1.2,ymax=1.2,zmin=-1.2,zmax=1.4, ...  
\>   implicit=1,angle=-30°,zoom=2.5,n=[10,100,60],\>anaglyph):


![images/Final%20Project%20Aplikom%20Semester%203-292.png](images/Final%20Project%20Aplikom%20Semester%203-292.png)

# Plot 3D Khusus

Fungsi plot3d memang bagus untuk dimiliki, tetapi tidak memenuhi semua
kebutuhan. Selain rutinitas yang lebih mendasar, Anda juga bisa
mendapatkan plot berbingkai dari objek apa pun yang Anda sukai.


Meskipun Euler bukan program 3D, namun dapat menggabungkan beberapa
objek dasar. Kami mencoba memvisualisasikan parabola dan garis
singgungnya.


\>function myplot ...


      y=-1:0.01:1; x=(-1:0.01:1)';
      plot3d(x,y,0.2*(x-0.1)/2,<scale,<frame,>hue, ..
        hues=0.5,>contour,color=orange);
      h=holding(1);
      plot3d(x,y,(x^2+y^2)/2,<scale,<frame,>contour,>hue);
      holding(h);
    endfunction
</pre>
Sekarang framedplot() menyediakan frame, dan mengatur tampilan.


\>framedplot("myplot",[-1,1,-1,1,0,1],height=0,angle=-30°, ...  
\>     center=[0,0,-0.7],zoom=3):


![images/Final%20Project%20Aplikom%20Semester%203-293.png](images/Final%20Project%20Aplikom%20Semester%203-293.png)

Dengan cara yang sama, Anda dapat memplot bidang kontur secara manual.
Perhatikan bahwa plot3d() mengatur jendela ke fullwindow() secara
default, namun plotcontourplane() mengasumsikannya.


\>x=-1:0.02:1.1; y=x'; z=x^2-y^4;

\>function myplot (x,y,z) ...  
\>  
<pre class="udf">      zoom(2);
      wi=fullwindow();
      plotcontourplane(x,y,z,level="auto",<scale);
      plot3d(x,y,z,>hue,<scale,>add,color=white,level="thin");
      window(wi);
      reset();
    endfunction
</pre>
\>myplot(x,y,z):


![images/Final%20Project%20Aplikom%20Semester%203-294.png](images/Final%20Project%20Aplikom%20Semester%203-294.png)

# Animasi

Euler dapat menggunakan frame untuk melakukan pra-komputasi animasi.


Salah satu fungsi yang memanfaatkan teknik ini adalah rotate. Fungsi
ini dapat mengubah sudut pandang dan menggambar ulang plot 3D. Fungsi
ini memanggil addpage() untuk setiap plot baru. Akhirnya fungsi ini
menganimasikan plot tersebut.


Silakan pelajari sumber dari rotate untuk melihat lebih detail.


\>function testplot () := plot3d("x^2+y^3"); ...  
\>   rotate("testplot"); testplot():


![images/Final%20Project%20Aplikom%20Semester%203-295.png](images/Final%20Project%20Aplikom%20Semester%203-295.png)

# Menggambar Povray

Dengan bantuan file Euler povray.e, Euler dapat menghasilkan file
Povray. Hasilnya sangat bagus untuk dilihat.


Anda perlu menginstal Povray (32bit atau 64bit) dari
  <a href="http://www.povray.org/, dan meletakkan sub-direktori “bin” dari Povray ke dalam jalur lingkungan, atau mengatur variabel “defaultpovray” dengan jalur lengkap yang mengarah ke “pvengine.exe”.">http://www.povray.org/, dan meletakkan sub-direktori “bin” dari Povray ke dalam jalur lingkungan, atau mengatur variabel “defaultpovray” dengan jalur lengkap yang mengarah ke “pvengine.exe”.</a>


Antarmuka Povray dari Euler menghasilkan file Povray di direktori home
pengguna, dan memanggil Povray untuk mengurai file-file ini. Nama file
default adalah current.pov, dan direktori defaultnya adalah
eulerhome(), biasanya c:\Users\Username\Euler. Povray menghasilkan
sebuah file PNG, yang dapat dimuat oleh Euler ke dalam notebook. Untuk
membersihkan berkas-berkas ini, gunakan povclear().


Fungsi pov3d memiliki semangat yang sama dengan plot3d. Fungsi ini
dapat menghasilkan grafik dari sebuah fungsi f(x,y), atau sebuah
permukaan dengan koordinat X,Y,Z dalam bentuk matriks, termasuk
garis-garis level yang bersifat opsional. Fungsi ini memulai raytracer
secara otomatis, dan memuat adegan ke dalam notebook Euler.


Selain pov3d(), ada banyak fungsi yang menghasilkan objek Povray.
Fungsi-fungsi ini mengembalikan string, yang berisi kode Povray untuk
objek. Untuk menggunakan fungsi-fungsi ini, mulai file Povray dengan
povstart(). Kemudian gunakan writeln(...) untuk menulis objek ke file
scene. Terakhir, akhiri file dengan povend(). Secara default,
raytracer akan dimulai, dan PNG akan dimasukkan ke dalam buku catatan
Euler.


Fungsi objek memiliki parameter yang disebut “look”, yang membutuhkan
sebuah string dengan kode povray untuk textu


\>load povray;


Pastikan direktori bin povray berada di dalam path. Jika tidak, edit
variabel berikut sehingga berisi jalur ke povray yang dapat
dieksekusi.


\>defaultpovray="C:\\Program Files\\POV-Ray\\v3.7\\bin\\pvengine.exe"


    C:\Program Files\POV-Ray\v3.7\bin\pvengine.exe

Untuk kesan pertama, kita plot sebuah fungsi sederhana. Perintah
berikut ini menghasilkan file povray di direktori pengguna Anda, dan
menjalankan Povray untuk melacak sinar pada file ini.


Jika Anda memulai perintah berikut, GUI Povray akan terbuka,
menjalankan file, dan menutup secara otomatis. Karena alasan keamanan,
Anda akan ditanya, apakah Anda ingin mengizinkan file exe dijalankan.
Anda dapat menekan cancel untuk menghentikan pertanyaan lebih lanjut.
Anda mungkin harus menekan OK pada jendela Povray untuk mengetahui
dialog awal Povray.


\>plot3d("x^2+y^2",zoom=2):


![images/Final%20Project%20Aplikom%20Semester%203-296.png](images/Final%20Project%20Aplikom%20Semester%203-296.png)

\>pov3d("x^2+y^2",zoom=3);


![images/Final%20Project%20Aplikom%20Semester%203-297.png](images/Final%20Project%20Aplikom%20Semester%203-297.png)

Kita dapat membuat fungsi menjadi transparan dan menambahkan hasil
akhir lainnya. Kita juga dapat menambahkan garis level ke plot fungsi.


\>pov3d("x^2+y^3",axiscolor=red,angle=-45°,\>anaglyph, ...  
\>     look=povlook(cyan,0.2),level=-1:0.5:1,zoom=3.8);


![images/Final%20Project%20Aplikom%20Semester%203-298.png](images/Final%20Project%20Aplikom%20Semester%203-298.png)

Kadang-kadang perlu untuk mencegah penskalaan fungsi, dan menskalakan
fungsi dengan tangan


Kami memplot kumpulan titik pada bidang kompleks, di mana hasil kali
jarak ke 1 dan -1 sama dengan 1.


\>pov3d("((x-1)^2+y^2)\*((x+1)^2+y^2)/40",r=2, ...  
\>     angle=-120°,level=1/40,dlevel=0.005,light=[-1,1,1],height=10°,n=50, ...  
\>     <fscale,zoom=3.8);


![images/Final%20Project%20Aplikom%20Semester%203-299.png](images/Final%20Project%20Aplikom%20Semester%203-299.png)

# Merencanakan dengan Koordinat

Alih-alih menggunakan fungsi, kita dapat memplot dengan koordinat.
Seperti pada plot3d, kita membutuhkan tiga matriks untuk
mendefinisikan objek.


Pada contoh, kita memutar sebuah fungsi pada sumbu z.


\>function f(x) := x^3-x+1; ...  
\>   x=-1:0.01:1; t=linspace(0,2pi,50)'; ...  
\>   Z=x; X=cos(t)\*f(x); Y=sin(t)\*f(x); ...  
\>   pov3d(X,Y,Z,angle=40°,look=povlook(red,0.1),height=50°,axis=0,zoom=4,light=[10,5,15]);


![images/Final%20Project%20Aplikom%20Semester%203-300.png](images/Final%20Project%20Aplikom%20Semester%203-300.png)

Pada contoh berikut, kami memplot gelombang teredam. Kami menghasilkan
gelombang dengan bahasa matriks euler.Kami menunjukkan bagaimana objek
tambahan dapat ditambahkan ke adegan pov3d. Untuk pembuatan objek,
lihat contoh berikut.


Perhatikan bahwa plot3d menskalakan plot, sehingga sesuai dengan kubus
satuan. 


\>r=linspace(0,1,80); phi=linspace(0,2pi,80)'; ...  
\>   x=r\*cos(phi); y=r\*sin(phi); z=exp(-5\*r)\*cos(8\*pi\*r)/3;  ...  
\>   pov3d(x,y,z,zoom=6,axis=0,height=30°,add=povsphere([0.5,0,0.25],0.15,povlook(red)), ...  
\>     w=500,h=300);


![images/Final%20Project%20Aplikom%20Semester%203-301.png](images/Final%20Project%20Aplikom%20Semester%203-301.png)

Dengan metode bayangan canggih Povray, hanya sedikit titik yang bisa
menghasilkan permukaan yang sangat halus. Hanya pada batas-batas dan
bayangan, trik ini bisa terlihat jelas.


Untuk itu, kita perlu menambahkan vektor normal di setiap titik
matriks.


\>Z &= x^2\*y^3


    
                                     2  3
                                    x  y
    

Persamaan permukaannya adalah [x,y,Z]. Kita menghitung dua turunan
terhadap x dan y dari persamaan ini dan mengambil hasil perkalian
silang sebagai normal.


\>dx &= diff([x,y,Z],x); dy &= diff([x,y,Z],y);


Kami mendefinisikan normal sebagai hasil kali silang dari turunan ini,
dan mendefinisikan fungsi koordinat.


\>N &= crossproduct(dx,dy); NX &= N[1]; NY &= N[2]; NZ &= N[3]; N,


    
                                   3       2  2
                           [- 2 x y , - 3 x  y , 1]
    

Kami hanya menggunakan 25 poin.


\>x=-1:0.5:1; y=x';

\>pov3d(x,y,Z(x,y),angle=10°, ...  
\>     xv=NX(x,y),yv=NY(x,y),zv=NZ(x,y),<shadow);


![images/Final%20Project%20Aplikom%20Semester%203-302.png](images/Final%20Project%20Aplikom%20Semester%203-302.png)

Berikut ini adalah simpul Trefoil yang dibuat oleh A. Busser di
Povray. Ada versi yang lebih baik dari ini dalam contoh.


Lihat: Contoh\ Simpul Trefoil | Simpul Trefoil


Untuk tampilan yang bagus dengan tidak terlalu banyak titik, kita
tambahkan vektor normal di sini. Kita menggunakan Maxima untuk
menghitung vektor normal untuk kita. Pertama, tiga fungsi untuk
koordinat sebagai ekspresi simbolik.


\>X &= ((4+sin(3\*y))+cos(x))\*cos(2\*y); ...  
\>   Y &= ((4+sin(3\*y))+cos(x))\*sin(2\*y); ...  
\>   Z &= sin(x)+2\*cos(3\*y);


Kemudian dua vektor turunan terhadap x dan y.


\>dx &= diff([X,Y,Z],x); dy &= diff([X,Y,Z],y);


Sekarang yang normal, yang merupakan produk silang dari dua turunan.


\>dn &= crossproduct(dx,dy);


Kami sekarang mengevaluasi semua ini secara numerik.


\>x:=linspace(-%pi,%pi,40); y:=linspace(-%pi,%pi,100)';


Vektor normal adalah evaluasi dari ekspresi simbolik dn[i] untuk
i=1,2,3. Sintaks untuk ini adalah &amp;“ekspresi”(parameter). Ini adalah
sebuah alternatif dari metode pada contoh sebelumnya, di mana kita
mendefinisikan ekspresi simbolik NX, NY, NZ terlebih dahulu.


\>pov3d(X(x,y),Y(x,y),Z(x,y),\>anaglyph,axis=0,zoom=5,w=450,h=350, ...  
\>     <shadow,look=povlook(blue), ...  
\>     xv=&"dn[1]"(x,y), yv=&"dn[2]"(x,y), zv=&"dn[3]"(x,y));


![images/Final%20Project%20Aplikom%20Semester%203-303.png](images/Final%20Project%20Aplikom%20Semester%203-303.png)

Kami juga dapat menghasilkan kisi-kisi dalam bentuk 3D.


\>povstart(zoom=4); ...  
\>   x=-1:0.5:1; r=1-(x+1)^2/6; ...  
\>   t=(0°:30°:360°)'; y=r\*cos(t); z=r\*sin(t); ...  
\>   writeln(povgrid(x,y,z,d=0.02,dballs=0.05)); ...  
\>   povend();


![images/Final%20Project%20Aplikom%20Semester%203-304.png](images/Final%20Project%20Aplikom%20Semester%203-304.png)

Dengan povgrid(), kurva dapat dibuat.


\>povstart(center=[0,0,1],zoom=3.6); ...  
\>   t=linspace(0,2,1000); r=exp(-t); ...  
\>   x=cos(2\*pi\*10\*t)\*r; y=sin(2\*pi\*10\*t)\*r; z=t; ...  
\>   writeln(povgrid(x,y,z,povlook(red))); ...  
\>   writeAxis(0,2,axis=3); ...  
\>   povend();


![images/Final%20Project%20Aplikom%20Semester%203-305.png](images/Final%20Project%20Aplikom%20Semester%203-305.png)

# Objek Povray

Di atas, kita telah menggunakan pov3d untuk memplot permukaan.
Antarmuka povray di Euler juga dapat menghasilkan objek Povray.
Objek-objek ini disimpan sebagai string di Euler, dan perlu ditulis ke
file Povray.


Kita memulai output dengan povstart().


\>povstart(zoom=4);


Pertama, kita mendefinisikan tiga silinder, dan menyimpannya dalam
bentuk string di Euler.


Fungsi povx() dll. hanya mengembalikan vektor [1,0,0], yang dapat
digunakan sebagai gantinya


\>c1=povcylinder(-povx,povx,1,povlook(red)); ...  
\>   c2=povcylinder(-povy,povy,1,povlook(yellow)); ...  
\>   c3=povcylinder(-povz,povz,1,povlook(blue)); ...  
\>  
String berisi kode Povray, yang tidak perlu kita pahami pada saat itu.


\>c2


    cylinder { &lt;0,0,-1&gt;, &lt;0,0,1&gt;, 1
     texture { pigment { color rgb &lt;0.941176,0.941176,0.392157&gt; }  } 
     finish { ambient 0.2 } 
     }

Seperti yang Anda lihat, kita menambahkan tekstur ke objek dalam tiga
warna berbeda.


Hal itu dilakukan dengan povlook(), yang mengembalikan sebuah string
dengan kode Povray yang relevan. Kita dapat menggunakan warna default
Euler, atau mendefinisikan warna kita sendiri. Kita juga dapat
menambahkan transparansi, atau mengubah cahaya sekitar.


\>povlook(rgb(0.1,0.2,0.3),0.1,0.5)


     texture { pigment { color rgbf &lt;0.101961,0.2,0.301961,0.1&gt; }  } 
     finish { ambient 0.5 } 
    



Sekarang kita mendefinisikan objek perpotongan, dan menulis hasilnya
ke file.


\>writeln(povintersection([c1,c2,c3]));


Perpotongan tiga silinder sulit untuk divisualisasikan, jika Anda
belum pernah melihatnya.


\>povend;


![images/Final%20Project%20Aplikom%20Semester%203-306.png](images/Final%20Project%20Aplikom%20Semester%203-306.png)

Fungsi-fungsi berikut ini menghasilkan fraktal secara rekursif.


Fungsi pertama menunjukkan, bagaimana Euler menangani objek Povray
sederhana. Fungsi povbox() mengembalikan sebuah string, yang berisi
koordinat kotak, tekstur dan hasil akhir.


\>function onebox(x,y,z,d) := povbox([x,y,z],[x+d,y+d,z+d],povlook());

\>function fractal (x,y,z,h,n) ...  
\>  
<pre class="udf">     if n==1 then writeln(onebox(x,y,z,h));
     else
       h=h/3;
       fractal(x,y,z,h,n-1);
       fractal(x+2*h,y,z,h,n-1);
       fractal(x,y+2*h,z,h,n-1);
       fractal(x,y,z+2*h,h,n-1);
       fractal(x+2*h,y+2*h,z,h,n-1);
       fractal(x+2*h,y,z+2*h,h,n-1);
       fractal(x,y+2*h,z+2*h,h,n-1);
       fractal(x+2*h,y+2*h,z+2*h,h,n-1);
       fractal(x+h,y+h,z+h,h,n-1);
     endif;
    endfunction
</pre>
\>povstart(fade=10,<shadow);

\>fractal(-1,-1,-1,2,4);

\>povend();


![images/Final%20Project%20Aplikom%20Semester%203-307.png](images/Final%20Project%20Aplikom%20Semester%203-307.png)

Perbedaan memungkinkan pemotongan satu objek dari objek lainnya.
Seperti persimpangan, ada bagian dari objek CSG Povray.


\>povstart(light=[5,-5,5],fade=10);


Untuk demonstrasi ini, kita akan mendefinisikan sebuah objek di
Povray, alih-alih menggunakan sebuah string di Euler. Definisi akan
langsung dituliskan ke file.


Koordinat kotak -1 berarti [-1,-1,-1].


\>povdefine("mycube",povbox(-1,1));


Kita dapat menggunakan objek ini dalam povobject(), yang mengembalikan
sebuah string seperti biasa.


\>c1=povobject("mycube",povlook(red));


Kami menghasilkan kubus kedua, dan memutar serta menskalakannya
sedikit.


\>c2=povobject("mycube",povlook(yellow),translate=[1,1,1], ...  
\>     rotate=xrotate(10°)+yrotate(10°), scale=1.2);


Kemudian kita ambil selisih dari kedua objek tersebut.


\>writeln(povdifference(c1,c2));


Sekarang tambahkan tiga sumbu.


\>writeAxis(-1.2,1.2,axis=1); ...  
\>   writeAxis(-1.2,1.2,axis=2); ...  
\>   writeAxis(-1.2,1.2,axis=4); ...  
\>   povend();


![images/Final%20Project%20Aplikom%20Semester%203-308.png](images/Final%20Project%20Aplikom%20Semester%203-308.png)

# Fungsi Implisit

Povray dapat memplot himpunan di mana f(x,y,z)=0, seperti parameter
implisit pada plot3d. Namun, hasilnya terlihat jauh lebih baik.


Sintaks untuk fungsi-fungsi tersebut sedikit berbeda. Anda tidak dapat
menggunakan output dari ekspresi Maxima atau Euler.


\>povstart(angle=70°,height=50°,zoom=4);

\>c=0.1; d=0.1; ...  
\>   writeln(povsurface("(pow(pow(x,2)+pow(y,2)-pow(c,2),2)+pow(pow(z,2)-1,2))\*(pow(pow(y,2)+pow(z,2)-pow(c,2),2)+pow(pow(x,2)-1,2))\*(pow(pow(z,2)+pow(x,2)-pow(c,2),2)+pow(pow(y,2)-1,2))-d",povlook(red))); ...  
\>   povend();


    Error : Povray error!
    
    Error generated by error() command
    
    povray:
        error("Povray error!");
    Try "trace errors" to inspect local variables after errors.
    povend:
        povray(file,w,h,aspect,exit); 

\>povstart(angle=25°,height=10°); 

\>writeln(povsurface("pow(x,2)+pow(y,2)\*pow(z,2)-1",povlook(blue),povbox(-2,2,"")));

\>povend();


![images/Final%20Project%20Aplikom%20Semester%203-309.png](images/Final%20Project%20Aplikom%20Semester%203-309.png)

\>povstart(angle=70°,height=50°,zoom=4);


Membuat permukaan implisit. Perhatikan sintaks yang berbeda dalam
ekspresi.


\>writeln(povsurface("pow(x,2)\*y-pow(y,3)-pow(z,2)",povlook(green))); ...  
\>   writeAxes(); ...  
\>   povend();


![images/Final%20Project%20Aplikom%20Semester%203-310.png](images/Final%20Project%20Aplikom%20Semester%203-310.png)

# Objek Jaring

Pada contoh ini, kami menunjukkan cara membuat objek mesh, dan
menggambarnya dengan informasi tambahan.


Kami ingin memaksimalkan xy di bawah kondisi x+y = 1 dan
mendemonstrasikan sentuhan tangensial dari garis level.


\>povstart(angle=-10°,center=[0.5,0.5,0.5],zoom=7);


Kita tidak dapat menyimpan objek dalam sebuah string seperti
sebelumnya, karena ukurannya terlalu besar. Jadi kita mendefinisikan
objek dalam file Povray menggunakan #declare. Fungsi povtriangle()
melakukan hal ini secara otomatis. Fungsi ini dapat menerima vektor
normal seperti halnya pov3d().


Berikut ini mendefinisikan objek mesh, dan menuliskannya langsung ke
dalam file.


\>x=0:0.02:1; y=x'; z=x\*y; vx=-y; vy=-x; vz=1;

\>mesh=povtriangles(x,y,z,"",vx,vy,vz);


Sekarang kita tentukan dua cakram, yang akan berpotongan dengan
permukaan.


\>cl=povdisc([0.5,0.5,0],[1,1,0],2); ...  
\>   ll=povdisc([0,0,1/4],[0,0,1],2);


Tuliskan permukaan dikurangi kedua cakram.


\>writeln(povdifference(mesh,povunion([cl,ll]),povlook(green)));


Tuliskan kedua perpotongan tersebut.


\>writeln(povintersection([mesh,cl],povlook(red))); ...  
\>   writeln(povintersection([mesh,ll],povlook(gray)));


Tuliskan titik maximum.


\>writeln(povpoint([1/2,1/2,1/4],povlook(gray),size=2\*defaultpointsize));


Tambahkan sumbu dan selesaikan.


\>writeAxes(0,1,0,1,0,1,d=0.015); ...  
\>   povend();


![images/Final%20Project%20Aplikom%20Semester%203-311.png](images/Final%20Project%20Aplikom%20Semester%203-311.png)

# Anaglyph dalam Povray

Untuk menghasilkan anaglyph untuk kacamata merah/cyan, Povray harus
dijalankan dua kali dari posisi kamera yang berbeda. Ini menghasilkan
dua file Povray dan dua file PNG, yang dimuat dengan fungsi
loadanaglyph().


Tentu saja, Anda membutuhkan kacamata merah/cyan untuk melihat contoh
berikut dengan benar.


Fungsi pov3d() memiliki sebuah tombol sederhana untuk menghasilkan
anaglyph.


\>pov3d("-exp(-x^2-y^2)/2",r=2,height=45°,\>anaglyph, ...  
\>     center=[0,0,0.5],zoom=3.5);


![images/Final%20Project%20Aplikom%20Semester%203-312.png](images/Final%20Project%20Aplikom%20Semester%203-312.png)

Fungsi povanaglyph() melakukan semua ini. Parameter-parameternya
seperti pada povstart() dan povend() yang digabungkan.


\>function myscene ...


      s=povsphere(povc,1);
      cl=povcylinder(-povz,povz,0.5);
      clx=povobject(cl,rotate=xrotate(90°));
      cly=povobject(cl,rotate=yrotate(90°));
      c=povbox([-1,-1,0],1);
      un=povunion([cl,clx,cly,c]);
      obj=povdifference(s,un,povlook(red));
      writeln(obj);
      writeAxes();
    endfunction
</pre>
Fungsi povanaglyph() melakukan semua ini. Parameter-parameternya
seperti pada povstart() dan povend() yang digabungkan.


\>povanaglyph("myscene",zoom=4.5);


![images/Final%20Project%20Aplikom%20Semester%203-313.png](images/Final%20Project%20Aplikom%20Semester%203-313.png)

# Mendefinisikan Objek sendiri

Antarmuka povray Euler berisi banyak objek. Namun Anda tidak dibatasi
pada objek-objek tersebut. Anda dapat membuat objek sendiri, yang
menggabungkan objek-objek lain, atau objek yang benar-benar baru.


Kami mendemonstrasikan sebuah torus. Perintah Povray untuk ini adalah
“torus”. Jadi kita mengembalikan sebuah string dengan perintah ini dan
parameternya. Perhatikan bahwa torus selalu berpusat pada titik asal.


\>function povdonat (r1,r2,look="") ...


      return "torus {"+r1+","+r2+look+"}";
    endfunction
</pre>
Inilah torus pertama kami.


\>t1=povdonat(0.8,0.2)


    torus {0.8,0.2}

Mari kita gunakan objek ini untuk membuat torus kedua, ditranslasikan
dan diputar.


\>t2=povobject(t1,rotate=xrotate(90°),translate=[0.8,0,0])


    object { torus {0.8,0.2}
     rotate 90 *x 
     translate &lt;0.8,0,0&gt;
     }

memanggil program Povray. Namun, jika terjadi kesalahan, program ini
tidak menampilkan kesalahan. Oleh karena itu, Anda harus menggunakan


Sekarang, kita tempatkan semua benda ini ke dalam suatu pemandangan.
Untuk tampilannya, kita menggunakan Phong Shading.


\>povstart(center=[0.4,0,0],angle=0°,zoom=3.8,aspect=1.5); ...  
\>   writeln(povobject(t1,povlook(green,phong=1))); ...  
\>   writeln(povobject(t2,povlook(green,phong=1))); ...  
\>  
 &gt;povend();  

memanggil program Povray. Namun, jika terjadi kesalahan, program ini
tidak menampilkan kesalahan. Oleh karena itu, Anda harus menggunakan


 &gt;povend(&lt;exit);  

jika ada yang tidak berhasil. Ini akan membiarkan jendela Povray
terbuka.


\>povend(h=320,w=480);


![images/Final%20Project%20Aplikom%20Semester%203-314.png](images/Final%20Project%20Aplikom%20Semester%203-314.png)

Berikut adalah contoh yang lebih rumit. Kami menyelesaikan


dan menunjukkan titik-titik yang layak dan optimal dalam plot 3D.


\>A=[10,8,4;5,6,8;6,3,2;9,5,6];

\>b=[10,10,10,10]';

\>c=[1,1,1];


Pertama, mari kita periksa, apakah contoh ini memiliki solusi atau
tidak.


\>x=simplex(A,b,c,\>max,\>check)'


    [0,  1,  0.5]

Ya, sudah.


Selanjutnya kita mendefinisikan dua objek. Yang pertama adalah pesawat


\>function oneplane (a,b,look="") ...


      return povplane(a,b,look)
    endfunction
</pre>
Kemudian kita tentukan perpotongan semua setengah ruang dan kubus.


\>function adm (A, b, r, look="") ...


      ol=[]
      loop 1 to rows(A); ol=ol|oneplane(A[#],b[#]); end;
      ol=ol|povbox([0,0,0],[r,r,r]);
      return povintersection(ol,look);
    endfunction
</pre>
Sekarang, kita bisa merencanakan adegan tersebut.


\>povstart(angle=120°,center=[0.5,0.5,0.5],zoom=3.5); ...  
\>   writeln(adm(A,b,2,povlook(green,0.4))); ...  
\>   writeAxes(0,1.3,0,1.6,0,1.5); ...  
\>  
Berikut ini adalah lingkaran di sekeliling optimal.


\>writeln(povintersection([povsphere(x,0.5),povplane(c,c.x')], ...  
\>     povlook(red,0.9)));


    []

Dan kesalahan pada arah yang optimal.


\>writeln(povarrow(x,c\*0.5,povlook(red)));


Kami menambahkan teks ke layar. Teks hanyalah sebuah objek 3D. Kita
perlu menempatkan dan memutarnya sesuai dengan pandangan kita.


\>writeln(povtext("Linear Problem",[0,0.2,1.3],size=0.05,rotate=5°)); ...  
\>   povend();


![images/Final%20Project%20Aplikom%20Semester%203-315.png](images/Final%20Project%20Aplikom%20Semester%203-315.png)

# More Examples

You can find some more examples for Povray in Euler in the following
files.


  <a href="Examples/Dandelin Spheres.html">Examples/Dandelin Spheres</a>  

  <a href="Examples/Donat Math.html">Examples/Donat Math</a>  

  <a href="Examples/Trefoil Knot.html">Examples/Trefoil Knot</a>  

  <a href="Examples/Optimization by Affine Scaling.html">Examples/Optimization by Affine Scaling</a>  

# Soal-Soal dan Pembahasan

1. buatkan gambar plot 3D dari persamaan 


\>aspect(1.5); plot3d("3\*x^2+4\*y+20",-5,5,0,r=pi):


![images/Final%20Project%20Aplikom%20Semester%203-316.png](images/Final%20Project%20Aplikom%20Semester%203-316.png)

2. Buatlah plot 3D dari persamaan




dengan rotate 2 dan grid 6


\>plot3d("3x^2+4y+20",a=-1,b=1,rotate=2,grid=6):


    Matrix 61x61 and 51x61 not compatible in size!
    Try "trace errors" to inspect local variables after errors.
    plot3d:
        n=size(xx,yy,zz)-1;

3. Buatlah Grafik fungsi kuadrat dua variabel dengan persamaan 


\>function f(x,y) := 2\*x^2+4\*x\*y+2\*y^2

\>plot3d("f"):


![images/Final%20Project%20Aplikom%20Semester%203-317.png](images/Final%20Project%20Aplikom%20Semester%203-317.png)

4. Buatlah plot 3D dari fungsi Implisit berikut


\>plot3d("3\*x^3+3\*y^3+3\*y\*z-3",r=1,implicit=1)

\>insimg


![images/Final%20Project%20Aplikom%20Semester%203-318.png](images/Final%20Project%20Aplikom%20Semester%203-318.png)

5. Buatlah grafik fungsi akar kuadrat dua variabel berikut ini


\>function g(x,y) &= sqrt(5\*x^2+y^2);

\>plot3d("g"):


![images/Final%20Project%20Aplikom%20Semester%203-319.png](images/Final%20Project%20Aplikom%20Semester%203-319.png)

# Kalkulus dengan EMT

Materi Kalkulus mencakup di antaranya:


* 
Fungsi (fungsi aljabar, trigonometri, eksponensial, logaritma, komposisi fungsi)

* 
Limit Fungsi,

* 
Turunan Fungsi,

* 
Integral Tak Tentu,

* 
Integral Tentu dan Aplikasinya,

* 
Barisan dan Deret (kekonvergenan barisan dan deret).


EMT (bersama Maxima) dapat digunakan untuk melakukan semua perhitungan di dalam kalkulus, baik secara numerik maupun analitik
(eksak).


## Mendefinisikan Fungsi

Terdapat beberapa cara mendefinisikan fungsi pada EMT, yakni:


* 
Menggunakan format nama_fungsi := rumus fungsi (untuk fungsi numerik),

* 
Menggunakan format nama_fungsi &amp;= rumus fungsi (untuk fungsi simbolik, namun dapat dihitung secara numerik),

* 
Menggunakan format nama_fungsi &amp;&amp;= rumus fungsi (untuk fungsi simbolik murni, tidak dapat dihitung langsung),

* 
Fungsi sebagai program EMT.


Setiap format harus diawali dengan perintah function (bukan sebagai ekspresi).


Berikut adalah adalah beberapa contoh cara mendefinisikan fungsi:


\>function f(x) := 2\*x^2+exp(sin(x)) // fungsi numerik

\>f(0), f(1), f(pi)


    1
    4.31977682472
    20.7392088022

\>f(a) // tidak dapat dihitung nilainya


    Variable or function a not found.
    Error in:
    f(a) // tidak dapat dihitung nilainya ...
       ^

Silakan Anda plot kurva fungsi di atas!


Berikutnya kita definisikan fungsi:


\>function g(x) := sqrt(x^2-3\*x)/(x+1)

\>g(3)


    0

\>g(0)


    0

\>g(1) // kompleks, tidak dapat dihitung oleh fungsi numerik


    Floating point error!
    Error in sqrt
    Try "trace errors" to inspect local variables after errors.
    g:
        useglobal; return sqrt(x^2-3*x)/(x+1) 
    Error in:
    g(1) // kompleks, tidak dapat dihitung oleh fungsi numerik ...
        ^

Silakan Anda plot kurva fungsi di atas!


\>f(g(5)) // komposisi fungsi


    2.20920171961

\>g(f(5))


    0.950898070639

\>function h(x) := f(g(x)) // definisi komposisi fungsi 

\>h(5) // sama dengan f(g(5))


    2.20920171961

Silakan Anda plot kurva fungsi komposisi fungsi f dan g:


dan


bersama-sama kurva fungsi f dan g dalam satu bidang koordinat.


\>f(0:10) // nilai-nilai f(0), f(1), f(2), ..., f(10)


    [1,  4.31978,  10.4826,  19.1516,  32.4692,  50.3833,  72.7562,
    99.929,  130.69,  163.51,  200.58]

\>fmap(0:10) // sama dengan f(0:10), berlaku untuk semua fungsi


    [1,  4.31978,  10.4826,  19.1516,  32.4692,  50.3833,  72.7562,
    99.929,  130.69,  163.51,  200.58]

\>gmap(200:210)


    [0.987534,  0.987596,  0.987657,  0.987718,  0.987778,  0.987837,
    0.987896,  0.987954,  0.988012,  0.988069,  0.988126]

Misalkan kita akan mendefinisikan fungsi


Fungsi tersebut tidak dapat didefinisikan sebagai fungsi numerik secara "inline" menggunakan
format :=, melainkan didefinisikan sebagai program. Perhatikan, kata "map" digunakan agar fungsi
dapat menerima vektor sebagai input, dan hasilnya berupa vektor. Jika tanpa kata "map" fungsinya
hanya dapat menerima input satu nilai.


\>function map f(x) ...


      if x>0 then return x^3
      else return x^2
      endif;
    endfunction
</pre>
\>f(1)


    1

\>f(-2)


    4

\>f(-5:5)


    [25,  16,  9,  4,  1,  0,  1,  8,  27,  64,  125]

\>aspect(1.5); plot2d("f(x)",-5,5):

\>function f(x) &= 2\*E^x // fungsi simbolik


    
                                        x
                                     2 E
    

\>$f(a) // nilai fungsi secara simbolik

\>f(E) // nilai fungsi berupa bilangan desimal


    30.308524483

\>$f(E), $float(%)

\>function g(x) &= 3\*x+1


    
                                   3 x + 1
    

\>function h(x) &= f(g(x)) // komposisi fungsi


    
                                     3 x + 1
                                  2 E
    

\>plot2d("h(x)",-1,1):


# Latihan

Bukalah buku Kalkulus. Cari dan pilih beberapa (paling sedikit 5 fungsi berbeda
tipe/bentuk/jenis) fungsi dari buku tersebut, kemudian definisikan fungsi-fungsi tersebut dan
komposisinya di EMT pada baris-baris perintah berikut (jika perlu tambahkan lagi). Untuk setiap
fungsi, hitung beberapa nilainya, baik untuk satu nilai maupun vektor. Gambar grafik
fungsi-fungsi tersebut dan komposisi-komposisi 2 fungsi.


Juga, carilah fungsi beberapa (dua) variabel. Lakukan hal sama seperti di atas.


\>function f(x):= 4\*x^2+exp(cos(x))

\>f(0)


    2.71828182846

\>function g(x):= 2\*x^4+exp(sin(x))

\>g(5)


    1250.383305

\>g(f(2))


    154059.255023

\>function f(x) &= 4\*E^x


    
                                        x
                                     4 E
    

\>function g(x) &= 2\*x+2


    
                                   2 x + 2
    

\>function h(x) &= f(g(x))


    
                                     2 x + 2
                                  4 E
    

# Menghitung Limit

Perhitungan limit pada EMT dapat dilakukan dengan menggunakan fungsi Maxima, yakni "limit".
Fungsi "limit" dapat digunakan untuk menghitung limit fungsi dalam bentuk ekspresi maupun fungsi
yang sudah didefinisikan sebelumnya. Nilai limit dapat dihitung pada sebarang nilai atau pada tak
hingga (-inf, minf, dan inf). Limit kiri dan limit kanan juga dapat dihitung, dengan cara memberi
opsi "plus" atau "minus". Hasil limit dapat berupa nilai, "und" (tak definisi), "ind" (tak tentu
namun terbatas), "infinity" (kompleks tak hingga).


Perhatikan beberapa contoh berikut. Perhatikan cara menampilkan perhitungan secara lengkap, tidak
hanya menampilkan hasilnya saja.


\>$showev('limit(sqrt(x^2-3\*x)/(x+1),x,inf))

\>$limit((x^3-13\*x^2+51\*x-63)/(x^3-4\*x^2-3\*x+18),x,3)


maxima: 'limit((x^3-13*x^2+51*x-63)/(x^3-4*x^2-3*x+18),x,3)=limit((x^3-13*x^2+51*x-63)/(x^3-4*x^2-3*x+18),x,3)


Fungsi tersebut diskontinu di titik x=3. Berikut adalah grafik fungsinya.


\>aspect(1.5); plot2d("(x^3-13\*x^2+51\*x-63)/(x^3-4\*x^2-3\*x+18)",0,4); plot2d(3,-4/5,\>points,style="ow",\>add):

\>$limit(2\*x\*sin(x)/(1-cos(x)),x,0)


maxima: 'limit(2*x*sin(x)/(1-cos(x)),x,0)=limit(2*x*sin(x)/(1-cos(x)),x,0)


Fungsi tersebut diskontinu di titik x=0. Berikut adalah grafik fungsinya.


\>plot2d("2\*x\*sin(x)/(1-cos(x))",-pi,pi); plot2d(0,4,\>points,style="ow",\>add):

\>$limit(cot(7\*h)/cot(5\*h),h,0)


maxima: showev('limit(cot(7*h)/cot(5*h),h,0))


Fungsi tersebut juga diskontinu (karena tidak terdefinisi) di x=0. Berikut adalah grafiknya.


\>plot2d("cot(7\*x)/cot(5\*x)",-0.001,0.001); plot2d(0,5/7,\>points,style="ow",\>add):

\>$showev('limit(((x/8)^(1/3)-1)/(x-8),x,8))


Tunjukkan limit tersebut dengan grafik, seperti contoh-contoh sebelumnya.


\>$showev('limit(1/(2\*x-1),x,0))


Tunjukkan limit tersebut dengan grafik, seperti contoh-contoh sebelumnya.


\>$showev('limit((x^2-3\*x-10)/(x-5),x,5))


Tunjukkan limit tersebut dengan grafik, seperti contoh-contoh sebelumnya.


\>$showev('limit(sqrt(x^2+x)-x,x,inf))


Tunjukkan limit tersebut dengan grafik, seperti contoh-contoh sebelumnya.


\>$showev('limit(abs(x-1)/(x-1),x,1,minus))


Hitung limit di atas untuk x menuju 1 dari kanan.


Tunjukkan limit tersebut dengan grafik, seperti contoh-contoh sebelumnya.


\>$showev('limit(sin(x)/x,x,0))

\>plot2d("sin(x)/x",-pi,pi); plot2d(0,1,\>points,style="ow",\>add):

\>$showev('limit(sin(x^3)/x,x,0))


Tunjukkan limit tersebut dengan grafik, seperti contoh-contoh sebelumnya.


\>$showev('limit(log(x), x, minf))

\>$showev('limit((-2)^x,x, inf))

\>$showev('limit(t-sqrt(2-t),t,2,minus))

\>$showev('limit(t-sqrt(2-t),t,2,plus))

\>$showev('limit(t-sqrt(2-t),t,5,plus)) // Perhatikan hasilnya

\>plot2d("x-sqrt(2-x)",0,2):

\>$showev('limit((x^2-9)/(2\*x^2-5\*x-3),x,3))


Tunjukkan limit tersebut dengan grafik, seperti contoh-contoh sebelumnya.


\>$showev('limit((1-cos(x))/x,x,0))


Tunjukkan limit tersebut dengan grafik, seperti contoh-contoh sebelumnya.


\>$showev('limit((x^2+abs(x))/(x^2-abs(x)),x,0))


Tunjukkan limit tersebut dengan grafik, seperti contoh-contoh sebelumnya.


\>$showev('limit((1+1/x)^x,x,inf))

\>plot2d("(1+1/x)^x",0,1000):

\>$showev('limit((1+k/x)^x,x,inf))

\>$showev('limit((1+x)^(1/x),x,0))


Tunjukkan limit tersebut dengan grafik, seperti contoh-contoh sebelumnya.


\>$showev('limit((x/(x+k))^x,x,inf))

\>$showev('limit((E^x-E^2)/(x-2),x,2))


Tunjukkan limit tersebut dengan grafik, seperti contoh-contoh sebelumnya.


\>$showev('limit(sin(1/x),x,0))

\>$showev('limit(sin(1/x),x,inf))

\>plot2d("sin(1/x)",-0.001,0.001):


# Latihan

Bukalah buku Kalkulus. Cari dan pilih beberapa (paling sedikit 5 fungsi berbeda
tipe/bentuk/jenis) fungsi dari buku tersebut, kemudian definisikan di EMT pada
baris-baris perintah berikut (jika perlu tambahkan lagi). Untuk setiap fungsi, hitung
nilai limit fungsi tersebut di beberapa nilai dan di tak hingga. Gambar grafik fungsi
tersebut untuk mengkonfirmasi nilai-nilai limit tersebut.


\>$limit((2\*x-4\*x^2),x,-1)

\>aspect(1.5); plot2d("(2\*x-4\*x^2)",0,4)

\>insimg

\>$limit((2\*x^2+x/sin(x)),x,0)

\>plot2d("(2\*x^2+x/sin(x))",-pi,pi)

\>insimg

\>$limit((x^3-13\*x^2+51\*x-63)/(x^3-4\*x^2-3\*x+18),x,3)

\>plot2d("x^3-13\*x^2+51\*x-63",-pi,pi); plot2d(0,1,\>points,style="ow",\>add):


\>$showev('limit(1/(2\*x-1),x,0))

\>plot2d("1/(2\*x-1)",-pi,pi); plot2d(0,1,\>points,style="ow",\>add):

\>$showev('limit((4\*x+7)/(x-1),x,inf))

\>plot2d("(4\*x+7)/(x-1)",-pi,pi); plot2d(0,1,\>points,style="ow",\>add):


# Turunan Fungsi

Definisi turunan:


Berikut adalah contoh-contoh menentukan turunan fungsi dengan menggunakan definisi turunan
(limit).


\>$showev('limit(((x+h)^2-x^2)/h,h,0)) // turunan x^2

\>p &= expand((x+h)^2-x^2)|simplify; $p //pembilang dijabarkan dan disederhanakan

\>q &=ratsimp(p/h); $q // ekspresi yang akan dihitung limitnya disederhanakan

\>$limit(q,h,0) // nilai limit sebagai turunan

\>$showev('limit(((x+h)^n-x^n)/h,h,0)) // turunan x^n


Mengapa hasilnya seperti itu? Tuliskan atau tunjukkan bahwa hasil limit tersebut
benar, sehingga benar turunan fungsinya benar.  Tulis penjelasan Anda di komentar
ini.


Sebagai petunjuk, ekspansikan (x+h)^n dengan menggunakan teorema binomial.


\>$showev('limit((sin(x+h)-sin(x))/h,h,0)) // turunan sin(x)


Mengapa hasilnya seperti itu? Tuliskan atau tunjukkan bahwa hasil limit tersebut


benar, sehingga benar turunan fungsinya benar.  Tulis penjelasan Anda di komentar
ini.


Sebagai petunjuk, ekspansikan sin(x+h) dengan menggunakan rumus jumlah dua sudut.


\>$showev('limit((log(x+h)-log(x))/h,h,0)) // turunan log(x)


Mengapa hasilnya seperti itu? Tuliskan atau tunjukkan bahwa hasil limit tersebut


benar, sehingga benar turunan fungsinya benar.  Tulis penjelasan Anda di komentar
ini.


Sebagai petunjuk, gunakan sifat-sifat logaritma dan hasil limit pada bagian
sebelumnya di atas.


\>$showev('limit((1/(x+h)-1/x)/h,h,0)) // turunan 1/x

\>$showev('limit((E^(x+h)-E^x)/h,h,0)) // turunan f(x)=e^x


    Answering "Is x an integer?" with "integer"
    Answering "Is x an integer?" with "integer"
    Answering "Is x an integer?" with "integer"
    Answering "Is x an integer?" with "integer"
    Answering "Is x an integer?" with "integer"
    Maxima is asking
    Acceptable answers are: yes, y, Y, no, n, N, unknown, uk
    Is x an integer?
    
    Use assume!
    Error in:
                                         ^

Maxima bermasalah dengan limit:


Oleh karena itu diperlukan trik khusus agar hasilnya benar.


\>$showev('limit((E^h-1)/h,h,0))

\>$showev('factor(E^(x+h)-E^x))

\>$showev('limit(factor((E^(x+h)-E^x)/h),h,0)) // turunan f(x)=e^x

\>function f(x) &= x^x


    
                                       x
                                      x
    

\>$showev('limit(f(x),x,0))


Silakan Anda gambar kurva


\>$showev('limit((f(x+h)-f(x))/h,h,0)) // turunan f(x)=x^x


Di sini Maxima juga bermasalah terkait limit:


Dalam hal ini diperlukan asumsi nilai x.


\>&assume(x\>0); $showev('limit((f(x+h)-f(x))/h,h,0)) // turunan f(x)=x^x


Mengapa hasilnya seperti itu? Tuliskan atau tunjukkan bahwa hasil limit tersebut benar, sehingga benar turunan fungsinya benar.
Tulis penjelasan Anda di komentar ini.


\>&forget(x\>0) // jangan lupa, lupakan asumsi untuk kembali ke semula


    
                                   [x &gt; 0]
    

\>&forget(x<0)


    
                                   [x &lt; 0]
    

\>&facts()


    
                                      []
    

\>$showev('limit((asin(x+h)-asin(x))/h,h,0)) // turunan arcsin(x)


Mengapa hasilnya seperti itu? Tuliskan atau tunjukkan bahwa hasil limit tersebut benar, sehingga
benar turunan fungsinya benar. Tulis penjelasan Anda di komentar ini.


\>$showev('limit((tan(x+h)-tan(x))/h,h,0)) // turunan tan(x)


Mengapa hasilnya seperti itu? Tuliskan atau tunjukkan bahwa hasil limit tersebut benar, sehingga
benar turunan fungsinya benar. Tulis penjelasan Anda di komentar ini.


\>function f(x) &= sinh(x) // definisikan f(x)=sinh(x)


    
                                   sinh(x)
    

\>function df(x) &= limit((f(x+h)-f(x))/h,h,0); $df(x) // df(x) = f'(x)


Hasilnya adalah cosh(x), karena


\>plot2d(["f(x)","df(x)"],-pi,pi,color=[blue,red]):

\>function f(x) &= sin(3\*x^5+7)^2


    
                                   2    5
                                sin (3 x  + 7)
    

\>diff(f,3), diffc(f,3)


    1198.32948904
    1198.72863721

Apakah perbedaan diff dan diffc?


\>$showev('diff(f(x),x))

\>$% with x=3

\>$float(%)

\>plot2d(f,0,3.1):

\>function f(x) &=5\*cos(2\*x)-2\*x\*sin(2\*x) // mendifinisikan fungsi f


    
                          5 cos(2 x) - 2 x sin(2 x)
    

\>function df(x) &=diff(f(x),x) // fd(x) = f'(x)


    
                         - 12 sin(2 x) - 4 x cos(2 x)
    

\>$'f(1)=f(1), $float(f(1)), $'f(2)=f(2), $float(f(2)) // nilai f(1) dan f(2)

\>xp=solve("df(x)",1,2,0) // solusi f'(x)=0 pada interval [1, 2]


    1.35822987384

\>df(xp), f(xp) // cek bahwa f'(xp)=0 dan nilai ekstrim di titik tersebut


    0
    -5.67530133759

\>plot2d(["f(x)","df(x)"],0,2\*pi,color=[blue,red]): //grafik fungsi dan turunannya


Perhatikan titik-titik "puncak" grafik y=f(x) dan nilai turunan pada saat grafik fungsinya mencapai titik "puncak" tersebut.


# Latihan

Bukalah buku Kalkulus. Cari dan pilih beberapa (paling sedikit 5 fungsi berbeda tipe/bentuk/jenis) fungsi dari buku tersebut,
kemudian definisikan di EMT pada baris-baris perintah berikut (jika perlu tambahkan lagi). Untuk setiap fungsi, tentukan turunannya
dengan menggunakan definisi turunan (limit), menggunakan perintah diff, dan secara manual (langkah demi langkah yang dihitung dengan
Maxima) seperti contoh-contoh di atas. Gambar grafik fungsi asli dan fungsi turunannya pada sumbu koordinat yang sama.


\>function f(x) := x^2+3\*x

\>$showev('limit(((x+h)^2+3\*(x+h)-(x^2+3\*x))/h,h,0)) // turunan x^2+3x

\>plot2d(["f(x)","df(x)"],-pi,pi,color=[blue,red]):

\>function f(x):= x^2 

\>$showev ('limit((((x+h)^2-x^2)/h),h,0)) /// turunan x^2

\>function df(x) &= limit((((x+h)^2-x^2)/h),h,0); $df(x)// df(x)=f'(x)

\>plot2d(["f(x)","df(x)"],-pi,pi,color=[blue,red]):

\>function f(x) := x^3

\>$showev ('limit((((x+h)^3-x^3)/h),h,0))

\>function df(x) &= limit((((x+h)^3-x^3)/h),h,0); $df(x)//df(x)=f'(x)

\>plot2d(["f(x)","df(x)"],-pi,pi,color=[blue,red]):

\>function f(x) := x^2+6

\>$showev('limit(((x+h)^2+6-x^2+6)/h,h,0))

\>function df(x) &= limit((((x+h)^2+6-x^2+6)/h),h,0); $df(x)//df(x)=f'(x)

\>plot2d(["f(x)","df(x)"],-pi,pi,color=[blue,red]):


    Variable infinity not found!
    Use global or local variables defined in function df.
    df:
        useglobal; return infinity 
    Error in expression: df(x)
     %ploteval:
        y0=f$(x[1],args());
    Try "trace errors" to inspect local variables after errors.
    plot2d:
        u=u_(%ploteval(xx[#],t;args()));

# Integral

EMT dapat digunakan untuk menghitung integral, baik integral tak tentu maupun
integral tentu. Untuk integral tak tentu (simbolik) sudah tentu EMT menggunakan
Maxima, sedangkan untuk perhitungan integral tentu EMT sudah menyediakan beberapa
fungsi yang mengimplementasikan algoritma kuadratur (perhitungan integral tentu
menggunakan metode numerik).


Pada notebook ini akan ditunjukkan perhitungan integral tentu dengan menggunakan
Teorema Dasar Kalkulus:


Fungsi untuk menentukan integral adalah integrate. Fungsi ini dapat digunakan untuk
menentukan, baik integral tentu maupun tak tentu (jika fungsinya memiliki
antiderivatif). Untuk perhitungan integral tentu fungsi integrate menggunakan metode
numerik (kecuali fungsinya tidak integrabel, kita tidak akan menggunakan metode ini).


\>$showev('integrate(x^n,x))


    Answering "Is n equal to -1?" with "no"

\>$showev('integrate(1/(1+x),x))

\>$showev('integrate(1/(1+x^2),x))

\>$showev('integrate(1/sqrt(1-x^2),x))

\>$showev('integrate(sin(x),x,0,pi))

\>plot2d("sin(x)",0,2\*pi):

\>$showev('integrate(sin(x),x,a,b))

\>$showev('integrate(x^n,x,a,b))


    Answering "Is n positive, negative or zero?" with "positive"

\>$showev('integrate(x^2\*sqrt(2\*x+1),x))

\>$showev('integrate(x^2\*sqrt(2\*x+1),x,0,2))

\>$ratsimp(%)

\>$showev('integrate((sin(sqrt(x)+a)\*E^sqrt(x))/sqrt(x),x,0,pi^2))

\>$factor(%)

\>function map f(x) &= E^(-x^2)


    
                                        2
                                     - x
                                    E
    

\>$showev('integrate(f(x),x))


Fungsi f tidak memiliki antiturunan, integralnya masih memuat integral lain.


Kita tidak dapat menggunakan teorema Dasar kalkulus untuk menghitung integral tentu fungsi tersebut jika semua batasnya berhingga.
Dalam hal ini dapat digunakan metode numerik (rumus kuadratur).


Misalkan kita akan menghitung:


maxima: 'integrate(f(x),x,0,pi)


\>x=0:0.1:pi-0.1; plot2d(x,f(x+0.1),\>bar); plot2d("f(x)",0,pi,\>add):


Integral tentu


maxima: 'integrate(f(x),x,0,pi)


dapat dihampiri dengan jumlah luas persegi-persegi panjang di bawah kurva y=f(x)
tersebut. Langkah-langkahnya adalah sebagai berikut.


\>t &= makelist(a,a,0,pi-0.1,0.1); // t sebagai list untuk menyimpan nilai-nilai x

\>fx &= makelist(f(t[i]+0.1),i,1,length(t)); // simpan nilai-nilai f(x)

\>// jangan menggunakan x sebagai list, kecuali Anda pakar Maxima!


Hasilnya adalah:


maxima: 'integrate(f(x),x,0,pi) = 0.1*sum(fx[i],i,1,length(fx))


Jumlah tersebut diperoleh dari hasil kali lebar sub-subinterval (=0.1) dan jumlah nilai-nilai f(x) untuk
x = 0.1, 0.2, 0.3, ..., 3.2.


\>0.1\*sum(f(x+0.1)) // cek langsung dengan perhitungan numerik EMT


    0.836219610253

Untuk mendapatkan nilai integral tentu yang mendekati nilai sebenarnya, lebar
sub-intervalnya dapat diperkecil lagi, sehingga daerah di bawah kurva tertutup
semuanya, misalnya dapat digunakan lebar subinterval 0.001. (Silakan dicoba!)


Meskipun Maxima tidak dapat menghitung integral tentu fungsi tersebut untuk
batas-batas yang berhingga, namun integral tersebut dapat dihitung secara eksak jika
batas-batasnya tak hingga. Ini adalah salah satu keajaiban di dalam matematika, yang
terbatas tidak dapat dihitung secara eksak, namun yang tak hingga malah dapat
dihitung secara eksak.


\>$showev('integrate(f(x),x,0,inf))


Tunjukkan kebenaran hasil di atas!


Berikut adalah contoh lain fungsi yang tidak memiliki antiderivatif, sehingga integral tentunya hanya
dapat dihitung dengan metode numerik.


\>function f(x) &= x^x


    
                                       x
                                      x
    

\>$showev('integrate(f(x),x,0,1))

\>x=0:0.1:1-0.01; plot2d(x,f(x+0.01),\>bar); plot2d("f(x)",0,1,\>add):


Maxima gagal menghitung integral tentu tersebut secara langsung menggunakan perintah
integrate. Berikut kita lakukan seperti contoh sebelumnya untuk mendapat hasil atau
pendekatan nilai integral tentu tersebut.


\>t &= makelist(a,a,0,1-0.01,0.01);

\>fx &= makelist(f(t[i]+0.01),i,1,length(t));


maxima: 'integrate(f(x),x,0,1) = 0.01*sum(fx[i],i,1,length(fx))


Apakah hasil tersebut cukup baik? perhatikan gambarnya.


\>function f(x) &= sin(3\*x^5+7)^2


    
                                   2    5
                                sin (3 x  + 7)
    

\>integrate(f,0,1)


    0.542581176074

\>&showev('integrate(f(x),x,0,1))


    
             1                           1              pi
            /                      gamma(-) sin(14) sin(--)
            [     2    5                 5              10
            I  sin (3 x  + 7) dx = ------------------------
            ]                                  1/5
            /                              10 6
             0
           4/5                  1          4/5                  1
     - (((6    gamma_incomplete(-, 6 I) + 6    gamma_incomplete(-, - 6 I))
                                5                               5
                 4/5                    1
     sin(14) + (6    I gamma_incomplete(-, 6 I)
                                        5
        4/5                    1                       pi
     - 6    I gamma_incomplete(-, - 6 I)) cos(14)) sin(--) - 60)/120
                               5                       10
    

\>&float(%)


    
             1.0
            /
            [       2      5
            I    sin (3.0 x  + 7.0) dx = 
            ]
            /
             0.0
    0.09820784258795788 - 0.008333333333333333
     (0.3090169943749474 (0.1367372182078336
     (4.192962712629476 I gamma__incomplete(0.2, 6.0 I)
     - 4.192962712629476 I gamma__incomplete(0.2, - 6.0 I))
     + 0.9906073556948704 (4.192962712629476 gamma__incomplete(0.2, 6.0 I)
     + 4.192962712629476 gamma__incomplete(0.2, - 6.0 I))) - 60.0)
    

\>$showev('integrate(x\*exp(-x),x,0,1)) // Integral tentu (eksak)


# Aplikasi Integral Tentu

\>plot2d("x^3-x",-0.1,1.1); plot2d("-x^2",\>add);  ...  
\>   b=solve("x^3-x+x^2",0.5); x=linspace(0,b,200); xi=flipx(x); ...  
\>   plot2d(x|xi,x^3-x|-xi^2,\>filled,style="|",fillcolor=1,\>add): // Plot daerah antara 2 kurva

\>a=solve("x^3-x+x^2",0), b=solve("x^3-x+x^2",1) // absis titik-titik potong kedua kurva


    0
    0.61803398875

\>integrate("(-x^2)-(x^3-x)",a,b) // luas daerah yang diarsir


    0.0758191713542

Hasil tersebut akan kita bandingkan dengan perhitungan secara analitik.


\>a &= solve((-x^2)-(x^3-x),x); $a // menentukan absis titik potong kedua kurva secara eksak

\>$showev('integrate(-x^2-x^3+x,x,0,(sqrt(5)-1)/2)) // Nilai integral secara eksak

\>$float(%)


## Panjang Kurva

Hitunglah panjang kurva berikut ini dan luas daerah di dalam kurva tersebut.


dengan


\>t=linspace(0,2pi,1000); r=1+sin(3\*t)/2; x=r\*cos(t); y=r\*sin(t); ...  
\>   plot2d(x,y,\>filled,fillcolor=red,style="/",r=1.5): // Kita gambar kurvanya terlebih dahulu

\>function r(t) &= 1+sin(3\*t)/2; $'r(t)=r(t)

\>function fx(t) &= r(t)\*cos(t); $'fx(t)=fx(t)

\>function fy(t) &= r(t)\*sin(t); $'fy(t)=fy(t)

\>function ds(t) &= trigreduce(radcan(sqrt(diff(fx(t),t)^2+diff(fy(t),t)^2))); $'ds(t)=ds(t)


    Maxima said:
    diff: second argument must be a variable; found errexp1
     -- an error. To debug this try: debugmode(true);
    
    Error in:
    ... e(radcan(sqrt(diff(fx(t),t)^2+diff(fy(t),t)^2))); $'ds(t)=ds(t ...
                                                         ^

\>$integrate(ds(x),x,0,2\*pi) //panjang (keliling) kurva


Maxima gagal melakukan perhitungan eksak integral tersebut.


Berikut kita hitung integralnya secara umerik dengan perintah EMT.


\>integrate("ds(x)",0,2\*pi)


    Function ds not found.
    Try list ... to find functions!
    Error in expression: ds(x)
     %mapexpression1:
        return expr(x,args());
    Error in map.
     %evalexpression:
        if maps then return %mapexpression1(x,f$;args());
    gauss:
        if maps then y=%evalexpression(f$,a+h-(h*xn)',maps;args());
    adaptivegauss:
        t1=gauss(f$,c,c+h;args(),=maps);
    Try "trace errors" to inspect local variables after errors.
    integrate:
        return adaptivegauss(f$,a,b,eps*1000;args(),=maps);

Spiral Logaritmik


\>a=0.1; plot2d("exp(a\*x)\*cos(x)","exp(a\*x)\*sin(x)",r=2,xmin=0,xmax=2\*pi):

\>&kill(a) // hapus expresi a


    
                                     done
    

\>function fx(t) &= exp(a\*t)\*cos(t); $'fx(t)=fx(t)

\>function fy(t) &= exp(a\*t)\*sin(t); $'fy(t)=fy(t)

\>function df(t) &= trigreduce(radcan(sqrt(diff(fx(t),t)^2+diff(fy(t),t)^2))); $'df(t)=df(t)


    Maxima said:
    diff: second argument must be a variable; found errexp1
     -- an error. To debug this try: debugmode(true);
    
    Error in:
    ... e(radcan(sqrt(diff(fx(t),t)^2+diff(fy(t),t)^2))); $'df(t)=df(t ...
                                                         ^

\>S &=integrate(df(t),t,0,2\*%pi); $S // panjang kurva (spiral)


    Maxima said:
    defint: variable of integration cannot be a constant; found errexp1
     -- an error. To debug this try: debugmode(true);
    
    Error in:
    S &amp;=integrate(df(t),t,0,2*%pi); $S // panjang kurva (spiral) ...
                                  ^

\>S(a=0.1) // Panjang kurva untuk a=0.1


    Function S not found.
    Try list ... to find functions!
    Error in:
    S(a=0.1) // Panjang kurva untuk a=0.1 ...
            ^

Soal:


Tunjukkan bahwa keliling lingkaran dengan jari-jari r adalah K=2.pi.r.


Berikut adalah contoh menghitung panjang parabola.


\>plot2d("x^2",xmin=-1,xmax=1):

\>$showev('integrate(sqrt(1+diff(x^2,x)^2),x,-1,1))

\>$float(%)

\>x=-1:0.2:1; y=x^2; plot2d(x,y);  ...  
\>     plot2d(x,y,points=1,style="o#",add=1):


Panjang tersebut dapat dihampiri dengan menggunakan jumlah panjang ruas-ruas garis yang menghubungkan titik-titik pada parabola
tersebut.


\>i=1:cols(x)-1; sum(sqrt((x[i+1]-x[i])^2+(y[i+1]-y[i])^2))


    2.95191957027

Hasilnya mendekati panjang yang dihitung secara eksak. Untuk mendapatkan hampiran yang cukup akurat, jarak antar titik dapat
diperkecil, misalnya 0.1, 0.05, 0.01, dan seterusnya. Cobalah Anda ulangi perhitungannya dengan nilai-nilai tersebut.


## Koordinat Kartesius

Berikut diberikan contoh perhitungan panjang kurva menggunakan koordinat Kartesius. Kita akan hitung panjang kurva dengan
persamaan implisit:


\>z &= x^3+y^3-3\*x\*y; $z

\>plot2d(z,r=2,level=0,n=100):


Kita tertarik pada kurva di kuadran pertama.


\>plot2d(z,a=0,b=2,c=0,d=2,level=[-10;0],n=100,contourwidth=3,style="/"):


Kita selesaikan persamaannya untuk x.


\>$z with y=l\*x, sol &= solve(%,x); $sol


Kita gunakan solusi tersebut untuk mendefinisikan fungsi dengan Maxima.


\>function f(l) &= rhs(sol[1]); $'f(l)=f(l)


Fungsi tersebut juga dapat digunaka untuk menggambar kurvanya. Ingat, bahwa fungsi tersebut adalah nilai x dan nilai y=l*x, yakni
x=f(l) dan y=l*f(l).


\>plot2d(&f(x),&x\*f(x),xmin=-0.5,xmax=2,a=0,b=2,c=0,d=2,r=1.5):


Elemen panjang kurva adalah:


\>function ds(l) &= ratsimp(sqrt(diff(f(l),l)^2+diff(l\*f(l),l)^2)); $'ds(l)=ds(l)

\>$integrate(ds(l),l,0,1)


Integral tersebut tidak dapat dihitung secara eksak menggunakan Maxima. Kita hitung integral etrsebut secara numerik dengan Euler.
Karena kurva simetris, kita hitung untuk nilai variabel integrasi dari 0 sampai 1, kemudian hasilnya dikalikan 2. 


\>2\*integrate("ds(x)",0,1)


    4.91748872168

\>2\*romberg(&ds(x),0,1)// perintah Euler lain untuk menghitung nilai hampiran integral yang sama


    4.91748872168

Perhitungan di datas dapat dilakukan untuk sebarang fungsi x dan y dengan mendefinisikan fungsi EMT, misalnya kita beri nama
panjangkurva. Fungsi ini selalu memanggil Maxima untuk menurunkan fungsi yang diberikan.


\>function panjangkurva(fx,fy,a,b) ...


    ds=mxm("sqrt(diff(@fx,x)^2+diff(@fy,x)^2)");
    return romberg(ds,a,b);
    endfunction
</pre>
\>panjangkurva("x","x^2",-1,1) // cek untuk menghitung panjang kurva parabola sebelumnya


    2.95788571509

Bandingkan dengan nilai eksak di atas.


\>2\*panjangkurva(mxm("f(x)"),mxm("x\*f(x)"),0,1) // cek contoh terakhir, bandingkan hasilnya!


    4.91748872168

Kita hitung panjang spiral Archimides berikut ini dengan fungsi tersebut.


\>plot2d("x\*cos(x)","x\*sin(x)",xmin=0,xmax=2\*pi,square=1):

\>panjangkurva("x\*cos(x)","x\*sin(x)",0,2\*pi)


    21.2562941482

Berikut kita definisikan fungsi yang sama namun dengan Maxima, untuk perhitungan eksak.


\>&kill(ds,x,fx,fy)


    
                                     done
    

\>function ds(fx,fy) &&= sqrt(diff(fx,x)^2+diff(fy,x)^2)


    
                               2              2
                      sqrt(diff (fy, x) + diff (fx, x))
    

\>sol &= ds(x\*cos(x),x\*sin(x)); $sol // Kita gunakan untuk menghitung panjang kurva terakhir di atas

\>$sol | trigreduce | expand, $integrate(%,x,0,2\*pi), %()


    21.2562941482

Hasilnya sama dengan perhitungan menggunakan fungsi EMT.


Berikut adalah contoh lain penggunaan fungsi Maxima tersebut.


\>plot2d("3\*x^2-1","3\*x^3-1",xmin=-1/sqrt(3),xmax=1/sqrt(3),square=1):

\>sol &= radcan(ds(3\*x^2-1,3\*x^3-1)); $sol

\>$showev('integrate(sol,x,0,1/sqrt(3))), $2\*float(%) // panjang kurva di atas


## Sikloid

Berikut kita akan menghitung panjang kurva lintasan (sikloid) suatu titik pada lingkaran yang berputar ke kanan pada permukaan
datar. Misalkan jari-jari lingkaran tersebut adalah r. Posisi titik pusat lingkaran pada saat t adalah:


Misalkan posisi titik pada lingkaran tersebut mula-mula (0,0) dan posisinya pada saat t adalah:


Berikut kita plot lintasan tersebut dan beberapa posisi lingkaran ketika t=0, t=pi/2, t=r*pi.


\>x &= r\*(t-sin(t))


    
            [0, 1.66665833335744e-7 r, 1.33330666692022e-6 r, 
    4.499797504338432e-6 r, 1.066581336583994e-5 r, 
    2.083072932167196e-5 r, 3.599352055540239e-5 r, 
    5.71526624672386e-5 r, 8.530603082730626e-5 r, 
    1.214508019889565e-4 r, 1.665833531718508e-4 r, 
    2.216991628251896e-4 r, 2.877927110806339e-4 r, 
    3.658573803051457e-4 r, 4.568853557635201e-4 r, 
    5.618675264007778e-4 r, 6.817933857540259e-4 r, 
    8.176509330039827e-4 r, 9.704265741758145e-4 r, 
    0.001141105023499428 r, 0.001330669204938795 r, 
    0.001540100153900437 r, 0.001770376919130678 r, 
    0.002022476464811601 r, 0.002297373572865413 r, 
    0.002596040745477063 r, 0.002919448107844891 r, 
    0.003268563311168871 r, 0.003644351435886262 r, 
    0.004047774895164447 r, 0.004479793338660443 r, 0.0049413635565565 r, 
    0.005433439383882244 r, 0.005956971605131645 r, 
    0.006512907859185624 r, 0.007102192544548636 r, 
    0.007725766724910044 r, 0.00838456803503801 r, 
    0.009079530587017326 r, 0.009811584876838586 r, 0.0105816576913495 r, 
    0.01139067201557714 r, 0.01223954694042984 r, 0.01312919757078923 r, 
    0.01406053493400045 r, 0.01503446588876983 r, 0.01605189303448024 r, 
    0.01711371462093175 r, 0.01822082445851714 r, 0.01937411182884202 r, 
    0.02057446139579705 r, 0.02182275311709253 r, 0.02311986215626333 r, 
    0.02446665879515308 r, 0.02586400834688696 r, 0.02731277106934082 r, 
    0.02881380207911666 r, 0.03036795126603076 r, 0.03197606320812652 r, 
    0.0336389770872163 r, 0.03535752660496472 r, 0.03713253989951881 r, 
    0.03896483946269502 r, 0.0408552420577305 r, 0.04280455863760801 r, 
    0.04481359426396048 r, 0.04688314802656623 r, 0.04901401296344043 r, 
    0.05120697598153157 r, 0.05346281777803219 r, 0.05578231276230905 r, 
    0.05816622897846346 r, 0.06061532802852698 r, 0.0631303649963022 r, 
    0.06571208837185505 r, 0.06836123997666599 r, 0.07107855488944881 r, 
    0.07386476137264342 r, 0.07672058079958999 r, 0.07964672758239233 r, 
    0.08264390910047736 r, 0.0857128256298576 r, 0.08885417027310427 r, 
    0.09206862889003742 r, 0.09535688002914089 r, 0.0987195948597075 r, 
    0.1021574371047232 r, 0.1056710629744951 r, 0.1092611211010309 r, 
    0.1129282524731764 r, 0.1166730903725168 r, 0.1204962603100498 r, 
    0.1243983799636342 r, 0.1283800591162231 r, 0.1324418995948859 r, 
    0.1365844952106265 r, 0.140808431699002 r, 0.1451142866615502 r, 
    0.1495026295080298 r, 0.1539740213994798 r]
    

\>y &= r\*(1-cos(t))


    
            [0, 4.999958333473664e-5 r, 1.999933334222437e-4 r, 
    4.499662510124569e-4 r, 7.998933390220841e-4 r, 
    0.001249739605033717 r, 0.00179946006479581 r, 
    0.002448999746720415 r, 0.003198293697380561 r, 
    0.004047266988005727 r, 0.004995834721974179 r, 
    0.006043902043303184 r, 0.00719136414613375 r, 0.00843810628521191 r, 
    0.009784003787362772 r, 0.01122892206395776 r, 0.01277271662437307 r, 
    0.01441523309043924 r, 0.01615630721187855 r, 0.01799576488272969 r, 
    0.01993342215875837 r, 0.02196908527585173 r, 0.02410255066939448 r, 
    0.02633360499462523 r, 0.02866202514797045 r, 0.03108757828935527 r, 
    0.03361002186548678 r, 0.03622910363410947 r, 0.03894456168922911 r, 
    0.04175612448730281 r, 0.04466351087439402 r, 0.04766643011428662 r, 
    0.05076458191755917 r, 0.0539576564716131 r, 0.05724533447165381 r, 
    0.06062728715262111 r, 0.06410317632206519 r, 0.06767265439396564 r, 
    0.07133536442348987 r, 0.07509094014268702 r, 0.07893900599711501 r, 
    0.08287917718339499 r, 0.08691105968769186 r, 0.09103425032511492 r, 
    0.09524833678003664 r, 0.09955289764732322 r, 0.1039475024744748 r, 
    0.1084317118046711 r, 0.113005077220716 r, 0.1176671413898787 r, 
    0.1224174381096274 r, 0.1272554923542488 r, 0.1321808203223502 r, 
    0.1371929294852391 r, 0.1422913186361759 r, 0.1474754779404944 r, 
    0.152744888986584 r, 0.1580990248377314 r, 0.1635373500848132 r, 
    0.1690593208998367 r, 0.1746643850903219 r, 0.1803519821545206 r, 
    0.1861215433374662 r, 0.1919724916878484 r, 0.1979042421157076 r, 
    0.2039162014509444 r, 0.2100077685026351 r, 0.216178334119151 r, 
    0.2224272812490723 r, 0.2287539850028937 r, 0.2351578127155118 r, 
    0.2416381240094921 r, 0.2481942708591053 r, 0.2548255976551299 r, 
    0.2615314412704124 r, 0.2683111311261794 r, 0.2751639892590951 r, 
    0.2820893303890569 r, 0.2890864619877229 r, 0.2961546843477643 r, 
    0.3032932906528349 r, 0.3105015670482534 r, 0.3177787927123868 r, 
    0.3251242399287333 r, 0.3325371741586922 r, 0.3400168541150183 r, 
    0.3475625318359485 r, 0.3551734527599992 r, 0.3628488558014202 r, 
    0.3705879734263036 r, 0.3783900317293359 r, 0.3862542505111889 r, 
    0.3941798433565377 r, 0.4021660177127022 r, 0.4102119749689023 r, 
    0.418316910536117 r, 0.4264800139275439 r, 0.4347004688396462 r, 
    0.4429774532337832 r, 0.451310139418413 r]
    

Berikut kita gambar sikloid untuk r=1.


\>ex &= x-sin(x); ey &= 1-cos(x); aspect(1);

\>plot2d(ex,ey,xmin=0,xmax=4pi,square=1); ...  
\>     plot2d("2+cos(x)","1+sin(x)",xmin=0,xmax=2pi,\>add,color=blue); ...  
\>     plot2d([2,ex(2)],[1,ey(2)],color=red,\>add); ...  
\>     plot2d(ex(2),ey(2),\>points,\>add,color=red); ...  
\>     plot2d("2pi+cos(x)","1+sin(x)",xmin=0,xmax=2pi,\>add,color=blue); ...  
\>     plot2d([2pi,ex(2pi)],[1,ey(2pi)],color=red,\>add);  ...  
\>     plot2d(ex(2pi),ey(2pi),\>points,\>add,color=red):


    Error : [0,1.66665833335744e-7*r-sin(1.66665833335744e-7*r),1.33330666692022e-6*r-sin(1.33330666692022e-6*r),4.499797504338432e-6*r-sin(4.499797504338432e-6*r),1.066581336583994e-5*r-sin(1.066581336583994e-5*r),2.083072932167196e-5*r-sin(2.083072932167196e-5*r),3.599352055540239e-5*r-sin(3.599352055540239e-5*r),5.71526624672386e-5*r-sin(5.71526624672386e-5*r),8.530603082730626e-5*r-sin(8.530603082730626e-5*r),1.214508019889565e-4*r-sin(1.214508019889565e-4*r),1.665833531718508e-4*r-sin(1.665833531718508e-4*r),2.216991628251896e-4*r-sin(2.216991628251896e-4*r),2.877927110806339e-4*r-sin(2.877927110806339e-4*r),3.658573803051457e-4*r-sin(3.658573803051457e-4*r),4.5688535576352e-4*r-sin(4.5688535576352e-4*r),5.618675264007778e-4*r-sin(5.618675264007778e-4*r),6.817933857540259e-4*r-sin(6.817933857540259e-4*r),8.176509330039827e-4*r-sin(8.176509330039827e-4*r),9.704265741758145e-4*r-sin(9.704265741758145e-4*r),0.001141105023499428*r-sin(0.001141105023499428*r),0.001330669204938795*r-sin(0.001330669204938795*r),0.001540100153900437*r-sin(0.001540100153900437*r),0.001770376919130678*r-sin(0.001770376919130678*r),0.002022476464811601*r-sin(0.002022476464811601*r),0.002297373572865413*r-sin(0.002297373572865413*r),0.002596040745477063*r-sin(0.002596040745477063*r),0.002919448107844891*r-sin(0.002919448107844891*r),0.003268563311168871*r-sin(0.003268563311168871*r),0.003644351435886262*r-sin(0.003644351435886262*r),0.004047774895164447*r-sin(0.004047774895164447*r),0.004479793338660443*r-sin(0.004479793338660443*r),0.0049413635565565*r-sin(0.0049413635565565*r),0.005433439383882244*r-sin(0.005433439383882244*r),0.005956971605131645*r-sin(0.005956971605131645*r),0.006512907859185624*r-sin(0.006512907859185624*r),0.007102192544548636*r-sin(0.007102192544548636*r),0.007725766724910044*r-sin(0.007725766724910044*r),0.00838456803503801*r-sin(0.00838456803503801*r),0.009079530587017326*r-sin(0.009079530587017326*r),0.009811584876838586*r-sin(0.009811584876838586*r),0.0105816576913495*r-sin(0.0105816576913495*r),0.01139067201557714*r-sin(0.01139067201557714*r),0.01223954694042984*r-sin(0.01223954694042984*r),0.01312919757078923*r-sin(0.01312919757078923*r),0.01406053493400045*r-sin(0.01406053493400045*r),0.01503446588876983*r-sin(0.01503446588876983*r),0.01605189303448024*r-sin(0.01605189303448024*r),0.01711371462093175*r-sin(0.01711371462093175*r),0.01822082445851714*r-sin(0.01822082445851714*r),0.01937411182884202*r-sin(0.01937411182884202*r),0.02057446139579705*r-sin(0.02057446139579705*r),0.02182275311709253*r-sin(0.02182275311709253*r),0.02311986215626333*r-sin(0.02311986215626333*r),0.02446665879515308*r-sin(0.02446665879515308*r),0.02586400834688696*r-sin(0.02586400834688696*r),0.02731277106934082*r-sin(0.02731277106934082*r),0.02881380207911666*r-sin(0.02881380207911666*r),0.03036795126603076*r-sin(0.03036795126603076*r),0.03197606320812652*r-sin(0.03197606320812652*r),0.0336389770872163*r-sin(0.0336389770872163*r),0.03535752660496472*r-sin(0.03535752660496472*r),0.03713253989951881*r-sin(0.03713253989951881*r),0.03896483946269502*r-sin(0.03896483946269502*r),0.0408552420577305*r-sin(0.0408552420577305*r),0.04280455863760801*r-sin(0.04280455863760801*r),0.04481359426396048*r-sin(0.04481359426396048*r),0.04688314802656623*r-sin(0.04688314802656623*r),0.04901401296344043*r-sin(0.04901401296344043*r),0.05120697598153157*r-sin(0.05120697598153157*r),0.05346281777803219*r-sin(0.05346281777803219*r),0.05578231276230905*r-sin(0.05578231276230905*r),0.05816622897846346*r-sin(0.05816622897846346*r),0.06061532802852698*r-sin(0.06061532802852698*r),0.0631303649963022*r-sin(0.0631303649963022*r),0.06571208837185505*r-sin(0.06571208837185505*r),0.06836123997666599*r-sin(0.06836123997666599*r),0.07107855488944881*r-sin(0.07107855488944881*r),0.07386476137264342*r-sin(0.07386476137264342*r),0.07672058079958999*r-sin(0.07672058079958999*r),0.07964672758239233*r-sin(0.07964672758239233*r),0.08264390910047736*r-sin(0.08264390910047736*r),0.0857128256298576*r-sin(0.0857128256298576*r),0.08885417027310427*r-sin(0.08885417027310427*r),0.09206862889003742*r-sin(0.09206862889003742*r),0.09535688002914089*r-sin(0.09535688002914089*r),0.0987195948597075*r-sin(0.0987195948597075*r),0.1021574371047232*r-sin(0.1021574371047232*r),0.1056710629744951*r-sin(0.1056710629744951*r),0.1092611211010309*r-sin(0.1092611211010309*r),0.1129282524731764*r-sin(0.1129282524731764*r),0.1166730903725168*r-sin(0.1166730903725168*r),0.1204962603100498*r-sin(0.1204962603100498*r),0.1243983799636342*r-sin(0.1243983799636342*r),0.1283800591162231*r-sin(0.1283800591162231*r),0.1324418995948859*r-sin(0.1324418995948859*r),0.1365844952106265*r-sin(0.1365844952106265*r),0.140808431699002*r-sin(0.140808431699002*r),0.1451142866615502*r-sin(0.1451142866615502*r),0.1495026295080298*r-sin(0.1495026295080298*r),0.1539740213994798*r-sin(0.1539740213994798*r)] does not produce a real or column vector
    
    Error generated by error() command
    
    adaptiveeval:
        error(f$|" does not produce a real or column vector"); 
    Try "trace errors" to inspect local variables after errors.
    plot2d:
        dw/n,dw/n^2,dw/n;args());

Berikut dihitung panjang lintasan untuk 1 putaran penuh. (Jangan salah menduga bahwa panjang lintasan 1 putaran penuh sama dengan
keliling lingkaran!)


\>ds &= radcan(sqrt(diff(ex,x)^2+diff(ey,x)^2)); $ds=trigsimp(ds) // elemen panjang kurva sikloid


    Maxima said:
    diff: second argument must be a variable; found errexp1
     -- an error. To debug this try: debugmode(true);
    
    Error in:
    ds &amp;= radcan(sqrt(diff(ex,x)^2+diff(ey,x)^2)); $ds=trigsimp(ds ...
                                                 ^

\>ds &= trigsimp(ds); $ds

\>$showev('integrate(ds,x,0,2\*pi)) // hitung panjang sikloid satu putaran penuh


    Maxima said:
    defint: variable of integration must be a simple or subscripted variable.
    defint: found errexp1
    #0: showev(f='integrate(ds,[0,1.66665833335744e-7*r,1.33330666692022e-6*r,4.499797504338432e-6*r,1.06658133658399...)
     -- an error. To debug this try: debugmode(true);
    
    Error in:
                                     ^

\>integrate(mxm("ds"),0,2\*pi) // hitung secara numerik


    Illegal function result in map.
     %evalexpression:
        if maps then return %mapexpression1(x,f$;args());
    gauss:
        if maps then y=%evalexpression(f$,a+h-(h*xn)',maps;args());
    adaptivegauss:
        t1=gauss(f$,c,c+h;args(),=maps);
    Try "trace errors" to inspect local variables after errors.
    integrate:
        return adaptivegauss(f$,a,b,eps*1000;args(),=maps);

\>romberg(mxm("ds"),0,2\*pi) // cara lain hitung secara numerik


    Wrong argument!
    
    Cannot combine a symbolic expression here.
    Did you want to create a symbolic expression?
    Then start with &amp;.
    
    Try "trace errors" to inspect local variables after errors.
    romberg:
        if cols(y)==1 then return y*(b-a); endif;
    Error in:
    romberg(mxm("ds"),0,2*pi) // cara lain hitung secara numerik ...
                             ^

Perhatikan, seperti terlihat pada gambar, panjang sikloid lebih besar daripada keliling lingkarannya, yakni:


## Kurvatur (Kelengkungan) Kurva

image: Osculating.png


Aslinya, kelengkungan kurva diferensiabel (yakni, kurva mulus yang tidak lancip) di titik P didefinisikan melalui lingkaran
oskulasi (yaitu, lingkaran yang melalui titik P dan terbaik memperkirakan, paling banyak menyinggung kurva di sekitar P). Pusat
dan radius kelengkungan kurva di P adalah pusat dan radius lingkaran oskulasi. Kelengkungan adalah kebalikan dari radius
kelengkungan:


dengan R adalah radius kelengkungan. (Setiap lingkaran memiliki kelengkungan ini pada setiap titiknya, dapat diartikan, setiap
lingkaran berputar 2pi sejauh 2piR.)


Definisi ini sulit dimanipulasi dan dinyatakan ke dalam rumus untuk kurva umum. Oleh karena itu digunakan definisi lain yang
ekivalen.


## Definisi Kurvatur dengan Fungsi Parametrik Panjang Kurva



Setiap kurva diferensiabel dapat dinyatakan dengan persamaan parametrik terhadap panjang kurva s:


dengan x dan y adalah fungsi riil yang diferensiabel, yang memenuhi:


Ini berarti bahwa vektor singgung


memiliki norm 1 dan merupakan vektor singgung satuan.


Apabila kurvanya memiliki turunan kedua, artinya turunan kedua x dan y ada, maka T'(s) ada. Vektor ini merupakan normal kurva yang
arahnya menuju pusat kurvatur, norm-nya merupakan nilai kurvatur (kelengkungan):


Nilai


disebut jari-jari (radius) kelengkungan kurva.


Bilangan riil


disebut nilai kelengkungan bertanda.


Contoh:


Akan ditentukan kurvatur lingkaran


\>fx &= r\*cos(t); fy &=r\*sin(t);

\>&assume(t\>0,r\>0); s &=integrate(sqrt(diff(fx,t)^2+diff(fy,t)^2),t,0,t); s // elemen panjang kurva, panjang busur lingkaran (s)


    Maxima said:
    diff: second argument must be a variable; found errexp1
     -- an error. To debug this try: debugmode(true);
    
    Error in:
    ... =integrate(sqrt(diff(fx,t)^2+diff(fy,t)^2),t,0,t); s // elemen ...
                                                         ^

\>&kill(s); fx &= r\*cos(s/r); fy &=r\*sin(s/r); // definisi ulang persamaan parametrik terhadap s dengan substitusi t=s/r

\>k &= trigsimp(sqrt(diff(fx,s,2)^2+diff(fy,s,2)^2)); $k // nilai kurvatur lingkaran dengan menggunakan definisi di atas


Untuk representasi parametrik umum, misalkan


merupakan persamaan parametrik untuk kurva bidang yang terdiferensialkan dua kali. Kurvatur untuk kurva tersebut didefinisikan
sebagai


Selanjutnya, pembilang pada persamaan di atas dapat dicari sebagai berikut.


Jadi, rumus kurvatur untuk kurva parametrik


adalah


Jika kurvanya dinyatakan dengan persamaan parametrik pada koordinat kutub


maka rumus kurvaturnya adalah


(Silakan Anda turunkan rumus tersebut!)


Contoh:


Lingkaran dengan pusat (0,0) dan jari-jari r dapat dinyatakan dengan persamaan parametrik


Nilai kelengkungan lingkaran tersebut adalah


Hasil cocok dengan definisi kurvatur suatu kelengkungan.


Kurva


dapat dinyatakan ke dalam persamaan parametrik


sehingga kurvaturnya adalah


Contoh:


Akan ditentukan kurvatur parabola


\>function f(x) &= a\*x^2+b\*x+c; $y=f(x)

\>function k(x) &= (diff(f(x),x,2))/(1+diff(f(x),x)^2)^(3/2); $'k(x)=k(x) // kelengkungan parabola 


    Maxima said:
    diff: second argument must be a variable; found errexp1
     -- an error. To debug this try: debugmode(true);
    
    Error in:
    ... (x) &amp;= (diff(f(x),x,2))/(1+diff(f(x),x)^2)^(3/2); $'k(x)=k(x)  ...
                                                         ^

\>function f(x) &= x^2+x+1; $y=f(x) // akan kita plot kelengkungan parabola untuk a=b=c=1

\>function k(x) &= (diff(f(x),x,2))/(1+diff(f(x),x)^2)^(3/2); $'k(x)=k(x) // kelengkungan parabola 


    Maxima said:
    diff: second argument must be a variable; found errexp1
     -- an error. To debug this try: debugmode(true);
    
    Error in:
    ... (x) &amp;= (diff(f(x),x,2))/(1+diff(f(x),x)^2)^(3/2); $'k(x)=k(x)  ...
                                                         ^

Berikut kita gambar parabola tersebut beserta kurva kelengkungan, kurva jari-jari kelengkungan dan salah satu lingkaran oskulasi
di titik puncak parabola. Perhatikan, puncak parabola dan jari-jari lingkaran oskulasi di puncak parabola adalah


sehingga pusat lingkaran oskulasi adalah (-1/2, 5/4).


\>plot2d(["f(x)", "k(x)"],-2,1, color=[blue,red]); plot2d("1/k(x)",-1.5,1,color=green,\>add); ...  
\>   plot2d("-1/2+1/k(-1/2)\*cos(x)","5/4+1/k(-1/2)\*sin(x)",xmin=0,xmax=2pi,\>add,color=blue):


    Error : f(x) does not produce a real or column vector
    
    Error generated by error() command
    
     %ploteval:
        error(f$|" does not produce a real or column vector"); 
    adaptiveevalone:
        s=%ploteval(g$,t;args());
    Try "trace errors" to inspect local variables after errors.
    plot2d:
        dw/n,dw/n^2,dw/n,auto;args());

Untuk kurva yang dinyatakan dengan fungsi implisit


dengan turunan-turunan parsial


berlaku


sehingga kurvaturnya adalah


(Silakan Anda turunkan sendiri!)


Contoh 1:


Parabola 


dapat dinyatakan ke dalam persamaan implisit


\>function F(x,y) &=a\*x^2+b\*x+c-y; $F(x,y)

\>Fx &= diff(F(x,y),x), Fxx &=diff(F(x,y),x,2), Fy &=diff(F(x,y),y), Fxy &=diff(diff(F(x,y),x),y), Fyy &=diff(F(x,y),y,2)  


    Maxima said:
    diff: second argument must be a variable; found errexp1
     -- an error. To debug this try: debugmode(true);
    
    Error in:
    Fx &amp;= diff(F(x,y),x), Fxx &amp;=diff(F(x,y),x,2), Fy &amp;=diff(F(x,y) ...
                        ^

\>function k(x) &= (Fy^2\*Fxx-2\*Fx\*Fy\*Fxy+Fx^2\*Fyy)/(Fx^2+Fy^2)^(3/2); $'k(x)=k(x) // kurvatur parabola tersebut


Hasilnya sama dengan sebelumnya yang menggunakan persamaan parabola biasa.


# Latihan

* 
Bukalah buku Kalkulus.

* 
Cari dan pilih beberapa (paling sedikit 5 fungsi berbeda
* tipe/bentuk/jenis) fungsi dari buku tersebut, kemudian definisikan di
* EMT pada baris-baris perintah berikut (jika perlu tambahkan lagi).

* 
Untuk setiap fungsi, tentukan anti turunannya (jika ada), hitunglah
* integral tentu dengan batas-batas yang menarik (Anda tentukan
* sendiri), seperti contoh-contoh tersebut.

* 
Lakukan hal yang sama untuk fungsi-fungsi yang tidak dapat
* diintegralkan (cari sedikitnya 3 fungsi).

* 
Gambar grafik fungsi dan daerah integrasinya pada sumbu koordinat
* yang sama.

* 
Gunakan integral tentu untuk mencari luas daerah yang dibatasi oleh
* dua kurva yang berpotongan di dua titik. (Cari dan gambar kedua kurva
* dan arsir (warnai) daerah yang dibatasi oleh keduanya.)

* 
Gunakan integral tentu untuk menghitung volume benda putar kurva y=
* f(x) yang diputar mengelilingi sumbu x dari x=a sampai x=b, yakni


(Pilih fungsinya dan gambar kurva dan benda putar yang dihasilkan.
Anda dapat mencari contoh-contoh bagaimana cara menggambar benda hasil
perputaran suatu kurva.)


- Gunakan integral tentu untuk menghitung panjang kurva y=f(x) dari
x=a sampai x=b dengan menggunakan rumus:


(Pilih fungsi dan gambar kurvanya.)


- Apabila fungsi dinyatakan dalam koordinat kutub x=f(r,t), y=g(r,t),
r=h(t), x=a bersesuaian dengan t=t0 dan x=b bersesuian dengan t=t1,
maka rumus di atas akan menjadi:


* 
Pilih beberapa kurva menarik (selain lingkaran dan parabola) dari
* buku  kalkulus. Nyatakan setiap kurva tersebut dalam bentuk:
*   a. koordinat Kartesius (persamaan y=f(x))
*   b. koordinat kutub ( r=r(theta))
*   c. persamaan parametrik x=x(t), y=y(t)
*   d. persamaan implit F(x,y)=0

* 
Tentukan kurvatur masing-masing kurva dengan menggunakan keempat
* representasi tersebut (hasilnya harus sama).

* 
Gambarlah kurva asli, kurva kurvatur, kurva jari-jari lingkaran
* oskulasi, dan salah satu lingkaran oskulasinya.


\>function f(x):= sin(x)

\>$showev('limit((sin(x+h)-sin(x))/h,h,0))

\>$showev(’integrate(sin(x),x,0,pi))


# Barisan dan Deret

(Catatan: bagian ini belum lengkap. Anda dapat membaca contoh-contoh pengguanaan EMT dan
Maxima untuk menghitung limit barisan, rumus jumlah parsial suatu deret, jumlah tak hingga
suatu deret konvergen, dan sebagainya. Anda dapat mengeksplor contoh-contoh di EMT atau
perbagai panduan penggunaan Maxima di software Maxima atau dari Internet.)


Barisan dapat didefinisikan dengan beberapa cara di dalam EMT, di antaranya:


* 
dengan cara yang sama seperti mendefinisikan vektor dengan elemen-elemen beraturan
* (menggunakan titik dua ":");

* 
menggunakan perintah "sequence" dan rumus barisan (suku ke -n);

* 
menggunakan perintah "iterate" atau "niterate";

* 
menggunakan fungsi Maxima "create_list" atau "makelist" untuk menghasilkan barisan
* simbolik;

* 
menggunakan fungsi biasa yang inputnya vektor atau barisan;

* 
menggunakan fungsi rekursif.


EMT menyediakan beberapa perintah (fungsi) terkait barisan, yakni:


* 
sum: menghitung jumlah semua elemen suatu barisan

* 
cumsum: jumlah kumulatif suatu barisan

* 
differences: selisih antar elemen-elemen berturutan


EMT juga dapat digunakan untuk menghitung jumlah deret berhingga maupun deret tak hingga,
dengan menggunakan perintah (fungsi) "sum". Perhitungan dapat dilakukan secara numerik
maupun simbolik dan eksak.


Berikut adalah beberapa contoh perhitungan barisan dan deret menggunakan EMT.


\>1:10 // barisan sederhana


    [1,  2,  3,  4,  5,  6,  7,  8,  9,  10]

\>1:2:30


    [1,  3,  5,  7,  9,  11,  13,  15,  17,  19,  21,  23,  25,  27,  29]

# Iterasi dan Barisan

EMT menyediakan fungsi iterate("g(x)", x0, n) untuk melakukan iterasi


Berikut ini disajikan contoh-contoh penggunaan iterasi dan rekursi dengan EMT. Contoh
pertama menunjukkan pertumbuhan dari nilai awal 1000 dengan laju pertambahan 5%, selama 10
periode.


\>q=1.05; iterate("x\*q",1000,n=10)'


             1000 
             1050 
           1102.5 
          1157.63 
          1215.51 
          1276.28 
           1340.1 
           1407.1 
          1477.46 
          1551.33 
          1628.89 

Contoh berikutnya memperlihatkan bahaya menabung di bank pada masa sekarang! Dengan bunga
tabungan sebesar 6% per tahun atau 0.5% per bulan dipotong pajak 20%, dan biaya administrasi
10000 per bulan, tabungan sebesar 1 juta tanpa diambil selama sekitar 10 tahunan akan habis
diambil oleh bank!


\>r=0.005; plot2d(iterate("(1+0.8\*r)\*x-10000",1000000,n=130)):


Silakan Anda coba-coba, dengan tabungan minimal berapa agar tidak akan habis diambil oleh
bank dengan ketentuan bunga dan biaya administrasi seperti di atas.


Berikut adalah perhitungan minimal tabungan agar aman di bank dengan bunga sebesar r dan
biaya administrasi a, pajak bunga 20%.


\>$solve(0.8\*r\*A-a,A), $% with [r=0.005, a=10] 


Berikut didefinisikan fungsi untuk menghitung saldo tabungan, kemudian dilakukan iterasi.


\>function saldo(x,r,a) := round((1+0.8\*r)\*x-a,2);

\>iterate({{"saldo",0.005,10}},1000,n=6)


    [1000,  994,  987.98,  981.93,  975.86,  969.76,  963.64]

\>iterate({{"saldo",0.005,10}},2000,n=6)


    [2000,  1998,  1995.99,  1993.97,  1991.95,  1989.92,  1987.88]

\>iterate({{"saldo",0.005,10}},2500,n=6)


    [2500,  2500,  2500,  2500,  2500,  2500,  2500]

Tabungan senilai 2,5 juta akan aman dan tidak akan berubah nilai (jika tidak ada penarikan),
sedangkan jika tabungan awal kurang dari 2,5 juta, lama kelamaan akan berkurang meskipun
tidak pernah dilakukan penarikan uang tabungan.


\>iterate({{"saldo",0.005,10}},3000,n=6)


    [3000,  3002,  3004.01,  3006.03,  3008.05,  3010.08,  3012.12]

Tabungan yang lebih dari 2,5 juta baru akan bertambah jika tidak ada penarikan.


Untuk barisan yang lebih kompleks dapat digunakan fungsi "sequence()". Fungsi ini menghitung
nilai-nilai x[n] dari semua nilai sebelumnya, x[1],...,x[n-1] yang diketahui.


Berikut adalah contoh barisan Fibonacci.


\>sequence("x[n-1]+x[n-2]",[1,1],15)


    [1,  1,  2,  3,  5,  8,  13,  21,  34,  55,  89,  144,  233,  377,  610]

Barisan Fibonacci memiliki banyak sifat menarik, salah satunya adalah akar pangkat ke-n suku
ke-n akan konvergen ke pecahan emas:


\>$'(1+sqrt(5))/2=float((1+sqrt(5))/2)

\>plot2d(sequence("x[n-1]+x[n-2]",[1,1],250)^(1/(1:250))):


Barisan yang sama juga dapat dihasilkan dengan menggunakan loop.


\>x=ones(500); for k=3 to 500; x[k]=x[k-1]+x[k-2]; end;


Rekursi dapat dilakukan dengan menggunakan rumus yang tergantung pada semua elemen
sebelumnya. Pada contoh berikut, elemen ke-n merupakan jumlah (n-1) elemen sebelumnya,
dimulai dengan 1 (elemen ke-1). Jelas, nilai elemen ke-n adalah 2^(n-2), untuk n=2, 4, 5,
....


\>sequence("sum(x)",1,10)


    [1,  1,  2,  4,  8,  16,  32,  64,  128,  256]

Selain menggunakan ekspresi dalam x dan n, kita juga dapat menggunakan fungsi.


Pada contoh berikut, digunakan iterasi


dengan A suatu matriks 2x2, dan setiap x[n] merupakan matriks/vektor 2x1.


\>A=[1,1;1,2]; function suku(x,n) := A.x[,n-1]

\>sequence("suku",[1;1],6)


    Real 2 x 6 matrix
    
                1             2             5            13     ...
                1             3             8            21     ...

Hasil yang sama juga dapat diperoleh dengan menggunakan fungsi perpangkatan matriks
"matrixpower()". Cara ini lebih cepat, karena hanya menggunakan perkalian matriks sebanyak
log_2(n).


\>sequence("matrixpower(A,n).[1;1]",1,6)


    Real 2 x 6 matrix
    
                1             5            13            34     ...
                1             8            21            55     ...

# Spiral Theodorus

image: Spiral_of_Theodorus.png


Spiral Theodorus (spiral segitiga siku-siku) dapat digambar secara rekursif. Rumus
rekursifnya adalah:


yang menghasilkan barisan bilangan kompleks.


\>function g(n) := 1+I/sqrt(n)


Rekursinya dapat dijalankan sebanyak 17 untuk menghasilkan barisan 17 bilangan kompleks,
kemudian digambar bilangan-bilangan kompleksnya.


\>x=sequence("g(n-1)\*x[n-1]",1,17); plot2d(x,r=3.5); textbox(latex("Spiral\\ Theodorus"),0.4):


Selanjutnya dihubungan titik 0 dengan titik-titik kompleks tersebut menggunakan loop.


\>for i=1:cols(x); plot2d([0,x[i]],\>add); end:

\> 


Spiral tersebut juga dapat didefinisikan menggunakan fungsi rekursif, yang tidak memmerlukan
indeks dan bilangan kompleks. Dalam hal ini diigunakan vektor kolom pada bidang.


\>function gstep (v) ...


    w=[-v[2];v[1]];
    return v+w/norm(w);
    endfunction
</pre>
Jika dilakukan iterasi 16 kali dimulai dari [1;0] akan didapatkan matriks yang memuat
vektor-vektor dari setiap iterasi.


\>x=iterate("gstep",[1;0],16); plot2d(x[1],x[2],r=3.5,\>points):


# Kekonvergenan

Terkadang kita ingin melakukan iterasi sampai konvergen. Apabila iterasinya tidak konvergen
setelah ditunggu lama, Anda dapat menghentikannya dengan menekan tombol [ESC].


\>iterate("cos(x)",1) // iterasi x(n+1)=cos(x(n)), dengan x(0)=1.


    0.739085133216

Iterasi tersebut konvergen ke penyelesaian persamaan


Iterasi ini juga dapat dilakukan pada interval, hasilnya adalah barisan interval yang memuat
akar tersebut.


\>hasil := iterate("cos(x)",~1,2~) //iterasi x(n+1)=cos(x(n)), dengan interval awal (1, 2)


    ~0.739085133211,0.7390851332133~

Jika interval hasil tersebut sedikit diperlebar, akan terlihat bahwa interval tersebut
memuat akar persamaan x=cos(x).


\>h=expand(hasil,100), cos(h) << h


    ~0.73908513309,0.73908513333~
    1

Iterasi juga dapat digunakan pada fungsi yang didefinisikan.


\>function f(x) := (x+2/x)/2


Iterasi x(n+1)=f(x(n)) akan konvergen ke akar kuadrat 2.


\>iterate("f",2), sqrt(2)


    1.41421356237
    1.41421356237

Jika pada perintah iterate diberikan tambahan parameter n, maka hasil iterasinya akan
ditampilkan mulai dari iterasi pertama sampai ke-n.


\>iterate("f",2,5)


    [2,  1.5,  1.41667,  1.41422,  1.41421,  1.41421]

Untuk iterasi ini tidak dapat dilakukan terhadap interval.


\>niterate("f",~1,2~,5)


    [ ~1,2~,  ~1,2~,  ~1,2~,  ~1,2~,  ~1,2~,  ~1,2~ ]

Perhatikan, hasil iterasinya sama dengan interval awal. Alasannya adalah perhitungan dengan
interval bersifat terlalu longgar. Untuk meingkatkan perhitungan pada ekspresi dapat
digunakan pembagian intervalnya, menggunakan fungsi ieval().


\>function s(x) := ieval("(x+2/x)/2",x,10)


Selanjutnya dapat dilakukan iterasi hingga diperoleh hasil optimal, dan intervalnya tidak
semakin mengecil. Hasilnya berupa interval yang memuat akar persamaan:


Satu-satunya solusi adalah


\>iterate("s",~1,2~)


    ~1.41421356236,1.41421356239~

Fungsi "iterate()" juga dapat bekerja pada vektor. Berikut adalah contoh fungsi vektor, yang
menghasilkan rata-rata aritmetika dan rata-rata geometri.


Iterasi ke-n disimpan pada vektor kolom x[n].


\>function g(x) := [(x[1]+x[2])/2;sqrt(x[1]\*x[2])]


Iterasi dengan menggunakan fungsi tersebut akan konvergen ke rata-rata aritmetika dan
geometri dari nilai-nilai awal. 


\>iterate("g",[1;5])


          2.60401 
          2.60401 

Hasil tersebut konvergen agak cepat, seperti kita cek sebagai berikut.


\>iterate("g",[1;5],4)


                1             3       2.61803       2.60403       2.60401 
                5       2.23607       2.59002       2.60399       2.60401 

Iterasi pada interval dapat dilakukan dan stabil, namun tidak menunjukkan bahwa limitnya
pada batas-batas yang dihitung.


\>iterate("g",[~1~;~5~],4)


    Interval 2 x 5 matrix
    
    ~0.999999999999999778,1.00000000000000022~     ...
    ~4.99999999999999911,5.00000000000000089~     ...

Iterasi berikut konvergen sangat lambat.


\>iterate("sqrt(x)",2,10)


    [2,  1.41421,  1.18921,  1.09051,  1.04427,  1.0219,  1.01089,
    1.00543,  1.00271,  1.00135,  1.00068]

Kekonvergenan iterasi tersebut dapat dipercepatdengan percepatan Steffenson:


\>steffenson("sqrt(x)",2,10)


    [1.04888,  1.00028,  1,  1]

# Iterasi menggunakan Loop yang ditulis Langsung

Berikut adalah beberapa contoh penggunaan loop untuk melakukan iterasi yang ditulis langsung
pada baris perintah.


\>x=2; repeat x=(x+2/x)/2; until x^2~=2; end; x,


    1.41421356237

Penggabungan matriks menggunakan tanda "|" dapat digunakan untuk menyimpan semua hasil
iterasi.


\>v=[1]; for i=2 to 8; v=v|(v[i-1]\*i); end; v,


    [1,  2,  6,  24,  120,  720,  5040,  40320]

hasil iterasi juga dapat disimpan pada vektor yang sudah ada.


\>v=ones(1,100); for i=2 to cols(v); v[i]=v[i-1]\*i; end; ...  
\>   plot2d(v,logplot=1); textbox(latex(&log(n)),x=0.5):

\>A =[0.5,0.2;0.7,0.1]; b=[2;2]; ...  
\>   x=[1;1]; repeat xnew=A.x-b; until all(xnew~=x); x=xnew; end; ...  
\>   x,


         -7.09677 
         -7.74194 

# Iterasi di dalam Fungsi

Fungsi atau program juga dapat menggunakan iterasi dan dapat digunakan untuk melakukan iterasi. Berikut adalah beberapa contoh
iterasi di dalam fungsi.


Contoh berikut adalah suatu fungsi untuk menghitung berapa lama suatu iterasi konvergen. Nilai fungsi tersebut adalah hasil akhir
iterasi dan banyak iterasi sampai konvergen.


\>function map hiter(f$,x0) ...


    x=x0;
    maxiter=0;
    repeat
      xnew=f$(x);
      maxiter=maxiter+1;
      until xnew~=x;
      x=xnew;
    end;
    return maxiter;
    endfunction
</pre>
Misalnya, berikut adalah iterasi untuk mendapatkan hampiran akar kuadrat 2, cukup cepat,
konvergen pada iterasi ke-5, jika dimulai dari hampiran awal 2.


\>hiter("(x+2/x)/2",2)


    5

Karena fungsinya didefinisikan menggunakan "map". maka nilai awalnya dapat berupa vektor.


\>x=1.5:0.1:10; hasil=hiter("(x+2/x)/2",x); ...  
\>     plot2d(x,hasil):


Dari gambar di atas terlihat bahwa kekonvergenan iterasinya semakin lambat, untuk nilai awal
semakin besar, namun penambahnnya tidak kontinu. Kita dapat menemukan kapan maksimum
iterasinya bertambah.


\>hasil[1:10]


    [4,  5,  5,  5,  5,  5,  6,  6,  6,  6]

\>x[nonzeros(differences(hasil))]


    [1.5,  2,  3.4,  6.6]

maksimum iterasi sampai konvergen meningkat pada saat nilai awalnya 1.5, 2, 3.4, dan 6.6.


Contoh berikutnya adalah metode Newton pada polinomial kompleks berderajat 3.


\>p &= x^3-1; newton &= x-p/diff(p,x); $newton


Selanjutnya didefinisikan fungsi untuk melakukan iterasi (aslinya 10 kali).


\>function iterasi(f$,x,n=10) ...


    loop 1 to n; x=f$(x); end;
    return x;
    endfunction
</pre>
Kita mulai dengan menentukan titik-titik grid pada bidang kompleksnya.


\>r=1.5; x=linspace(-r,r,501); Z=x+I\*x'; W=iterasi(newton,Z);


Berikut adalah akar-akar polinomial di atas.


\>z=&solve(p)()


    [ -0.5+0.866025i,  -0.5-0.866025i,  1+0i  ]

Untuk menggambar hasil iterasinya, dihitung jarak dari hasil iterasi ke-10 ke masing-masing
akar, kemudian digunakan untuk menghitung warna yang akan digambar, yang menunjukkan limit
untuk masing-masing nilai awal. 


Fungsi plotrgb() menggunakan jendela gambar terkini untuk menggambar warna RGB sebagai
matriks.


\>C=rgb(max(abs(W-z[1]),1),max(abs(W-z[2]),1),max(abs(W-z[3]),1)); ...  
\>     plot2d(none,-r,r,-r,r); plotrgb(C):


# Iterasi Simbolik

Seperti sudah dibahas sebelumnya, untuk menghasilkan barisan ekspresi simbolik dengan Maxima
dapat digunakan fungsi makelist().


\>&powerdisp:true // untuk menampilkan deret pangkat mulai dari suku berpangkat terkecil


    
                                     true
    

\>deret &= makelist(taylor(exp(x),x,0,k),k,1,3); $deret // barisan deret Taylor untuk e^x


Untuk mengubah barisan deret tersebut menjadi vektor string di EMT digunakan fungsi
mxm2str(). Selanjutnya, vektor string/ekspresi hasilnya dapat digambar seperti menggambar
vektor eskpresi pada EMT.


\>plot2d("exp(x)",0,3); // plot fungsi aslinya, e^x

\>plot2d(mxm2str("deret"),\>add,color=4:6): // plot ketiga deret taylor hampiran fungsi tersebut


Selain cara di atas dapat juga dengan cara menggunakan indeks pada vektor/list yang
dihasilkan.


\>$deret[3]

\>plot2d(["exp(x)",&deret[1],&deret[2],&deret[3]],0,3,color=1:4):

\>$sum(sin(k\*x)/k,k,1,5)


Berikut adalah cara menggambar kurva


\>plot2d(&sum(sin((2\*k+1)\*x)/(2\*k+1),k,0,20),0,2pi):


Hal serupa juga dapat dilakukan dengan menggunakan matriks, misalkan kita akan menggambar
kurva


\>x=linspace(0,2pi,1000); k=1:100; y=sum(sin(k\*x')/k)'; plot2d(x,y):


# Tabel Fungsi

Terdapat cara menarik untuk menghasilkan barisan dengan ekspresi Maxima. Perintah
mxmtable() berguna untuk menampilkan dan menggambar barisan dan menghasilkan barisan sebagai
vektor kolom. 


Sebagai contoh berikut adalah barisan turunan ke-n x^x di x=1.


\>mxmtable("diffat(x^x,x=1,n)","n",1,8,frac=1);


            1 
            2 
            3 
            8 
           10 
           54 
          -42 
          944 

\>$'sum(k, k, 1, n) = factor(ev(sum(k, k, 1, n),simpsum=true)) // simpsum:menghitung deret secara simbolik

\>$'sum(1/(3^k+k), k, 0, inf) = factor(ev(sum(1/(3^k+k), k, 0, inf),simpsum=true))


Di sini masih gagal, hasilnya tidak dihitung.


\>$'sum(1/x^2, x, 1, inf)= ev(sum(1/x^2, x, 1, inf),simpsum=true) // ev: menghitung nilai ekspresi

\>$'sum((-1)^(k-1)/k, k, 1, inf) = factor(ev(sum((-1)^(x-1)/x, x, 1, inf),simpsum=true))


Di sini masih gagal, hasilnya tidak dihitung.


\>$'sum((-1)^k/(2\*k-1), k, 1, inf) = factor(ev(sum((-1)^k/(2\*k-1), k, 1, inf),simpsum=true))

\>$ev(sum(1/n!, n, 0, inf),simpsum=true)


Di sini masih gagal, hasilnya tidak dihitung, harusnya hasilnya e.


\>&assume(abs(x)<1); $'sum(a\*x^k, k, 0, inf)=ev(sum(a\*x^k, k, 0, inf),simpsum=true), &forget(abs(x)<1);


Deret geometri tak hingga, dengan asumsi rasional antara -1 dan 1.


\>$'sum(x^k/k!,k,0,inf)=ev(sum(x^k/k!,k,0,inf),simpsum=true)

\>$limit(sum(x^k/k!,k,0,n),n,inf)

\>function d(n) &= sum(1/(k^2-k),k,2,n); $'d(n)=d(n)

\>$d(10)=ev(d(10),simpsum=true)

\>$d(100)=ev(d(100),simpsum=true)


# Deret Taylor

Deret Taylor suatu fungsi f yang diferensiabel sampai tak hingga di sekitar x=a adalah:


\>$'e^x =taylor(exp(x),x,0,10) // deret Taylor e^x di sekitar x=0, sampai suku ke-11

\>$'log(x)=taylor(log(x),x,1,10)// deret log(x) di sekitar x=1


# Visualisasi dan Perhitungan Geometri dengan EMT

Euler menyediakan beberapa fungsi untuk melakukan visualisasi dan perhitungan geometri, baik
secara numerik maupun analitik (seperti biasanya tentunya, menggunakan Maxima).
Fungsi-fungsi untuk visualisasi dan perhitungan geometeri tersebut disimpan di dalam file
program "geometry.e", sehingga file tersebut harus dipanggil sebelum menggunakan
fungsi-fungsi atau perintah-perintah untuk geometri.


\>load geometry


    Numerical and symbolic geometry.

## Fungsi-fungsi Geometri

Fungsi-fungsi untuk Menggambar Objek Geometri:


  defaultd:=textheight()*1.5: nilai asli untuk parameter d  
  setPlotrange(x1,x2,y1,y2): menentukan rentang x dan y pada bidang koordinat  
  setPlotRange(r): pusat bidang koordinat (0,0) dan batas-batas sumbu-x dan y adalah -r sd r  
  plotPoint (P, "P"): menggambar titik P dan diberi label "P"  
  plotSegment (A,B, "AB", d): menggambar ruas garis AB, diberi label "AB" sejauh d  
  plotLine (g, "g", d): menggambar garis g diberi label "g" sejauh d  
  plotCircle (c,"c",v,d): Menggambar lingkaran c dan diberi label "c"  
  plotLabel (label, P, V, d): menuliskan label pada posisi P  

Fungsi-fungsi Geometri Analitik (numerik maupun simbolik):


  turn(v, phi): memutar vektor v sejauh phi  
  turnLeft(v):   memutar vektor v ke kiri  
  turnRight(v):  memutar vektor v ke kanan  
  normalize(v): normal vektor v  
  crossProduct(v, w): hasil kali silang vektorv dan w.  
  lineThrough(A, B): garis melalui A dan B, hasilnya [a,b,c] sdh. ax+by=c.  
  lineWithDirection(A,v): garis melalui A searah vektor v  
  getLineDirection(g): vektor arah (gradien) garis g  
  getNormal(g): vektor normal (tegak lurus) garis g  
  getPointOnLine(g):  titik pada garis g  
  perpendicular(A, g):  garis melalui A tegak lurus garis g  
  parallel (A, g):  garis melalui A sejajar garis g  
  lineIntersection(g, h):  titik potong garis g dan h  
  projectToLine(A, g):   proyeksi titik A pada garis g  
  distance(A, B):  jarak titik A dan B  
  distanceSquared(A, B):  kuadrat jarak A dan B  
  quadrance(A, B): kuadrat jarak A dan B  
  areaTriangle(A, B, C):  luas segitiga ABC  
  computeAngle(A, B, C):   besar sudut &lt;ABC  
  angleBisector(A, B, C): garis bagi sudut &lt;ABC  
  circleWithCenter (A, r): lingkaran dengan pusat A dan jari-jari r  
  getCircleCenter(c):  pusat lingkaran c  
  getCircleRadius(c):  jari-jari lingkaran c  
  circleThrough(A,B,C):  lingkaran melalui A, B, C  
  middlePerpendicular(A, B): titik tengah AB  
  lineCircleIntersections(g, c): titik potong garis g dan lingkran c  
  circleCircleIntersections (c1, c2):  titik potong lingkaran c1 dan c2  
  planeThrough(A, B, C):  bidang melalui titik A, B, C  

Fungsi-fungsi Khusus Untuk Geometri Simbolik:


  getLineEquation (g,x,y): persamaan garis g dinyatakan dalam x dan y  
  getHesseForm (g,x,y,A): bentuk Hesse garis g dinyatakan dalam x dan y dengan titik A pada  
  sisi positif (kanan/atas) garis  
  quad(A,B): kuadrat jarak AB  
  spread(a,b,c): Spread segitiga dengan panjang sisi-sisi a,b,c, yakni sin(alpha)^2 dengan  
  alpha sudut yang menghadap sisi a.  
  crosslaw(a,b,c,sa): persamaan 3 quads dan 1 spread pada segitiga dengan panjang sisi a, b, c.  
  triplespread(sa,sb,sc): persamaan 3 spread sa,sb,sc yang memebntuk suatu segitiga  
  doublespread(sa): Spread sudut rangkap Spread 2*phi, dengan sa=sin(phi)^2 spread a.  

## Contoh 1: Luas, Lingkaran Luar, Lingkaran Dalam Segitiga

Untuk menggambar objek-objek geometri, langkah pertama adalah menentukan rentang sumbu-sumbu
koordinat. Semua objek geometri akan digambar pada satu bidang koordinat, sampai didefinisikan
bidang koordinat yang baru.


\>setPlotRange(-0.5,2.5,-0.5,2.5); // mendefinisikan bidang koordinat baru 


Sekarang tetapkan tiga titik dan plotlah.


\>A=[1,0]; plotPoint(A,"A"); // definisi dan gambar tiga titik

\>B=[0,1]; plotPoint(B,"B");

\>C=[2,2]; plotPoint(C,"C");


Lalu tiga segmen.


\>plotSegment(A,B,"c"); // c=AB

\>plotSegment(B,C,"a"); // a=BC

\>plotSegment(A,C,"b"); // b=AC


Fungsi geometri mencakup fungsi untuk membuat garis dan lingkaran.
Format untuk garis adalah [a,b,c], yang merepresentasikan garis dengan
persamaan ax+by=c.


\>lineThrough(B,C) // garis yang melalui B dan C


    [-1,  2,  2]

Hitunglah garis tegak lurus melalui A pada BC.


\>h=perpendicular(A,lineThrough(B,C)); // garis h tegak lurus BC melalui A


Dan persimpangannya dengan BC.


\>D=lineIntersection(h,lineThrough(B,C)); // D adalah titik potong h dan BC


Gambarkan itu.


\>plotPoint(D,value=1); // koordinat D ditampilkan

\>aspect(1); plotSegment(A,D): // tampilkan semua gambar hasil plot...()


![images/Final%20Project%20Aplikom%20Semester%203-320.png](images/Final%20Project%20Aplikom%20Semester%203-320.png)

Hitung luas ABC:


\>norm(A-D)\*norm(B-C)/2 // AD=norm(A-D), BC=norm(B-C)


    1.5

Compare with determinant formula.


\>areaTriangle(A,B,C) // hitung luas segitiga langusng dengan fungsi


    1.5

Cara lain menghitung luas segitigas ABC:


\>distance(A,D)\*distance(B,C)/2


    1.5

Sudut di C.


\>degprint(computeAngle(B,C,A))


    36°52'11.63''

Sekarang lingkaran luar segitiga.


\>c=circleThrough(A,B,C); // lingkaran luar segitiga ABC

\>R=getCircleRadius(c); // jari2 lingkaran luar 

\>O=getCircleCenter(c); // titik pusat lingkaran c 

\>plotPoint(O,"O"); // gambar titik "O"

\>plotCircle(c,"Lingkaran luar segitiga ABC"):


![images/Final%20Project%20Aplikom%20Semester%203-321.png](images/Final%20Project%20Aplikom%20Semester%203-321.png)

Tampilkan koordinat titik pusat dan jari-jari lingkaran luar.


\>O, R


    [1.16667,  1.16667]
    1.17851130198

Sekarang akan digambar lingkaran dalam segitiga ABC. Titik pusat lingkaran dalam adalah
titik potong garis-garis bagi sudut.


\>l=angleBisector(A,C,B); // garis bagi <ACB

\>g=angleBisector(C,A,B); // garis bagi <CAB

\>P=lineIntersection(l,g) // titik potong kedua garis bagi sudut


    [0.86038,  0.86038]

Tambahkan semuanya ke dalam alur cerita.


\>color(5); plotLine(l); plotLine(g); color(1); // gambar kedua garis bagi sudut

\>plotPoint(P,"P"); // gambar titik potongnya

\>r=norm(P-projectToLine(P,lineThrough(A,B))) // jari-jari lingkaran dalam


    0.509653732104

\>plotCircle(circleWithCenter(P,r),"Lingkaran dalam segitiga ABC"): // gambar lingkaran dalam


![images/Final%20Project%20Aplikom%20Semester%203-322.png](images/Final%20Project%20Aplikom%20Semester%203-322.png)

## Latihan

1. Tentukan ketiga titik singgung lingkaran dalam dengan sisi-sisi
segitiga ABC.


\>setPlotRange(-2.5,4.5,-2.5,4.5);

\>A=[-2,1]; plotPoint(A,"A");

\>B=[1,-2]; plotPoint(B,"B");

\>C=[4,4]; plotPoint(C,"C");


2. Gambar segitiga dengan titik-titik sudut ketiga titik singgung
tersebut.


\>plotSegment(A,B,"c")

\>plotSegment(B,C,"a")

\>plotSegment(A,C,"b")

\>aspect(1):


![images/Final%20Project%20Aplikom%20Semester%203-323.png](images/Final%20Project%20Aplikom%20Semester%203-323.png)

3. Tunjukkan bahwa garis bagi sudut yang ke tiga juga melalui titik
pusat lingkaran dalam.


\>l=angleBisector(A,C,B);

\>g=angleBisector(C,A,B);

\>P=lineIntersection(l,g)


    [0.581139,  0.581139]

\>color(5); plotLine(l); plotLine(g); color(1);

\>plotPoint(P,"P");

\>r=norm(P-projectToLine(P,lineThrough(A,B)))


    1.52896119631

\>plotCircle(circleWithCenter(P,r),"Lingkaran dalam segitiga ABC"):


![images/Final%20Project%20Aplikom%20Semester%203-324.png](images/Final%20Project%20Aplikom%20Semester%203-324.png)

Jadi, terbukti bahwa garis bagi sudut yang ketiga juga melalui titik
pusat lingkaran dalam.


4. Gambar jari-jari lingkaran dalam.


\>r=norm(P-projectToLine(P,lineThrough(A,B)))


    1.52896119631

\>plotCircle(circleWithCenter(P,r),"Lingkaran dalam segitiga ABC"):


![images/Final%20Project%20Aplikom%20Semester%203-325.png](images/Final%20Project%20Aplikom%20Semester%203-325.png)

# Contoh 2: Geometri Smbolik

Kita dapat menghitung geometri eksak dan simbolik menggunakan Maxima.


File geometry.e menyediakan fungsi yang sama (dan lebih banyak lagi)
di Maxima. Akan tetapi, kita sekarang dapat menggunakan perhitungan
simbolik.


\>A &= [1,0]; B &= [0,1]; C &= [2,2]; // menentukan tiga titik A, B, C


Fungsi untuk garis dan lingkaran bekerja seperti fungsi Euler, tetapi
menyediakan perhitungan simbolis.


\>c &= lineThrough(B,C) // c=BC


    
                                 [- 1, 2, 2]
    

Kita dapat memperoleh persamaan garis dengan mudah.


\>$getLineEquation(c,x,y), $solve(%,y) | expand // persamaan garis c


$$2\,y-x=2$$$$\left[ y=\frac{x}{2}+1 \right] $$\>$getLineEquation(lineThrough([x1,y1],[x2,y2]),x,y), $solve(%,y) // persamaan garis melalui(x1, y1) dan (x2, y2)


$$x\,\left({\it y_1}-{\it y_2}\right)+\left({\it x_2}-{\it x_1}
 \right)\,y={\it x_1}\,\left({\it y_1}-{\it y_2}\right)+\left(
 {\it x_2}-{\it x_1}\right)\,{\it y_1}$$$$\left[ y=\frac{-\left({\it x_1}-x\right)\,{\it y_2}-\left(x-
 {\it x_2}\right)\,{\it y_1}}{{\it x_2}-{\it x_1}} \right] $$\>$getLineEquation(lineThrough(A,[x1,y1]),x,y) // persamaan garis melalui A dan (x1, y1)


$$\left({\it x_1}-1\right)\,y-x\,{\it y_1}=-{\it y_1}$$\>h &= perpendicular(A,lineThrough(B,C)) // h melalui A tegak lurus BC


    
                                  [2, 1, 2]
    

\>Q &= lineIntersection(c,h) // Q titik potong garis c=BC dan h


    
                                     2  6
                                    [-, -]
                                     5  5
    

\>$projectToLine(A,lineThrough(B,C)) // proyeksi A pada BC


$$\left[ \frac{2}{5} , \frac{6}{5} \right] $$\>$distance(A,Q) // jarak AQ


$$\frac{3}{\sqrt{5}}$$\>cc &= circleThrough(A,B,C); $cc // (titik pusat dan jari-jari) lingkaran melalui A, B, C


$$\left[ \frac{7}{6} , \frac{7}{6} , \frac{5}{3\,\sqrt{2}} \right] $$\>r&=getCircleRadius(cc); $r , $float(r) // tampilkan nilai jari-jari


$$\frac{5}{3\,\sqrt{2}}$$$$1.178511301977579$$\>$computeAngle(A,C,B) // nilai <ACB


$$\arccos \left(\frac{4}{5}\right)$$\>$solve(getLineEquation(angleBisector(A,C,B),x,y),y)[1] // persamaan garis bagi <ACB


$$y=x$$\>P &= lineIntersection(angleBisector(A,C,B),angleBisector(C,B,A)); $P // titik potong 2 garis bagi sudut


$$\left[ \frac{\sqrt{2}\,\sqrt{5}+2}{6} , \frac{\sqrt{2}\,\sqrt{5}+2
 }{6} \right] $$\>P() // hasilnya sama dengan perhitungan sebelumnya


    [0.86038,  0.86038]

## Garis dan Lingkaran yang Berpotongan

Tentu saja, kita juga dapat membuat garis berpotongan dengan
lingkaran, dan lingkaran dengan lingkaran.


\>A &:= [1,0]; c=circleWithCenter(A,4);

\>B &:= [1,2]; C &:= [2,1]; l=lineThrough(B,C);

\>setPlotRange(5); plotCircle(c); plotLine(l);


Perpotongan garis dengan lingkaran menghasilkan dua titik dan jumlah
titik perpotongan.


\>{P1,P2,f}=lineCircleIntersections(l,c);

\>P1, P2, f


    [4.64575,  -1.64575]
    [-0.645751,  3.64575]
    2

\>plotPoint(P1); plotPoint(P2):


![images/Final%20Project%20Aplikom%20Semester%203-339.png](images/Final%20Project%20Aplikom%20Semester%203-339.png)

Sama halnya di Maxima.


\>c &= circleWithCenter(A,4) // lingkaran dengan pusat A jari-jari 4


    
                                  [1, 0, 4]
    

\>l &= lineThrough(B,C) // garis l melalui B dan C


    
                                  [1, 1, 3]
    

\>$lineCircleIntersections(l,c) | radcan, // titik potong lingkaran c dan garis l


$$\left[ \left[ \sqrt{7}+2 , 1-\sqrt{7} \right]  , \left[ 2-\sqrt{7}
  , \sqrt{7}+1 \right]  \right] $$Akan ditunjukkan bahwa sudut-sudut yang menghadap bsuusr yang sama adalah sama besar.


\>C=A+normalize([-2,-3])\*4; plotPoint(C); plotSegment(P1,C); plotSegment(P2,C);

\>degprint(computeAngle(P1,C,P2))


    69°17'42.68''

\>C=A+normalize([-4,-3])\*4; plotPoint(C); plotSegment(P1,C); plotSegment(P2,C);

\>degprint(computeAngle(P1,C,P2))


    69°17'42.68''

\>insimg;


![images/Final%20Project%20Aplikom%20Semester%203-341.png](images/Final%20Project%20Aplikom%20Semester%203-341.png)

## Garis Sumbu

Berikut adalah langkah-langkah menggambar garis sumbu ruas garis AB:


1. Gambar lingkaran dengan pusat A melalui B.


2. Gambar lingkaran dengan pusat B melalui A.


3. Tarik garis melallui kedua titik potong kedua lingkaran tersebut. Garis ini merupakan
garis sumbu (melalui titik tengah dan tegak lurus) AB.


\>A=[2,2]; B=[-1,-2];

\>c1=circleWithCenter(A,distance(A,B));

\>c2=circleWithCenter(B,distance(A,B));

\>{P1,P2,f}=circleCircleIntersections(c1,c2);

\>l=lineThrough(P1,P2);

\>setPlotRange(5); plotCircle(c1); plotCircle(c2);

\>plotPoint(A); plotPoint(B); plotSegment(A,B); plotLine(l):


![images/Final%20Project%20Aplikom%20Semester%203-342.png](images/Final%20Project%20Aplikom%20Semester%203-342.png)

Selanjutnya, kita melakukan hal yang sama di Maxima dengan koordinat
umum.


\>A &= [a1,a2]; B &= [b1,b2];

\>c1 &= circleWithCenter(A,distance(A,B));

\>c2 &= circleWithCenter(B,distance(A,B));

\>P &= circleCircleIntersections(c1,c2); P1 &= P[1]; P2 &= P[2];


Persamaan untuk perpotongan cukup rumit. Namun, kita dapat
menyederhanakannya, jika kita mencari nilai y.


\>g &= getLineEquation(lineThrough(P1,P2),x,y);

\>$solve(g,y)


$$\left[ y=\frac{-\left(2\,{\it b_1}-2\,{\it a_1}\right)\,x+{\it b_2}
 ^2+{\it b_1}^2-{\it a_2}^2-{\it a_1}^2}{2\,{\it b_2}-2\,{\it a_2}}
  \right] $$Ini memang sama dengan tegak lurus tengah, yang dihitung dengan cara
yang sepenuhnya berbeda.


\>$solve(getLineEquation(middlePerpendicular(A,B),x,y),y)


$$\left[ y=\frac{-\left(2\,{\it b_1}-2\,{\it a_1}\right)\,x+{\it b_2}
 ^2+{\it b_1}^2-{\it a_2}^2-{\it a_1}^2}{2\,{\it b_2}-2\,{\it a_2}}
  \right] $$\>h &=getLineEquation(lineThrough(A,B),x,y);

\>$solve(h,y)


$$\left[ y=\frac{\left({\it b_2}-{\it a_2}\right)\,x-{\it a_1}\,
 {\it b_2}+{\it a_2}\,{\it b_1}}{{\it b_1}-{\it a_1}} \right] $$Perhatikan hasil kali gradien garis g dan h adalah:


Artinya kedua garis tegak lurus.


# Contoh 3: Rumus Heron

Rumus Heron menyatakan bahwa luas segitiga dengan panjang sisi-sisi a,
b dan c adalah:


atau bisa ditulis dalam bentuk lain:


Untuk membuktikan hal ini kita misalkan C(0,0), B(a,0) dan A(x,y),
b=AC, c=AB. Luas segitiga ABC adalah


Nilai y didapat dengan menyelesaikan sistem persamaan:


\>setPlotRange(-1,10,-1,8); plotPoint([0,0], "C(0,0)"); plotPoint([5.5,0], "B(a,0)");  ...  
\>    plotPoint([7.5,6], "A(x,y)");

\>plotSegment([0,0],[5.5,0], "a",25); plotSegment([5.5,0],[7.5,6],"c",15);  ...  
\>   plotSegment([0,0],[7.5,6],"b",25); 

\>plotSegment([7.5,6],[7.5,0],"t=y",25):


![images/Final%20Project%20Aplikom%20Semester%203-346.png](images/Final%20Project%20Aplikom%20Semester%203-346.png)

\>&assume(a\>0); sol &= solve([x^2+y^2=b^2,(x-a)^2+y^2=c^2],[x,y])


    
                                      []
    

Ekstrak solusi y.


\>ysol &= y with sol[2][2]; $'y=sqrt(factor(ysol^2))


    Maxima said:
    part: invalid index of list or matrix.
     -- an error. To debug this try: debugmode(true);
    
    Error in:
    ysol &amp;= y with sol[2][2]; $'y=sqrt(factor(ysol^2)) ...
                            ^

Kita mendapatkan rumus Heron.


\>function H(a,b,c) &= sqrt(factor((ysol\*a/2)^2)); $'H(a,b,c)=H(a,b,c)


$$H\left(a , b , \left[ 1 , 0 , 4 \right] \right)=\frac{a\,\left| 
 {\it ysol}\right| }{2}$$\>$'Luas=H(2,5,6) // luas segitiga dengan panjang sisi-sisi 2, 5, 6


$${\it Luas}=\left| {\it ysol}\right| $$Tentu saja, setiap segitiga siku-siku adalah kasus yang terkenal.


\>H(3,4,5) //luas segitiga siku-siku dengan panjang sisi 3, 4, 5


    Variable or function ysol not found.
    Try "trace errors" to inspect local variables after errors.
    H:
        useglobal; return a*abs(ysol)/2 
    Error in:
    H(3,4,5) //luas segitiga siku-siku dengan panjang sisi 3, 4, 5 ...
            ^

Dan jelas pula, bahwa ini adalah segitiga dengan luas maksimal dan dua
sisinya 3 dan 4.


\>aspect (1.5); plot2d(&H(3,4,x),1,7): // Kurva luas segitiga sengan panjang sisi 3, 4, x (1<= x <=7)


    Variable or function ysol not found.
    Error in expression: 3*abs(ysol)/2
    %ploteval:
        y0=f$(x[1],args());
    adaptiveevalone:
        s=%ploteval(g$,t;args());
    Try "trace errors" to inspect local variables after errors.
    plot2d:
        dw/n,dw/n^2,dw/n,auto;args());

Kasus umum juga berfungsi.


\>$solve(diff(H(a,b,c)^2,c)=0,c)


    Maxima said:
    diff: second argument must be a variable; found [1,0,4]
     -- an error. To debug this try: debugmode(true);
    
    Error in:
    $solve(diff(H(a,b,c)^2,c)=0,c) ...
                                  ^

Sekarang mari kita cari himpunan semua titik di mana b+c=d untuk suatu
konstanta d. Diketahui bahwa ini adalah elips.


\>s1 &= subst(d-c,b,sol[2]); $s1


    Maxima said:
    part: invalid index of list or matrix.
     -- an error. To debug this try: debugmode(true);
    
    Error in:
    s1 &amp;= subst(d-c,b,sol[2]); $s1 ...
                             ^

Dan buat fungsi ini.


\>function fx(a,c,d) &= rhs(s1[1]); $fx(a,c,d), function fy(a,c,d) &= rhs(s1[2]); $fy(a,c,d)


$$0$$$$0$$Sekarang kita dapat menggambar himpunannya. Sisi b bervariasi dari 1
hingga 4. Diketahui bahwa kita mendapatkan elips.


\>aspect(1); plot2d(&fx(3,x,5),&fy(3,x,5),xmin=1,xmax=4,square=1):


![images/Final%20Project%20Aplikom%20Semester%203-351.png](images/Final%20Project%20Aplikom%20Semester%203-351.png)

Kita dapat memeriksa persamaan umum untuk elips ini, yaitu:


di mana (xm,ym) adalah pusat, dan u dan v adalah sumbu setengah.


\>$ratsimp((fx(a,c,d)-a/2)^2/u^2+fy(a,c,d)^2/v^2 with [u=d/2,v=sqrt(d^2-a^2)/2])


$$\left[ \frac{a^2}{d^2} , \frac{a^2}{d^2} , \frac{a^2}{d^2} , \frac{
 a^2}{d^2} , \frac{a^2}{d^2} , \frac{a^2}{d^2} , \frac{a^2}{d^2} , 
 \frac{a^2}{d^2} , \frac{a^2}{d^2} , \frac{a^2}{d^2} , \frac{a^2}{d^2
 } \right] $$Kita melihat bahwa tinggi dan luas segitiga tersebut adalah maksimum
untuk x=0. Jadi luas segitiga dengan a+b+c=d adalah maksimum, jika
segitiga tersebut sama sisi. Kita ingin memperolehnya secara analitis.


\>eqns &= [diff(H(a,b,d-(a+b))^2,a)=0,diff(H(a,b,d-(a+b))^2,b)=0]; $eqns


$$\left[ \frac{a\,{\it ysol}^2}{2}=0 , 0=0 \right] $$Kita memperoleh beberapa nilai minimum, yang dimiliki oleh segitiga
dengan satu sisi 0, dan solusinya a=b=c=d/3.


\>$solve(eqns,[a,b])


$$\left[ \left[ a=0 , b={\it \%r_1} \right]  \right] $$Ada juga metode Lagrange, yang memaksimalkan H(a,b,c)^2 terhadap
a+b+d=d.


\>&solve([diff(H(a,b,c)^2,a)=la,diff(H(a,b,c)^2,b)=la, ...  
\>      diff(H(a,b,c)^2,c)=la,a+b+c=d],[a,b,c,la])


    Maxima said:
    diff: second argument must be a variable; found [1,0,4]
     -- an error. To debug this try: debugmode(true);
    
    Error in:
    ... la,    diff(H(a,b,c)^2,c)=la,a+b+c=d],[a,b,c,la]) ...
                                                         ^

Kita bisa membuat plot dari situasinya


Pertama-tama atur titik di Maxima.


\>A &= at([x,y],sol[2]); $A


    Maxima said:
    part: invalid index of list or matrix.
     -- an error. To debug this try: debugmode(true);
    
    Error in:
    A &amp;= at([x,y],sol[2]); $A ...
                         ^

\>B &= [0,0]; $B, C &= [a,0]; $C


$$\left[ 0 , 0 \right] $$$$\left[ a , 0 \right] $$Kemudian atur rentang plot dan plot titik-titiknya.


\>setPlotRange(0,5,-2,3); ...  
\>   a=4; b=3; c=2; ...  
\>   plotPoint(mxmeval("B"),"B"); plotPoint(mxmeval("C"),"C"); ...  
\>   plotPoint(mxmeval("A"),"A"):


    Variable a1 not found!
    Use global variables or parameters for string evaluation.
    Error in Evaluate, superfluous characters found.
    Try "trace errors" to inspect local variables after errors.
    mxmeval:
        return evaluate(mxm(s));
    Error in:
    ... otPoint(mxmeval("C"),"C"); plotPoint(mxmeval("A"),"A"): ...
                                                         ^

Plot segmen.


\>splotSegment(mxmeval("A"),mxmeval("C")); ...  
\>   plotSegment(mxmeval("B"),mxmeval("C")); ...  
\>   plotSegment(mxmeval("B"),mxmeval("A")):


    Variable a1 not found!
    Use global variables or parameters for string evaluation.
    Error in Evaluate, superfluous characters found.
    Try "trace errors" to inspect local variables after errors.
    mxmeval:
        return evaluate(mxm(s));
    Error in:
    splotSegment(mxmeval("A"),mxmeval("C")); plotSegment(mxmeval(" ...
                             ^

Hitunglah garis tegak lurus tengah di Maxima.


\>h &= middlePerpendicular(A,B); g &= middlePerpendicular(B,C);


Dan pusat kelilingnya.


\>U &= lineIntersection(h,g);


Kita mendapatkan rumus untuk jari-jari lingkaran luar.


\>&assume(a\>0,b\>0,c\>0); $distance(U,B) | radcan


$$\frac{\sqrt{{\it a_2}^2+{\it a_1}^2}\,\sqrt{{\it a_2}^2+{\it a_1}^2
 -2\,a\,{\it a_1}+a^2}}{2\,\left| {\it a_2}\right| }$$Mari kita tambahkan ini ke dalam alur cerita.


\>plotPoint(U()); ...  
\>   plotCircle(circleWithCenter(mxmeval("U"),mxmeval("distance(U,C)"))):


    Variable a2 not found!
    Use global variables or parameters for string evaluation.
    Error in ^
    Error in expression: [a/2,(a2^2+a1^2-a*a1)/(2*a2)]
    Error in:
    plotPoint(U()); plotCircle(circleWithCenter(mxmeval("U"),mxmev ...
                 ^

Dengan menggunakan geometri, kita peroleh rumus sederhana


untuk jari-jari. Kita dapat memeriksa apakah ini benar dengan Maxima.
Maxima akan memfaktorkan ini hanya jika kita mengkuadratkannya.


\>$c^2/sin(computeAngle(A,B,C))^2  | factor


$$\left[ \frac{{\it a_2}^2+{\it a_1}^2}{{\it a_2}^2} , 0 , \frac{16\,
 \left({\it a_2}^2+{\it a_1}^2\right)}{{\it a_2}^2} \right] $$# Contoh 4: Garis Euler dan Parabola

Garis Euler adalah garis yang ditentukan dari sembarang segitiga yang
tidak sama sisi. Garis ini merupakan garis pusat segitiga, dan
melewati beberapa titik penting yang ditentukan dari segitiga
tersebut, termasuk orthocenter, circumcenter, centroid, titik Exeter,
dan titik pusat lingkaran sembilan titik pada segitiga tersebut.


Sebagai contoh, kita hitung dan plot garis Euler dalam sebuah
segitiga.


Pertama, kita definisikan sudut-sudut segitiga dalam Euler. Kita
gunakan definisi, yang terlihat dalam ekspresi simbolik.


\>A::=[-1,-1]; B::=[2,0]; C::=[1,2];


Untuk memplot objek geometris, kita menyiapkan area plot, dan
menambahkan titik-titik ke dalamnya. Semua plot objek geometris
ditambahkan ke plot saat ini.


\>setPlotRange(3); plotPoint(A,"A"); plotPoint(B,"B"); plotPoint(C,"C");


Kita juga dapat menambahkan sisi-sisi segitiga.


\>plotSegment(A,B,""); plotSegment(B,C,""); plotSegment(C,A,""):


![images/Final%20Project%20Aplikom%20Semester%203-359.png](images/Final%20Project%20Aplikom%20Semester%203-359.png)

Berikut adalah luas segitiga, menggunakan rumus determinan. Tentu
saja, kita harus mengambil nilai absolut dari hasil ini.


\>$areaTriangle(A,B,C)


$$-\frac{7}{2}$$Kita dapat menghitung koefisien sisi c.


\>c &= lineThrough(A,B)


    
                                [- 1, 3, - 2]
    

Dan dapatkan juga rumus untuk garis ini.


\>$getLineEquation(c,x,y)


$$3\,y-x=-2$$Untuk bentuk Hesse, kita perlu menentukan suatu titik, sehingga titik
tersebut berada di sisi positif bentuk Hesse. Memasukkan titik akan
menghasilkan jarak positif ke garis.


\>$getHesseForm(c,x,y,C), $at(%,[x=C[1],y=C[2]])


$$\frac{3\,y-x+2}{\sqrt{10}}$$$$\frac{7}{\sqrt{10}}$$Sekarang kita hitung lingkaran luar ABC.


\>LL &= circleThrough(A,B,C); $getCircleEquation(LL,x,y)


$$\left(y-\frac{5}{14}\right)^2+\left(x-\frac{3}{14}\right)^2=\frac{
 325}{98}$$\>O &= getCircleCenter(LL); $O


$$\left[ \frac{3}{14} , \frac{5}{14} \right] $$Gambarkan lingkaran dan titik pusatnya. Cu dan U adalah simbol. Kita
evaluasi ekspresi ini untuk Euler.


\>plotCircle(LL()); plotPoint(O(),"O"):


![images/Final%20Project%20Aplikom%20Semester%203-366.png](images/Final%20Project%20Aplikom%20Semester%203-366.png)

Kita dapat menghitung perpotongan tinggi di ABC (orthocenter) secara
numerik dengan perintah berikut.


\>H &= lineIntersection(perpendicular(A,lineThrough(C,B)),...  
\>     perpendicular(B,lineThrough(A,C))); $H


$$\left[ \frac{11}{7} , \frac{2}{7} \right] $$Sekarang kita dapat menghitung garis Euler dari segitiga tersebut.


\>el &= lineThrough(H,O); $getLineEquation(el,x,y)


$$-\frac{19\,y}{14}-\frac{x}{14}=-\frac{1}{2}$$Tambahkan ke plot kita.


\>plotPoint(H(),"H"); plotLine(el(),"Garis Euler"):


![images/Final%20Project%20Aplikom%20Semester%203-369.png](images/Final%20Project%20Aplikom%20Semester%203-369.png)

Pusat gravitasi seharusnya berada pada garis ini.


\>M &= (A+B+C)/3; $getLineEquation(el,x,y) with [x=M[1],y=M[2]]


$$-\frac{1}{2}=-\frac{1}{2}$$\>plotPoint(M(),"M"): // titik berat


![images/Final%20Project%20Aplikom%20Semester%203-371.png](images/Final%20Project%20Aplikom%20Semester%203-371.png)

Teori ini memberi tahu kita MH=2*MO. Kita perlu menyederhanakannya
dengan radcan untuk mencapainya.


\>$distance(M,H)/distance(M,O)|radcan


$$2$$Fungsinya termasuk fungsi untuk sudut juga.


\>$computeAngle(A,C,B), degprint(%())


$$\arccos \left(\frac{4}{\sqrt{5}\,\sqrt{13}}\right)$$    60°15'18.43''

Persamaan untuk pusat lingkaran dalam tidak terlalu bagus.


\>Q &= lineIntersection(angleBisector(A,C,B),angleBisector(C,B,A))|radcan; $Q


$$\left[ \frac{\left(2^{\frac{3}{2}}+1\right)\,\sqrt{5}\,\sqrt{13}-15
 \,\sqrt{2}+3}{14} , \frac{\left(\sqrt{2}-3\right)\,\sqrt{5}\,\sqrt{
 13}+5\,2^{\frac{3}{2}}+5}{14} \right] $$Mari kita hitung juga ekspresi untuk jari-jari lingkaran dalam.


\>r &= distance(Q,projectToLine(Q,lineThrough(A,B)))|ratsimp; $r


$$\frac{\sqrt{\left(-41\,\sqrt{2}-31\right)\,\sqrt{5}\,\sqrt{13}+115
 \,\sqrt{2}+614}}{7\,\sqrt{2}}$$\>LD &=  circleWithCenter(Q,r); // Lingkaran dalam


Mari kita tambahkan ini ke dalam alur cerita.


\>color(5); plotCircle(LD()):


![images/Final%20Project%20Aplikom%20Semester%203-376.png](images/Final%20Project%20Aplikom%20Semester%203-376.png)

## Parabola

Selanjutnya akan dicari persamaan tempat kedudukan titik-titik yang berjarak sama ke titik C
dan ke garis AB.


\>p &= getHesseForm(lineThrough(A,B),x,y,C)-distance([x,y],C); $p='0


$$\frac{3\,y-x+2}{\sqrt{10}}-\sqrt{\left(2-y\right)^2+\left(1-x
 \right)^2}=0$$Persamaan tersebut dapat digambar menjadi satu dengan gambar sebelumnya.


\>plot2d(p,level=0,add=1,contourcolor=6):


![images/Final%20Project%20Aplikom%20Semester%203-378.png](images/Final%20Project%20Aplikom%20Semester%203-378.png)

Ini seharusnya merupakan suatu fungsi, tetapi penyelesai default
Maxima hanya dapat menemukan solusinya, jika kita mengkuadratkan
persamaannya. Akibatnya, kita mendapatkan solusi palsu.


\>akar &= solve(getHesseForm(lineThrough(A,B),x,y,C)^2-distance([x,y],C)^2,y)


    
            [y = - 3 x - sqrt(70) sqrt(9 - 2 x) + 26, 
                                  y = - 3 x + sqrt(70) sqrt(9 - 2 x) + 26]
    

Solusi pertama adalah


maxima: akar[1]


Dengan menambahkan solusi pertama ke dalam plot, terlihat bahwa itu
memang jalur yang kita cari. Teori tersebut memberi tahu kita bahwa
itu adalah parabola yang diputar.


\>plot2d(&rhs(akar[1]),add=1):


![images/Final%20Project%20Aplikom%20Semester%203-379.png](images/Final%20Project%20Aplikom%20Semester%203-379.png)

\>function g(x) &= rhs(akar[1]); $'g(x)= g(x)// fungsi yang mendefinisikan kurva di atas


$$g\left(x\right)=-3\,x-\sqrt{70}\,\sqrt{9-2\,x}+26$$\>T &=[-1, g(-1)]; // ambil sebarang titik pada kurva tersebut

\>dTC &= distance(T,C); $fullratsimp(dTC), $float(%) // jarak T ke C


$$\sqrt{1503-54\,\sqrt{11}\,\sqrt{70}}$$$$2.135605779339061$$\>U &= projectToLine(T,lineThrough(A,B)); $U // proyeksi T pada garis AB 


$$\left[ \frac{80-3\,\sqrt{11}\,\sqrt{70}}{10} , \frac{20-\sqrt{11}\,
 \sqrt{70}}{10} \right] $$\>dU2AB &= distance(T,U); $fullratsimp(dU2AB), $float(%) // jatak T ke AB


$$\sqrt{1503-54\,\sqrt{11}\,\sqrt{70}}$$$$2.135605779339061$$Ternyata jarak T ke C sama dengan jarak T ke AB. Coba Anda pilih titik
T yang lain dan ulangi perhitungan-perhitungan di atas untuk
menunjukkan bahwa hasilnya juga sama.


# Contoh 5: Trigonometri Rasional

Hal ini terinspirasi dari ceramah N.J.Wildberger. Dalam bukunya
"Divine Proportions", Wildberger mengusulkan untuk mengganti konsep
klasik jarak dan sudut dengan kuadran dan sebaran. Dengan menggunakan
konsep ini, memang memungkinkan untuk menghindari fungsi trigonometri
dalam banyak contoh, dan tetap "rasional".


Berikut ini, saya memperkenalkan konsep-konsep tersebut, dan
memecahkan beberapa masalah. Saya menggunakan perhitungan simbolik
Maxima di sini, yang menyembunyikan keuntungan utama trigonometri
rasional bahwa perhitungan dapat dilakukan hanya dengan kertas dan
pensil. Anda diundang untuk memeriksa hasilnya tanpa komputer.


Intinya adalah bahwa perhitungan simbolik rasional sering kali
menghasilkan hasil yang sederhana. Sebaliknya, trigonometri klasik
menghasilkan hasil trigonometri yang rumit, yang hanya mengevaluasi
perkiraan numerik.


\>load geometry;


Untuk pengenalan pertama, kami menggunakan segitiga siku-siku dengan
proporsi Mesir yang terkenal yaitu 3, 4, dan 5. Perintah berikut
adalah perintah Euler untuk memplot geometri bidang yang terdapat
dalam file Euler "geometry.e".


\>C&:=[0,0]; A&:=[4,0]; B&:=[0,3]; ...  
\>   setPlotRange(-1,5,-1,5); ...  
\>   plotPoint(A,"A"); plotPoint(B,"B"); plotPoint(C,"C"); ...  
\>   plotSegment(B,A,"c"); plotSegment(A,C,"b"); plotSegment(C,B,"a"); ...  
\>   insimg(30);


![images/Final%20Project%20Aplikom%20Semester%203-386.png](images/Final%20Project%20Aplikom%20Semester%203-386.png)

Tentu saja,


di mana wa adalah sudut di A. Cara yang biasa untuk menghitung sudut
ini adalah dengan mengambil kebalikan dari fungsi sinus. Hasilnya
adalah sudut yang tidak dapat dicerna, yang hanya dapat dicetak secara
perkiraan.


\>wa := arcsin(3/5); degprint(wa)


    36°52'11.63''

Trigonometri rasional mencoba menghindari hal ini.


Gagasan pertama trigonometri rasional adalah kuadran, yang
menggantikan jarak. Faktanya, itu hanyalah kuadrat jarak. Dalam
persamaan berikut, a, b, dan c menunjukkan kuadran sisi-sisi.


Teorema Pythogoras menjadi a+b=c.


\>a &= 3^2; b &= 4^2; c &= 5^2; &a+b=c


    
                                   25 = 25
    

Gagasan kedua trigonometri rasional adalah sebaran. Sebaran mengukur
bukaan antara garis. Nilainya 0, jika garis sejajar, dan 1, jika garis
persegi panjang. Nilainya adalah kuadrat sinus sudut antara dua garis.


Sebaran garis AB dan AC pada gambar di atas didefinisikan sebagai


di mana a dan c adalah kuadran dari setiap segitiga persegi panjang
dengan satu sudut di A.


\>sa &= a/c; $sa


$$\frac{9}{25}$$Tentu saja, ini lebih mudah dihitung daripada sudut. Namun, Anda
kehilangan sifat bahwa sudut dapat ditambahkan dengan mudah.


Tentu saja, kita dapat mengubah nilai perkiraan untuk sudut wa menjadi
sprad, dan mencetaknya sebagai pecahan.


\>fracprint(sin(wa)^2)


    9/25

Hukum kosinus dari trgonometri klasik diterjemahkan ke dalam "hukum
silang" berikut.


Di sini a, b, dan c adalah kuadran sisi-sisi segitiga, dan sa adalah
sebaran di sudut A. Sisi a, seperti biasa, berseberangan dengan sudut
A.


Hukum-hukum ini diimplementasikan dalam berkas geometry.e yang kami
muat ke Euler.


\>$crosslaw(aa,bb,cc,saa)


$$\left[ \left({\it bb}-{\it aa}+\frac{7}{6}\right)^2 , \left(
 {\it bb}-{\it aa}+\frac{7}{6}\right)^2 , \left({\it bb}-{\it aa}+
 \frac{5}{3\,\sqrt{2}}\right)^2 \right] =\left[ \frac{14\,{\it bb}\,
 \left(1-{\it saa}\right)}{3} , \frac{14\,{\it bb}\,\left(1-{\it saa}
 \right)}{3} , \frac{5\,2^{\frac{3}{2}}\,{\it bb}\,\left(1-{\it saa}
 \right)}{3} \right] $$Dalam kasus kami, kami mendapatkan


\>$crosslaw(a,b,c,sa)


$$1024=1024$$Mari kita gunakan hukum silang ini untuk menemukan sebaran di A. Untuk
melakukannya, kita buat hukum silang untuk kuadran a, b, dan c, dan
selesaikan untuk sebaran yang tidak diketahui sa.


Anda dapat melakukannya dengan mudah secara manual, tetapi saya
menggunakan Maxima. Tentu saja, kita mendapatkan hasil yang sudah kita
miliki.


\>$crosslaw(a,b,c,x), $solve(%,x)


$$1024=1600\,\left(1-x\right)$$$$\left[ x=\frac{9}{25} \right] $$Kita sudah tahu ini. Definisi sebaran adalah kasus khusus dari hukum
silang.


Kita juga dapat memecahkan ini untuk a,b,c umum. Hasilnya adalah rumus
yang menghitung sebaran sudut segitiga yang diberikan kuadran ketiga
sisinya.


\>$solve(crosslaw(aa,bb,cc,x),x)


$$\left[ \left[ \frac{168\,{\it bb}\,x+36\,{\it bb}^2+\left(-72\,
 {\it aa}-84\right)\,{\it bb}+36\,{\it aa}^2-84\,{\it aa}+49}{36} , 
 \frac{168\,{\it bb}\,x+36\,{\it bb}^2+\left(-72\,{\it aa}-84\right)
 \,{\it bb}+36\,{\it aa}^2-84\,{\it aa}+49}{36} , \frac{15\,2^{\frac{
 5}{2}}\,{\it bb}\,x+18\,{\it bb}^2+\left(-36\,{\it aa}-15\,2^{\frac{
 3}{2}}\right)\,{\it bb}+18\,{\it aa}^2-15\,2^{\frac{3}{2}}\,{\it aa}
 +25}{18} \right] =0 \right] $$Kita dapat membuat fungsi dari hasil tersebut. Fungsi tersebut telah
didefinisikan dalam berkas geometry.e milik Euler.


\>$spread(a,b,c)


$$\frac{9}{25}$$Sebagai contoh, kita dapat menggunakannya untuk menghitung sudut
segitiga dengan sisi-sisi


Hasilnya rasional, yang tidak mudah didapat jika kita menggunakan
trigonometri klasik.


\>$spread(a,a,4\*a/7)


$$\frac{6}{7}$$Ini adalah sudut dalam derajat.


\>degprint(arcsin(sqrt(6/7)))


    67°47'32.44''

## Contoh Lain

Sekarang, mari kita coba contoh yang lebih maju.


Kita tentukan tiga sudut segitiga sebagai berikut.


\>A&:=[1,2]; B&:=[4,3]; C&:=[0,4]; ...  
\>   setPlotRange(-1,5,1,7); ...  
\>   plotPoint(A,"A"); plotPoint(B,"B"); plotPoint(C,"C"); ...  
\>   plotSegment(B,A,"c"); plotSegment(A,C,"b"); plotSegment(C,B,"a"); ...  
\>   insimg;


![images/Final%20Project%20Aplikom%20Semester%203-395.png](images/Final%20Project%20Aplikom%20Semester%203-395.png)

Dengan menggunakan Pythogoras, mudah untuk menghitung jarak antara dua
titik. Pertama-tama saya menggunakan fungsi distance dari file Euler
untuk geometri. Fungsi distance menggunakan geometri klasik.


\>$distance(A,B)


$$\sqrt{10}$$Euler juga memuat fungsi untuk kuadran antara dua titik.


Dalam contoh berikut, karena c+b bukan a, segitiga tersebut bukan
persegi panjang.


\>c &= quad(A,B); $c, b &= quad(A,C); $b, a &= quad(B,C); $a,


$$10$$$$5$$$$17$$Pertama, mari kita hitung sudut tradisional. Fungsi computeAngle
menggunakan metode biasa berdasarkan perkalian titik dua vektor.
Hasilnya adalah beberapa perkiraan floating point.


\>wb &= computeAngle(A,B,C); $wb, $(wb/pi\*180)()


$$\arccos \left(\frac{11}{\sqrt{10}\,\sqrt{17}}\right)$$    32.4711922908

Dengan menggunakan pensil dan kertas, kita dapat melakukan hal yang
sama dengan hukum silang. Kita masukkan kuadran a, b, dan c ke dalam
hukum silang dan selesaikan untuk x.


\>$crosslaw(a,b,c,x), $solve(%,x), //(b+c-a)^=4b.c(1-x)


$$4=200\,\left(1-x\right)$$$$\left[ x=\frac{49}{50} \right] $$Yaitu, apa yang dilakukan fungsi sebaran yang didefinisikan dalam
"geometry.e".


\>sb &= spread(b,a,c); $sb


$$\frac{49}{170}$$Maxima memperoleh hasil yang sama dengan menggunakan trigonometri
biasa, jika kita memaksakannya. Maxima memang menyelesaikan suku
sin(arccos(...)) menjadi hasil pecahan. Sebagian besar siswa tidak
dapat melakukan ini.


\>$sin(computeAngle(A,B,C))^2


$$\frac{49}{170}$$Setelah kita memiliki sebaran di B, kita dapat menghitung tinggi ha
pada sisi a. Ingat bahwa


menurut definisi.


\>ha &= c\*sb; $ha


$$\frac{49}{17}$$Gambar berikut ini dibuat dengan program geometri C.a.R., yang dapat
menggambar kuadran dan sebaran.


image: (20) Rational_Geometry_CaR.png


Menurut definisi, panjang ha adalah akar kuadrat dari kuadrannya.


\>$sqrt(ha)


$$\frac{7}{\sqrt{17}}$$Sekarang kita bisa menghitung luas segitiga. Jangan lupa, bahwa kita
sedang membahas tentang kuadran!


\>$sqrt(ha)\*sqrt(a)/2


$$\frac{7}{2}$$Rumus determinan yang biasa menghasilkan hasil yang sama.


\>$areaTriangle(B,A,C)


$$\frac{7}{2}$$## Rumus Heron

Sekarang, mari kita selesaikan masalah ini secara umum!


\>&remvalue(a,b,c,sb,ha);


Pertama-tama kita hitung sebaran di B untuk segitiga dengan sisi a, b,
dan c. Kemudian kita hitung luas kuadrat (yang disebut "quadrea"?),
faktorkan dengan Maxima, dan kita dapatkan rumus Heron yang terkenal.


Memang, ini sulit dilakukan dengan pensil dan kertas.


\>$spread(b^2,c^2,a^2), $factor(%\*c^2\*a^2/4)


$$\frac{-c^4-\left(-2\,b^2-2\,a^2\right)\,c^2-b^4+2\,a^2\,b^2-a^4}{4
 \,a^2\,c^2}$$$$\frac{\left(-c+b+a\right)\,\left(c-b+a\right)\,\left(c+b-a\right)\,
 \left(c+b+a\right)}{16}$$## Aturan Triple Spread

Kerugian spread adalah tidak lagi sekadar menambahkan sudut yang sama.


Namun, tiga spread segitiga memenuhi aturan "triple spread" berikut.


\>&remvalue(sa,sb,sc); $triplespread(sa,sb,sc)


$$\left({\it sc}+{\it sb}+{\it sa}\right)^2=2\,\left({\it sc}^2+
 {\it sb}^2+{\it sa}^2\right)+4\,{\it sa}\,{\it sb}\,{\it sc}$$Aturan ini berlaku untuk tiga sudut yang jumlahnya mencapai 180°.


Karena sebaran


sama, aturan sebaran rangkap tiga juga berlaku, jika


Karena sebaran sudut negatif sama, aturan sebaran rangkap tiga juga
berlaku, jika


Misalnya, kita dapat menghitung sebaran sudut 60°. Yaitu 3/4.
Persamaan tersebut memiliki solusi kedua, di mana semua sebarannya
adalah 0.


\>$solve(triplespread(x,x,x),x)


$$\left[ x=\frac{3}{4} , x=0 \right] $$Sebaran 90° jelas adalah 1. Jika dua sudut dijumlahkan menjadi 90°,
sebarannya memecahkan persamaan sebaran rangkap tiga dengan a,b,1.
Dengan perhitungan berikut kita memperoleh a+b=1.


\>$triplespread(x,y,1), $solve(%,x)


$$\left(y+x+1\right)^2=2\,\left(y^2+x^2+1\right)+4\,x\,y$$$$\left[ x=1-y \right] $$Karena sebaran 180°-t sama dengan sebaran t, rumus sebaran rangkap
tiga juga berlaku, jika satu sudut adalah jumlah atau selisih dari dua
sudut lainnya.


Jadi kita dapat menemukan sebaran sudut yang digandakan. Perhatikan
bahwa ada dua solusi lagi. Kita buat ini menjadi fungsi.


\>$solve(triplespread(a,a,x),x), function doublespread(a) &= factor(rhs(%[1]))


$$\left[ x=4\,a-4\,a^2 , x=0 \right] $$    
                                - 4 (a - 1) a
    

## Garis Bagi Sudut

Kita sudah tahu situasinya seperti ini.


\>C&:=[0,0]; A&:=[4,0]; B&:=[0,3]; ...  
\>   setPlotRange(-1,5,-1,5); ...  
\>   plotPoint(A,"A"); plotPoint(B,"B"); plotPoint(C,"C"); ...  
\>   plotSegment(B,A,"c"); plotSegment(A,C,"b"); plotSegment(C,B,"a"); ...  
\>   insimg;


![images/Final%20Project%20Aplikom%20Semester%203-416.png](images/Final%20Project%20Aplikom%20Semester%203-416.png)

Mari kita hitung panjang garis bagi sudut di A. Namun, kita ingin
menyelesaikannya untuk a,b,c umum.


\>&remvalue(a,b,c);


Jadi pertama-tama kita hitung sebaran sudut yang dibagi dua di A,
menggunakan rumus sebaran rangkap tiga.


Masalah dengan rumus ini muncul lagi. Rumus ini memiliki dua solusi.
Kita harus memilih yang benar. Solusi lainnya mengacu pada sudut yang
dibagi dua 180°-wa.


\>$triplespread(x,x,a/(a+b)), $solve(%,x), sa2 &= rhs(%[1]); $sa2


$$\left(2\,x+\frac{a}{b+a}\right)^2=2\,\left(2\,x^2+\frac{a^2}{\left(
 b+a\right)^2}\right)+\frac{4\,a\,x^2}{b+a}$$$$\left[ x=\frac{-\sqrt{b}\,\sqrt{b+a}+b+a}{2\,b+2\,a} , x=\frac{
 \sqrt{b}\,\sqrt{b+a}+b+a}{2\,b+2\,a} \right] $$$$\frac{-\sqrt{b}\,\sqrt{b+a}+b+a}{2\,b+2\,a}$$Mari kita periksa persegi panjang Mesir.


\>$sa2 with [a=3^2,b=4^2]


$$\frac{1}{10}$$Kita dapat mencetak sudut dalam Euler, setelah mentransfer sebaran ke
radian.


\>wa2 := arcsin(sqrt(1/10)); degprint(wa2)


    18°26'5.82''

Titik P merupakan perpotongan garis bagi sudut dengan sumbu y.


\>P := [0,tan(wa2)\*4]


    [0,  1.33333]

\>plotPoint(P,"P"); plotSegment(A,P):


![images/Final%20Project%20Aplikom%20Semester%203-421.png](images/Final%20Project%20Aplikom%20Semester%203-421.png)

Mari kita periksa sudut-sudut pada contoh spesifik kita.


\>computeAngle(C,A,P), computeAngle(P,A,B)


    0.321750554397
    0.321750554397

Sekarang kita hitung panjang garis bagi AP.


Kita gunakan teorema sinus dalam segitiga APC. Teorema ini menyatakan
bahwa


berlaku di sembarang segitiga. Kuadratkan, maka akan menghasilkan apa
yang disebut "hukum sebaran"


di mana a,b,c menunjukkan kuadran.


Karena CPA sebaran adalah 1-sa2, kita peroleh darinya bisa/1=b/(1-sa2)
dan dapat menghitung bisa (kuadran garis bagi sudut).


\>&factor(ratsimp(b/(1-sa2))); bisa &= %; $bisa


$$\frac{2\,b\,\left(b+a\right)}{\sqrt{b}\,\sqrt{b+a}+b+a}$$Mari kita periksa rumus ini untuk nilai-nilai Mesir kita.


\>sqrt(mxmeval("at(bisa,[a=3^2,b=4^2])")), distance(A,P)


    4.21637021356
    4.21637021356

Kita juga dapat menghitung P menggunakan rumus spread.


\>py&=factor(ratsimp(sa2\*bisa)); $py


$$-\frac{b\,\left(\sqrt{b}\,\sqrt{b+a}-b-a\right)}{\sqrt{b}\,\sqrt{b+
 a}+b+a}$$Nilainya sama dengan yang kita dapatkan dengan rumus trigonometri.


\>sqrt(mxmeval("at(py,[a=3^2,b=4^2])"))


    1.33333333333

## Sudut Tali

Perhatikan situasi berikut.


\>setPlotRange(1.2); ...  
\>   color(1); plotCircle(circleWithCenter([0,0],1)); ...  
\>   A:=[cos(1),sin(1)]; B:=[cos(2),sin(2)]; C:=[cos(6),sin(6)]; ...  
\>   plotPoint(A,"A"); plotPoint(B,"B"); plotPoint(C,"C"); ...  
\>   color(3); plotSegment(A,B,"c"); plotSegment(A,C,"b"); plotSegment(C,B,"a"); ...  
\>   color(1); O:=[0,0];  plotPoint(O,"0"); ...  
\>   plotSegment(A,O); plotSegment(B,O); plotSegment(C,O,"r"); ...  
\>   insimg;


![images/Final%20Project%20Aplikom%20Semester%203-424.png](images/Final%20Project%20Aplikom%20Semester%203-424.png)

Kita dapat menggunakan Maxima untuk memecahkan rumus penyebaran
rangkap tiga untuk sudut-sudut di pusat O untuk r. Dengan demikian,
kita memperoleh rumus untuk jari-jari kuadrat pericircle dalam bentuk
kuadran sisi-sisinya.


Kali ini, Maxima menghasilkan beberapa nol kompleks, yang kita
abaikan.


\>&remvalue(a,b,c,r); // hapus nilai-nilai sebelumnya untuk perhitungan baru

\>rabc &= rhs(solve(triplespread(spread(b,r,r),spread(a,r,r),spread(c,r,r)),r)[4]); $rabc


$$-\frac{a\,b\,c}{c^2-2\,b\,c+a\,\left(-2\,c-2\,b\right)+b^2+a^2}$$Kita dapat menjadikannya fungsi Euler.


\>function periradius(a,b,c) &= rabc;


Mari kita periksa hasilnya untuk titik A, B, C.


\>a:=quadrance(B,C); b:=quadrance(A,C); c:=quadrance(A,B);


Radiusnya memang 1.


\>periradius(a,b,c)


    1

Faktanya, sebaran CBA hanya bergantung pada b dan c. Ini adalah
teorema sudut tali busur.


\>$spread(b,a,c)\*rabc | ratsimp


$$\frac{b}{4}$$Faktanya, sebarannya adalah b/(4r), dan kita melihat bahwa sudut tali
busur b adalah setengah sudut pusat.


\>$doublespread(b/(4\*r))-spread(b,r,r) | ratsimp


$$0$$# Contoh 6: Jarak Minimal pada Bidang

## Catatan awal

Fungsi yang, pada titik M di bidang, menetapkan jarak AM antara titik
tetap A dan M, memiliki garis datar yang agak sederhana: lingkaran
yang berpusat di A.


\>&remvalue();

\>A=[-1,-1];

\>function d1(x,y):=sqrt((x-A[1])^2+(y-A[2])^2)

\>fcontour("d1",xmin=-2,xmax=0,ymin=-2,ymax=0,hue=1, ...  
\>   title="If you see ellipses, please set your window square"):


![images/Final%20Project%20Aplikom%20Semester%203-428.png](images/Final%20Project%20Aplikom%20Semester%203-428.png)

dan grafiknya cukup sederhana: bagian atas kerucut:


\>plot3d("d1",xmin=-2,xmax=0,ymin=-2,ymax=0):


![images/Final%20Project%20Aplikom%20Semester%203-429.png](images/Final%20Project%20Aplikom%20Semester%203-429.png)

Tentu saja minimum 0 dicapai di A.


## Dua titik

Sekarang kita lihat fungsi MA+MB di mana A dan B adalah dua titik
(tetap). Merupakan "fakta yang diketahui" bahwa kurva level adalah
elips, titik fokusnya adalah A dan B; kecuali untuk minimum AB yang
konstan pada segmen [AB]:


\>B=[1,-1];

\>function d2(x,y):=d1(x,y)+sqrt((x-B[1])^2+(y-B[2])^2)

\>fcontour("d2",xmin=-2,xmax=2,ymin=-3,ymax=1,hue=1):


![images/Final%20Project%20Aplikom%20Semester%203-430.png](images/Final%20Project%20Aplikom%20Semester%203-430.png)

Grafiknya lebih menarik:


\>plot3d("d2",xmin=-2,xmax=2,ymin=-3,ymax=1):


![images/Final%20Project%20Aplikom%20Semester%203-431.png](images/Final%20Project%20Aplikom%20Semester%203-431.png)

Pembatasan pada garis (AB) lebih terkenal:


\>plot2d("abs(x+1)+abs(x-1)",xmin=-3,xmax=3):


![images/Final%20Project%20Aplikom%20Semester%203-432.png](images/Final%20Project%20Aplikom%20Semester%203-432.png)

## Tiga poin

Sekarang semuanya menjadi kurang sederhana: Tidak banyak yang tahu
bahwa MA+MB+MC mencapai nilai minimumnya di satu titik bidang, tetapi
menentukannya tidaklah sesederhana itu:


1) Jika salah satu sudut segitiga ABC lebih dari 120° (misalkan di A),
maka nilai minimumnya tercapai di titik ini (misalkan AB+AC).


Contoh:


\>C=[-4,1];

\>function d3(x,y):=d2(x,y)+sqrt((x-C[1])^2+(y-C[2])^2)

\>plot3d("d3",xmin=-5,xmax=3,ymin=-4,ymax=4);

\>insimg;


![images/Final%20Project%20Aplikom%20Semester%203-433.png](images/Final%20Project%20Aplikom%20Semester%203-433.png)

\>fcontour("d3",xmin=-4,xmax=1,ymin=-2,ymax=2,hue=1,title="The minimum is on A");

\>P=(A\_B\_C\_A)'; plot2d(P[1],P[2],add=1,color=12);

\>insimg;


![images/Final%20Project%20Aplikom%20Semester%203-434.png](images/Final%20Project%20Aplikom%20Semester%203-434.png)

2) Namun jika semua sudut segitiga ABC kurang dari 120°, maka nilai
minimumnya berada di titik F di bagian dalam segitiga, yang merupakan
satu-satunya titik yang sudut-sudut sisi ABC-nya sama (masing-masing
sudutnya 120°):


\>C=[-0.5,1];

\>plot3d("d3",xmin=-2,xmax=2,ymin=-2,ymax=2):


![images/Final%20Project%20Aplikom%20Semester%203-435.png](images/Final%20Project%20Aplikom%20Semester%203-435.png)

\>fcontour("d3",xmin=-2,xmax=2,ymin=-2,ymax=2,hue=1,title="The Fermat point");

\>P=(A\_B\_C\_A)'; plot2d(P[1],P[2],add=1,color=12);

\>insimg;


![images/Final%20Project%20Aplikom%20Semester%203-436.png](images/Final%20Project%20Aplikom%20Semester%203-436.png)

Merupakan aktivitas yang menarik untuk mewujudkan gambar di atas
dengan perangkat lunak geometri; misalnya, saya mengetahui perangkat
lunak yang ditulis dalam Java yang memiliki instruksi "garis
kontur"...


Semua ini ditemukan oleh seorang hakim Prancis bernama Pierre de
Fermat; ia menulis surat kepada para dilettan lain seperti pendeta
Marin Mersenne dan Blaise Pascal yang bekerja di pajak penghasilan.
Jadi titik unik F sehingga FA+FB+FC minimal, disebut titik Fermat dari
segitiga tersebut. Namun tampaknya beberapa tahun sebelumnya,
Torriccelli dari Italia telah menemukan titik ini sebelum Fermat
menemukannya! Bagaimanapun tradisinya adalah mencatat titik F ini...


## Empat titik

Langkah berikutnya adalah menambahkan titik ke-4 D dan mencoba
meminimalkan MA+MB+MC+MD; katakanlah Anda adalah operator TV kabel dan
ingin mencari di bidang mana Anda harus meletakkan antena Anda
sehingga Anda dapat menyalurkan sinyal ke empat desa dan menggunakan
panjang kabel sesedikit mungkin!


\>D=[1,1];

\>function d4(x,y):=d3(x,y)+sqrt((x-D[1])^2+(y-D[2])^2)

\>plot3d("d4",xmin=-1.5,xmax=1.5,ymin=-1.5,ymax=1.5):


![images/Final%20Project%20Aplikom%20Semester%203-437.png](images/Final%20Project%20Aplikom%20Semester%203-437.png)

\>fcontour("d4",xmin=-1.5,xmax=1.5,ymin=-1.5,ymax=1.5,hue=1);

\>P=(A\_B\_C\_D)'; plot2d(P[1],P[2],points=1,add=1,color=12);

\>insimg;


![images/Final%20Project%20Aplikom%20Semester%203-438.png](images/Final%20Project%20Aplikom%20Semester%203-438.png)

Masih terdapat nilai minimum dan tidak tercapai di titik A, B, C,
maupun D:


\>function f(x):=d4(x[1],x[2])

\>neldermin("f",[0.2,0.2])


    [0.142858,  0.142857]

Tampaknya dalam kasus ini, koordinat titik optimal bersifat rasional
atau mendekati rasional...


Sekarang ABCD adalah persegi, kita mengharapkan bahwa titik optimal
akan menjadi pusat ABCD:


\>C=[-1,1];

\>plot3d("d4",xmin=-1,xmax=1,ymin=-1,ymax=1):


![images/Final%20Project%20Aplikom%20Semester%203-439.png](images/Final%20Project%20Aplikom%20Semester%203-439.png)

\>fcontour("d4",xmin=-1.5,xmax=1.5,ymin=-1.5,ymax=1.5,hue=1);

\>P=(A\_B\_C\_D)'; plot2d(P[1],P[2],add=1,color=12,points=1);

\>insimg;


![images/Final%20Project%20Aplikom%20Semester%203-440.png](images/Final%20Project%20Aplikom%20Semester%203-440.png)

# Contoh 7: Bola Dandelin dengan Povray

Anda dapat menjalankan demonstrasi ini, jika Anda telah menginstal
Povray, dan pvengine.exe di jalur program.


Pertama, kita hitung jari-jari bola.


Jika Anda melihat gambar di bawah, Anda melihat bahwa kita memerlukan
dua lingkaran yang menyentuh dua garis yang membentuk kerucut, dan
satu garis yang membentuk bidang yang memotong kerucut.


Kami menggunakan file geometry.e milik Euler untuk ini.


\>load geometry;


Pertama dua garis membentuk kerucut.


\>g1 &= lineThrough([0,0],[1,a])


    
                                 [- a, 1, 0]
    

\>g2 &= lineThrough([0,0],[-1,a])


    
                                [- a, - 1, 0]
    

Lalu baris ketiga.


\>g &= lineThrough([-1,0],[1,1])


    
                                 [- 1, 2, 1]
    

Kita merencanakan segalanya sejauh ini.


\>setPlotRange(-1,1,0,2);

\>color(black); plotLine(g(),"")

\>a:=2; color(blue); plotLine(g1(),""), plotLine(g2(),""):


![images/Final%20Project%20Aplikom%20Semester%203-441.png](images/Final%20Project%20Aplikom%20Semester%203-441.png)

Sekarang kita ambil titik umum pada sumbu y.


\>P &= [0,u]


    
                                    [0, u]
    

Hitunglah jarak ke g1.


\>d1 &= distance(P,projectToLine(P,g1)); $d1


$$\sqrt{\left(\frac{a^2\,u}{a^2+1}-u\right)^2+\frac{a^2\,u^2}{\left(a
 ^2+1\right)^2}}$$Hitunglah jarak ke g.


\>d &= distance(P,projectToLine(P,g)); $d


$$\sqrt{\left(\frac{u+2}{5}-u\right)^2+\frac{\left(2\,u-1\right)^2}{
 25}}$$Dan temukan pusat kedua lingkaran, yang jaraknya sama.


\>sol &= solve(d1^2=d^2,u); $sol


$$\left[ u=\frac{-\sqrt{5}\,\sqrt{a^2+1}+2\,a^2+2}{4\,a^2-1} , u=
 \frac{\sqrt{5}\,\sqrt{a^2+1}+2\,a^2+2}{4\,a^2-1} \right] $$Ada dua solusi.


Kita mengevaluasi solusi simbolik, dan menemukan kedua pusat, dan
kedua jarak.


\>u := sol()


    [0.333333,  1]

\>dd := d()


    [0.149071,  0.447214]

Gambarkan lingkaran-lingkaran tersebut ke dalam gambar.


\>color(red);

\>plotCircle(circleWithCenter([0,u[1]],dd[1]),"");

\>plotCircle(circleWithCenter([0,u[2]],dd[2]),"");

\>insimg;


![images/Final%20Project%20Aplikom%20Semester%203-445.png](images/Final%20Project%20Aplikom%20Semester%203-445.png)

## Plot dengan Povray

Selanjutnya kita plot semuanya dengan Povray. Perhatikan bahwa Anda
mengubah perintah apa pun dalam urutan perintah Povray berikut, dan
menjalankan kembali semua perintah dengan Shift-Return.


Pertama-tama kita memuat fungsi povray.


\>load povray;

\>defaultpovray="C:\\Program Files\\POV-Ray\\v3.7\\bin\\pvengine.exe"


    C:\Program Files\POV-Ray\v3.7\bin\pvengine.exe

Kami menyiapkan suasananya dengan tepat.


\>povstart(zoom=11,center=[0,0,0.5],height=10°,angle=140°);


Berikutnya kita menulis kedua bola itu ke dalam file Povray.


\>writeln(povsphere([0,0,u[1]],dd[1],povlook(red)));

\>writeln(povsphere([0,0,u[2]],dd[2],povlook(red)));


Dan kerucutnya, transparan.


\>writeln(povcone([0,0,0],0,[0,0,a],1,povlook(lightgray,1)));


Kita buat bidang yang dibatasi pada kerucut.


\>gp=g();

\>pc=povcone([0,0,0],0,[0,0,a],1,"");

\>vp=[gp[1],0,gp[2]]; dp=gp[3];

\>writeln(povplane(vp,dp,povlook(blue,0.5),pc));


Sekarang kita buat dua titik pada lingkaran, di mana bola menyentuh
kerucut.


\>function turnz(v) := return [-v[2],v[1],v[3]]

\>P1=projectToLine([0,u[1]],g1()); P1=turnz([P1[1],0,P1[2]]);

\>writeln(povpoint(P1,povlook(yellow)));

\>P2=projectToLine([0,u[2]],g1()); P2=turnz([P2[1],0,P2[2]]);

\>writeln(povpoint(P2,povlook(yellow)));


Kemudian kita buat dua titik tempat bola-bola tersebut menyentuh
bidang. Titik-titik ini adalah fokus elips.


\>P3=projectToLine([0,u[1]],g()); P3=[P3[1],0,P3[2]];

\>writeln(povpoint(P3,povlook(yellow)));

\>P4=projectToLine([0,u[2]],g()); P4=[P4[1],0,P4[2]];

\>writeln(povpoint(P4,povlook(yellow)));


Berikutnya kita hitung perpotongan P1P2 dengan bidang.


\>t1=scalp(vp,P1)-dp; t2=scalp(vp,P2)-dp; P5=P1+t1/(t1-t2)\*(P2-P1);

\>writeln(povpoint(P5,povlook(yellow)));


Kita menghubungkan titik-titik dengan segmen garis.


\>writeln(povsegment(P1,P2,povlook(yellow)));

\>writeln(povsegment(P5,P3,povlook(yellow)));

\>writeln(povsegment(P5,P4,povlook(yellow)));


Sekarang kita buat pita abu-abu, di mana bola-bola menyentuh kerucut.


\>pcw=povcone([0,0,0],0,[0,0,a],1.01);

\>pc1=povcylinder([0,0,P1[3]-defaultpointsize/2],[0,0,P1[3]+defaultpointsize/2],1);

\>writeln(povintersection([pcw,pc1],povlook(gray)));

\>pc2=povcylinder([0,0,P2[3]-defaultpointsize/2],[0,0,P2[3]+defaultpointsize/2],1);

\>writeln(povintersection([pcw,pc2],povlook(gray)));


Mulai program Povray.


\>povend();


![images/Final%20Project%20Aplikom%20Semester%203-446.png](images/Final%20Project%20Aplikom%20Semester%203-446.png)

Untuk mendapatkan Anaglyph ini, kita perlu memasukkan semuanya ke
dalam fungsi scene. Fungsi ini akan digunakan dua kali nanti.


\>function scene () ...


    global a,u,dd,g,g1,defaultpointsize;
    writeln(povsphere([0,0,u[1]],dd[1],povlook(red)));
    writeln(povsphere([0,0,u[2]],dd[2],povlook(red)));
    writeln(povcone([0,0,0],0,[0,0,a],1,povlook(lightgray,1)));
    gp=g();
    pc=povcone([0,0,0],0,[0,0,a],1,"");
    vp=[gp[1],0,gp[2]]; dp=gp[3];
    writeln(povplane(vp,dp,povlook(blue,0.5),pc));
    P1=projectToLine([0,u[1]],g1()); P1=turnz([P1[1],0,P1[2]]);
    writeln(povpoint(P1,povlook(yellow)));
    P2=projectToLine([0,u[2]],g1()); P2=turnz([P2[1],0,P2[2]]);
    writeln(povpoint(P2,povlook(yellow)));
    P3=projectToLine([0,u[1]],g()); P3=[P3[1],0,P3[2]];
    writeln(povpoint(P3,povlook(yellow)));
    P4=projectToLine([0,u[2]],g()); P4=[P4[1],0,P4[2]];
    writeln(povpoint(P4,povlook(yellow)));
    t1=scalp(vp,P1)-dp; t2=scalp(vp,P2)-dp; P5=P1+t1/(t1-t2)*(P2-P1);
    writeln(povpoint(P5,povlook(yellow)));
    writeln(povsegment(P1,P2,povlook(yellow)));
    writeln(povsegment(P5,P3,povlook(yellow)));
    writeln(povsegment(P5,P4,povlook(yellow)));
    pcw=povcone([0,0,0],0,[0,0,a],1.01);
    pc1=povcylinder([0,0,P1[3]-defaultpointsize/2],[0,0,P1[3]+defaultpointsize/2],1);
    writeln(povintersection([pcw,pc1],povlook(gray)));
    pc2=povcylinder([0,0,P2[3]-defaultpointsize/2],[0,0,P2[3]+defaultpointsize/2],1);
    writeln(povintersection([pcw,pc2],povlook(gray)));
    endfunction
</pre>
Anda memerlukan kacamata merah/cyan untuk menghargai efek berikut.


\>povanaglyph("scene",zoom=11,center=[0,0,0.5],height=10°,angle=140°);


![images/Final%20Project%20Aplikom%20Semester%203-447.png](images/Final%20Project%20Aplikom%20Semester%203-447.png)

# Contoh 8: Geometri Bumi

Dalam buku catatan ini, kami ingin melakukan beberapa perhitungan
sferis. Fungsi-fungsi tersebut terdapat dalam berkas "spherical.e" di
folder contoh. Kami perlu memuat berkas tersebut terlebih dahulu.


\>load "spherical.e";


Untuk memasukkan posisi geografis, kami menggunakan vektor dengan dua
koordinat dalam radian (utara dan timur, nilai negatif untuk selatan
dan barat). Berikut ini adalah koordinat untuk Kampus FMIPA UNY.


\>FMIPA=[rad(-7,-46.467),rad(110,23.05)]


    [-0.13569,  1.92657]

Anda dapat mencetak posisi ini dengan sposprint (cetak posisi bulat).


\>sposprint(FMIPA) // posisi garis lintang dan garis bujur FMIPA UNY


    S 7°46.467' E 110°23.050'

Mari kita tambahkan dua kota lagi, Solo dan Semarang.


\>Solo=[rad(-7,-34.333),rad(110,49.683)]; Semarang=[rad(-6,-59.05),rad(110,24.533)];

\>sposprint(Solo), sposprint(Semarang),


    S 7°34.333' E 110°49.683'
    S 6°59.050' E 110°24.533'

Pertama, kita hitung vektor dari satu ke yang lain pada bola ideal.
Vektor ini adalah [arah, jarak] dalam radian. Untuk menghitung jarak
di bumi, kita kalikan dengan jari-jari bumi pada garis lintang 7°.


\>br=svector(FMIPA,Solo); degprint(br[1]), br[2]\*rearth(7°)-\>km // perkiraan jarak FMIPA-Solo


    65°20'26.60''
    53.8945384608

Ini adalah perkiraan yang bagus. Rutin berikut menggunakan perkiraan
yang lebih baik lagi. Pada jarak yang pendek, hasilnya hampir sama.


\>esdist(FMIPA,Semarang)-\>" km"; // perkiraan jarak FMIPA-Semarang


Ada fungsi untuk judul, yang memperhitungkan bentuk elips bumi. Sekali
lagi, kami mencetak dengan cara yang canggih.


\>sdegprint(esdir(FMIPA,Solo))


         65.34°

Sudut suatu segitiga melebihi 180° pada bola.


\>asum=sangle(Solo,FMIPA,Semarang)+sangle(FMIPA,Solo,Semarang)+sangle(FMIPA,Semarang,Solo); degprint(asum)


    180°0'10.77''

Ini dapat digunakan untuk menghitung luas segitiga. Catatan: Untuk
segitiga kecil, ini tidak akurat karena kesalahan pengurangan dalam
asum-pi.


\>(asum-pi)\*rearth(48°)^2-\>" km^2"; // perkiraan luas segitiga FMIPA-Solo-Semarang


Ada fungsi untuk ini, yang menggunakan lintang rata-rata segitiga
untuk menghitung jari-jari bumi, dan menangani kesalahan pembulatan
untuk segitiga yang sangat kecil.


\>esarea(Solo,FMIPA,Semarang)-\>" km^2", //perkiraan yang sama dengan fungsi esarea()


    2123.64310526 km^2

Kita juga dapat menambahkan vektor ke posisi. Vektor berisi arah dan
jarak, keduanya dalam radian. Untuk mendapatkan vektor, kita
menggunakan svector. Untuk menambahkan vektor ke posisi, kita
menggunakan saddvector.


\>v=svector(FMIPA,Solo); sposprint(saddvector(FMIPA,v)), sposprint(Solo),


    S 7°34.333' E 110°49.683'
    S 7°34.333' E 110°49.683'

Fungsi-fungsi ini mengasumsikan bentuk bola yang ideal. Sama halnya di
bumi.


\>sposprint(esadd(FMIPA,esdir(FMIPA,Solo),esdist(FMIPA,Solo))), sposprint(Solo),


    S 7°34.333' E 110°49.683'
    S 7°34.333' E 110°49.683'

Mari kita lihat contoh yang lebih besar, Tugu Jogja dan Monas Jakarta
(menggunakan Google Earth untuk mencari koordinatnya).


\>Tugu=[-7.7833°,110.3661°]; Monas=[-6.175°,106.811944°];

\>sposprint(Tugu), sposprint(Monas)


    S 7°46.998' E 110°21.966'
    S 6°10.500' E 106°48.717'

Menurut Google Earth, jaraknya adalah 429,66 km. Kami memperoleh
perkiraan yang baik.


\>esdist(Tugu,Monas)-\>" km"; // perkiraan jarak Tugu Jogja - Monas Jakarta


Judulnya sama dengan yang dihitung di Google Earth.


\>degprint(esdir(Tugu,Monas))


    294°17'2.85''

Akan tetapi, kita tidak lagi memperoleh posisi target yang tepat, jika
kita menambahkan arah dan jarak ke posisi awal. Hal ini terjadi karena
kita tidak menghitung fungsi invers secara tepat, tetapi mengambil
perkiraan radius bumi di sepanjang lintasan.


\>sposprint(esadd(Tugu,esdir(Tugu,Monas),esdist(Tugu,Monas)))


    S 6°10.500' E 106°48.717'

Namun, kesalahannya tidak besar.


\>sposprint(Monas),


    S 6°10.500' E 106°48.717'

Tentu saja, kita tidak dapat berlayar dengan arah yang sama dari satu
tujuan ke tujuan lain, jika kita ingin mengambil jalur terpendek.
Bayangkan, Anda terbang ke arah timur laut mulai dari titik mana pun
di bumi. Kemudian Anda akan berputar ke kutub utara. Lingkaran besar
tidak mengikuti arah yang konstan!


Perhitungan berikut menunjukkan bahwa kita jauh dari tujuan yang
benar, jika kita menggunakan arah yang sama selama perjalanan kita.


\>dist=esdist(Tugu,Monas); hd=esdir(Tugu,Monas);


Sekarang kita tambahkan 10 dikalikan sepersepuluh jaraknya, dengan
memakai arah ke Monas, kita sampai di Tugu.


\>p=Tugu; loop 1 to 10; p=esadd(p,hd,dist/10); end;


Hasilnya sangat jauh.


\>sposprint(p), skmprint(esdist(p,Monas))


    S 6°11.250' E 106°48.372'
         1.529km

Sebagai contoh lain, mari kita ambil dua titik di bumi pada garis
lintang yang sama.


\>P1=[30°,10°]; P2=[30°,50°];


Lintasan terpendek dari P1 ke P2 bukanlah lingkaran lintang 30°,
tetapi lintasan yang lebih pendek yang dimulai 10° lebih jauh ke utara
di P1.


\>sdegprint(esdir(P1,P2))


         79.69°

Namun, jika kita mengikuti pembacaan kompas ini, kita akan berputar ke
kutub utara! Jadi kita harus menyesuaikan arah kita di sepanjang
jalan. Untuk tujuan kasar, kita menyesuaikannya pada 1/10 dari total
jarak.


\>p=P1;  dist=esdist(P1,P2); ...  
\>     loop 1 to 10; dir=esdir(p,P2); sdegprint(dir), p=esadd(p,dir,dist/10); end;


         79.69°
         81.67°
         83.71°
         85.78°
         87.89°
         90.00°
         92.12°
         94.22°
         96.29°
         98.33°

Jaraknya tidak tepat, karena kita akan menambahkan sedikit kesalahan,
jika kita mengikuti arah yang sama terlalu lama.


\>skmprint(esdist(p,P2))


         0.203km

Kita memperoleh perkiraan yang baik, jika kita menyesuaikan arah
setelah setiap 1/100 jarak total dari Tugu ke Monas.


\>p=Tugu; dist=esdist(Tugu,Monas); ...  
\>     loop 1 to 100; p=esadd(p,esdir(p,Monas),dist/100); end;

\>skmprint(esdist(p,Monas))


         0.000km

Untuk keperluan navigasi, kita bisa mendapatkan urutan posisi GPS
sepanjang lingkaran besar menuju Monas dengan fungsi navigasi.


\>load spherical; v=navigate(Tugu,Monas,10); ...  
\>     loop 1 to rows(v); sposprint(v[#]), end;


    S 7°46.998' E 110°21.966'
    S 7°37.422' E 110°0.573'
    S 7°27.829' E 109°39.196'
    S 7°18.219' E 109°17.834'
    S 7°8.592' E 108°56.488'
    S 6°58.948' E 108°35.157'
    S 6°49.289' E 108°13.841'
    S 6°39.614' E 107°52.539'
    S 6°29.924' E 107°31.251'
    S 6°20.219' E 107°9.977'
    S 6°10.500' E 106°48.717'

Kita menulis suatu fungsi yang memplot bumi, dua posisi, dan posisi di
antaranya.


\>function testplot ...


    useglobal;
    plotearth;
    plotpos(Tugu,"Tugu Jogja"); plotpos(Monas,"Tugu Monas");
    plotposline(v);
    endfunction
</pre>
Sekarang rencanakan semuanya.


\>plot3d("testplot",angle=25, height=6,\>own,\>user,zoom=4):


![images/Final%20Project%20Aplikom%20Semester%203-448.png](images/Final%20Project%20Aplikom%20Semester%203-448.png)

Atau gunakan plot3d untuk mendapatkan tampilan anaglifnya. Ini tampak
sangat bagus dengan kaca mata merah/biru kehijauan.


\>plot3d("testplot",angle=25,height=6,distance=5,own=1,anaglyph=1,zoom=4):


![images/Final%20Project%20Aplikom%20Semester%203-449.png](images/Final%20Project%20Aplikom%20Semester%203-449.png)

# Latihan

1. Gambarlah segi-n beraturan jika diketahui titik pusat O, n, dan
jarak titik pusat ke titik-titik sudut segi-n tersebut (jari-jari
lingkaran luar segi-n), r.


Petunjuk:


* 
Besar sudut pusat yang menghadap masing-masing sisi segi-n adalah
* (360/n).

* 
Titik-titik sudut segi-n merupakan perpotongan lingkaran luar segi-n
* dan garis-garis yang melalui pusat dan saling membentuk sudut sebesar
* kelipatan (360/n).

* 
Untuk n ganjil, pilih salah satu titik sudut adalah di atas.

* 
Untuk n genap, pilih 2 titik di kanan dan kiri lurus dengan titik
* pusat.

* 
Anda dapat menggambar segi-3, 4, 5, 6, 7, dst beraturan.


\>load geometry


    Numerical and symbolic geometry.

\>setPlotRange(-3.5,3.5,-3.5,3.5);

\>A=[-2,-2]; plotPoint(A,"A");

\>B=[2,-2]; plotPoint(B,"B");

\>C=[0,3]; plotPoint(C,"C");

\>plotSegment(A,B,"c");

\>plotSegment(B,C,"a");

\>plotSegment(A,C,"b");

\>aspect(1):


![images/Final%20Project%20Aplikom%20Semester%203-450.png](images/Final%20Project%20Aplikom%20Semester%203-450.png)

\>c=circleThrough(A,B,C);

\>R=getCircleRadius(c);

\>O=getCircleCenter(c);

\>plotPoint(O,"O");

\>l=angleBisector(A,C,B);

\>color(2); plotLine(l); color(1);

\>plotCircle(c,"Lingkaran luar segitiga ABC"):


![images/Final%20Project%20Aplikom%20Semester%203-451.png](images/Final%20Project%20Aplikom%20Semester%203-451.png)

2. Gambarlah suatu parabola yang melalui 3 titik yang diketahui.


Petunjuk:


- Misalkan persamaan parabolanya y= ax^2+bx+c.


- Substitusikan koordinat titik-titik yang diketahui ke persamaan
tersebut.


- Selesaikan SPL yang terbentuk untuk mendapatkan nilai-nilai a, b, c.


\>load geometry;

\>setPlotRange(5); P=[2,0]; Q=[4,0]; R=[0,-4];

\>plotPoint(P,"P"); plotPoint(Q,"Q"); plotPoint(R,"R"):


![images/Final%20Project%20Aplikom%20Semester%203-452.png](images/Final%20Project%20Aplikom%20Semester%203-452.png)

\>sol &= solve([a+b=-c,16\*a+4\*b=-c,c=-4],[a,b,c])


    
                         [[a = - 1, b = 5, c = - 4]]
    

\>function y&=-x^2+5\*x-4


    
                                   2
                                - x  + 5 x - 4
    

\>plot2d("-x^2+5\*x-4",-5,5,-5,5):


![images/Final%20Project%20Aplikom%20Semester%203-453.png](images/Final%20Project%20Aplikom%20Semester%203-453.png)

3. Gambarlah suatu segi-4 yang diketahui keempat titik sudutnya,
misalnya A, B, C, D.


   - Tentukan apakah segi-4 tersebut merupakan segi-4 garis singgung
(sisinya-sisintya merupakan garis singgung lingkaran yang sama yakni
lingkaran dalam segi-4 tersebut).


   - Suatu segi-4 merupakan segi-4 garis singgung apabila keempat
garis bagi sudutnya bertemu di satu titik.


   - Jika segi-4 tersebut merupakan segi-4 garis singgung, gambar
lingkaran dalamnya.


   - Tunjukkan bahwa syarat suatu segi-4 merupakan segi-4 garis
singgung apabila hasil kali panjang sisi-sisi yang berhadapan sama.


\>load geometry


    Numerical and symbolic geometry.

\>setPlotRange(-4.5,4.5,-4.5,4.5);

\>A=[-3,-3]; plotPoint(A,"A");

\>B=[3,-3]; plotPoint(B,"B");

\>C=[3,3]; plotPoint(C,"C");

\>D=[-3,3]; plotPoint(D,"D");

\>plotSegment(A,B,"");

\>plotSegment(B,C,"");

\>plotSegment(C,D,"");

\>plotSegment(A,D,"");

\>aspect(1):


![images/Final%20Project%20Aplikom%20Semester%203-454.png](images/Final%20Project%20Aplikom%20Semester%203-454.png)

\>l=angleBisector(A,B,C);

\>m=angleBisector(B,C,D);

\>P=lineIntersection(l,m);

\>color(5); plotLine(l); plotLine(m); color(1);

\>plotPoint(P,"P"):


![images/Final%20Project%20Aplikom%20Semester%203-455.png](images/Final%20Project%20Aplikom%20Semester%203-455.png)

Dari gambar diatas terlihat bahwa keempat garis bagi sudutnya bertemu
di satu titik yaitu titik P.


\>r=norm(P-projectToLine(P,lineThrough(A,B)));

\>plotCircle(circleWithCenter(P,r),"Lingkaran dalam segiempat ABCD"):


![images/Final%20Project%20Aplikom%20Semester%203-456.png](images/Final%20Project%20Aplikom%20Semester%203-456.png)

Dari gambar diatas, terlihat bahwa sisi-sisinya merupakan garis
singgung lingkaran yang sama yaitu lingkaran dalam segiempat.


Akan ditunjukkan bahwa hasil kali panjang sisi-sisi yang berhadapan
sama.


\>AB=norm(A-B) //panjang sisi AB


    6

\>CD=norm(C-D) //panjang sisi CD


    6

\>AD=norm(A-D) //panjang sisi AD


    6

\>BC=norm(B-C) //panjang sisi BC


    6

\>AB.CD


    36

\>AD.BC


    36

Terbukti bahwa hasil kali panjang sisi-sisi yang berhadapan sama yaitu
36. Jadi dapat dipastikan bahwa segiempat tersebut merupakan segiempat
garis singgung.


4. Gambarlah suatu ellips jika diketahui kedua titik fokusnya,
misalnya P dan Q. Ingat ellips dengan fokus P dan Q adalah tempat
kedudukan titik-titik yang jumlah jarak ke P dan ke Q selalu sama
(konstan).


Penyelesaian :


Diketahui kedua titik fokus P = [-1,-1] dan Q = [1,-1]


\>P=[-1,-1]; Q=[1,-1];

\>function d1(x,y):=sqrt((x-P[1])^2+(y-P[2])^2)

\>Q=[1,-1]; function d2(x,y):=sqrt((x-P[1])^2+(y-P[2])^2)+sqrt((x-Q[1])^2+(y-Q[2])^2)

\>fcontour("d2",xmin=-2,xmax=2,ymin=-3,ymax=1,hue=1):


![images/Final%20Project%20Aplikom%20Semester%203-457.png](images/Final%20Project%20Aplikom%20Semester%203-457.png)

Grafik yang lebih menarik


\>plot3d("d2",xmin=-2,xmax=2,ymin=-3,ymax=1):


![images/Final%20Project%20Aplikom%20Semester%203-458.png](images/Final%20Project%20Aplikom%20Semester%203-458.png)

Batasan ke garis PQ


\>plot2d("abs(x+1)+abs(x-1)",xmin=-3,xmax=3):


![images/Final%20Project%20Aplikom%20Semester%203-459.png](images/Final%20Project%20Aplikom%20Semester%203-459.png)

5. Gambarlah suatu hiperbola jika diketahui kedua titik fokusnya,
misalnya P dan Q. Ingat ellips dengan fokus P dan Q adalah tempat
kedudukan titik-titik yang selisih jarak ke P dan ke Q selalu sama
(konstan).


\>P=[-1,-1]; Q=[1,-1];

\>function d1(x,y):=sqrt((x-p[1])^2+(y-p[2])^2)

\>Q=[1,-1]; function d2(x,y):=sqrt((x-P[1])^2+(y-P[2])^2)+sqrt((x+Q[1])^2+(y+Q[2])^2)

\>fcontour("d2",xmin=-2,xmax=2,ymin=-3,ymax=1,hue=1):


![images/Final%20Project%20Aplikom%20Semester%203-460.png](images/Final%20Project%20Aplikom%20Semester%203-460.png)

\>plot3d("d2",xmin=-2,xmax=2,ymin=-3,ymax=1):


![images/Final%20Project%20Aplikom%20Semester%203-461.png](images/Final%20Project%20Aplikom%20Semester%203-461.png)

\>plot2d("abs(x+1)+abs(x-1)",xmin=-3,xmax=3):


![images/Final%20Project%20Aplikom%20Semester%203-462.png](images/Final%20Project%20Aplikom%20Semester%203-462.png)

\>load geometry


    Numerical and symbolic geometry.

\>setPlotRange(-5,10,-5,10);

\>A=[1,8]; plotPoint(A,"A");

\>B=[-1,2]; plotPoint(B,"B");

\>C=[3,2]; plotPoint(C,"C");

\>plotSegment(A,B,"c");

\>plotSegment(B,C,"a");

\>plotSegment(A,C,"b");

\>lineThrough(B,C)


    [0,  4,  8]

\>h=perpendicular(A,lineThrough(B,C));

\>D=lineIntersection(h,lineThrough(B,C));

\>plotPoint(D,value=1); // koordinat D ditampilkan

\>aspect(1); plotSegment(A,D): // tampilkan semua gambar hasil plot...()


![images/Final%20Project%20Aplikom%20Semester%203-463.png](images/Final%20Project%20Aplikom%20Semester%203-463.png)

\>distance(A,D)\*distance(B,C)/2


    12

\>c=circleThrough(A,B,C); // lingkaran luar segitiga ABC

\>R=getCircleRadius(c); // jari2 lingkaran luar

\>O=getCircleCenter(c); // titik pusat lingkaran c

\>plotPoint(O,"O"); // gambar titik "O"

\>plotCircle(c,"Lingkaran luar segitiga ABC"):


![images/Final%20Project%20Aplikom%20Semester%203-464.png](images/Final%20Project%20Aplikom%20Semester%203-464.png)

\>O, R


    [1,  4.66667]
    3.33333333333

\>l=angleBisector(A,C,B); // garis bagi <ACB

\>g=angleBisector(C,A,B); // garis bagi <CAB

\>P=lineIntersection(l,g) // titik potong kedua garis bagi sudut


    [1,  3.44152]

# EMT untuk Statistika

Dalam buku catatan ini, kami mendemonstrasikan plot statistik utama,
tes dan distribusi dalam Euler.


Mari kita mulai dengan beberapa statistik deskriptif. Ini bukanlah
sebuah pengantar statistik. Jadi, Anda mungkin memerlukan beberapa
latar belakang untuk memahami detailnya.


Asumsikan pengukuran berikut ini. Kita ingin menghitung nilai
rata-rata dan deviasi standar yang diukur.


\>M=[1000,1004,998,997,1002,1001,998,1004,998,997]; ...  
\>   median(M), mean(M), dev(M),


    999
    999.9
    2.72641400622

Kita dapat memplot plot kotak dan kumis untuk data tersebut. Dalam
kasus kami, tidak ada pencilan.


\>aspect(1.75); boxplot(M):


![images/Final%20Project%20Aplikom%20Semester%203-465.png](images/Final%20Project%20Aplikom%20Semester%203-465.png)

Kami menghitung probabilitas bahwa suatu nilai lebih besar dari 1005,
dengan mengasumsikan nilai yang diukur dari distribusi normal.


Semua fungsi untuk distribusi dalam Euler diakhiri dengan ...dis dan
menghitung distribusi probabilitas kumulatif (CPF).


Kami mencetak hasilnya dalam % dengan akurasi 2 digit menggunakan
fungsi cetak.


\>print((1-normaldis(1005,mean(M),dev(M)))\*100,2,unit=" %")


          3.07 %

Untuk contoh berikutnya, kami mengasumsikan jumlah pria berikut ini
dalam rentang ukuran tertentu.


\>r=155.5:4:187.5; v=[22,71,136,169,139,71,32,8];


Berikut ini adalah plot distribusinya.


\>plot2d(r,v,a=150,b=200,c=0,d=190,bar=1,style="\\/"):


![images/Final%20Project%20Aplikom%20Semester%203-466.png](images/Final%20Project%20Aplikom%20Semester%203-466.png)

Kita dapat memasukkan data mentah tersebut ke dalam tabel.


Tabel adalah sebuah metode untuk menyimpan data statistik. Tabel kita
harus berisi tiga kolom: Awal rentang, akhir rentang, jumlah orang
dalam rentang.


Tabel dapat dicetak dengan header. Kami menggunakan vektor string
untuk mengatur header.


\>T:=r[1:8]' | r[2:9]' | v'; writetable(T,labc=["BB","BA","Frek"])


            BB        BA      Frek
         155.5     159.5        22
         159.5     163.5        71
         163.5     167.5       136
         167.5     171.5       169
         171.5     175.5       139
         175.5     179.5        71
         179.5     183.5        32
         183.5     187.5         8

Jika kita membutuhkan nilai rata-rata dan statistik lain dari ukuran,
kita perlu menghitung titik tengah rentang. Kita dapat menggunakan dua
kolom pertama dari tabel kita untuk hal ini.


Sumbol “|” digunakan untuk memisahkan kolom, fungsi “writetable”
digunakan untuk menulis tabel, dengan opsi “labc” untuk menentukan
judul kolom.


\>(T[,1]+T[,2])/2 // the midpoint of each interval


            157.5 
            161.5 
            165.5 
            169.5 
            173.5 
            177.5 
            181.5 
            185.5 

Tetapi akan lebih mudah, untuk melipat rentang dengan vektor
[1/2,1/2].


\>M=fold(r,[0.5,0.5])


    [157.5,  161.5,  165.5,  169.5,  173.5,  177.5,  181.5,  185.5]

Sekarang kita dapat menghitung rata-rata dan deviasi sampel dengan
frekuensi yang diberikan.


\>{m,d}=meandev(M,v); m, d,


    169.901234568
    5.98912964449

Mari kita tambahkan distribusi normal dari nilai-nilai tersebut ke
dalam diagram batang di atas. Rumus untuk distribusi normal dengan
rata-rata m dan deviasi standar d adalah:


Karena nilainya antara 0 dan 1, untuk memplotnya pada diagram batang,
nilai tersebut harus dikalikan dengan 4 kali jumlah data.


\>plot2d("qnormal(x,m,d)\*sum(v)\*4", ...  
\>     xmin=min(r),xmax=max(r),thickness=3,add=1):


![images/Final%20Project%20Aplikom%20Semester%203-467.png](images/Final%20Project%20Aplikom%20Semester%203-467.png)

# Tabel

Dalam direktori buku catatan ini, Anda dapat menemukan file dengan
tabel. Data tersebut mewakili hasil survei. Berikut adalah empat baris
pertama dari file tersebut. Data berasal dari buku online berbahasa
Jerman “Einführung in die Statistik mit R” oleh A. Handl.


\>printfile("table.dat",4);


    Could not open the file
    table.dat
    for reading!
    Try "trace errors" to inspect local variables after errors.
    printfile:
        open(filename,"r");

Tabel berisi 7 kolom angka atau token (string). Kita ingin membaca
tabel tersebut dari file. Pertama, kita menggunakan terjemahan kita
sendiri untuk token-token tersebut.


Untuk itu, kita mendefinisikan set token. Fungsi strtokens()
mendapatkan vektor string token dari string yang diberikan.


\>mf:=["m","f"]; yn:=["y","n"]; ev:=strtokens("g vg m b vb");


Sekarang kita membaca tabel dengan terjemahan ini.


Argumen tok2, tok4, dan lain-lain adalah terjemahan dari kolom-kolom
tabel. Argumen-argumen ini tidak ada dalam daftar parameter
readtable(), jadi Anda harus menyediakannya dengan “:=”.


\>{MT,hd}=readtable("table.dat",tok2:=mf,tok4:=yn,tok5:=ev,tok7:=yn);


    Could not open the file
    table.dat
    for reading!
    Try "trace errors" to inspect local variables after errors.
    readtable:
        if filename!=none then open(filename,"r"); endif;

\>load over statistics;


Untuk mencetak, kita perlu menentukan set token yang sama. Kami
mencetak empat baris pertama saja.


\>writetable(MT[1:10],labc=hd,wc=5,tok2:=mf,tok4:=yn,tok5:=ev,tok7:=yn);


    MT is not a variable!
    Error in:
    writetable(MT[1:10],labc=hd,wc=5,tok2:=mf,tok4:=yn,tok5:=ev,to ...
                       ^

Tanda titik “.” mewakili nilai yang tidak tersedia.


Jika kita tidak ingin menentukan token untuk terjemahan sebelumnya,
kita hanya perlu menentukan kolom mana yang berisi token dan bukan
angka.


\>ctok=[2,4,5,7]; {MT,hd,tok}=readtable("table.dat",ctok=ctok);


    Could not open the file
    table.dat
    for reading!
    Try "trace errors" to inspect local variables after errors.
    readtable:
        if filename!=none then open(filename,"r"); endif;

Fungsi readtable() sekarang mengembalikan satu set token.


\>tok


    Variable tok not found!
    Error in:
    tok ...
       ^

Tabel berisi entri dari file dengan token yang diterjemahkan ke angka.


String khusus NA=“.” ditafsirkan sebagai “Tidak Tersedia”, dan
mendapatkan NAN (bukan angka) dalam tabel. Terjemahan ini dapat diubah
dengan parameter NA, dan NAval.


\>MT[1]


    MT is not a variable!
    Error in:
    MT[1] ...
         ^

Berikut ini adalah isi tabel dengan angka yang tidak diterjemahkan.


\>writetable(MT,wc=5)


    Variable or function MT not found.
    Error in:
    writetable(MT,wc=5) ...
                 ^

Untuk kenyamanan, Anda dapat menaruh output dari readtable() ke dalam
sebuah daftar.


\>Table={{readtable("table.dat",ctok=ctok)}};


    Could not open the file
    table.dat
    for reading!
    Try "trace errors" to inspect local variables after errors.
    readtable:
        if filename!=none then open(filename,"r"); endif;

Dengan menggunakan kolom token yang sama dan token yang dibaca dari
file, kita dapat mencetak tabel. Kita dapat menentukan ctok, tok, dll.
atau menggunakan daftar Tabel.


\>writetable(Table,ctok=ctok,wc=5);


    Variable or function Table not found.
    Error in:
    writetable(Table,ctok=ctok,wc=5); ...
                    ^

Fungsi tablecol() mengembalikan nilai kolom dari tabel, melewatkan
setiap baris dengan nilai NAN (“.” dalam file), dan indeks kolom, yang
berisi nilai-nilai ini.


\>{c,i}=tablecol(MT,[5,6]);


    Variable or function MT not found.
    Error in:
    {c,i}=tablecol(MT,[5,6]); ...
                     ^

Kita dapat menggunakan ini untuk mengekstrak kolom dari tabel untuk
tabel baru.


\>j=[1,5,6]; writetable(MT[i,j],labc=hd[j],ctok=[2],tok=tok)


    MT is not a variable!
    Error in:
    j=[1,5,6]; writetable(MT[i,j],labc=hd[j],ctok=[2],tok=tok) ...
                                 ^

Tentu saja, kita perlu mengekstrak tabel itu sendiri dari daftar Tabel
dalam kasus ini.


\>MT=Table[1];


    Table is not a variable!
    Error in:
    MT=Table[1]; ...
               ^

Tentu saja, kita juga dapat menggunakannya untuk menentukan nilai
rata-rata kolom atau nilai statistik lainnya.


\>mean(tablecol(MT,6))


    Variable or function MT not found.
    Error in:
    mean(tablecol(MT,6)) ...
                    ^

Fungsi getstatistics() mengembalikan elemen-elemen dalam sebuah
vektor, dan jumlahnya. Kita menerapkannya pada nilai “m” dan “f” pada
kolom kedua tabel kita.


\>{xu,count}=getstatistics(tablecol(MT,2)); xu, count,


    Variable or function MT not found.
    Error in:
    {xu,count}=getstatistics(tablecol(MT,2)); xu, count, ...
                                        ^

Kita bisa mencetak hasilnya dalam tabel baru.


\>writetable(count',labr=tok[xu])


    Variable count not found!
    Error in:
    writetable(count',labr=tok[xu]) ...
                     ^

Fungsi selecttable() mengembalikan sebuah tabel baru dengan nilai
dalam satu kolom yang dipilih dari vektor indeks. Pertama, kita
mencari indeks dari dua nilai kita dalam tabel token.


\>v:=indexof(tok,["g","vg"])


    Variable or function tok not found.
    Error in:
    v:=indexof(tok,["g","vg"]) ...
                  ^

Sekarang kita dapat memilih baris-baris dari tabel, yang memiliki
salah satu nilai dalam v di baris ke-5.


\>MT1:=MT[selectrows(MT,5,v)]; i:=sortedrows(MT1,5);


    Variable or function MT not found.
    Error in:
    MT1:=MT[selectrows(MT,5,v)]; i:=sortedrows(MT1,5); ...
                         ^

Sekarang kita dapat mencetak tabel, dengan nilai yang diekstrak dan
diurutkan di kolom ke-5.


\>writetable(MT1[i],labc=hd,ctok=ctok,tok=tok,wc=7);


    MT1 is not a variable!
    Error in:
    writetable(MT1[i],labc=hd,ctok=ctok,tok=tok,wc=7); ...
                     ^

Untuk statistik berikutnya, kita ingin menghubungkan dua kolom tabel.
Jadi kita mengekstrak kolom 2 dan 4 dan mengurutkan tabel.


\>i=sortedrows(MT,[2,4]);  ...  
\>     writetable(tablecol(MT[i],[2,4])',ctok=[1,2],tok=tok)


    Variable or function MT not found.
    Error in:
    i=sortedrows(MT,[2,4]);    writetable(tablecol(MT[i],[2,4])',c ...
                   ^

Dengan getstatistics(), kita juga dapat menghubungkan hitungan dalam
dua kolom tabel satu sama lain.


\>MT24=tablecol(MT,[2,4]); ...  
\>   {xu1,xu2,count}=getstatistics(MT24[1],MT24[2]); ...  
\>   writetable(count,labr=tok[xu1],labc=tok[xu2])


    Variable or function MT not found.
    Error in:
    MT24=tablecol(MT,[2,4]); {xu1,xu2,count}=getstatistics(MT24[1] ...
                    ^

Tabel dapat ditulis ke sebuah file.


\>filename="test.dat"; ...  
\>   writetable(count,labr=tok[xu1],labc=tok[xu2],file=filename);


    Variable or function count not found.
    Error in:
    filename="test.dat"; writetable(count,labr=tok[xu1],labc=tok[x ...
                                         ^

Kemudian kita dapat membaca tabel dari file tersebut.


\>{MT2,hd,tok2,hdr}=readtable(filename,\>clabs,\>rlabs); ...  
\>   writetable(MT2,labr=hdr,labc=hd)


    Could not open the file
    test.dat
    for reading!
    Try "trace errors" to inspect local variables after errors.
    readtable:
        if filename!=none then open(filename,"r"); endif;

Dan hapus file tersebut.


\>fileremove(filename);


# Distribusi

Dengan plot2d, ada metode yang sangat mudah untuk memplot distribusi
data eksperimen.


\>p=normal(1,1000); //1000 random normal-distributed sample p

\>plot2d(p,distribution=20,style="\\/"); // plot the random sample p

\>plot2d("qnormal(x,0,1)",add=1): // add the standard normal distribution plot


![images/Final%20Project%20Aplikom%20Semester%203-468.png](images/Final%20Project%20Aplikom%20Semester%203-468.png)

Perhatikan perbedaan antara plot batang (sampel) dan kurva normal
(distribusi sesungguhnya). Masukkan kembali ketiga perintah tersebut
untuk melihat hasil pengambilan sampel yang lain.


Berikut ini adalah perbandingan 10 simulasi dari 1000 nilai
terdistribusi normal dengan menggunakan apa yang disebut plot kotak.
Plot ini menunjukkan median, kuartil 25% dan 75%, nilai minimal dan
maksimal, serta pencilan.


\>p=normal(10,1000); boxplot(p):


![images/Final%20Project%20Aplikom%20Semester%203-469.png](images/Final%20Project%20Aplikom%20Semester%203-469.png)

Untuk menghasilkan bilangan bulat acak, Euler memiliki intrandom. Mari
kita simulasikan pelemparan dadu dan memplot distribusinya.


Kita menggunakan fungsi getmultiplicities(v,x), yang menghitung
seberapa sering elemen-elemen dari v muncul di dalam x. Kemudian kita
memplot hasilnya menggunakan columnsplot().


\>k=intrandom(1,6000,6);  ...  
\>   columnsplot(getmultiplicities(1:6,k));  ...  
\>   ygrid(1000,color=red):


![images/Final%20Project%20Aplikom%20Semester%203-470.png](images/Final%20Project%20Aplikom%20Semester%203-470.png)

Meskipun intrandom(n,m,k) menghasilkan bilangan bulat yang
terdistribusi secara seragam dari 1 sampai k, adalah mungkin untuk
menggunakan distribusi bilangan bulat yang lain dengan randpint().


Pada contoh berikut, probabilitas untuk 1,2,3 adalah 0.4, 0.1, 0.5
secara berurutan.


\>randpint(1,1000,[0.4,0.1,0.5]); getmultiplicities(1:3,%)


    [391,  105,  504]

Euler dapat menghasilkan nilai acak dari lebih banyak distribusi.
Lihatlah ke dalam referensi.


Misalnya, kita mencoba distribusi eksponensial. Sebuah variabel acak
kontinu X dikatakan memiliki distribusi eksponensial, jika PDF-nya
diberikan oleh




with parameter


\>plot2d(randexponential(1,1000,2),\>distribution):


![images/Final%20Project%20Aplikom%20Semester%203-471.png](images/Final%20Project%20Aplikom%20Semester%203-471.png)

Untuk banyak distribusi, Euler dapat menghitung fungsi distribusi dan
kebalikannya.


\>plot2d("normaldis",-4,4): 


![images/Final%20Project%20Aplikom%20Semester%203-472.png](images/Final%20Project%20Aplikom%20Semester%203-472.png)

Berikut ini adalah salah satu cara untuk memplot kuantil.


\>plot2d("qnormal(x,1,1.5)",-4,6);  ...  
\>   plot2d("qnormal(x,1,1.5)",a=2,b=5,\>add,\>filled):


![images/Final%20Project%20Aplikom%20Semester%203-473.png](images/Final%20Project%20Aplikom%20Semester%203-473.png)



Probabilitas untuk berada di area hijau adalah sebagai berikut.


\>normaldis(5,1,1.5)-normaldis(2,1,1.5)


    0.248662156979

Hal ini dapat dihitung secara numerik dengan integral berikut ini.


\>gauss("qnormal(x,1,1.5)",2,5)


    0.248662156979

Mari kita bandingkan distribusi binomial dengan distribusi normal
dengan rata-rata dan deviasi yang sama. Fungsi invbindis()
menyelesaikan interpolasi linier antara nilai bilangan bulat.


\>invbindis(0.95,1000,0.5), invnormaldis(0.95,500,0.5\*sqrt(1000))


    525.516721219
    526.007419394

Fungsi qdis() adalah densitas dari distribusi chi-square. Seperti
biasa, Euler memetakan vektor ke fungsi ini. Dengan demikian kita
mendapatkan plot semua distribusi chi-kuadrat dengan derajat 5 hingga
30 dengan mudah dengan cara berikut.


\>plot2d("qchidis(x,(5:5:50)')",0,50):


![images/Final%20Project%20Aplikom%20Semester%203-474.png](images/Final%20Project%20Aplikom%20Semester%203-474.png)

Euler memiliki fungsi-fungsi yang akurat untuk mengevaluasi
distribusi-distribusi. Mari kita periksa chidis() dengan sebuah
integral.


Penamaannya diusahakan untuk konsisten. Sebagai contoh,


* 
distribusi chi-kuadrat adalah chidis(),

* 
fungsi kebalikannya adalah invchidis(),

* 
densitasnya adalah qchidis().


Pelengkap dari distribusi (ekor atas) adalah chicdis().


\>chidis(1.5,2), integrate("qchidis(x,2)",0,1.5)


    0.527633447259
    0.527633447259

# Distribusi Diskrit

Untuk menentukan distribusi diskrit Anda sendiri, Anda dapat
menggunakan metode berikut.


Pertama, kita tetapkan fungsi distribusinya.


\>wd = 0|((1:6)+[-0.01,0.01,0,0,0,0])/6


    [0,  0.165,  0.335,  0.5,  0.666667,  0.833333,  1]

Artinya, dengan probabilitas wd[i+1]-wd[i] kita menghasilkan nilai
acak i.


Ini hampir merupakan distribusi yang seragam. Mari kita definisikan
sebuah generator bilangan acak untuk ini. Fungsi find(v,x) menemukan
nilai x dalam vektor v. Fungsi ini juga dapat digunakan untuk vektor
x.


\>function wrongdice (n,m) := find(wd,random(n,m))


Kesalahan ini sangat halus sehingga kita hanya bisa melihatnya setelah
melakukan iterasi yang sangat banyak.


\>columnsplot(getmultiplicities(1:6,wrongdice(1,1000000))):


![images/Final%20Project%20Aplikom%20Semester%203-475.png](images/Final%20Project%20Aplikom%20Semester%203-475.png)

Berikut ini adalah fungsi sederhana untuk memeriksa distribusi seragam
dari nilai 1... K dalam v. Kami menerima hasilnya, jika untuk semua
frekuensi


\>function checkrandom (v, delta=1) ...


      K=max(v); n=cols(v);
      fr=getfrequencies(v,1:K);
      return max(fr/n-1/K)<delta/sqrt(n);
      endfunction
</pre>
Memang fungsi ini menolak distribusi seragam.


\>checkrandom(wrongdice(1,1000000))


    0

Dan ini menerima generator acak bawaan.


\>checkrandom(intrandom(1,1000000,6))


    1

Kita dapat menghitung distribusi binomial. Pertama, ada binomialsum(),
yang mengembalikan probabilitas i atau kurang dari n percobaan.


\>bindis(410,1000,0.4)


    0.751401349654

Fungsi Beta invers digunakan untuk menghitung interval kepercayaan
Clopper-Pearson untuk parameter p. Tingkat defaultnya adalah alpha.


Arti dari interval ini adalah jika p berada di luar interval, hasil
yang diamati sebesar 410 dalam 1000 jarang terjadi.


\>clopperpearson(410,1000)


    [0.37932,  0.441212]

Perintah berikut ini adalah cara langsung untuk mendapatkan hasil di
atas. Tetapi untuk n yang besar, penjumlahan langsung tidak akurat dan
lambat.


\>p=0.4; i=0:410; n=1000; sum(bin(n,i)\*p^i\*(1-p)^(n-i))


    0.751401349655

Omong-omong, invbinsum() menghitung kebalikan dari binomialsum().


\>invbindis(0.75,1000,0.4)


    409.932733047

Dalam Bridge, kita mengasumsikan 5 kartu yang terbuka (dari 52 kartu)
di dua tangan (26 kartu). Mari kita hitung probabilitas distribusi
yang lebih buruk dari 3:2 (misalnya 0:5, 1:4, 4:1, atau 5:0).


\>2\*hypergeomsum(1,5,13,26)


    0.321739130435

Ada juga simulasi distribusi multinomial.


\>randmultinomial(10,1000,[0.4,0.1,0.5])


              419            99           482 
              407           103           490 
              397            93           510 
              419            97           484 
              412           103           485 
              404            99           497 
              400           105           495 
              368           127           505 
              414            96           490 
              377           125           498 

# Memplot Data

Untuk memplot data, kami mencoba hasil pemilihan umum Jerman sejak
tahun 1990, yang diukur dalam kursi.


\>BW := [ ...  
\>   1990,662,319,239,79,8,17; ...  
\>   1994,672,294,252,47,49,30; ...  
\>   1998,669,245,298,43,47,36; ...  
\>   2002,603,248,251,47,55,2; ...  
\>   2005,614,226,222,61,51,54; ...  
\>   2009,622,239,146,93,68,76; ...  
\>   2013,631,311,193,0,63,64];


Untuk pesta, kami menggunakan serangkaian nama.


\>P:=["CDU/CSU","SPD","FDP","Gr","Li"];


Mari kita cetak persentasenya dengan baik.


Pertama kita ekstrak kolom-kolom yang diperlukan. Kolom 3 sampai 7
adalah kursi masing-masing partai, dan kolom 2 adalah jumlah total
kursi. kolom adalah tahun pemilihan.


\>BT:=BW[,3:7]; BT:=BT/sum(BT); YT:=BW[,1]';


Kemudian kita mencetak statistik dalam bentuk tabel. Kita menggunakan
nama sebagai judul kolom, dan tahun sebagai judul baris. Lebar default
untuk kolom adalah wc = 10, tetapi kami lebih suka output yang lebih
padat. Kolom-kolom akan diperluas untuk label-label kolom, jika perlu.


\>writetable(BT\*100,wc=6,dc=0,\>fixed,labc=P,labr=YT)


           CDU/CSU   SPD   FDP    Gr    Li
      1990      48    36    12     1     3
      1994      44    38     7     7     4
      1998      37    45     6     7     5
      2002      41    42     8     9     0
      2005      37    36    10     8     9
      2009      38    23    15    11    12
      2013      49    31     0    10    10

Perkalian matriks berikut ini mengekstrak jumlah persentase dua partai
besar yang menunjukkan bahwa partai-partai kecil telah memperoleh
suara di parlemen hingga tahun 2009.


\>BT1:=(BT.[1;1;0;0;0])'\*100


    [84.29,  81.25,  81.1659,  82.7529,  72.9642,  61.8971,  79.8732]

Ada juga plot statistik sederhana. Kita menggunakannya untuk
menampilkan garis dan titik secara bersamaan. Alternatif lainnya
adalah memanggil plot2d dua kali dengan &gt;add.


\>statplot(YT,BT1,"b"):


![images/Final%20Project%20Aplikom%20Semester%203-476.png](images/Final%20Project%20Aplikom%20Semester%203-476.png)

Tentukan beberapa warna untuk masing-masing pihak.


\>CP:=[rgb(0.5,0.5,0.5),red,yellow,green,rgb(0.8,0,0)];


Sekarang kita dapat memplot hasil pemilu 2009 dan perubahannya ke
dalam satu plot menggunakan figure. Kita dapat menambahkan vektor
kolom pada setiap plot.


\>figure(2,1);  ...  
\>   figure(1); columnsplot(BW[6,3:7],P,color=CP); ...  
\>   figure(2); columnsplot(BW[6,3:7]-BW[5,3:7],P,color=CP);  ...  
\>   figure(0):


![images/Final%20Project%20Aplikom%20Semester%203-477.png](images/Final%20Project%20Aplikom%20Semester%203-477.png)

Plot data menggabungkan baris data statistik dalam satu plot.


\>J:=BW[,1]'; DP:=BW[,3:7]'; ...  
\>   dataplot(YT,BT',color=CP);  ...  
\>   labelbox(P,colors=CP,styles="[]",\>points,w=0.2,x=0.3,y=0.4):


![images/Final%20Project%20Aplikom%20Semester%203-478.png](images/Final%20Project%20Aplikom%20Semester%203-478.png)

Plot kolom 3D menunjukkan deretan data statistik dalam bentuk kolom.
Kami menyediakan label untuk baris dan kolom. angle adalah sudut
pandang.


\>columnsplot3d(BT,scols=P,srows=YT, ...  
\>     angle=30°,ccols=CP):


![images/Final%20Project%20Aplikom%20Semester%203-479.png](images/Final%20Project%20Aplikom%20Semester%203-479.png)

Representasi lainnya adalah plot mosaik. Perhatikan bahwa kolom-kolom
pada plot mewakili kolom-kolom pada matriks di sini. Karena panjangnya
label CDU/CSU, kita mengambil jendela yang lebih kecil dari biasanya.


\>shrinkwindow(\>smaller);  ...  
\>   mosaicplot(BT',srows=YT,scols=P,color=CP,style="#"); ...  
\>   shrinkwindow():


![images/Final%20Project%20Aplikom%20Semester%203-480.png](images/Final%20Project%20Aplikom%20Semester%203-480.png)

Kita juga bisa membuat diagram lingkaran. Karena warna hitam dan
kuning membentuk sebuah koalisi, kita menyusun ulang elemen-elemennya.


\>i=[1,3,5,4,2]; piechart(BW[6,3:7][i],color=CP[i],lab=P[i]):


![images/Final%20Project%20Aplikom%20Semester%203-481.png](images/Final%20Project%20Aplikom%20Semester%203-481.png)

Berikut ini jenis plot yang lain.


\>starplot(normal(1,10)+4,lab=1:10,\>rays):


![images/Final%20Project%20Aplikom%20Semester%203-482.png](images/Final%20Project%20Aplikom%20Semester%203-482.png)

Beberapa plot di plot2d bagus untuk statika. Berikut ini adalah plot
impuls dari data acak, yang terdistribusi secara seragam dalam [0,1].


\>plot2d(makeimpulse(1:10,random(1,10)),\>bar):


![images/Final%20Project%20Aplikom%20Semester%203-483.png](images/Final%20Project%20Aplikom%20Semester%203-483.png)

Tetapi untuk data yang terdistribusi secara eksponensial, kita mungkin
memerlukan plot logaritmik.


\>logimpulseplot(1:10,-log(random(1,10))\*10):


![images/Final%20Project%20Aplikom%20Semester%203-484.png](images/Final%20Project%20Aplikom%20Semester%203-484.png)

Fungsi columnsplot() lebih mudah digunakan, karena hanya membutuhkan
sebuah vektor nilai. Selain itu, fungsi ini dapat mengatur labelnya
menjadi apa pun yang kita inginkan, kita telah mendemonstrasikan hal
ini dalam tutorial ini.


Berikut ini adalah aplikasi lain, di mana kita menghitung karakter
dalam sebuah kalimat dan memplot statistik.


\>v=strtochar("the quick brown fox jumps over the lazy dog"); ...  
\>   w=ascii("a"):ascii("z"); x=getmultiplicities(w,v); ...  
\>   cw=[]; for k=w; cw=cw|char(k); end; ...  
\>   columnsplot(x,lab=cw,width=0.05):


![images/Final%20Project%20Aplikom%20Semester%203-485.png](images/Final%20Project%20Aplikom%20Semester%203-485.png)

Anda juga dapat menetapkan sumbu secara manual.


\>n=10; p=0.4; i=0:n; x=bin(n,i)\*p^i\*(1-p)^(n-i); ...  
\>   columnsplot(x,lab=i,width=0.05,<frame,<grid); ...  
\>   yaxis(0,0:0.1:1,style="-\>",\>left); xaxis(0,style="."); ...  
\>   label("p",0,0.25), label("i",11,0); ...  
\>   textbox(["Binomial distribution","with p=0.4"]):


![images/Final%20Project%20Aplikom%20Semester%203-486.png](images/Final%20Project%20Aplikom%20Semester%203-486.png)

Berikut ini adalah cara untuk memplot frekuensi angka dalam vektor.


Kami membuat vektor angka acak bilangan bulat 1 hingga 6.


\>v:=intrandom(1,10,10)


    [4,  9,  10,  2,  8,  8,  3,  6,  9,  7]

Kemudian ekstrak nomor unik dalam v.


\>vu:=unique(v)


    [2,  3,  4,  6,  7,  8,  9,  10]

Dan memplot frekuensi dalam plot kolom.


\>columnsplot(getmultiplicities(vu,v),lab=vu,style="/"):


![images/Final%20Project%20Aplikom%20Semester%203-487.png](images/Final%20Project%20Aplikom%20Semester%203-487.png)

Kami ingin mendemonstrasikan fungsi untuk distribusi nilai empiris.


\>x=normal(1,20);


Fungsi empdist(x,vs) membutuhkan larik nilai yang telah diurutkan.
Jadi kita harus mengurutkan x sebelum dapat menggunakannya.


\>xs=sort(x);


Kemudian kita memplot distribusi empiris dan beberapa batang kepadatan
ke dalam satu plot. Alih-alih plot batang untuk distribusi, kali ini
kami menggunakan plot gigi gergaji.


\>figure(2,1); ...  
\>   figure(1); plot2d("empdist",-4,4;xs); ...  
\>   figure(2); plot2d(histo(x,v=-4:0.2:4,<bar));  ...  
\>   figure(0):


![images/Final%20Project%20Aplikom%20Semester%203-488.png](images/Final%20Project%20Aplikom%20Semester%203-488.png)

Plot sebaran mudah dilakukan di Euler dengan plot titik biasa. Grafik
berikut ini menunjukkan bahwa X dan X+Y berkorelasi positif secara
jelas.


\>x=normal(1,100); plot2d(x,x+rotright(x),\>points,style=".."):


![images/Final%20Project%20Aplikom%20Semester%203-489.png](images/Final%20Project%20Aplikom%20Semester%203-489.png)

Sering kali, kita ingin membandingkan dua sampel dari distribusi yang
berbeda. Hal ini dapat dilakukan dengan plot kuantil-kuantil.


Untuk pengujian, kami mencoba distribusi student-t dan distribusi
eksponensial.


\>x=randt(1,1000,5); y=randnormal(1,1000,mean(x),dev(x)); ...  
\>   plot2d("x",r=6,style="--",yl="normal",xl="student-t",\>vertical); ...  
\>   plot2d(sort(x),sort(y),\>points,color=red,style="x",\>add):


![images/Final%20Project%20Aplikom%20Semester%203-490.png](images/Final%20Project%20Aplikom%20Semester%203-490.png)

Plot ini dengan jelas menunjukkan bahwa nilai yang terdistribusi
normal cenderung lebih kecil pada ujung yang ekstrim.


Jika kita memiliki dua distribusi dengan ukuran yang berbeda, kita
dapat memperluas distribusi yang lebih kecil atau memperkecil
distribusi yang lebih besar. Fungsi berikut ini bagus untuk keduanya.
Fungsi ini mengambil nilai median dengan persentase antara 0 dan 1.


\>function medianexpand (x,n) := median(x,p=linspace(0,1,n-1));


Mari kita bandingkan dua distribusi yang sama.


\>x=random(1000); y=random(400); ...  
\>   plot2d("x",0,1,style="--"); ...  
\>   plot2d(sort(medianexpand(x,400)),sort(y),\>points,color=red,style="x",\>add):


![images/Final%20Project%20Aplikom%20Semester%203-491.png](images/Final%20Project%20Aplikom%20Semester%203-491.png)

# Regresi dan Korelasi

Regresi linier dapat dilakukan dengan fungsi polyfit() atau berbagai
fungsi kecocokan.


Sebagai permulaan, kita mencari garis regresi untuk data univariat
dengan polyfit(x,y,1).


\>x=1:10; y=[2,3,1,5,6,3,7,8,9,8]; writetable(x'|y',labc=["x","y"])


             x         y
             1         2
             2         3
             3         1
             4         5
             5         6
             6         3
             7         7
             8         8
             9         9
            10         8

Kami ingin membandingkan kecocokan tanpa bobot dan dengan bobot.
Pertama, koefisien dari kecocokan linier.


\>p=polyfit(x,y,1)


    [0.733333,  0.812121]

Sekarang, koefisien dengan bobot yang menekankan nilai terakhir.


\>w &= "exp(-(x-10)^2/10)"; pw=polyfit(x,y,1,w=w(x))


    [4.71566,  0.38319]

Kami menempatkan semuanya ke dalam satu plot untuk titik-titik dan
garis regresi, dan untuk bobot yang digunakan.


\>figure(2,1);  ...  
\>   figure(1); statplot(x,y,"b",xl="Regression"); ...  
\>     plot2d("evalpoly(x,p)",\>add,color=blue,style="--"); ...  
\>     plot2d("evalpoly(x,pw)",5,10,\>add,color=red,style="--"); ...  
\>   figure(2); plot2d(w,1,10,\>filled,style="/",fillcolor=red,xl=w); ...  
\>   figure(0):


![images/Final%20Project%20Aplikom%20Semester%203-492.png](images/Final%20Project%20Aplikom%20Semester%203-492.png)

Untuk contoh lain, kita membaca survei tentang siswa, usia mereka,
usia orang tua mereka, dan jumlah saudara kandung dari sebuah file.


Tabel ini berisi “m” dan “f” pada kolom kedua. Kita menggunakan
variabel tok2 untuk mengatur terjemahan yang tepat dan bukannya
membiarkan readtable() mengumpulkan terjemahan.


\>{MS,hd}:=readtable("table1.dat",tok2:=["m","f"]);  ...  
\>   writetable(MS,labc=hd,tok2:=["m","f"]);


    Could not open the file
    table1.dat
    for reading!
    Try "trace errors" to inspect local variables after errors.
    readtable:
        if filename!=none then open(filename,"r"); endif;

Bagaimana usia saling bergantung satu sama lain? Kesan pertama datang
dari scatterplot berpasangan.


\>scatterplots(tablecol(MS,3:5),hd[3:5]):


    Variable or function MS not found.
    Error in:
    scatterplots(tablecol(MS,3:5),hd[3:5]): ...
                            ^

Jelas bahwa usia ayah dan ibu saling bergantung satu sama lain. Mari
kita tentukan dan plot garis regresinya.


\>cs:=MS[,4:5]'; ps:=polyfit(cs[1],cs[2],1)


    MS is not a variable!
    Error in:
    cs:=MS[,4:5]'; ps:=polyfit(cs[1],cs[2],1) ...
                ^

Ini jelas merupakan model yang salah. Garis regresinya adalah s = 17 +
0,74t, di mana t adalah usia ibu dan s adalah usia ayah. Perbedaan
usia mungkin sedikit bergantung pada usia, tetapi tidak terlalu
banyak.


Sebaliknya, kita menduga fungsi seperti s = a + t. Kemudian a adalah
rata-rata dari s-t. Ini adalah perbedaan usia rata-rata antara ayah
dan ibu.


\>da:=mean(cs[2]-cs[1])


    cs is not a variable!
    Error in:
    da:=mean(cs[2]-cs[1]) ...
                  ^

Mari kita plotkan ini ke dalam satu scatter plot.


\>plot2d(cs[1],cs[2],\>points);  ...  
\>   plot2d("evalpoly(x,ps)",color=red,style=".",\>add);  ...  
\>   plot2d("x+da",color=blue,\>add):


    cs is not a variable!
    Error in:
    plot2d(cs[1],cs[2],&gt;points);  plot2d("evalpoly(x,ps)",color=re ...
                ^

Berikut ini adalah plot kotak dari kedua usia tersebut. Ini hanya
menunjukkan, bahwa usia keduanya berbeda.


\>boxplot(cs,["mothers","fathers"]):


    Variable or function cs not found.
    Error in:
    boxplot(cs,["mothers","fathers"]): ...
              ^

Sangat menarik bahwa perbedaan dalam median tidak sebesar perbedaan
dalam mean.


\>median(cs[2])-median(cs[1])


    cs is not a variable!
    Error in:
    median(cs[2])-median(cs[1]) ...
                ^

Koefisien korelasi menunjukkan korelasi positif.


\>correl(cs[1],cs[2])


    cs is not a variable!
    Error in:
    correl(cs[1],cs[2]) ...
                ^

Korelasi peringkat adalah ukuran untuk urutan yang sama dalam kedua
vektor. Korelasi ini juga cukup positif.


\>rankcorrel(cs[1],cs[2])


    cs is not a variable!
    Error in:
    rankcorrel(cs[1],cs[2]) ...
                    ^

# Membuat Fungsi baru

Tentu saja, bahasa EMT dapat digunakan untuk memprogram fungsi baru.
Misalnya, kita mendefinisikan fungsi kemiringan.


di mana m adalah rata-rata dari x.


\>function skew (x:vector) ...


    m=mean(x);
    return sqrt(cols(x))*sum((x-m)^3)/(sum((x-m)^2))^(3/2);
    endfunction
</pre>
Seperti yang Anda lihat, kita dapat dengan mudah menggunakan bahasa
matriks untuk mendapatkan implementasi yang sangat singkat dan
efisien. Mari kita coba fungsi ini.


\>data=normal(20); skew(normal(10))


    0.375530094756

Berikut ini adalah fungsi lain, yang disebut koefisien kemencengan
Pearson.


\>function skew1 (x) := 3\*(mean(x)-median(x))/dev(x)

\>skew1(data)


    0.232434653125

# Simulasi Monte Carlo

Euler dapat digunakan untuk mensimulasikan kejadian acak. Kita telah
melihat contoh sederhana di atas. Berikut ini adalah contoh lainnya,
yang mensimulasikan 1000 kali pelemparan 3 dadu, dan menanyakan
distribusi dari jumlah tersebut.


\>ds:=sum(intrandom(1000,3,6))';  fs=getmultiplicities(3:18,ds)


    [5,  12,  37,  47,  65,  77,  126,  128,  131,  105,  95,  81,  41,
    31,  15,  4]

Kita bisa merencanakan ini sekarang.


\>columnsplot(fs,lab=3:18):


![images/Final%20Project%20Aplikom%20Semester%203-493.png](images/Final%20Project%20Aplikom%20Semester%203-493.png)

Untuk menentukan distribusi yang diharapkan tidaklah mudah. Kami
menggunakan rekursi tingkat lanjut untuk hal ini.


Fungsi berikut ini menghitung jumlah cara angka k dapat
direpresentasikan sebagai jumlah n angka dalam rentang 1 hingga m.
Fungsi ini bekerja secara rekursif dengan cara yang jelas.


\>function map countways (k; n, m) ...


      if n==1 then return k>=1 && k<=m
      else
        sum=0; 
        loop 1 to m; sum=sum+countways(k-#,n-1,m); end;
        return sum;
      end;
    endfunction
</pre>
Berikut ini adalah hasil dari tiga lemparan dadu.


\>countways(5:25,5,5)


    [1,  5,  15,  35,  70,  121,  185,  255,  320,  365,  381,  365,  320,
    255,  185,  121,  70,  35,  15,  5,  1]

\>cw=countways(3:18,3,6)


    [1,  3,  6,  10,  15,  21,  25,  27,  27,  25,  21,  15,  10,  6,  3,
    1]

Kami menambahkan nilai yang diharapkan ke plot.


\>plot2d(cw/6^3\*1000,\>add); plot2d(cw/6^3\*1000,\>points,\>add):


![images/Final%20Project%20Aplikom%20Semester%203-494.png](images/Final%20Project%20Aplikom%20Semester%203-494.png)

Untuk simulasi lainnya, deviasi nilai rata-rata dari n variabel acak
berdistribusi normal 0-1 adalah 1/sqrt(n).


\>longformat; 1/sqrt(10)


    0.316227766017

Mari kita periksa hal ini dengan sebuah simulasi. Kami menghasilkan
10.000 kali 10 vektor acak.


\>M=normal(10000,10); dev(mean(M)')


    0.313601622006

\>plot2d(mean(M)',\>distribution):


![images/Final%20Project%20Aplikom%20Semester%203-495.png](images/Final%20Project%20Aplikom%20Semester%203-495.png)

Median dari 10 bilangan acak berdistribusi normal 0-1 memiliki deviasi
yang lebih besar.


\>dev(median(M)')


    0.370775442713

Karena kita dapat dengan mudah menghasilkan jalan acak, kita dapat
mensimulasikan proses Wiener. Kami mengambil 1000 langkah dari 1000
proses. Kami kemudian memplot deviasi standar dan rata-rata dari
langkah ke-n dari proses-proses ini bersama dengan nilai yang
diharapkan dalam warna merah.


\>n=1000; m=1000; M=cumsum(normal(n,m)/sqrt(m)); ...  
\>   t=(1:n)/n; figure(2,1); ...  
\>   figure(1); plot2d(t,mean(M')'); plot2d(t,0,color=red,\>add); ...  
\>   figure(2); plot2d(t,dev(M')'); plot2d(t,sqrt(t),color=red,\>add); ...  
\>   figure(0):


![images/Final%20Project%20Aplikom%20Semester%203-496.png](images/Final%20Project%20Aplikom%20Semester%203-496.png)

# Tes

Tes adalah alat yang penting dalam statistik. Dalam Euler, banyak tes
yang diterapkan. Semua tes ini mengembalikan kesalahan yang kita
terima jika kita menolak hipotesis nol.


Sebagai contoh, kita menguji lemparan dadu untuk distribusi yang
seragam. Pada 600 lemparan, kita mendapatkan nilai berikut, yang kita
masukkan ke dalam uji chi-kuadrat.


\>chitest([90,103,114,101,103,89],dup(100,6)')


    0.498830517952

Uji chi-square juga memiliki mode, yang menggunakan simulasi Monte
Carlo untuk menguji statistik. Hasilnya seharusnya hampir sama.
Parameter &gt;p menginterpretasikan vektor y sebagai vektor probabilitas.


\>chitest([90,103,114,101,103,89],dup(1/6,6)',\>p,\>montecarlo)


    0.491

Kesalahan ini terlalu besar. Jadi kita tidak bisa menolak distribusi
seragam. Ini tidak membuktikan bahwa dadu kita adil. Tetapi kita tidak
dapat menolak hipotesis kita.


Selanjutnya kita buat 1000 lemparan dadu dengan menggunakan generator
bilangan acak, dan lakukan pengujian yang sama.


\>n=1000; t=random([1,n\*6]); chitest(count(t\*6,6),dup(n,6)')


    0.63887454567

Mari kita uji nilai rata-rata 100 dengan uji-t.


\>s=200+normal([1,100])\*10; ...  
\>   ttest(mean(s),dev(s),100,200)


    0.153527036467

The function ttest() needs the mean value, the deviation, the number
of data, and the mean value to test for.


Now let us check two measurements for the same mean. We reject the
hypothesis that they have the same mean, if the result is &lt;0.05.


\>tcomparedata(normal(1,10),normal(1,10))


    0.364370037281

Jika kita menambahkan bias pada satu distribusi, kita akan mendapatkan
lebih banyak penolakan. Ulangi simulasi ini beberapa kali untuk
melihat efeknya.


\>tcomparedata(normal(1,10),normal(1,10)+2)


    1.30849019413e-05

Pada contoh berikut, kita membuat 20 lemparan dadu secara acak
sebanyak 100 kali dan menghitung jumlah dadu yang muncul. Rata-rata
harus ada 20/6 = 3,3 mata dadu.


\>R=random(100,20); R=sum(R\*6<=1)'; mean(R)


    3.56

Sekarang kita bandingkan jumlah satu dengan distribusi binomial.
Pertama, kita memplot distribusi angka satu.


\>plot2d(R,distribution=max(R)+1,even=1,style="\\/"):


![images/Final%20Project%20Aplikom%20Semester%203-497.png](images/Final%20Project%20Aplikom%20Semester%203-497.png)

\>t=count(R,21);


Kemudian kami menghitung nilai yang diharapkan.


\>n=0:20; b=bin(20,n)\*(1/6)^n\*(5/6)^(20-n)\*100;


Kami harus mengumpulkan beberapa angka untuk mendapatkan kategori yang
cukup besar.


\>t1=sum(t[1:2])|t[3:7]|sum(t[8:21]); ...  
\>   b1=sum(b[1:2])|b[3:7]|sum(b[8:21]);


Uji chi-square menolak hipotesis bahwa distribusi kita adalah
distribusi binomial, jika hasilnya &lt;0,05.


\>chitest(t1,b1)


    0.0367816071845

Contoh berikut ini berisi hasil dari dua kelompok orang (laki-laki dan
perempuan, katakanlah) yang memberikan suara untuk satu dari enam
partai.


\>A=[23,37,43,52,64,74;27,39,41,49,63,76];  ...  
\>     writetable(A,wc=6,labr=["m","f"],labc=1:6)


               1     2     3     4     5     6
         m    23    37    43    52    64    74
         f    27    39    41    49    63    76

Kami ingin menguji independensi suara dari jenis kelamin. Uji tabel
chi^2 melakukan hal ini. Hasilnya terlalu besar untuk menolak
independensi. Jadi kita tidak dapat mengatakan, jika pemungutan suara
tergantung pada jenis kelamin dari data ini.


\>tabletest(A)


    0.990701632326

Berikut ini adalah tabel yang diharapkan, jika kita mengasumsikan
frekuensi pemungutan suara yang diamati.


\>writetable(expectedtable(A),wc=6,dc=1,labr=["m","f"],labc=1:6)


               1     2     3     4     5     6
         m  24.9  37.9  41.9  50.3  63.3  74.7
         f  25.1  38.1  42.1  50.7  63.7  75.3

Kita dapat menghitung koefisien kontingensi terkoreksi. Karena
koefisien ini sangat dekat dengan 0, kami menyimpulkan bahwa
pemungutan suara tidak bergantung pada jenis kelamin.


\>contingency(A)


    0.0427225484717

# Beberapa Tes Lainnya

Selanjutnya kita menggunakan analisis varians (uji F) untuk menguji
tiga sampel data yang terdistribusi secara normal dengan nilai
rata-rata yang sama. Metode ini disebut ANOVA (analisis varians).
Dalam Euler, fungsi varanalysis() digunakan.


\>x1=[109,111,98,119,91,118,109,99,115,109,94]; mean(x1),


    106.545454545

\>x2=[120,124,115,139,114,110,113,120,117]; mean(x2),


    119.111111111

\>x3=[120,112,115,110,105,134,105,130,121,111]; mean(x3)


    116.3

\>varanalysis(x1,x2,x3)


    0.0138048221371

Ini berarti, kami menolak hipotesis nilai rata-rata yang sama. Kami
melakukan ini dengan probabilitas kesalahan sebesar 1,3%.


Ada juga uji median, yang menolak sampel data dengan distribusi
rata-rata yang berbeda dengan menguji median dari sampel gabungan.


\>a=[56,66,68,49,61,53,45,58,54];

\>b=[72,81,51,73,69,78,59,67,65,71,68,71];

\>mediantest(a,b)


    0.0241724220052

Uji lain tentang kesetaraan adalah uji peringkat. Uji ini jauh lebih
tajam daripada uji median.


\>ranktest(a,b)


    0.00199969612469

Dalam contoh berikut ini, kedua distribusi memiliki rata-rata yang
sama.


\>ranktest(random(1,100),random(1,50)\*3-1)


    0.438220440816

Sekarang mari kita coba mensimulasikan dua perawatan a dan b yang
diterapkan pada orang yang berbeda.


\>a=[8.0,7.4,5.9,9.4,8.6,8.2,7.6,8.1,6.2,8.9];

\>b=[6.8,7.1,6.8,8.3,7.9,7.2,7.4,6.8,6.8,8.1];


Uji signum memutuskan, apakah a lebih baik daripada b.


\>signtest(a,b)


    0.0546875

Ini adalah kesalahan yang terlalu besar. Kita tidak dapat menolak
bahwa a sama baiknya dengan b.


Uji Wilcoxon lebih tajam daripada uji ini, tetapi bergantung pada
nilai kuantitatif dari perbedaan.


\>wilcoxon(a,b)


    0.0296680599405

Mari kita coba dua pengujian lagi dengan menggunakan rangkaian yang
dihasilkan.


\>wilcoxon(normal(1,20),normal(1,20)-1)


    0.00085650881911

\>wilcoxon(normal(1,20),normal(1,20))


    0.963430965414

# Bilangan Acak

Berikut ini adalah tes untuk generator bilangan acak. Euler
menggunakan generator yang sangat bagus, jadi kita tidak perlu
mengharapkan adanya masalah.


Pertama, kita akan membangkitkan sepuluh juta bilangan acak dalam
[0,1].


\>n:=10000000; r:=random(1,n);


Selanjutnya, kami menghitung jarak antara dua angka yang kurang dari
0,05.


\>a:=0.05; d:=differences(nonzeros(r<a));


Terakhir, kami memplot berapa kali, setiap jarak yang terjadi, dan
membandingkannya dengan nilai yang diharapkan.


\>m=getmultiplicities(1:100,d); plot2d(m); ...  
\>     plot2d("n\*(1-a)^(x-1)\*a^2",color=red,\>add):


![images/Final%20Project%20Aplikom%20Semester%203-498.png](images/Final%20Project%20Aplikom%20Semester%203-498.png)

Menghapus data.


\>remvalue n;


# Pengantar untuk Pengguna Proyek R

Jelas, EMT tidak bersaing dengan R sebagai sebuah paket statistik.
Namun, ada banyak prosedur dan fungsi statistik yang tersedia di EMT
juga. Jadi EMT dapat memenuhi kebutuhan dasar. Bagaimanapun, EMT hadir
dengan paket numerik dan sistem aljabar komputer.


Buku ini diperuntukkan bagi Anda yang sudah terbiasa dengan R, tetapi
perlu mengetahui perbedaan sintaks EMT dan R. Kami mencoba memberikan
gambaran umum mengenai hal-hal yang jelas dan kurang jelas yang perlu
Anda ketahui.


Selain itu, kami juga membahas cara-cara untuk bertukar data di antara
kedua sistem tersebut.


Perhatikan bahwa ini adalah pekerjaan yang sedang berlangsung.


# Sintaks Dasar

Hal pertama yang Anda pelajari dalam R adalah membuat sebuah vektor.
Dalam EMT, perbedaan utamanya adalah bahwa operator : dapat mengambil
ukuran langkah. Selain itu, operator ini memiliki daya ikat yang
rendah.


\>n=10; 0:n/20:n-1


    [0,  0.5,  1,  1.5,  2,  2.5,  3,  3.5,  4,  4.5,  5,  5.5,  6,  6.5,
    7,  7.5,  8,  8.5,  9]

Fungsi c() tidak ada. Anda dapat menggunakan vektor untuk
menggabungkan beberapa hal.


Contoh berikut ini, seperti banyak contoh lainnya, berasal dari
“Interoduksi ke R” yang disertakan dengan proyek R. Jika Anda membaca
PDF ini, Anda akan menemukan bahwa saya mengikuti alurnya dalam
tutorial ini.


\>x=[10.4, 5.6, 3.1, 6.4, 21.7]; [x,0,x]


    [10.4,  5.6,  3.1,  6.4,  21.7,  0,  10.4,  5.6,  3.1,  6.4,  21.7]

Operator titik dua dengan ukuran langkah EMT digantikan oleh fungsi
seq() dalam R. Kita dapat menulis fungsi ini dalam EMT.


\>function seq(a,b,c) := a:b:c; ...  
\>   seq(0,-0.1,-1)


    [0,  -0.1,  -0.2,  -0.3,  -0.4,  -0.5,  -0.6,  -0.7,  -0.8,  -0.9,  -1]

Fungsi rep() dari R tidak ada dalam EMT. Untuk input vektor, dapat
dituliskan sebagai berikut.


\>function rep(x:vector,n:index) := flatten(dup(x,n)); ...  
\>   rep(x,2)


    [10.4,  5.6,  3.1,  6.4,  21.7,  10.4,  5.6,  3.1,  6.4,  21.7]

Perhatikan bahwa “=” atau “:=” digunakan untuk penugasan. Operator
“-&gt;” digunakan untuk unit dalam EMT.


\>125km -\> " miles"


    77.6713990297 miles

Operator “&lt;-” untuk penugasan menyesatkan, dan bukan ide yang baik
untuk R. Berikut ini akan membandingkan a dan -4 dalam EMT.


\>a=2; a<-4


    0

Dalam R, “a&lt;-4&lt;3” bisa digunakan, tetapi “a&lt;-4&lt;-3” tidak. Saya juga
mengalami ambiguitas yang sama di EMT, tetapi saya mencoba untuk
menghilangkannya.


EMT dan R memiliki vektor dengan tipe boolean. Tetapi dalam EMT, angka
0 dan 1 digunakan untuk merepresentasikan salah dan benar. Dalam R,
nilai benar dan salah tetap dapat digunakan dalam aritmatika biasa
seperti dalam EMT.


\>x<5, %\*x


    [0,  0,  1,  0,  0]
    [0,  0,  3.1,  0,  0]

EMT melempar kesalahan atau menghasilkan NAN tergantung pada flag
“kesalahan”.


\>errors off; 0/0, isNAN(sqrt(-1)), errors on;


    NAN
    1

String sama saja dalam R dan EMT. Keduanya berada di lokal saat ini,
bukan di Unicode.


Dalam R ada paket-paket untuk Unicode. Dalam EMT, sebuah string dapat
berupa string Unicode. Sebuah string Unicode dapat diterjemahkan ke
pengkodean lokal dan sebaliknya. Selain itu, u“...” dapat berisi
entitas HTML.


\>u"&#169; Ren&eacut; Grothmann"


    © René Grothmann

Berikut ini mungkin atau mungkin tidak ditampilkan dengan benar pada
sistem Anda sebagai A dengan titik dan tanda hubung di atasnya. Hal
ini tergantung pada jenis huruf yang Anda gunakan.


\>chartoutf([480])


    Ǡ

Penggabungan string dilakukan dengan “+” atau “|”. Ini dapat
menyertakan angka, yang akan dicetak dalam format saat ini.


\>"pi = "+pi


    pi = 3.14159265359

# Pengindeksan

Sebagian besar waktu, ini akan bekerja seperti pada R.


Tetapi EMT akan menginterpretasikan indeks negatif dari bagian
belakang vektor, sementara R menginterpretasikan x[n] sebagai x tanpa
elemen ke-n.


\>x, x[1:3], x[-2]


    [10.4,  5.6,  3.1,  6.4,  21.7]
    [10.4,  5.6,  3.1]
    6.4

Perilaku R dapat dicapai dalam EMT dengan drop().


\>drop(x,2)


    [10.4,  3.1,  6.4,  21.7]

Vektor logika tidak diperlakukan secara berbeda dengan indeks di EMT,
berbeda dengan R. Anda harus mengekstrak elemen-elemen yang bukan nol
terlebih dahulu di EMT.


\>x, x\>5, x[nonzeros(x\>5)]


    [10.4,  5.6,  3.1,  6.4,  21.7]
    [1,  1,  0,  1,  1]
    [10.4,  5.6,  6.4,  21.7]

Sama seperti di R, vektor indeks dapat berisi pengulangan.


\>x[[1,2,2,1]]


    [10.4,  5.6,  5.6,  10.4]

Namun pemberian nama untuk indeks tidak dimungkinkan dalam EMT. Untuk
paket statistik, hal ini mungkin sering diperlukan untuk memudahkan
akses ke elemen-elemen vektor.


Untuk meniru perilaku ini, kita dapat mendefinisikan sebuah fungsi
sebagai berikut.


\>function sel (v,i,s) := v[indexof(s,i)]; ...  
\>   s=["first","second","third","fourth"]; sel(x,["first","third"],s)


    
    Trying to overwrite protected function sel!
    Error in:
    function sel (v,i,s) := v[indexof(s,i)]; ... ...
                 ^
    
    Trying to overwrite protected function sel!
    Error in:
    function sel (v,i,s) := v[indexof(s,i)]; ... ...
                 ^
    
    Trying to overwrite protected function sel!
    Error in:
    function sel (v,i,s) := v[indexof(s,i)]; ... ...
                 ^
    
    Trying to overwrite protected function sel!
    Error in:
    function sel (v,i,s) := v[indexof(s,i)]; ... ...
                 ^
    
    Trying to overwrite protected function sel!
    Error in:
    function sel (v,i,s) := v[indexof(s,i)]; ... ...
                 ^
    [10.4,  3.1]

# Tipe Data

EMT memiliki lebih banyak tipe data yang tetap dibandingkan R. Jelas,
dalam R terdapat vektor yang berkembang. Anda bisa mengatur sebuah
vektor numerik kosong v dan memberikan sebuah nilai pada elemen v[17].
Hal ini tidak mungkin dilakukan dalam EMT.


Hal berikut ini sedikit tidak efisien.


\>v=[]; for i=1 to 10000; v=v|i; end;


EMT sekarang akan membuat vektor dengan v dan i yang ditambahkan pada
tumpukan dan menyalin vektor tersebut kembali ke variabel global v.


Semakin efisien mendefinisikan vektor terlebih dahulu.


\>v=zeros(10000); for i=1 to 10000; v[i]=i; end;


Untuk mengubah jenis tanggal di EMT, Anda dapat menggunakan fungsi
seperti complex().


\>complex(1:4)


    [ 1+0i ,  2+0i ,  3+0i ,  4+0i  ]

Konversi ke string hanya dapat dilakukan untuk tipe data dasar. Format
saat ini digunakan untuk penggabungan string sederhana. Tetapi ada
fungsi-fungsi seperti print() atau frac().


Untuk vektor, Anda dapat dengan mudah menulis fungsi Anda sendiri.


\>function tostr (v) ...


    s="[";
    loop 1 to length(v);
       s=s+print(v[#],2,0);
       if #<length(v) then s=s+","; endif;
    end;
    return s+"]";
    endfunction
</pre>
\>tostr(linspace(0,1,10))


    [0.00,0.10,0.20,0.30,0.40,0.50,0.60,0.70,0.80,0.90,1.00]

Untuk komunikasi dengan Maxima, ada sebuah fungsi convertmxm(), yang
juga dapat digunakan untuk memformat vektor untuk output.


\>convertmxm(1:10)


    [1,2,3,4,5,6,7,8,9,10]

Untuk Latex, perintah tex dapat digunakan untuk mendapatkan perintah
Latex.


\>tex(&[1,2,3])


    \left[ 1 , 2 , 3 \right] 

# Faktor dan Tabel

Pada pengantar R terdapat sebuah contoh dengan apa yang disebut
faktor.


Berikut ini adalah daftar wilayah dari 30 negara bagian.


\>austates = ["tas", "sa", "qld", "nsw", "nsw", "nt", "wa", "wa", ...  
\>   "qld", "vic", "nsw", "vic", "qld", "qld", "sa", "tas", ...  
\>   "sa", "nt", "wa", "vic", "qld", "nsw", "nsw", "wa", ...  
\>   "sa", "act", "nsw", "vic", "vic", "act"];


Asumsikan, kita memiliki pendapatan yang sesuai di setiap negara
bagian.


\>incomes = [60, 49, 40, 61, 64, 60, 59, 54, 62, 69, 70, 42, 56, ...  
\>   61, 61, 61, 58, 51, 48, 65, 49, 49, 41, 48, 52, 46, ...  
\>   59, 46, 58, 43];


Sekarang, kita ingin menghitung rata-rata pendapatan di wilayah
tersebut. Sebagai sebuah program statistik, R memiliki fungsi factor()
dan tappy() untuk hal ini.


EMT dapat melakukan hal ini dengan mencari indeks dari wilayah-wilayah
di dalam daftar unik dari wilayah-wilayah tersebut.


\>auterr=sort(unique(austates)); f=indexofsorted(auterr,austates)


    [6,  5,  4,  2,  2,  3,  8,  8,  4,  7,  2,  7,  4,  4,  5,  6,  5,  3,
    8,  7,  4,  2,  2,  8,  5,  1,  2,  7,  7,  1]

Pada titik ini, kita dapat menulis fungsi perulangan kita sendiri
untuk melakukan berbagai hal untuk satu faktor saja.


Atau kita dapat meniru fungsi tapply() dengan cara berikut.


\>function map tappl (i; f$:call, cat, x) ...


    u=sort(unique(cat));
    f=indexof(u,cat);
    return f$(x[nonzeros(f==indexof(u,i))]);
    endfunction
</pre>
Ini sedikit tidak efisien, karena menghitung wilayah unik untuk setiap
i, tetapi berfungsi.


\>tappl(auterr,"mean",austates,incomes)


    [44.5,  57.3333333333,  55.5,  53.6,  55,  60.5,  56,  52.25]

Perhatikan bahwa ini bekerja untuk setiap vektor wilayah.


\>tappl(["act","nsw"],"mean",austates,incomes)


    [44.5,  57.3333333333]

Sekarang, paket statistik EMT mendefinisikan tabel seperti halnya di
R. Fungsi readtable() dan writetable() dapat digunakan untuk input dan
output.


Jadi kita dapat mencetak rata-rata pendapatan negara di wilayah dengan
cara yang ramah.


\>writetable(tappl(auterr,"mean",austates,incomes),labc=auterr,wc=7)


        act    nsw     nt    qld     sa    tas    vic     wa
       44.5  57.33   55.5   53.6     55   60.5     56  52.25

Kita juga dapat mencoba meniru perilaku R sepenuhnya.


Faktor-faktor tersebut harus disimpan dengan jelas dalam sebuah
koleksi dengan jenis dan kategorinya (negara bagian dan wilayah dalam
contoh kita). Untuk EMT, kita menambahkan indeks yang telah dihitung
sebelumnya.


\>function makef (t) ...


    ## Factor data
    ## Returns a collection with data t, unique data, indices.
    ## See: tapply
    u=sort(unique(t));
    return {{t,u,indexofsorted(u,t)}};
    endfunction
</pre>
\>statef=makef(austates);


Sekarang elemen ketiga dari koleksi ini akan berisi indeks.


\>statef[3]


    [6,  5,  4,  2,  2,  3,  8,  8,  4,  7,  2,  7,  4,  4,  5,  6,  5,  3,
    8,  7,  4,  2,  2,  8,  5,  1,  2,  7,  7,  1]

Sekarang kita dapat meniru tapply() dengan cara berikut. Ini akan
mengembalikan sebuah tabel sebagai kumpulan data tabel dan judul
kolom.


\>function tapply (t:vector,tf,f$:call) ...


    ## Makes a table of data and factors
    ## tf : output of makef()
    ## See: makef
    uf=tf[2]; f=tf[3]; x=zeros(length(uf));
    for i=1 to length(uf);
       ind=nonzeros(f==i);
       if length(ind)==0 then x[i]=NAN;
       else x[i]=f$(t[ind]);
       endif;
    end;
    return {{x,uf}};
    endfunction
</pre>
Kami tidak menambahkan banyak pemeriksaan tipe di sini. Satu-satunya
tindakan pencegahan adalah kategori (faktor) yang tidak memiliki data.
Tetapi kita harus memeriksa panjang t yang benar dan kebenaran koleksi
tf.


Tabel ini bisa dicetak sebagai sebuah tabel dengan writetable().


\>writetable(tapply(incomes,statef,"mean"),wc=7)


        act    nsw     nt    qld     sa    tas    vic     wa
       44.5  57.33   55.5   53.6     55   60.5     56  52.25

# Larik

EMT hanya memiliki dua dimensi untuk array. Tipe datanya disebut
matriks. Akan lebih mudah untuk menulis fungsi untuk dimensi yang
lebih tinggi atau pustaka C untuk ini.


R memiliki lebih dari dua dimensi. Dalam R, larik adalah sebuah vektor
dengan sebuah bidang dimensi.


Dalam EMT, sebuah vektor adalah sebuah matriks dengan satu baris. Ini
bisa dibuat menjadi sebuah matriks dengan redim().


\>shortformat; X=redim(1:20,4,5)


            1         2         3         4         5 
            6         7         8         9        10 
           11        12        13        14        15 
           16        17        18        19        20 

Ekstraksi baris dan kolom, atau sub-matriks, sama seperti di R.


\>X[,2:3]


            2         3 
            7         8 
           12        13 
           17        18 

Namun, dalam R dimungkinkan untuk mengatur daftar indeks tertentu dari
vektor ke suatu nilai. Hal yang sama juga dapat dilakukan dalam EMT
hanya dengan sebuah perulangan.


\>function setmatrixvalue (M, i, j, v) ...


    loop 1 to max(length(i),length(j),length(v))
       M[i{#},j{#}] = v{#};
    end;
    endfunction
</pre>
Kami mendemonstrasikan hal ini untuk menunjukkan bahwa matriks
diteruskan dengan referensi dalam EMT. Jika Anda tidak ingin mengubah
matriks asli M, Anda perlu menyalinnya dalam fungsi.


\>setmatrixvalue(X,1:3,3:-1:1,0); X,


            1         2         0         4         5 
            6         0         8         9        10 
            0        12        13        14        15 
           16        17        18        19        20 

Hasil kali luar dalam EMT hanya dapat dilakukan di antara vektor. Hal
ini otomatis karena bahasa matriks. Satu vektor harus berupa vektor
kolom dan vektor baris.


\>(1:5)\*(1:5)'


            1         2         3         4         5 
            2         4         6         8        10 
            3         6         9        12        15 
            4         8        12        16        20 
            5        10        15        20        25 

Dalam pengantar PDF untuk R ada sebuah contoh, yang menghitung
distribusi ab-cd untuk a, b, c, d yang dipilih dari 0 sampai n secara
acak. Solusinya dalam R adalah membentuk sebuah matriks 4 dimensi dan
menjalankan table() di atasnya.


Tentu saja, ini bisa dicapai dengan sebuah perulangan. Tetapi
perulangan tidak efektif dalam EMT atau R. Dalam EMT, kita bisa
menulis perulangan dalam C dan itu adalah solusi tercepat.


Tetapi kita ingin meniru perilaku R. Untuk ini, kita perlu meratakan
perkalian ab dan membuat sebuah matriks ab-cd.


\>a=0:6; b=a'; p=flatten(a\*b); q=flatten(p-p'); ...  
\>   u=sort(unique(q)); f=getmultiplicities(u,q); ...  
\>   statplot(u,f,"h"):


![images/Final%20Project%20Aplikom%20Semester%203-499.png](images/Final%20Project%20Aplikom%20Semester%203-499.png)

Selain kelipatan yang tepat, EMT dapat menghitung frekuensi dalam
vektor.


\>getfrequencies(q,-50:10:50)


    [0,  23,  132,  316,  602,  801,  333,  141,  53,  0]

Cara yang paling mudah untuk memplot ini sebagai distribusi adalah
sebagai berikut.


\>plot2d(q,distribution=11):


![images/Final%20Project%20Aplikom%20Semester%203-500.png](images/Final%20Project%20Aplikom%20Semester%203-500.png)

Tetapi juga memungkinkan untuk menghitung jumlah dalam interval yang
dipilih sebelumnya. Tentu saja, berikut ini menggunakan
getfrequencies() secara internal.


Karena fungsi histo() mengembalikan frekuensi, kita perlu
menskalakannya sehingga integral di bawah grafik batang adalah 1.


\>{x,y}=histo(q,v=-55:10:55); y=y/sum(y)/differences(x); ...  
\>   plot2d(x,y,\>bar,style="/"):


![images/Final%20Project%20Aplikom%20Semester%203-501.png](images/Final%20Project%20Aplikom%20Semester%203-501.png)

# Daftar

EMT memiliki dua jenis daftar. Pertama adalah daftar global yang dapat
diubah, dan yang kedua adalah jenis daftar yang tidak dapat diubah.
Kita tidak peduli dengan daftar global di sini.


Tipe daftar yang tidak dapat diubah disebut koleksi dalam EMT. Ia
berperilaku seperti struktur dalam C, tetapi elemen-elemennya hanya
diberi nomor dan tidak diberi nama.


\>L={{"Fred","Flintstone",40,[1990,1992]}}


    Fred
    Flintstone
    40
    [1990,  1992]

Saat ini elemen-elemen tersebut tidak memiliki nama, meskipun nama
dapat ditetapkan untuk tujuan khusus. Elemen-elemen tersebut diakses
dengan angka.


\>(L[4])[2]


    1992

# Input dan Output File (Membaca dan Menulis Data)

Anda mungkin sering ingin mengimpor matriks data dari sumber lain ke
EMT. Tutorial ini akan menjelaskan kepada Anda tentang berbagai cara
untuk melakukan hal tersebut. Fungsi yang sederhana adalah
writematrix() dan readmatrix().


Mari kita tunjukkan bagaimana cara membaca dan menulis sebuah vektor
real ke sebuah file.


\>a=random(1,100); mean(a), dev(a),


    0.48158
    0.30444

Untuk menulis data ke sebuah berkas, kita menggunakan fungsi
writematrix().


Karena pengenalan ini kemungkinan besar berada di sebuah direktori, di
mana pengguna tidak memiliki akses tulis, kita menulis data ke
direktori home pengguna. Untuk notebook sendiri, hal ini tidak
diperlukan, karena file data akan ditulis ke dalam direktori yang
sama.


\>filename="test.dat";


Sekarang kita tuliskan vektor kolom a' ke dalam file. Hal ini akan
menghasilkan satu angka pada setiap baris file.


\>writematrix(a',filename);


Untuk membaca data, kita menggunakan readmatrix().


\>a=readmatrix(filename)';


Dan hapus file tersebut.


\>fileremove(filename);

\>mean(a), dev(a),


    0.48158
    0.30444

Fungsi writematrix() atau writetable() dapat dikonfigurasi untuk
bahasa lain.


Sebagai contoh, jika Anda memiliki sistem bahasa Indonesia (titik
desimal dengan koma), Excel Anda membutuhkan nilai dengan koma desimal
yang dipisahkan oleh titik koma dalam file csv (defaultnya adalah
nilai yang dipisahkan dengan koma). File “test.csv” berikut ini akan
muncul di folder cuurent Anda.


\>filename="test.csv"; ...  
\>   writematrix(random(5,3),file=filename,separator=",");


Anda sekarang dapat membuka file ini dengan Excel Indonesia secara
langsung.


\>fileremove(filename);


Terkadang kita memiliki string dengan token seperti berikut ini.


\>s1:="f m m f m m m f f f m m f";  ...  
\>   s2:="f f f m m f f";


Untuk menandai ini, kita mendefinisikan vektor token.


\>tok:=["f","m"]


    f
    m

Kemudian kita dapat menghitung berapa kali setiap token muncul dalam
string, dan memasukkan hasilnya ke dalam tabel.


\>M:=getmultiplicities(tok,strtokens(s1))\_ ...  
\>     getmultiplicities(tok,strtokens(s2));


Tulis tabel dengan tajuk token.


\>writetable(M,labc=tok,labr=1:2,wc=8)


                   f       m
           1       6       7
           2       5       2

Untuk statika, EMT dapat membaca dan menulis tabel.


\>file="test.dat"; open(file,"w"); ...  
\>   writeln("A,B,C"); writematrix(random(3,3)); ...  
\>   close();


File terlihat seperti ini.


\>printfile(file)


    A,B,C
    0.4235650636269853,0.6413568381757155,0.4668362707277215
    0.7155729261337308,0.09030283646459743,0.4873740875286969
    0.675758211146783,0.6665406118407622,0.316102105131689
    

Fungsi readtable() dalam bentuknya yang paling sederhana dapat membaca
ini dan mengembalikan sebuah koleksi nilai dan baris judul.


\>L=readtable(file,\>list);


Koleksi ini dapat dicetak dengan writetable() ke buku catatan, atau ke
sebuah file.


\>writetable(L,wc=10,dc=5)


             A         B         C
       0.42357   0.64136   0.46684
       0.71557    0.0903   0.48737
       0.67576   0.66654    0.3161

Matriks nilai adalah elemen pertama dari L. Perhatikan bahwa mean()
dalam EMT menghitung nilai rata-rata dari baris-baris matriks.


\>mean(L[1])


      0.51059 
      0.43108 
       0.5528 

# File CSV

Pertama, mari kita tulis sebuah matriks ke dalam sebuah file. Untuk
keluarannya, kami membuat file di direktori kerja saat ini.


\>file="test.csv";  ...  
\>   M=random(3,3); writematrix(M,file);


Berikut ini adalah isi file ini.


\>printfile(file)


    0.5765633396841044,0.7389491064523691,0.2155664890646709
    0.5162874930000104,0.4441465142892924,0.1743147879916974
    0.3474452116213939,0.4726249287711079,0.1725991105991064
    

CVS ini dapat dibuka di sistem bahasa Inggris ke Excel dengan klik dua
kali. Jika Anda mendapatkan file seperti itu pada sistem Jerman, Anda
perlu mengimpor data ke Excel dengan memperhatikan titik desimal.


Namun, titik desimal juga merupakan format default untuk EMT. Anda
dapat membaca sebuah matriks dari sebuah file dengan readmatrix().


\>readmatrix(file)


      0.57656   0.73895   0.21557 
      0.51629   0.44415   0.17431 
      0.34745   0.47262    0.1726 

Dimungkinkan untuk menulis beberapa matriks ke dalam satu file.
Perintah open() dapat membuka file untuk menulis dengan parameter “w”.
Standarnya adalah “r” untuk membaca.


\>open(file,"w"); writematrix(M); writematrix(M'); close();


Matriks-matriks tersebut dipisahkan oleh sebuah baris kosong. Untuk
membaca matriks, buka file dan panggil readmatrix() beberapa kali.


\>open(file); A=readmatrix(); B=readmatrix(); A==B, close();


            1         0         0 
            0         1         0 
            0         0         1 

Di Excel atau spreadsheet serupa, Anda dapat mengekspor matriks
sebagai CSV (nilai yang dipisahkan dengan koma). Pada Excel 2007,
gunakan “save as” dan “format lain”, lalu pilih “CSV”. Pastikan, tabel
saat ini hanya berisi data yang ingin Anda ekspor.


Berikut ini adalah contohnya.


\>printfile("excel-data.csv")


    Could not open the file
    excel-data.csv
    for reading!
    Try "trace errors" to inspect local variables after errors.
    printfile:
        open(filename,"r");

Seperti yang Anda lihat, sistem Jerman saya menggunakan titik koma
sebagai pemisah dan koma desimal. Anda dapat mengubahnya di pengaturan
sistem atau di Excel, tetapi tidak perlu untuk membaca matriks ke
dalam EMT.


Cara termudah untuk membaca ini ke dalam Euler adalah readmatrix().
Semua koma digantikan oleh titik dengan parameter &gt;comma. Untuk CSV
bahasa Inggris, hilangkan saja parameter ini.


\>M=readmatrix("excel-data.csv",\>comma)


    Could not open the file
    excel-data.csv
    for reading!
    Try "trace errors" to inspect local variables after errors.
    readmatrix:
        if filename&lt;&gt;"" then open(filename,"r"); endif;

Mari kita rencanakan ini.


\>plot2d(M'[1],M'[2:3],\>points,color=[red,green]'):


![images/Final%20Project%20Aplikom%20Semester%203-502.png](images/Final%20Project%20Aplikom%20Semester%203-502.png)

Ada beberapa cara yang lebih mendasar untuk membaca data dari file.
Anda dapat membuka file dan membaca angka baris demi baris. Fungsi
getvectorline() akan membaca angka dari sebuah baris data. Secara
default, fungsi ini mengharapkan sebuah titik desimal. Tetapi fungsi
ini juga dapat menggunakan koma desimal, jika Anda memanggil
setdecimaldot(“,”) sebelum menggunakan fungsi ini.


Fungsi berikut ini adalah contohnya. Fungsi ini akan berhenti pada
akhir file atau baris kosong.


\>function myload (file) ...


    open(file);
    M=[];
    repeat
       until eof();
       v=getvectorline(3);
       if length(v)>0 then M=M_v; else break; endif;
    end;
    return M;
    close(file);
    endfunction
</pre>
\>myload(file)


      0.57656         0   0.73895         0   0.21557 
      0.51629         0   0.44415         0   0.17431 
      0.34745         0   0.47262         0    0.1726 

Anda juga dapat membaca semua angka dalam file tersebut dengan
getvector().


\>open(file); v=getvector(10000); close(); redim(v[1:9],3,3)


      0.57656         0   0.73895 
            0   0.21557   0.51629 
            0   0.44415         0 

Dengan demikian, sangat mudah untuk menyimpan vektor nilai, satu nilai
di setiap baris dan membaca kembali vektor ini.


\>v=random(1000); mean(v)


    0.50145

\>writematrix(v',file); mean(readmatrix(file)')


    0.50145

# Menggunakan Tabel

Tabel dapat digunakan untuk membaca atau menulis data numerik. Sebagai
contoh, kita menulis tabel dengan judul baris dan kolom ke file.


\>file="test.tab"; M=random(3,3);  ...  
\>   open(file,"w");  ...  
\>   writetable(M,separator=",",labc=["one","two","three"]);  ...  
\>   close(); ...  
\>   printfile(file)


    one,two,three
          0.67,      0.84,       0.8
          0.51,      0.58,      0.94
          0.08,      0.49,      0.61

File ini dapat diimpor ke Excel.


Untuk membaca file di EMT, kita menggunakan readtable().


\>{M,headings}=readtable(file,\>clabs); ...  
\>   writetable(M,labc=headings)


           one       two     three
          0.67      0.84       0.8
          0.51      0.58      0.94
          0.08      0.49      0.61

# Menganalisis Garis

Anda bahkan dapat mengevaluasi setiap baris dengan tangan. Misalkan,
kita memiliki baris dengan format berikut.


\>line="2020-11-03,Tue,1'114.05"


    2020-11-03,Tue,1'114.05

First we can tokenize the line.


\>vt=strtokens(line)


    2020-11-03
    Tue
    1'114.05

Kemudian, kita dapat mengevaluasi setiap elemen garis dengan
menggunakan evaluasi yang sesuai.


\>day(vt[1]),  ...  
\>   indexof(["mon","tue","wed","thu","fri","sat","sun"],tolower(vt[2])),  ...  
\>   strrepl(vt[3],"'","")()


    7.3816e+05
    2
    1114

Dengan menggunakan ekspresi reguler, Anda dapat mengekstrak hampir
semua informasi dari sebuah baris data.


Anggaplah kita memiliki baris dokumen HTML berikut ini.


\>line="<tr\><td\>1145.45</td\><td\>5.6</td\><td\>-4.5</td\><tr\>"


    &lt;tr&gt;&lt;td&gt;1145.45&lt;/td&gt;&lt;td&gt;5.6&lt;/td&gt;&lt;td&gt;-4.5&lt;/td&gt;&lt;tr&gt;

Untuk mengekstrak ini, kita menggunakan ekspresi reguler, yang mencari


 - tanda kurung tutup &gt;,  
 - setiap string yang tidak mengandung tanda kurung dengan  

sub-pencocokan “(...)”,


 - kurung pembuka dan kurung penutup menggunakan solusi terpendek,


 - sekali lagi, semua string yang tidak mengandung tanda kurung,


 - dan sebuah kurung pembuka &lt;.


Ekspresi reguler agak sulit untuk dipelajari tetapi sangat kuat.


\>{pos,s,vt}=strxfind(line,"\>([^<\>]+)<.+?\>([^<\>]+)<");


Hasilnya adalah posisi kecocokan, string yang cocok, dan vektor string
untuk sub-cocokan.


\>for k=1:length(vt); vt[k](), end;


    1145.5
    5.6

Berikut ini adalah fungsi yang membaca semua item numerik antara &lt;td&gt;
dan &lt;/td&gt;.


\>function readtd (line) ...


    v=[]; cp=0;
    repeat
       {pos,s,vt}=strxfind(line,"<td.*?>(.+?)</td>",cp);
       until pos==0;
       if length(vt)>0 then v=v|vt[1]; endif;
       cp=pos+strlen(s);
    end;
    return v;
    endfunction
</pre>
\>readtd(line+"<td\>non-numerical</td\>")


    1145.45
    5.6
    -4.5
    non-numerical

# Membaca dari Web

Situs web atau file dengan URL dapat dibuka di EMT dan dapat dibaca
baris demi baris.


Dalam contoh, kita membaca versi saat ini dari situs EMT. Kami
menggunakan ekspresi reguler untuk memindai “Versi ...” dalam judul.


\>function readversion () ...


    urlopen("http://www.euler-math-toolbox.de/Programs/Changes.html");
    repeat
      until urleof();
      s=urlgetline();
      k=strfind(s,"Version ",1);
      if k>0 then substring(s,k,strfind(s,"<",k)-1), break; endif;
    end;
    urlclose();
    endfunction
</pre>
\>readversion


    Version 2024-01-12

# Masukan dan Keluaran Variabel

Anda dapat menulis variabel dalam bentuk definisi Euler ke file atau
ke baris perintah.


\>writevar(pi,"mypi");


    mypi = 3.141592653589793;

Untuk pengujian, kami membuat file Euler di direktori kerja EMT.


\>file="test.e"; ...  
\>   writevar(random(2,2),"M",file); ...  
\>   printfile(file,3)


    M = [ ..
    0.7018632700938628, 0.4610667290122583;
    0.2534612377845706, 0.4009688999887353];

Sekarang kita dapat memuat file tersebut. Ini akan mendefinisikan
matriks M.


\>load(file); show M,


    M = 
      0.70186   0.46107 
      0.25346   0.40097 

Sebagai catatan, jika writevar() digunakan pada sebuah variabel, maka
ia akan mencetak definisi variabel dengan nama variabel tersebut.


\>writevar(M); writevar(inch$)


    M = [ ..
    0.7018632700938628, 0.4610667290122583;
    0.2534612377845706, 0.4009688999887353];
    inch$ = 0.0254;

Kita juga dapat membuka file baru atau menambahkan ke file yang sudah
ada. Dalam contoh ini, kami menambahkan ke file yang telah dibuat
sebelumnya..


\>open(file,"a"); ...  
\>   writevar(random(2,2),"M1"); ...  
\>   writevar(random(3,1),"M2"); ...  
\>   close();

\>load(file); show M1; show M2;


    M1 = 
      0.46735   0.76609 
      0.13485   0.48387 
    M2 = 
      0.63738 
       0.9386 
      0.48331 

Untuk menghapus file, gunakan fileremove().


\>fileremove(file);


Sebuah vektor baris dalam sebuah file tidak membutuhkan koma, jika
setiap angka berada dalam baris baru. Mari kita buat file seperti itu,
dengan menulis setiap baris satu per satu dengan writeln().


\>open(file,"w"); writeln("M = ["); ...  
\>   for i=1 to 5; writeln(""+random()); end; ...  
\>   writeln("];"); close(); ...  
\>   printfile(file)


    M = [
    0.335382867375
    0.0437559600543
    0.912466569599
    0.931550760372
    0.593106410659
    ];

\>load(file); M


    [0.33538,  0.043756,  0.91247,  0.93155,  0.59311]

# Lataihan Soal dan Pembahasan

# Contoh soal 1 

1. Buatlah boxplot dari data berikut ini dan sertakan penjelasan dari
bloxplot tersebut (kuartil, median, nilai max/min)


P = (9,10,8,12,7,6,5,3,4,20,16,17,11,13,14)


\>P = [9,10,8,12,7,6,5,3,4,20,16,17,11,13,14]


    [9,  10,  8,  12,  7,  6,  5,  3,  4,  20,  16,  17,  11,  13,  14]

\>boxplot(P):


![images/Final%20Project%20Aplikom%20Semester%203-503.png](images/Final%20Project%20Aplikom%20Semester%203-503.png)

# Contoh soal 2 

Diberikan data dari penjualan kendaraan pada tahun 2045


Januari = 100


Februari = 200


Maret = 250


April = 50


Mei = 300


Juni = 500


Juli = 680


Agustus = 300


September = 450


Oktober = 450


November = 600


Desember = 700


buatlah diagram batang dengan color : hijau dab buatlah star plotnya


\>month=["Januari","Februari","Maret","April","Mei","Juni","Juli","Agustus","September","Oktober","November","Desember"];

\>values=[100,200,250,50,300,500,680,300,450,450,600,700];

\>columnsplot(values,lab=month,color=green);

\>title("Data Penjualan Kendaraan pada Tahun 2045")

\>insimg;


![images/Final%20Project%20Aplikom%20Semester%203-504.png](images/Final%20Project%20Aplikom%20Semester%203-504.png)

\>starplot(values,lab=month,\>rays):


![images/Final%20Project%20Aplikom%20Semester%203-505.png](images/Final%20Project%20Aplikom%20Semester%203-505.png)

# Soal 3

\>printfile("sample.csv",7)


    Could not open the file
    sample.csv
    for reading!
    Try "trace errors" to inspect local variables after errors.
    printfile:
        open(filename,"r");

\>ctok=[1]; {MT,hd,tok}=readtable("sample.csv",ctok=ctok);


    Could not open the file
    sample.csv
    for reading!
    Try "trace errors" to inspect local variables after errors.
    readtable:
        if filename!=none then open(filename,"r"); endif;

\>MT[2]


    MT is not a variable!
    Error in:
    MT[2] ...
         ^

\>writetable(MT[1:6],wc=5,labc=hd)


    MT is not a variable!
    Error in:
    writetable(MT[1:6],wc=5,labc=hd) ...
                      ^

# Soal 4

1. Diketahui data usia(dalam tahun) penduduk suatu daerah adalah
sebagai berikut:


6,7,9,7,8,8,4,3,5,7,11,12,13


hitunglah rata-rata usia penduduk tersebut.


\>mean([6,7,9,7,8,8,4,3,5,7,11,12,13])


    7.6923

