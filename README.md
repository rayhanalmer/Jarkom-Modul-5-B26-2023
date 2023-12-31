# Jarkom-Modul-5-B26-2023

## Anggota Kelompok B26
|   Nama                             | NRP      |
| ------                             | ------   |
|  Rayhan Almer Kusumah              |5025211115|
|  Nur Azizah                        |5025211252|
|  Faiz Haq Noviandra Ciptadi Putra  |5025211132|

## Soal
Setelah pandai mengatur jalur-jalur khusus, kalian diminta untuk membantu North Area menjaga wilayah mereka dan kalian dengan senang hati membantunya karena ini merupakan tugas terakhir.  

- (A) Tugas pertama, buatlah peta wilayah sesuai berikut ini:
  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/03291954-d06f-4d26-a595-39ec015b2100)  

- (B) Untuk menghitung rute-rute yang diperlukan, gunakan perhitungan dengan metode VLSM. Buat juga pohonnya, dan lingkari subnet yang dilewati.  


- (C) Kemudian buatlah rute sesuai dengan pembagian IP yang kalian lakukan.  


- (D) Tugas berikutnya adalah memberikan ip pada subnet SchwerMountain, LaubHills, TurkRegion, dan GrobeForest menggunakan bantuan DHCP.  

### Penyelesaian
Setelah topologi berhasil dibuat pada GNS3, langkah selanjutnya yang dilakukan adalah membuat rute dan melakukan subnetting. Berikut adalah hasil dari pembuatan rute serta subnetting yang sudah dilakukan:  
- Topology GNS3
  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/2e6e1bd8-48fa-41c3-a88f-16f275a8f44d)  

- Rute
  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/91bf21d5-5a39-4f75-becd-f42aa8f8b643)  

- Tree VLSM
  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/6527579d-e7f2-4507-a190-d27f3ca3a61d)  

- Pembagian Network ID & Broadcast
  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/f78b9e06-8bed-4063-a687-312a0cdf041e)  

- Pembagian IP Node
  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/3ba8e036-2d64-44d2-a289-4b7ef0ba3009)  

- Konfigurasi Node  
Setelah melakukan subnetting, maka langkah selanjutnya adalah melakukan kongfigurasi untuk setiap node. Berikut adalah kongfigurasi untuk tiap node dalam topologi pada soal praktikum:  

  - Aura
  ```
  auto eth0
  iface eth0 inet dhcp
  
  auto eth1
  iface eth1 inet static
  	address 192.191.14.129
  	netmask 255.255.255.252
  
  auto eth2
  iface eth2 inet static
  	address 192.191.14.133
  	netmask 255.255.255.252
  ```

  - Richter  
  ```
  auto eth0
  iface eth0 inet static
  	address 192.191.14.146
  	netmask 255.255.255.252
      gateway 192.191.14.145
  ```
  
  - Revolte  
  ```
  auto eth0
  iface eth0 inet static
  	address 192.191.14.150
  	netmask 255.255.255.252
      gateway 192.191.14.149
  ```
  
  - Sein  
  ```
  auto eth0
  iface eth0 inet static
  	address 192.191.8.2
  	netmask 255.255.252.0
  	gateway 192.191.8.1
  ```
  
  - Stark  
  ```
  auto eth0
  iface eth0 inet static
  	address 192.191.14.138
  	netmask 255.255.255.252
      gateway 192.191.14.137
  ```
  
  - Heiter  
  ```
  auto eth0
  iface eth0 inet static
  	address 192.191.14.130
  	netmask 255.255.255.252
          	gateway 192.191.14.129
  
  auto eth1
  iface eth1 inet static
  	address 192.191.0.1
  	netmask 255.255.248.0
  
  auto eth2
  iface eth2 inet static
  	address 192.191.8.1
  	netmask 255.255.252.0
  ```
  
  - Frieren  
  ```
  auto eth0
  iface eth0 inet static
  	address 192.191.14.134
  	netmask 255.255.255.252
      gateway 192.191.14.133
  
  auto eth1
  iface eth1 inet static
  	address 192.191.14.141
  	netmask 255.255.255.252
  
  auto eth2
  iface eth2 inet static
  	address 192.191.14.137
  	netmask 255.255.255.252
  ```
  
  - Himmels  
  ```
  auto eth0
  iface eth0 inet static
  	address 192.191.14.142
  	netmask 255.255.255.252
          gateway 192.191.14.141
  
  auto eth1
  iface eth1 inet static
  	address 192.191.12.1
  	netmask 255.255.254.0
  
  auto eth2
  iface eth2 inet static
  	address 192.191.14.1
  	netmask 255.255.255.128
  ```
  
  - Fern  
  ```
  auto eth0
  iface eth0 inet static
  	address 192.191.14.2
  	netmask 255.255.255.128
          	gateway 192.191.14.1
  
  auto eth1
  iface eth1 inet static
  	address 192.191.14.145
  	netmask 255.255.255.252
  
  auto eth2
  iface eth2 inet static
      address 192.191.14.149
  	netmask 255.255.255.252
  ```
    
  - SchwerMountain  
  ```
  auto eth0
  iface eth0 inet dhcp
  ```
    
  - LaubHills  
  ```
  auto eth0
  iface eth0 inet dhcp
  ```
    
  - TurkRegion  
  ```
  auto eth0
  iface eth0 inet dhcp
  ```
    
  - GrobeForest  
  ```
  auto eth0
  iface eth0 inet dhcp
  ```

