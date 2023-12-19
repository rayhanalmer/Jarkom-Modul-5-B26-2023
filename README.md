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

Penjelasan:  

Output:  
  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/9e0c13d5-63eb-42f7-9eef-402dcff1fd4e)  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/2600abec-0267-45cd-afdf-98b4498bd02e)  


## Soal 2
Kalian diminta untuk melakukan drop semua TCP dan UDP kecuali port 8080 pada TCP.

### Penyelesaian

Penjelasan  

Output:  
  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/99a69618-5f9c-4336-a826-99021df16d5f)  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/d91102ca-49c2-468d-b2e6-02dbc03bcab3)  

## Soal 3
Kepala Suku North Area meminta kalian untuk membatasi DHCP dan DNS Server hanya dapat dilakukan ping oleh maksimal 3 device secara bersamaan, selebihnya akan di drop.

### Penyelesaian

Penjelasan  

Output:  
  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/00bfe60f-145c-471e-a243-1c055fe630a5)  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/3eb3dff4-c63b-4883-91c0-f4e037b9e1df)  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/c1813681-fde0-4ad0-8700-05551d6b226a)  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/6be2466f-a6b0-4532-be47-20990dc47429)  

## Soal 4
Lakukan pembatasan sehingga koneksi SSH pada Web Server hanya dapat dilakukan oleh masyarakat yang berada pada GrobeForest.

### Penyelesaian

Penjelasan  

Output:  
  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/1705bb6f-781c-46c4-b925-d8ec26d50d1f)  
![image](https://github.com/rayhanalmer/Jarkom-Modul-5-B26-2023/assets/103409628/565fb1c8-ebe7-459e-b5f7-ad70c064b5ad)  

## Soal 5
Selain itu, akses menuju WebServer hanya diperbolehkan saat jam kerja yaitu Senin-Jumat pada pukul 08.00-16.00.

### Penyelesaian

## Soal 6
Lalu, karena ternyata terdapat beberapa waktu di mana network administrator dari WebServer tidak bisa stand by, sehingga perlu ditambahkan rule bahwa akses pada hari Senin - Kamis pada jam 12.00 - 13.00 dilarang (istirahat maksi cuy) dan akses di hari Jumat pada jam 11.00 - 13.00 juga dilarang (maklum, Jumatan rek).

### Penyelesaian

## Soal 7
Karena terdapat 2 WebServer, kalian diminta agar setiap client yang mengakses Sein dengan Port 80 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan dan request dari client yang mengakses Stark dengan port 443 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan.

### Penyelesaian

## Soal 8
Karena berbeda koalisi politik, maka subnet dengan masyarakat yang berada pada Revolte dilarang keras mengakses WebServer hingga masa pencoblosan pemilu kepala suku 2024 berakhir. Masa pemilu (hingga pemungutan dan penghitungan suara selesai) kepala suku bersamaan dengan masa pemilu Presiden dan Wakil Presiden Indonesia 2024.

### Penyelesaian

## Soal 9
Sadar akan adanya potensial saling serang antar kubu politik, maka WebServer harus dapat secara otomatis memblokir  alamat IP yang melakukan scanning port dalam jumlah banyak (maksimal 20 scan port) di dalam selang waktu 10 menit.  
(clue: test dengan nmap)

### Penyelesaian

## Soal 10
Karena kepala suku ingin tau paket apa saja yang di-drop, maka di setiap node server dan router ditambahkan logging paket yang di-drop dengan standard syslog level.

### Penyelesaian

