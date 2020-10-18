# Jarkom_Modul1_Lapres_D06

 - **Rafid Ferdianto - 051118400000032**
 - **Abdur Rohman - 05111840000100**

## Soal
![Soal](https://github.com/Raferto/Jarkom_Modul1_Lapres_D06/blob/main/images/image1.png)

## Jawaban

 1. **Sebutkan webserver yang digunakan pada "[testing.mekanis.me](http://testing.mekanis.me/)"!**

Jelasin fid

2. **Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!**

Pada soal ini kita diminta untuk menyimpan gambar Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg.
Cara pertama bisa menggunakan fungsi export object dari wireshark dengan memfilter nama file yang diminta.

![Export Object](https://github.com/Raferto/Jarkom_Modul1_Lapres_D06/blob/main/images/images25.jpg)

Jika menggunkan filter maka pertama temukan informasi mengenai gambar dengan filter `http contains Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg` 

![Hasil FIlter](https://github.com/Raferto/Jarkom_Modul1_Lapres_D06/blob/main/images/image26.jpg)

Terdapat info kita dapat paket 20863 yang mengandung kata Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg dikirim dari client ke server. 

Kemudian kita cari responsenya dengan filter `http.request_in == 20863 && image-jfif` .  `http.request_in` untuk mencari paket dari request yang bersangkutan, `image-jfif` untuk memfilter JPEG File Interchange Format.

Kemudian klik kanan pada filed JPEG File Intercharged Format dan pilih Export Packets Bytes.

![Hasil FIlter](https://github.com/Raferto/Jarkom_Modul1_Lapres_D06/blob/main/images/image27.jpg)

3.  **Cari username dan password ketika login di "[ppid.dpr.go.id](http://ppid.dpr.go.id/)"!**

jawab
    

4. **Temukan paket dari web-web yang menggunakan basic authentication method!**

jawab

5. **Ikuti perintah di [aku.pengen.pw](http://aku.pengen.pw/)! Username dan password bisa didapatkan dari file .pcapng!**

Ketika membuka aku.pengen.pw maka kita akan diminta untuk memasukan username dan password kita gunakan filter `**http.host== aku.pengen.pw && http.authbasic**
`

![Hasil FIlter](https://github.com/Raferto/Jarkom_Modul1_Lapres_D06/blob/main/images/image28.jpg)

Didapat username  `kakakgamtenk` dan password `hartatahtabermuda`
kemudian tinggal kita ikuti perintah yang ada pada website itu'

![Intruksi Website](https://github.com/Raferto/Jarkom_Modul1_Lapres_D06/blob/main/images/image7.png)

6. **Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).**

pjunten
    
7. **Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut.  
    Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf"**

kerj
    
8. **Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!**

kerj
    
9. **Cari username dan password ketika login FTP pada localhost!**

kerjain fid

 
10. **Cari file .pdf di wireshark lalu download dan buka file tersebut!
clue: "25 50 44 46"**

Untuk mencari file pdf kita bisa menggunakan `frame contains "application/pdf"
 ` atau `frame contains "\x25\x50\x44\x46"`
 
![Dispay FIlter](https://github.com/Raferto/Jarkom_Modul1_Lapres_D06/blob/main/images/image10.png)

Kemudian follow tcp stream dari paket yang ditemukan, kemudian save as raw data nya.

![Follow TCP Stream Raw Data](https://github.com/Raferto/Jarkom_Modul1_Lapres_D06/blob/main/images/image18.png)

Raw data di save sebagai .pdf. 

![Follow TCP Stream Raw Data](https://github.com/Raferto/Jarkom_Modul1_Lapres_D06/blob/main/images/image29.png)

10.  **Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!**

Capture filter yang digunakan adalah `port 21` yaitu untuk memfilter semua koneksi yang berasal dan menuju port 21.
    ![Demo Capture FIlter](https://github.com/Raferto/Jarkom_Modul1_Lapres_D06/blob/main/images/image19.png)

11.  **Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!**

Capture filter yang digunakan adalah `src port 80` yaitu untuk memfilter semua koneksi yang berasal dari port 80.
    ![Demo Capture FIlter](https://github.com/Raferto/Jarkom_Modul1_Lapres_D06/blob/main/images/image16.png)
    
13.  **Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!** 

Capture filter yang digunakan adalah `dst port 443` yaitu untuk memfilter semua koneksi yang menuju port 443.
    ![Demo Capture FIlter](https://github.com/Raferto/Jarkom_Modul1_Lapres_D06/blob/main/images/image12.png)
    
14.  **Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!**

Pertama untuk mengetahui ip client digunakan perintah `ipconfig` pada `cmd`.
Setelah itu tinggal memasukan capture filter `src host 192.168.1.10`.
    ![Demo Capture FIlter](https://github.com/Raferto/Jarkom_Modul1_Lapres_D06/blob/main/images/image9.png)
    
15.  **Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!'**

Pertama untuk mengetahui ip monta.if.its.ac.id digunakan perintah `ping` pada `cmd` menuju monta.if.ac.id. Diketahui bahwa ip dari website yang dituju adalah 103.94.190.11.
Setelah itu tinggal memasukan capture filter `dst host 103.94.190.11`.
![Demo Capture FIlter](https://github.com/Raferto/Jarkom_Modul1_Lapres_D06/blob/main/images/image24.png)