## Soal 1
Agar topologi yang kalian buat dapat mengakses keluar, kalian diminta untuk mengkonfigurasi Aura menggunakan iptables, tetapi tidak ingin menggunakan MASQUERADE.

### Penyelesaian

```
ETH0_IP=$(ip -4 addr show eth0 | grep -oP '(?<=inet\s)\d+(\.\d+){3}')

iptables -t nat -A POSTROUTING -o eth0 -j SNAT --to-source $ETH0_IP
```

Penjelasan:  
- `ETH0_IP=$(ip -4 addr show eth0 | grep -oP '(?<=inet\s)\d+(.\d+){3}')`  
`ip -4 addr show eth0`: Ini adalah perintah untuk menampilkan informasi alamat IP untuk antarmuka jaringan `eth0`.  
`grep -oP '(?<=inet\s)\d+(\.\d+){3}'`: Ini menggunakan `grep` dengan opsi `-oP` yang mengizinkan penggunaan ekspresi reguler Perl (`P`). Ekspresi reguler ini mencari pola yang sesuai dengan alamat IPv4 (`\d+(\.\d+){3}`) yang terdapat setelah kata "inet" di output sebelumnya. Hasilnya akan berupa alamat IP dari antarmuka `eth0`.  
`ETH0_IP=$(...)`: Menggunakan perintah substitusi untuk menetapkan hasil eksekusi perintah di dalam tanda kurung ke dalam variabel `ETH0_IP`.  
- `iptables -t nat -A POSTROUTING -o eth0 -j SNAT --to-source $ETH0_IP`  
`iptables`: Ini adalah perintah untuk mengonfigurasi tabel iptables.  
`-t nat`: Menentukan tabel yang akan diubah, dalam hal ini, tabel "nat" (Network Address Translation).  
`-A POSTROUTING`: Menambahkan aturan ke chain POSTROUTING, yang akan dijalankan setelah proses routing.  
`-o eth0`: Spesifikasi bahwa aturan ini akan diterapkan hanya untuk paket yang keluar melalui antarmuka jaringan `eth0`.  
`-j SNAT`: Menentukan target aturan, di sini, SNAT (Source NAT), yang digunakan untuk mengganti alamat sumber paket.  
`--to-source $ETH0_IP`: Menentukan alamat IP yang akan digunakan sebagai alamat sumber yang baru. Nilainya diambil dari variabel `ETH0_IP`, yang berisi alamat IP dari antarmuka `eth0` yang ditemukan sebelumnya.  

