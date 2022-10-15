# Importing Spreadsheets or CSV files

Pada kali ini Kita akan mengimpor file teks dengan lokasi gempa dalam format tab-separated values (TSV) ke QGIS dan membuat layer poin.

## Hal - Hal yang Dibutuhkan

- Komputer / Laptop
- APK QGIS3
- Mengunduh salinan data [ne_10m_populated_places_simple.zip] (https://www.qgistutorials.com/downloads/earthquakes_2021_11_25_14_31_59_+0530.tsv)

## Pengambilan Data

1. Untuk tutorial ini kita akan mendownload dataset gempa bumi antara tahun 1900-2000 dari National Geophysical Data Center NOAA menghasilkan dataset besar dari semua gempa bumi signifikan sejak 2150 SM. Kunjungi portal NOAA NCEI dan masukkan Min as 1900dan Max as 2000. Ini akan mengembalikan semua insiden gempa yang terjadi dan dicatat oleh NOAA antara tahun-tahun itu. Untuk hasil spesifik lainnya, Anda dapat memfilter dengan parameter berbeda. Klik Cari .

2. Hasilnya, kami mendapat 2585 insiden gempa. Klik pada ikon Unduh TSV .

## Prosedur

1. Periksa sumber data tabular Anda. Basis data gempa yang diunduh berisi Latitudedan Longitudebidang yang menunjukkan lokasi episentrum gempa dan atribut terkait lainnya. Kami akan menggunakan bidang ini untuk mengimpor file sebagai lapisan titik. Buka data dalam editor teks seperti Notepad/TextMate untuk melihat isinya. Anda akan melihat bahwa TAB memisahkan setiap bidang.

------

Catatan :
Jika Anda memiliki spreadsheet, gunakan fungsi Save As di program Anda untuk menyimpannya sebagai File Tab Delimited atau file Comma Separated Values (CSV).

------

2. QGIS hadir dengan pengelola data terpadu yang memungkinkan Anda memuat semua berbagai format data yang didukung. Klik tombol Buka Pengelola Sumber Data pada Bilah Alat Sumber Data. Anda juga dapat menggunakan pintasan keyboard.Ctrl + L

3. Dalam kotak dialog Pengelola Sumber Data , alihkan ke tab Teks Dibatasi . Klik tombol ... di sebelah nama File.

4. Tergantung pada sistem operasinya, Anda mungkin atau mungkin tidak melihat file di lokasi yang diunduh. Dalam format File, alihkan ke untuk melihat file tsv .All files (*; *.*)

5. Sekarang Anda akan melihat file yang diunduh. Pilih itu dan klik Buka.

6. Di kotak dialog Pengelola Sumber Data , jalur ke file akan tersedia di Nama File . Ubah nama Lapisan menjadi 1900_2000_earthquakes. Di bagian Format file , pilih Pembatas khusus dan centang Tab. Di bagian Definisi geometri , pilih Koordinat titik . Secara default , nilai bidang X dan bidang Y akan terisi secara otomatis jika menemukan bidang nama yang sesuai di input. Dalam kasus kami, mereka adalah Longitudedan Latitude. Anda dapat mengubahnya jika impor memilih bidang yang salah. Anda dapat membiarkan Geometry CRS ke defaultEPSG:4326 - WGS 84CRS. Jika file Anda berisi koordinat dalam CRS yang berbeda, Anda dapat memilih CRS yang sesuai di sini. Klik Tambahkan.

-------

Catatan:

Sangat mudah untuk bingung antara koordinat X dan Y. Lintang menentukan posisi utara-selatan suatu titik dan karenanya merupakan koordinat Y. Demikian pula Bujur menentukan posisi timur-barat suatu titik dan itu adalah koordinat X.

---------

7. Anda sekarang akan melihat bahwa data akan diimpor dan ditampilkan di kanvas QGIS sebagai layer baru yang disebut 1900_2000_earthquakesdengan CRS EPSG:4326.





