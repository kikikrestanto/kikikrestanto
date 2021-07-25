1. Soal Story Logic
Pak budi mempunyai sebidang sawah berbentuk persegi, Karena sakit pak budi menjual 1/4 tanahnya. Ketika pak budi meninggal, pak budi meninggalkan 4 orang anak yang menunggu harta warisan sebidang sawah.


![image](https://user-images.githubusercontent.com/35162041/126903323-d404cc83-bd34-4326-8782-fbf83f26e473.png)


Instruksi:
- Bagaimana membagi tanah 3/4 kepada 4 orang anak sama rata dan sama bentuk.
- Berikan dalam bentuk gambar

Jawaban 

![image](https://user-images.githubusercontent.com/35162041/126903482-bb45e980-fd74-43d2-89dc-abe4adeeef69.png)


2.Buat sebuah form input text dengan 1 tombol submit Pada form tersebut user akan memasukkan text dengan format Nama Usia Kota Contoh : Dimas Saputra 27 Bandung.

Ketika di klik tombol submit, akan di cetak dalam bentuk tabel:

![image](https://user-images.githubusercontent.com/35162041/126903514-4b9eec8b-cd1d-432b-977d-10abd0f0754a.png)

Instruksi:
-Gunakan bahasa pemrograman PHP
-Program harus bisa menghandle kata TH atau kata Tahun yang biasanya tanpa sengaja ditambahkan oleh user pada saat mengetik USIA, contoh Edy Suprayitno 25th Malang
-Text nama dan Kota tidak boleh dibatasi
-Text nama dan kota hanya memuat huruf alphabet
-Text usia hanya memuat numeric tanpa kata tahun / th
-Jika tidak punya server, Upload ke repo github masing2, jangan lupa berika link nya.

Jawaban 
Link repo saya
https://github.com/kikikrestanto/formphp

3. soal RDBMS
-Tampilkan nama film dengan artis bayaran terendah dalam bentuk query
select nm_film, artis,nm_artis, MIN(bayaran) As BayaranTerendah
from public.film,  public.artis

-Tampilkan nama film yang dibintangi oleh artis yang huruf depannya 'j' dalam bentuk query
select nm_film,artis ,nm_artis
from public.film, public.artis
where nm_artis LIKE 'j%';

-Tampilkan jumlah film dari masing2 produser dalam bentuk query
select nm_film, produser, nm_produser,
max(filmCount) as filmCount, produser
from (
select nm_film, produser, nm_produser,
count(*) as filmCount
from product.film
group by nm_film, produser, nm_produser
)
group by produser

-Tampilkan nama artis yang bermain film dengan genre horror dalam bentuk query
 tidak ada film dengan genre horror