Output:  
  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/9e0c13d5-63eb-42f7-9eef-402dcff1fd4e)  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/2600abec-0267-45cd-afdf-98b4498bd02e)  


## Soal 2
Kalian diminta untuk melakukan drop semua TCP dan UDP kecuali port 8080 pada TCP.

### Penyelesaian

```
iptables -F

iptables -A INPUT -p icmp -j ACCEPT

iptables -A INPUT -p tcp --dport 8080 -j ACCEPT

iptables -A INPUT -p tcp -j DROP

iptables -A INPUT -p udp -j DROP
```

Penjelasan:  
- `iptables -F`  
`-F`: Perintah ini digunakan untuk menghapus semua aturan (rules) yang telah ada sebelumnya di semua chain iptables.  
- `iptables -A INPUT -p icmp -j ACCEPT`  
`-A INPUT`: Menambahkan aturan ke chain INPUT, yang digunakan untuk mengatur paket yang menuju ke sistem.  
`-p icmp`: Menentukan protokol yang diizinkan, dalam hal ini ICMP (ping).  
`-j ACCEPT`: Menentukan target aturan, yaitu ACCEPT, yang berarti paket ICMP akan diterima.  
- `iptables -A INPUT -p tcp --dport 8080 -j ACCEPT`  
`-A INPUT`: Menambahkan aturan ke chain INPUT.  
`-p tcp`: Menentukan protokol yang diizinkan, yaitu TCP.  
`--dport 8080`: Menentukan port tujuan (destination port) yang diizinkan, dalam hal ini, port 8080.  
`-j ACCEPT`: Menentukan target aturan, yaitu ACCEPT, yang berarti paket TCP dengan port tujuan 8080 akan diterima.  
- `iptables -A INPUT -p tcp -j DROP`  
`-A INPUT`: Menambahkan aturan ke chain INPUT.  
`-p tcp`: Menentukan protokol yang diizinkan, yaitu TCP.  
`-j DROP`: Menentukan target aturan, yaitu DROP, yang berarti semua paket TCP akan ditolak.  
- `iptables -A INPUT -p udp -j DROP`  
`-A INPUT`: Menambahkan aturan ke chain INPUT.  
`-p udp`: Menentukan protokol yang diizinkan, yaitu UDP.  
`-j DROP`: Menentukan target aturan, yaitu DROP, yang berarti semua paket UDP akan ditolak.  

Output:  
  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/99a69618-5f9c-4336-a826-99021df16d5f)  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/d91102ca-49c2-468d-b2e6-02dbc03bcab3)  

## Soal 3
Kepala Suku North Area meminta kalian untuk membatasi DHCP dan DNS Server hanya dapat dilakukan ping oleh maksimal 3 device secara bersamaan, selebihnya akan di drop.

### Penyelesaian

```
iptables -A INPUT -m state --state ESTABLISHED,RELATED -j ACCEPT

iptables -A INPUT -p icmp -m connlimit --connlimit-above 3 --connlimit-mask 0 -j DROP
```

