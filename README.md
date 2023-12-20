# Jarkom-Modul-5-B10-2023

### Nama Anggota B10
<table>
	<tr>
		<td> Nama </td>
		<td> NRP </td>
		<td> Kontribusi Modul 1 </td>
		<td> Kontribusi Modul 2 </td>
		<td> Kontribusi Modul 3 </td>
		<td> Kontribusi Modul 4 </td>
		<td> Kontribusi Modul 5 </td>
	</tr>
	<tr>
		<td> Yusuf Hasan Nazila </td>
		<td> 5025211225</td>
		<td> 50%</td>
		<td> 50%</td>
		<td> 50%</td>
		<td> 50%</td>
		<td> 50%</td>
	</tr>
	<tr>
		<td> Farhan Dwi Putra </td>
		<td> 5025211093</td>
		<td> 50%</td>
		<td> 50%</td>
		<td> 50%</td>
		<td> 50%</td>
		<td> 50%</td>
	</tr>
</table>




## Topologi
![image](https://github.com/hnazila71/Jarkom-Modul-5-B10-2023/assets/114125438/a2cd4f5e-b937-41fb-bb62-48c76709c727)


## Routing IP 

<table>
  <tr>
    <th>Nama Subnet</th>
    <th>Rute</th>
    <th>Jumlah IP</th>
    <th>Netmask</th>
  </tr>
  <tr>
    <td>A1</td>
    <td>Heiter-Switch3-Sein-Switch3-GrobeForest</td>
    <td>514</td>
    <td>/22</td>
  </tr>
  <tr>
    <td>A2</td>
    <td>Heiter-TurkRegion</td>
    <td>1023</td>
    <td>/21</td>
  </tr>
  <tr>
    <td>A3</td>
    <td>Aura-Heiter</td>
    <td>2</td>
    <td>/30</td>
  </tr>
  <tr>
    <td>A4</td>
    <td>Aura-Frieren</td>
    <td>2</td>
    <td>/30</td>
  </tr>
  <tr>
    <td>A5</td>
    <td>Frieren-Stark</td>
    <td>2</td>
    <td>/30</td>
  </tr>
  <tr>
    <td>A6</td>
    <td>Frieren-Himmel</td>
    <td>2</td>
    <td>/30</td>
  </tr>
  <tr>
    <td>A7</td>
    <td>Himmel-LaubHils</td>
    <td>256</td>
    <td>/23</td>
  </tr>
  <tr>
    <td>A8</td>
    <td>Himmel-Switch1-SchweMountains-Switch1-Fern</td>
    <td>66</td>
    <td>/25</td>
  </tr>
  <tr>
    <td>A9</td>
    <td>Fern-Ritcher</td>
    <td>2</td>
    <td>/30</td>
  </tr>
  <tr>
    <td>A10</td>
    <td>Fern-Switch2-Revoltte</td>
    <td>2</td>
    <td>/30</td>
  </tr>
  <tr>
    <td>Total</td>
    <td></td>
    <td>1871</td>
    <td>/20</td>
  </tr>
</table>

## Pembagian IP
<table>
  <tr>
    <th>Subnet</th>
    <th>Network ID</th>
    <th>Netmask</th>
    <th>Prefix Length</th>
    <th>Broadcast</th>
  </tr>
  <tr>
    <td>A2</td>
    <td>192.183.0.0</td>
    <td>255.255.248.0</td>
    <td>/21</td>
    <td>192.168.7.255</td>
  </tr>
  <tr>
    <td>A1</td>
    <td>192.183.8.0</td>
    <td>255.255.252.0</td>
    <td>/22</td>
    <td>192.168.3.255</td>
  </tr>
  <tr>
    <td>A7</td>
    <td>192.183.12.0</td>
    <td>255.255.254.0</td>
    <td>/23</td>
    <td>192.168.1.255</td>
  </tr>
  <tr>
    <td>A8</td>
    <td>192.183.14.0</td>
    <td>255.255.255.128</td>
    <td>/25</td>
    <td>192.168.0.127</td>
  </tr>
  <tr>
    <td>A3</td>
    <td>192.183.14.148</td>
    <td>255.255.255.252</td>
    <td>/30</td>
    <td>192.168.0.3</td>
  </tr>
  <tr>
    <td>A4</td>
    <td>192.183.14.144</td>
    <td>255.255.255.252</td>
    <td>/30</td>
    <td>192.168.0.3</td>
  </tr>
  <tr>
    <td>A5</td>
    <td>192.183.14.140</td>
    <td>255.255.255.252</td>
    <td>/30</td>
    <td>192.168.0.3</td>
  </tr>
  <tr>
    <td>A6</td>
    <td>192.183.14.136</td>
    <td>255.255.255.252</td>
    <td>/30</td>
    <td>192.168.0.3</td>
  </tr>
  <tr>
    <td>A9</td>
    <td>192.183.14.132</td>
    <td>255.255.255.252</td>
    <td>/30</td>
    <td>192.168.0.3</td>
  </tr>
  <tr>
    <td>A10</td>
    <td>192.183.14.128</td>
    <td>255.255.255.252</td>
    <td>/30</td>
    <td>192.168.0.3</td>
  </tr>
</table>


## Konfigurasi
### DNS SERVER (Richter)
```
auto eth0
iface eth0 inet static
	address 192.183.14.134
	netmask 255.255.255.252
	gateway 192.183.14.133
```
### Revolte (DHCP Server)
```
auto eth0
iface eth0 inet static
	address 192.183.14.130
	netmask 255.255.255.252
	gateway 192.183.14.129
```

### Web Server
- Sein
```
auto eth0
iface eth0 inet static
	address 192.183.8.2
	netmask 255.255.252.0
	gateway 192.183.8.1
  ```
- Stark
```
auto eth0
iface eth0 inet static
	address 192.183.14.142
	netmask 255.255.255.252
	gateway 192.183.14.141

```
### Aura
```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
	address 192.183.14.149
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 192.183.14.145
	netmask 255.255.255.252


```

### Heiter
```
auto eth0
iface eth0 inet static
	address 192.183.14.150
	netmask 255.255.255.252
	gateway 192.183.14.149

auto eth1
iface eth1 inet static
	address 192.183.0.1
	netmask 255.255.248.0 

auto eth2
iface eth2 inet static
	address 192.183.8.1
	netmask 255.255.252.0
```

### Frieren
```
auto eth0
iface eth0 inet static
	address 192.183.14.146
	netmask 255.255.255.252
	gateway 192.183.14.145

auto eth1
iface eth1 inet static
	address 192.183.14.141
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 192.183.14.137
	netmask 255.255.255.252
```

### Himmel
```
auto eth0
iface eth0 inet static
	address 192.183.14.146
	netmask 255.255.255.252
	gateway 192.183.14.145

auto eth1
iface eth1 inet static
	address 192.183.14.141
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 192.183.14.137
	netmask 255.255.255.252
```

### Fern
```
auto eth0
iface eth0 inet static
	address 192.183.14.3
	netmask 255.255.255.128
	gateway 192.183.14.1

auto eth1
iface eth1 inet static
	address 192.183.14.133
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 192.183.14.129
	netmask 255.255.255.252
```
- SchwerMountain, LaubHills, TurkRegion, GrobeForest
```
auto eth0
iface eth0 inet dhcp
```

## Routing
### Aura
```
route add -net 192.183.0.0    netmask 255.255.248.0   gw 192.183.14.150
route add -net 192.183.8.0    netmask 255.255.252.0   gw 192.183.14.150
route add -net 192.183.12.0   netmask 255.255.254.0   gw 192.183.14.146
route add -net 192.183.14.0   netmask 255.255.255.128 gw 192.183.14.146
route add -net 192.183.14.140 netmask 255.255.255.252 gw 192.183.14.146
route add -net 192.183.14.136 netmask 255.255.255.252 gw 192.183.14.146
route add -net 192.183.14.132 netmask 255.255.255.252 gw 192.183.14.146
route add -net 192.183.14.128 netmask 255.255.255.252 gw 192.183.14.146
```
## Heiter
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.183.14.149
```
## Frieren
```
route add -net 0.0.0.0        netmask 0.0.0.0         gw 192.183.14.145
route add -net 192.183.12.0   netmask 255.255.254.0   gw 192.183.14.138
route add -net 192.183.14.0   netmask 255.255.255.128 gw 192.183.14.138
route add -net 192.183.14.132 netmask 255.255.255.252 gw 192.183.14.138
route add -net 192.183.14.128 netmask 255.255.255.252 gw 192.183.14.138
```
### Himmel
```
route add -net 0.0.0.0        netmask 0.0.0.0         gw 192.183.14.137 
route add -net 192.183.14.132 netmask 255.255.255.252 gw 192.183.14.3
route add -net 192.183.14.128 netmask 255.255.255.252 gw 192.183.14.3
```
### Fern
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.183.14.1
```

### Konfigurasi Richter
```
apt-get update
apt-get install bind9 -y
```
### Konfigurasi Revolte
```
apt-get update
apt-get install isc-dhcp-server -y
dhcpd --version

service isc-dhcp-server start
```
- ISC DHCP konfigurasi pada ```/etc/dhcp/dhcpd.conf``` Untuk range harus lebih dari yang pernah digunakan, semisal 192.183.0.0 itu di pakai sampai 192.183.0.2 maka range mulai 192.183.0.3 dan sampai max tidak masalah
```
option domain-name "example.org";
option domain-name-servers ns1.example.org, ns2.example.org;
default-lease-time 600;
max-lease-time 7200;
ddns-update-style none;
subnet 192.183.14.128 netmask 255.255.255.252 {
    option routers 192.183.14.129;
}

subnet 192.183.14.132 netmask 255.255.255.252 {
}

subnet 192.183.14.136 netmask 255.255.255.252 {
    option routers 192.183.14.136;
}

subnet 192.183.14.140 netmask 255.255.255.252 {
}

subnet 192.183.14.144 netmask 255.255.255.252 {
    option routers 192.183.14.145;
}

subnet 192.183.14.148 netmask 255.255.255.252 {
    option routers 192.183.14.150;
}
subnet 192.183.0.0 netmask 255.255.248.0 {
    range 192.183.0.2 192.183.4.4;
    option routers 192.183.0.1;
    option broadcast-address 192.183.7.255;
    option domain-name-servers 192.183.14.134;
    default-lease-time 720;
    max-lease-time 5760;
}
subnet 192.183.8.0 netmask 255.255.252.0 {
    range 192.183.8.3 192.183.10.5;
    option routers 192.183.8.1;
    option broadcast-address 192.183.11.255;
    option domain-name-servers 192.183.14.134;
    default-lease-time 720;
    max-lease-time 5760;
}
subnet 192.183.12.0 netmask 255.255.254.0 {
    range 192.183.12.2 192.183.13.1;
    option routers 192.183.12.1;
    option broadcast-address 192.183.13.255;
    option domain-name-servers 192.183.14.134;
    default-lease-time 720;
    max-lease-time 5760;
}

subnet 192.183.14.0 netmask 255.255.255.128 {
    range 192.183.14.4 192.183.14.67;
    option routers 192.183.14.1;
    option broadcast-address 192.183.14.127;
    option domain-name-servers 192.183.14.134;
    default-lease-time 720;
    max-lease-time 5760;
}
```
```
service isc-dhcp-server restart
apt-get install netcat
```

### Konfigurasi Himmel dan Heiter
```
apt-get update
apt-get install isc-dhcp-relay -y
service isc-dhcp-relay start

echo '
SERVERS="192.183.14.130"
INTERFACES="eth0 eth1 eth2"
OPTIONS=""
' > /etc/default/isc-dhcp-relay

echo '
net.ipv4.ip_forward=1
' > /etc/sysctl.conf

service isc-dhcp-relay restart
```
### Konfigurasi Aura
```
ETH0_IP=$(ip -4 addr show eth0 | grep -oP '(?<=inet\s)\d+(\.\d+){3}')

iptables -t nat -A POSTROUTING -o eth0 -j SNAT --to-source $ETH0_IP

apt-get update
apt-get install isc-dhcp-relay -y
service isc-dhcp-relay start

echo '
SERVERS="192.183.14.130"
INTERFACES="eth1 eth2"
OPTIONS=""
' > /etc/default/isc-dhcp-relay

echo '
net.ipv4.ip_forward=1
' > /etc/sysctl.conf

service isc-dhcp-relay restart
```
### Konfigurasi Sein dan Stark 
```
apt-get update
apt-get install netcat
```

## SOAL NO 1
Agar topologi yang kalian buat dapat mengakses keluar, kalian diminta untuk mengkonfigurasi Aura menggunakan iptables, tetapi tidak ingin menggunakan MASQUERADE.
```
iptables -t nat -A POSTROUTING -o eth0 -j SNAT --to-source $ETH0_IP
```
Perintah ini mengatur iptables untuk memproses paket yang keluar melalui antarmuka jaringan eth0. Setiap paket yang keluar akan mengalami proses Network Address Translation (NAT), di mana alamat IP sumber (source) dari paket tersebut akan diganti dengan nilai dari variabel $ETH0_IP. Ini digunakan untuk mengubah alamat sumber paket sebelum meninggalkan sistem.

Setelah itu coba ping di Stark 
```
ping google.com 
```
#### Hasil
![image](https://github.com/hnazila71/Jarkom-Modul-5-B10-2023/assets/114125438/bcb7977a-f582-4346-a2e6-62e57e1c063b)

## SOAL NO 2
Kalian diminta untuk melakukan drop semua TCP dan UDP kecuali port 8080 pada TCP.
- Kita konfigurasi dulu untuk pembatasan akses ke layanan tertentu pada TurkRegion
```
iptables -F
iptables -A INPUT -p tcp --dport 8080 -j ACCEPT
iptables -A INPUT -p tcp ! --dport 8080 -j DROP
iptables -A INPUT -p udp -j DROP
```
- iptables -F:
Menghapus semua aturan (flush) dalam tabel iptables. Ini memastikan bahwa konfigurasi firewall sebelumnya dibersihkan sebelum menambahkan aturan baru.

- iptables -A INPUT -p tcp --dport 8080 -j ACCEPT:
Menerima (ACCEPT) paket TCP yang menuju port 8080.
Aturan ini memungkinkan akses ke layanan yang berjalan pada port 8080 menggunakan protokol TCP.

- iptables -A INPUT -p tcp ! --dport 8080 -j DROP:
Menolak (DROP) paket TCP yang tidak menuju port 8080.
Aturan ini mengabaikan (menolak) semua paket TCP ke port selain 8080, sehingga hanya paket yang ditujukan ke port 8080 yang akan diterima.

- iptables -A INPUT -p udp -j DROP:
Menolak (DROP) semua paket UDP.
Aturan ini secara umum menolak semua paket yang menggunakan protokol UDP, tanpa mempertimbangkan port tujuan. Sebagai contoh, ini bisa digunakan untuk menutup semua layanan yang menggunakan UDP.

Kita tes menggunakan Turk Region
- Cari IP TurkRegion dengan ```ip a```
- Lalu ```nc -l -p 80``` pada TurkRegion dan ```apt-get install netcat``` terlebih dahulu.
Perintah nc -l -p 80 menggunakan Netcat untuk mendengarkan koneksi pada port 80, membuat sistem siap menerima koneksi masuk. Ini umumnya digunakan untuk membuat server sederhana atau mendengarkan koneksi untuk keperluan.
 - ```nc 192.183.0.2 80 ``` pada Revolte

## Tes Sebelum
- Revolte

![image](https://github.com/hnazila71/Jarkom-Modul-5-B10-2023/assets/114125438/4df9f8c9-d368-4d74-a8cc-8b4a2e29ddbf)

- Turk Region

![image](https://github.com/hnazila71/Jarkom-Modul-5-B10-2023/assets/114125438/96bc5de3-8451-41fa-9dec-37cc77be0a10)

## Tes Sesudah

- Revolte

![image](https://github.com/hnazila71/Jarkom-Modul-5-B10-2023/assets/114125438/f03cd1d8-c182-44d5-bf85-daf2bdc88ca3)

- TurkRegion

![image](https://github.com/hnazila71/Jarkom-Modul-5-B10-2023/assets/114125438/1664e252-424a-407a-bfe9-0de081b4f12c)

## Soal NO 3
Kepala Suku North Area meminta kalian untuk membatasi DHCP dan DNS Server hanya dapat dilakukan ping oleh maksimal 3 device secara bersamaan, selebihnya akan di drop.
- Pada Revolte dan Richter
```
iptables -A INPUT -p icmp -m connlimit --connlimit-above 3 --connlimit-mask 0 -j DROP
```
Perintah iptables tersebut memblokir lalu lintas ICMP yang memiliki lebih dari 3 koneksi dalam waktu yang sama, dengan mengabaikan alamat IP, dan mengarahkan untuk menjatuhkan (DROP) paket-paket tersebut.
Tes
- 1. Sein

 ![image](https://github.com/hnazila71/Jarkom-Modul-5-B10-2023/assets/114125438/3dfce426-f361-4f6b-b529-1e17a6cd790e) 
- 2. Turk Region
![image](https://github.com/hnazila71/Jarkom-Modul-5-B10-2023/assets/114125438/d35aaded-6361-4bd2-9f8d-2258aa3ddc87)
- 3. SchwerMontain
![image](https://github.com/hnazila71/Jarkom-Modul-5-B10-2023/assets/114125438/e18074e6-67cf-4673-91a0-58f25d8160db)
- 4. LaubHills (DROP)
![image](https://github.com/hnazila71/Jarkom-Modul-5-B10-2023/assets/114125438/0151f475-512d-4e9f-acef-816ce9b5bff9)

- Adanya paket loss karena terus mengirimkan setelah ping ke 4 LaubHills dan di drop semua jadi loss

## Soal NO 4
Lakukan pembatasan sehingga koneksi SSH pada Web Server hanya dapat dilakukan oleh masyarakat yang berada pada GrobeForest.
Kita Konfigurasi pada Sein dan Stark
```
iptables -A INPUT -p tcp --dport 22 -s 192.183.8.0/22 -j ACCEPT #A1
iptables -A INPUT -p tcp --dport 22 -j DROP
```


### Testing
```
nmap 192.183.8.2 -p 22
```
- LaubHills

![image](https://github.com/hnazila71/Jarkom-Modul-5-B10-2023/assets/114125438/a9eb527d-1f28-4e94-86e9-5a3c35002ce4)


- GrobeForest

![image](https://github.com/hnazila71/Jarkom-Modul-5-B10-2023/assets/114125438/f0d50ac0-7a0d-4194-9073-572c0437ef21)


## SOAL NO 5
Selain itu, akses menuju WebServer hanya diperbolehkan saat jam kerja yaitu Senin-Jumat pada pukul 08.00-16.00.
Pada Sein dan Stark
```
iptables -A INPUT -p tcp --dport 80 -m time --timestart 08:00 --timestop 16:00 --weekdays Mon,Tue,Wed,Thu,Fri -j ACCEPT
iptables -A INPUT -p tcp --dport 80 -j DROP
```
Pada aura
```
curl 192.183.8.2 -v
```
Tes pada Sein dan Stark
```
nc -l -p 80
```

### Testing


![Screenshot (156)](https://github.com/hnazila71/Jarkom-Modul-5-B10-2023/assets/128909158/ddff83c2-ae0a-445c-893c-413cb61398cc)

## SOAL NO 6
Lalu, karena ternyata terdapat beberapa waktu di mana network administrator dari WebServer tidak bisa stand by, sehingga perlu ditambahkan rule bahwa akses pada hari Senin - Kamis pada jam 12.00 - 13.00 dilarang (istirahat maksi cuy) dan akses di hari Jumat pada jam 11.00 - 13.00 juga dilarang (maklum, Jumatan rek).

Allow HTTP access only outside restricted hours (Monday-Thursday 12:00-13:00, Friday 11:00-13:00)
```
iptables -A INPUT -p tcp --dport 80 -m time --timestart 13:01 --timestop 10:59 --weekdays Mon,Tue,Wed,Thu,Fri -j ACCEPT
```
Drop HTTP traffic during restricted hours (Monday-Thursday 12:00-13:00, Friday 11:00-13:00)
```
iptables -A INPUT -p tcp --dport 80 -m time --timestart 12:00 --timestop 13:00 --weekdays Mon,Tue,Wed,Thu -j DROP
iptables -A INPUT -p tcp --dport 80 -m time --timestart 11:00 --timestop 13:00 --weekdays Fri -j DROP
```
Drop other HTTP traffic
```
iptables -A INPUT -p tcp --dport 80 -j DROP
```
check server time
```
date
```
night server
```
date 121319002023.00
```
day server
```
date 121313002023.00
```
### Testing

testing webserver
```
nc -l -p 80
```
testing client
```
nc ipwebserver 80
```

![Screenshot (156)](https://github.com/hnazila71/Jarkom-Modul-5-B10-2023/assets/128909158/319e376e-771e-40ee-841c-72967fa19c33)

## Soal NO 7

Karena terdapat 2 WebServer, kalian diminta agar setiap client yang mengakses Sein dengan Port 80 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan dan request dari client yang mengakses Stark dengan port 443 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan.

```
iptables -A PREROUTING -t nat -p tcp --dport 80 -d 192.183.8.2 -m statistic --mode nth --every 2 --packet 0 -j DNAT --to-destination 192.183.8.2

iptables -A PREROUTING -t nat -p tcp --dport 80 -d 192.183.8.2 -j DNAT --to-destination 192.183.14.142

iptables -A PREROUTING -t nat -p tcp --dport 443 -d 192.183.14.142 -m statistic --mode nth --every 2 --packet 0 -j DNAT --to-destination 192.183.14.142

iptables -A PREROUTING -t nat -p tcp --dport 443 -d 192.183.14.142 -j DNAT --to-destination 192.183.8.2
```

## Soal NO 8

Karena berbeda koalisi politik, maka subnet dengan masyarakat yang berada pada Revolte dilarang keras mengakses WebServer hingga masa pencoblosan pemilu kepala suku 2024 berakhir. Masa pemilu (hingga pemungutan dan penghitungan suara selesai) kepala suku bersamaan dengan masa pemilu Presiden dan Wakil Presiden Indonesia 2024.

```
iptables -A INPUT -s 192.183.14.130 -p tcp --dport 80 -m time --datestart "2023-12-14" --datestop "2024-06-26" -j DROP
```

### Testing

![Screenshot (156)](https://github.com/hnazila71/Jarkom-Modul-5-B10-2023/assets/128909158/7be12a06-27c0-4b12-9be7-dd8ada54c1cd)

## Soal NO 9

Sadar akan adanya potensial saling serang antar kubu politik, maka WebServer harus dapat secara otomatis memblokir  alamat IP yang melakukan scanning port dalam jumlah banyak (maksimal 20 scan port) di dalam selang waktu 10 menit. 
(clue: test dengan nmap)

```
iptables -N scan_port

iptables -A INPUT -m recent --name scan_port --update --seconds 600 --hitcount 20 -j DROP
iptables -A FORWARD -m recent --name scan_port --update --seconds 600 --hitcount 20 -j DROP

iptables -A INPUT -m recent --name scan_port --set -j ACCEPT
iptables -A FORWARD -m recent --name scan_port --set -j ACCEPT
```

### Testing

![Screenshot (157)](https://github.com/hnazila71/Jarkom-Modul-5-B10-2023/assets/128909158/46950a92-55c9-443b-b1d4-1f5967c2185f)

## Soal NO 10

Karena kepala suku ingin tau paket apa saja yang di-drop, maka di setiap node server dan router ditambahkan logging paket yang di-drop dengan standard syslog level. 

```
iptables -A INPUT  -j LOG --log-level debug --log-prefix 'Packet Drop 1/second --limit-burst 10
```
