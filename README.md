# Jarkom-Modul-1-E04-2022

### Anggota Kelompok E04
Muhammad Afif Dwi Ardhiansyah /	5025201212 </br>
Muhammad Rafif Fadhil Naufal / 5025201273 </br>
M Labib Alfaraby / 5025201083 </br>

## Soal dan Jawaban
### Soal 1
Sebutkan web server yang digunakan pada "monta.if.its.ac.id"! 

### Jawaban
Langkah pertama yang dilakukan adalah dengan mem-filter `http contains "monta.if.its.ac.id"` </br></br>
<img width="663" alt="image" src="https://user-images.githubusercontent.com/87472849/191511340-9c14205b-f905-4669-834d-90a7fe40b3ae.png"> </br></br>
Lalu dengan menampilkan TCP akan didapatkan web servernya yaitu `ngingx/1.10.3` </br></br>
<img width="664" alt="image" src="https://user-images.githubusercontent.com/87472849/191511774-bdcafc8f-4506-4ee0-aa98-de58bb44c8a4.png">

### Soal 2
Ishaq sedang bingung mencari topik ta untuk semester ini , lalu ia datang ke website monta dan menemukan detail topik pada website “monta.if.its.ac.id” , judul TA apa yang dibuka oleh ishaq ?

### Jawaban
Pertama filter `http contains “monta.if.its.ac.id”`</br></br>
<img width="564" alt="image" src="https://user-images.githubusercontent.com/87472849/191514383-36218c12-cef7-4d72-847b-e56b2419ce93.png"></br></br>
Dari gambar di atas terdapat `detailTopik/194`. Lalu filter dengan `http` dan cari `text/html` di bawah `detailTopik/194`. Dilihat dari paket data maka akan ditemukan judul TA yaitu `Evaluasi unjuk kerja User Space Filesystem`</br></br>
<img width="565" alt="image" src="https://user-images.githubusercontent.com/87472849/191515135-51cfa82a-452c-4535-a87e-222d83162251.png"></br>
<img width="560" alt="image" src="https://user-images.githubusercontent.com/87472849/191515240-08e48cae-3d17-4f5c-9611-ddc377e45f6e.png">

### Soal 3
Filter sehingga wireshark hanya menampilkan paket yang menuju port 80!

### Jawaban
Untuk menampilkan paket yang menuju port 80 dapat dilakukan filter `tcp.dstport == 80`</br></br>
<img width="562" alt="image" src="https://user-images.githubusercontent.com/87472849/191528872-a5e3e836-6601-49cf-9347-55e1577407bd.png">

### Soal 4
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 21!

### Jawaban
Untuk menampilkan paket yang berasal dari port 21 dapat dilakukan filter `tcp.srcport == 21`</br></br>
<img width="564" alt="image" src="https://user-images.githubusercontent.com/87472849/191529528-bf10a16c-10af-45a2-ad2b-251f28419123.png">

### Soal 5
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 443!

### Jawaban
Untuk menampilkan paket yang berasal dari port 443 dapat dilakukan filter `tcp.srcport == 443`</br></br>
<img width="563" alt="image" src="https://user-images.githubusercontent.com/87472849/191530097-4dafa208-f026-4f84-98f1-5f04d771f6eb.png">

### Soal 6
Filter sehingga wireshark hanya menampilkan paket yang menuju ke lipi.go.id !

### Jawaban
Pertama perlu tahu dulu ip address dari lipi.go.id dengan cara ping pada command prompt sebagai berikut</br></br>
<img width="400" alt="image" src="https://user-images.githubusercontent.com/87472849/191530702-695d58d2-a7a0-4a0c-92e5-067964e88c90.png"></br></br>
Dari gambar di atas didapatkan ip address lipi.go.id adalah 203.160.128.158. Kemudian filter dengan `ip.dst == 203.160.128.158`</br></br>
<img width="565" alt="image" src="https://user-images.githubusercontent.com/87472849/191531254-720b0bc2-0043-49e2-873f-186338bc5c5a.png">