Penjelasan:  
- `iptables -A INPUT -m state --state ESTABLISHED,RELATED -j ACCEPT`  
`-A INPUT`: Menambahkan aturan ke chain INPUT, yang digunakan untuk mengatur paket yang menuju ke sistem.  
`-m state`: Menggunakan modul state, yang memungkinkan kita untuk menentukan aturan berdasarkan status koneksi.  
`--state ESTABLISHED,RELATED`: Menentukan bahwa aturan ini akan diterapkan pada paket-paket yang memiliki status koneksi "ESTABLISHED" atau "RELATED". Paket "ESTABLISHED" adalah paket yang terkait dengan koneksi yang sudah ada, sedangkan "RELATED" adalah paket yang terkait dengan koneksi yang sudah ada, tetapi bukan bagian dari koneksi itu sendiri (misalnya, paket ICMP yang terkait dengan koneksi TCP).  
`-j ACCEPT`: Menentukan target aturan, yaitu ACCEPT, yang berarti paket-paket dengan status koneksi "ESTABLISHED" atau "RELATED" akan diterima.  
- `iptables -A INPUT -p icmp -m connlimit --connlimit-above 3 --connlimit-mask 0 -j DROP`  
`-A INPUT`: Menambahkan aturan ke chain INPUT.  
`-p icmp`: Menentukan protokol yang diizinkan, yaitu ICMP.  
`-m connlimit`: Menggunakan modul connlimit, yang memungkinkan kita untuk menentukan aturan berdasarkan jumlah koneksi.  
`--connlimit-above 3`: Menentukan bahwa aturan ini akan diterapkan pada paket ICMP yang melebihi 3 koneksi.  
`--connlimit-mask 0`: Menentukan bahwa seluruh alamat IP akan dihitung, tanpa pembatasan berdasarkan subnet (mask 0).  
`-j DROP`: Menentukan target aturan, yaitu DROP, yang berarti paket-paket ICMP yang melebihi batasan koneksi akan ditolak.  

Output:  
  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/00bfe60f-145c-471e-a243-1c055fe630a5)  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/3eb3dff4-c63b-4883-91c0-f4e037b9e1df)  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/c1813681-fde0-4ad0-8700-05551d6b226a)  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/6be2466f-a6b0-4532-be47-20990dc47429)  

## Soal 4
Lakukan pembatasan sehingga koneksi SSH pada Web Server hanya dapat dilakukan oleh masyarakat yang berada pada GrobeForest.

### Penyelesaian

```
iptables -A INPUT -p tcp --dport 22 -s 192.191.8.0/22 -j ACCEPT

iptables -A INPUT -p tcp --dport 22 -j DROP
```

Penjelasan:  
- `iptables -A INPUT -p tcp --dport 22 -s 192.191.8.0/22 -j ACCEPT`  
`-A INPUT`: Menambahkan aturan ke chain INPUT, yang digunakan untuk mengatur paket yang menuju ke sistem.  
`-p tcp`: Menentukan protokol yang diizinkan, yaitu TCP.  
`--dport 22`: Menentukan port tujuan (destination port), dalam hal ini, port 22 (SSH).  
`-s 192.191.8.0/22`: Menentukan alamat IP sumber yang diizinkan, dalam hal ini, rentang alamat IP dari 192.191.8.0 hingga 192.191.11.255.  
`-j ACCEPT`: Menentukan target aturan, yaitu ACCEPT, yang berarti paket TCP dengan port tujuan 22 dan berasal dari alamat IP yang diizinkan akan diterima.  
- `iptables -A INPUT -p tcp --dport 22 -j DROP`  
`-A INPUT`: Menambahkan aturan ke chain INPUT.  
`-p tcp`: Menentukan protokol yang diizinkan, yaitu TCP.  
`--dport 22`: Menentukan port tujuan (destination port), dalam hal ini, port 22 (SSH).  
`-j DROP`: Menentukan target aturan, yaitu DROP, yang berarti semua paket TCP dengan port tujuan 22 akan ditolak.  

Output:  
  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/1705bb6f-781c-46c4-b925-d8ec26d50d1f)  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/565fb1c8-ebe7-459e-b5f7-ad70c064b5ad)  

## Soal 5
Selain itu, akses menuju WebServer hanya diperbolehkan saat jam kerja yaitu Senin-Jumat pada pukul 08.00-16.00.

### Penyelesaian

```
iptables -A INPUT -p tcp --dport 22 -s 192.191.8.0/22 -m time --timestart 08:00 --timestop 16:00 --weekdays Mon,Tue,Wed,Thu,Fri -j ACCEPT

iptables -A INPUT -p tcp --dport 22 -j DROP
```

