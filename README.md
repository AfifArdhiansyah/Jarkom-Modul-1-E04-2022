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

