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
Terdapat info kita dapat paket 20863 yang mengandung kata Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg dikirim dari client ke server. Kemudian kita cari responsenya dengan filter `http.request_in == 20863 && image-jfif` .  `http.request_in` untuk mencari paket dari request yang bersangkutan, `image-jfif` untuk memfilter JPEG File Interchange Format. Kemudian klik kanan pada filed JPEG File Intercharged Format dan pilih Export Packets Bytes.
![Hasil FIlter](https://github.com/Raferto/Jarkom_Modul1_Lapres_D06/blob/main/images/image27.jpg)

3.  Semangat Fid
4. Semangat Fid
5. Ikuti perintah di [aku.pengen.pw](http://aku.pengen.pw/)! Username dan password bisa didapatkan dari file .pcapng!
ketika buka aku.pengen.pw maka kita akan diminta untuk memasukan username dan password kita gunakan filter `**http.host== aku.pengen.pw && http.authbasic**
`
![Hasil FIlter](https://github.com/Raferto/Jarkom_Modul1_Lapres_D06/blob/main/images/image28.jpg)
Didapat username  `kakakgamtenk` dan password `hartatahtabermuda`
kemudian tinggal kita ikuti perintah yang ada pada website itu
![Intruksi Website](https://github.com/Raferto/Jarkom_Modul1_Lapres_D06/blob/main/images/image7.png)

6. semangat fid
7. semangat fid
8. semmangat fid
9. semangat fid
10. Cari file .pdf di wireshark lalu download dan buka file tersebut!
clue: "25 50 44 46" 
Untuk mencari file pdf kita bisa menggunakan `frame contains "application/pdf"
 ` atau `frame contains "\x25\x50\x44\x46"`
![Dispay FIlter](https://github.com/Raferto/Jarkom_Modul1_Lapres_D06/blob/main/images/image10.png)
Kemudian follow tcp stream dari paket yang ditemukan, kemudian save as raw data nya.
![Follow TCP Stream Raw Data](https://github.com/Raferto/Jarkom_Modul1_Lapres_D06/blob/main/images/image18.png)
Raw data di save sebagai .pdf. 
![Follow TCP Stream Raw Data](https://github.com/Raferto/Jarkom_Modul1_Lapres_D06/blob/main/images/image14.png)