Penjelasan:  
- `iptables -A INPUT -p tcp --dport 22 -s 192.191.8.0/22 -m time --timestart 08:00 --timestop 16:00 --weekdays Mon,Tue,Wed,Thu,Fri -j ACCEPT`  
`-A INPUT`: Menambahkan aturan ke chain INPUT, yang digunakan untuk mengatur paket yang menuju ke sistem.  
`-p tcp`: Menentukan protokol yang diizinkan, yaitu TCP.  
`--dport 22`: Menentukan port tujuan (destination port), dalam hal ini, port 22 (SSH).  
`-s 192.191.8.0/22`: Menentukan alamat IP sumber yang diizinkan, dalam hal ini, rentang alamat IP dari 192.191.8.0 hingga 192.191.11.255.  
`-m time --timestart 08:00 --timestop 16:00 --weekdays Mon,Tue,Wed,Thu,Fri`: Menggunakan modul time untuk menentukan waktu di mana aturan ini berlaku. Aturan ini hanya berlaku pada waktu mulai dari pukul 08:00 hingga 16:00 pada hari Senin sampai Jumat.  
`-j ACCEPT`: Menentukan target aturan, yaitu ACCEPT, yang berarti paket TCP dengan port tujuan 22, berasal dari alamat IP yang diizinkan, dan sesuai dengan jadwal waktu yang ditentukan akan diterima.  
- `iptables -A INPUT -p tcp --dport 22 -j DROP`  
`-A INPUT`: Menambahkan aturan ke chain INPUT.  
`-p tcp`: Menentukan protokol yang diizinkan, yaitu TCP.  
`--dport 22`: Menentukan port tujuan (destination port), dalam hal ini, port 22 (SSH).  
`-j DROP`: Menentukan target aturan, yaitu DROP, yang berarti semua paket TCP dengan port tujuan 22 akan ditolak.  

Output:  
  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/d683e64c-38ba-45e9-9ec8-5f540e8a321d)  

## Soal 6
Lalu, karena ternyata terdapat beberapa waktu di mana network administrator dari WebServer tidak bisa stand by, sehingga perlu ditambahkan rule bahwa akses pada hari Senin - Kamis pada jam 12.00 - 13.00 dilarang (istirahat maksi cuy) dan akses di hari Jumat pada jam 11.00 - 13.00 juga dilarang (maklum, Jumatan rek).

### Penyelesaian

```
iptables -A INPUT -p tcp --dport 22 -s 192.191.8.0/22 -m time --timestart 12:00 --timestop 13:00 --weekdays Mon,Tue,Wed,Thu -j DROP

iptables -A INPUT -p tcp --dport 22 -s 192.191.8.0/22 -m time --timestart 11:00 --timestop 13:00 --weekdays Fri -j DROP
```

Penjelasan:  
- `iptables -A INPUT -p tcp --dport 22 -s 192.191.8.0/22 -m time --timestart 12:00 --timestop 13:00 --weekdays Mon,Tue,Wed,Thu -j DROP`  
`-A INPUT`: Menambahkan aturan ke chain INPUT, yang digunakan untuk mengatur paket yang menuju ke sistem.  
`-p tcp`: Menentukan protokol yang diizinkan, yaitu TCP.  
`--dport 22`: Menentukan port tujuan (destination port), dalam hal ini, port 22 (SSH).  
`-s 192.191.8.0/22`: Menentukan alamat IP sumber yang diizinkan, dalam hal ini, rentang alamat IP dari 192.191.8.0 hingga 192.191.11.255.  
`-m time --timestart 12:00 --timestop 13:00 --weekdays Mon,Tue,Wed,Thu`: Menggunakan modul time untuk menentukan waktu di mana aturan ini berlaku. Aturan ini hanya berlaku pada waktu mulai dari pukul 12:00 hingga 13:00 pada hari Senin sampai Kamis.  
`-j DROP`: Menentukan target aturan, yaitu DROP, yang berarti paket TCP dengan port tujuan 22, berasal dari alamat IP yang diizinkan, dan sesuai dengan jadwal waktu yang ditentukan akan ditolak.  
- `iptables -A INPUT -p tcp --dport 22 -s 192.191.8.0/22 -m time --timestart 11:00 --timestop 13:00 --weekdays Fri -j DROP`  
`-A INPUT`: Menambahkan aturan ke chain INPUT.  
`-p tcp`: Menentukan protokol yang diizinkan, yaitu TCP.  
`--dport 22`: Menentukan port tujuan (destination port), dalam hal ini, port 22 (SSH).  
`-s 192.191.8.0/22`: Menentukan alamat IP sumber yang diizinkan, dalam hal ini, rentang alamat IP dari 192.191.8.0 hingga 192.191.11.255.  
`-m time --timestart 11:00 --timestop 13:00 --weekdays Fri`: Menggunakan modul time untuk menentukan waktu di mana aturan ini berlaku. Aturan ini hanya berlaku pada waktu mulai dari pukul 11:00 hingga 13:00 pada hari Jumat.  
`-j DROP`: Menentukan target aturan, yaitu DROP, yang berarti paket TCP dengan port tujuan 22, berasal dari alamat IP yang diizinkan, dan sesuai dengan jadwal waktu yang ditentukan akan ditolak.  