### Soal 7
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
### Jawaban
Pertama kita buka CMD, lalu ketik ipconfig<br>
![image](https://user-images.githubusercontent.com/81162174/191536113-a82919e1-6a14-4252-9ca4-bf38902a8806.png)<br>
Cari Ip anda di bagian Wireless LAN adapter WIFI di row IPv4 Address <br>
![image](https://user-images.githubusercontent.com/81162174/191536623-55b809e8-ef0a-4167-8610-c36ba6ec4b79.png)<br>
Lalu tekan Capture option dan tekan WIFI lalu masukan di captuure filter src host (IP kalian)<br>
![image](https://user-images.githubusercontent.com/81162174/191537235-261981ab-b52b-42e2-b9d5-137e8966c12b.png)<br>


### Soal 8
Telusuri aliran paket dalam file .pcap yang diberikan, cari informasi berguna berupa percakapan antara dua mahasiswa terkait tindakan kecurangan pada kegiatan praktikum.<br> Percakapan tersebut dilaporkan menggunakan protokol jaringan dengan tingkat keandalan yang tinggi dalam pertukaran datanya sehingga kalian perlu menerapkan filter dengan protokol yang tersebut.<br>
### Jawaban
Terdapat tiga buah pesan rahasia yang ditemukan. Pertama, gunakan command tcp.stream eq 12 untuk menemukan percakapan antar host yang diinginkan.<br> 
Kita menggunakan tcp.stream karena untuk mendapatkan konversasi dengan cepat, kenapa 12 karena index percakapan mereka berada di index 12<br>
![image](https://user-images.githubusercontent.com/81162174/191540837-a8f06f5b-89e4-43c7-a0cc-ce3df60f546d.png)<br>
Click salah satu lalu click kanan -> follow -> TCP STREAM nanti muncul percakapan mereka<br>
![image](https://user-images.githubusercontent.com/81162174/191541028-c14cfa22-1864-4cf2-8df2-10554127ee11.png)

Dengan menggunakan langkah yang sama, kita akan mencari percakapan rahasia lainnya. Selanjutnya, gunakan command tcp.stream eq 41 maka ditemukan percakapan yang kedua
![Screenshot 2022-09-22 193027](https://user-images.githubusercontent.com/96496752/191747947-e0a5b609-fc22-4663-ac59-53519b843430.jpg)

Terakhir, gunakan command tcp.stream eq 90 maka ditemukan percakapan yang ketiga
![Screenshot 2022-09-22 193108](https://user-images.githubusercontent.com/96496752/191748061-53aedac3-ca24-4e45-a8ca-d0e59dd95dbe.jpg)


### Soal 9
Terdapat laporan adanya pertukaran file yang dilakukan oleh kedua mahasiswa dalam percakapan yang diperoleh, carilah file yang dimaksud! Untuk memudahkan laporan kepada atasan, beri nama file yang ditemukan dengan format [nama_kelompok].des3 dan simpan output file dengan nama “flag.txt”.
### Jawaban
File yang dimaksud pada soal ini berupa data dalam bentuk string. Terdapat clue pada soal, yaitu penyimpanan file dengan extension .des3, yang tak lain merupakan salah satu metode enkripsi sehingga data bisa berisi string yang telah  terenkripsi. Kita gunakan command tcp.stream eq 29 untuk menemukan file yang dimaksud, nilai eq 29 merupakan index dari file. Selanjutnya, kita simpan file dalam bentuk raw dan beri penamaan E04.des3.

<img width="451" alt="Picture3" src="https://user-images.githubusercontent.com/96496752/191625037-efb46666-0391-4838-a8cd-a4272bb7ee98.png">

### Soal 10
Temukan password rahasia (flag) dari organisasi bawah tanah yang disebutkan di atas!
### Jawaban
Pada soal 8 kita telah menemukan pesan percakapan dua mahasiswa. Salah satu topik pembicaraan keduanyan, yaitu mengenai password. Password yang dimaksud adalah password / key untuk dekripsi .des3 dari file yang telah kita peroleh pada soal 9. Langkah - langkah yang dilakukan untuk melakukan deskripsi adalah sebagai berikut,

1. Membuka cmd / git bash/ terminal lain. Kelompok kami menggunakan cmd dengan ketentuan telah mendownload openssl.
2. Gunakan command [openssl des3 -d -in (nama file input) -out (nama file output)]
3. kemudian masukkan password deskripsi, yaitu 'nakano' sesuai dengan isi percakapan soal 8
4. lihat file output, maka diperoleh password rahasia yang dimaksud. Yaitu "JaRkOm2022{8uK4N_CtF_k0k_h3h3h3}"

![Picture2](https://user-images.githubusercontent.com/96496752/191625008-419c4f28-3d9a-46f4-87be-f43fc205301d.png)
![Picture1](https://user-images.githubusercontent.com/96496752/191625031-ab0a25b0-fcba-4970-9730-37571c312c42.png)