Output:  
  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/a3ee0abf-859a-44d0-bede-744176395cab)  

## Soal 7
Karena terdapat 2 WebServer, kalian diminta agar setiap client yang mengakses Sein dengan Port 80 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan dan request dari client yang mengakses Stark dengan port 443 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan.

### Penyelesaian

```
iptables -A PREROUTING -t nat -p tcp --dport 80 -d 192.191.8.2 -m statistic --mode nth --every 2 --packet 0 -j DNAT --to-destination 192.191.14.138

iptables -A PREROUTING -t nat -p tcp --dport 80 -d 192.191.8.2 -j DNAT --to-destination 192.191.14.138

iptables -A PREROUTING -t nat -p tcp --dport 443 -d 192.191.14.138 -m statistic --mode nth --every 2 --packet 0 -j DNAT --to-destination 192.191.8.2

iptables -A PREROUTING -t nat -p tcp --dport 443 -d 192.191.14.138 -j DNAT --to-destination 192.191.8.2
```

Penjelasan:  
- `iptables -A PREROUTING -t nat -p tcp --dport 80 -d 192.191.8.2 -m statistic --mode nth --every 2 --packet 0 -j DNAT --to-destination 192.191.14.138`  
`-A PREROUTING`: Menambahkan aturan ke chain PREROUTING pada tabel nat. Chain ini digunakan untuk mengatur paket sebelum melewati proses routing.  
`-t nat`: Menentukan tabel yang akan diubah, dalam hal ini, tabel "nat" (Network Address Translation).  
`-p tcp`: Menentukan protokol yang diizinkan, yaitu TCP.  
`--dport 80`: Menentukan port tujuan (destination port), dalam hal ini, port 80 (HTTP).  
`-d 192.191.8.2`: Menentukan alamat tujuan (destination address), dalam hal ini, alamat IP 192.191.8.2.  
`-m statistic --mode nth --every 2 --packet 0`: Menggunakan modul statistic untuk memilih paket berdasarkan urutan statistik. Dalam hal ini, setiap paket kedua (every 2) yang sesuai dengan kondisi akan diambil (packet 0).  
`-j DNAT --to-destination 192.191.14.138`: Menentukan target aturan, yaitu DNAT (Destination NAT), yang digunakan untuk mengganti alamat tujuan paket. Alamat IP tujuan akan diubah menjadi 192.191.14.138.  
- `iptables -A PREROUTING -t nat -p tcp --dport 80 -d 192.191.8.2 -j DNAT --to-destination 192.191.14.138`  
Parameter dan fungsinya sama seperti pada baris pertama, namun tanpa modul `statistic`.  
- `iptables -A PREROUTING -t nat -p tcp --dport 443 -d 192.191.14.138 -m statistic --mode nth --every 2 --packet 0 -j DNAT --to-destination 192.191.8.2`  
Parameter dan fungsinya sama seperti pada baris pertama, namun dengan port tujuan 443 (HTTPS) dan alamat tujuan awal 192.191.14.138.  
- `iptables -A PREROUTING -t nat -p tcp --dport 443 -d 192.191.14.138 -j DNAT --to-destination 192.191.8.2`  
Parameter dan fungsinya sama seperti pada baris kedua, namun dengan port tujuan 443 (HTTPS) dan alamat tujuan awal 192.191.14.138.  

Kemudian dapat dilakukan testing dengan cara membuka koneksi pada webserver yaitu sein dan stark dengan syntax berikut  

Untuk port 80    
`while true; do nc -l -p 80 -c 'echo "ini sein"'; done` dan  
`while true; do nc -l -p 80 -c 'echo "ini stark"'; done.`  
  
Untuk port 443  
`while true; do nc -l -p 443 -c 'echo "ini sein"'; done` dan  
`while true; do nc -l -p 443 -c 'echo "ini stark"'; done`  

Output:  
  


## Soal 8
Karena berbeda koalisi politik, maka subnet dengan masyarakat yang berada pada Revolte dilarang keras mengakses WebServer hingga masa pencoblosan pemilu kepala suku 2024 berakhir. Masa pemilu (hingga pemungutan dan penghitungan suara selesai) kepala suku bersamaan dengan masa pemilu Presiden dan Wakil Presiden Indonesia 2024.

### Penyelesaian

Di web server (Sein dan Stark), lakukan seperti di bawah ini  
```
iptables -A INPUT -s 192.191.14.150 -p tcp --dport 80 -m time --datestart 2023-12-14 --datestop 2024-06-26 -j DROP
```

Penjelasan:  
`-A INPUT`: Menambahkan aturan ke chain INPUT, yang digunakan untuk mengatur paket yang menuju ke sistem.  
`-s 192.191.14.150`: Menentukan alamat IP sumber yang akan diaplikasikan aturan, dalam hal ini, alamat IP 192.191.14.150.  
`-p tcp`: Menentukan protokol yang diizinkan, yaitu TCP.  
`--dport 80`: Menentukan port tujuan (destination port), dalam hal ini, port 80 (HTTP).  
`-m time --datestart 2023-12-14 --datestop 2024-06-26`: Menggunakan modul time untuk menentukan aturan berdasarkan tanggal. Aturan ini hanya berlaku dari tanggal 14 Desember 2023 hingga 26 Juni 2024.  
`-j DROP`: Menentukan target aturan, yaitu DROP, yang berarti paket dari alamat IP sumber 192.191.14.150, dengan protokol TCP dan tujuan port 80, yang sesuai dengan jadwal waktu yang ditentukan, akan ditolak.  

Lalu, lakukan testing di Revolte dengan mengganti date teerlebih dahulu dan memasukkan syntax berikut  
```
nmap 192.191.8.2 80
nmap 192.191.14.138 80
```

Output:  


## Soal 9
Sadar akan adanya potensial saling serang antar kubu politik, maka WebServer harus dapat secara otomatis memblokir  alamat IP yang melakukan scanning port dalam jumlah banyak (maksimal 20 scan port) di dalam selang waktu 10 menit.  
(clue: test dengan nmap)

### Penyelesaian

Lakukan setting di wweb server (sein dan stark) dan masukkan configurasi sebagai berikut  
```
iptables -N scan_port

iptables -A INPUT -m recent --name scan_port --update --seconds 600 --hitcount 20 -j DROP

iptables -A FORWARD -m recent --name scan_port --update --seconds 600 --hitcount 20 -j DROP

iptables -A INPUT -m recent --name scan_port --set -j ACCEPT

iptables -A FORWARD -m recent --name scan_port --set -j ACCEPT
```

Penjelasan:  
- `iptables -N scan_port`  
`-N scan_port`: Membuat chain baru dengan nama "scan_port" (penanda atau tempat untuk aturan-aturan khusus).  
- `iptables -A INPUT -m recent --name scan_port --update --seconds 600 --hitcount 20 -j DROP`  
`-A INPUT`: Menambahkan aturan ke chain INPUT, yang digunakan untuk mengatur paket yang menuju ke sistem.  
`-m recent --name scan_port --update --seconds 600 --hitcount 20`: Menggunakan modul recent untuk mendeteksi aktivitas pemindaian port. Aturan ini akan men-drop (DROP) paket yang mencoba melakukan pemindaian port dengan frekuensi lebih dari 20 kali dalam waktu 600 detik.  
`-j DROP`: Menentukan target aturan, yaitu DROP, yang berarti paket yang memenuhi kondisi di atas akan ditolak.  
- `iptables -A FORWARD -m recent --name scan_port --update --seconds 600 --hitcount 20 -j DROP`  
`-A FORWARD`: Menambahkan aturan ke chain FORWARD, yang digunakan untuk mengatur paket yang dialihkan melalui sistem.  
Parameter dan fungsinya sama seperti pada baris sebelumnya, namun untuk chain FORWARD. Ini berarti paket yang mencoba melakukan pemindaian port pada paket yang dialihkan juga akan ditolak.  
- `iptables -A INPUT -m recent --name scan_port --set -j ACCEPT`  
`-A INPUT`: Menambahkan aturan ke chain INPUT.  
`-m recent --name scan_port --set`: Menggunakan modul recent untuk menetapkan penanda "scan_port" pada paket yang baru datang.  
`-j ACCEPT`: Menentukan target aturan, yaitu ACCEPT, yang berarti paket yang memenuhi kondisi di atas akan diterima.  
- `iptables -A FORWARD -m recent --name scan_port --set -j ACCEPT`  
`-A FORWARD`: Menambahkan aturan ke chain FORWARD.  
Parameter dan fungsinya sama seperti pada baris sebelumnya, namun untuk chain FORWARD. Ini berarti paket yang mencoba melakukan pemindaian port pada paket yang dialihkan juga akan diizinkan.  

Lalu, lakukan setting dengan menjalankan syntax berikut di GrobeForest  
```
ping 192.191.8.2
ping 192.191.14.138
```

Output:  


## Soal 10
Karena kepala suku ingin tau paket apa saja yang di-drop, maka di setiap node server dan router ditambahkan logging paket yang di-drop dengan standard syslog level.

### Penyelesaian

Masukkan syntax berikut ke setiap node server (DNS, DHCP, Web) dan setiap router  
```
iptables -A INPUT  -j LOG --log-level debug --log-prefix 'Dropped Packet' -m limit --limit 1/second --limit-burst 10
```

Penjelasan:  
`-A INPUT`: Menambahkan aturan ke chain INPUT, yang digunakan untuk mengatur paket yang menuju ke sistem.  
`-j LOG`: Menentukan target aturan, yaitu LOG, yang berarti paket yang memenuhi kondisi aturan akan dicatat dalam log sistem.  
`--log-level debug`: Menentukan level log yang akan digunakan. Dalam hal ini, level log diatur sebagai "debug". Level log ini menunjukkan tingkat detail log yang akan dicatat.  
`--log-prefix 'Dropped Packet'`: Menentukan awalan atau prefiks untuk pesan log. Dalam hal ini, pesan log akan diawali dengan teks "Dropped Packet".  
`-m limit --limit 1/second --limit-burst 10`: Menggunakan modul limit untuk mengontrol seberapa sering log dibuat. Parameter-parameter ini menentukan bahwa setiap detiknya hanya satu log yang akan dibuat (1/second), dan jika ada lebih dari satu log yang mencoba dibuat dalam satu detik, sebanyak 10 log yang melebihi akan diperbolehkan (limit-burst 10).  

Output:  



