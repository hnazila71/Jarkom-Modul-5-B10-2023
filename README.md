# Jarkom-Modul-5-B10-2023

### Nama Anggota B10
 <table>
 	<tr>
 		<td> Nama </td>
 		<td> NRP </td>
 	</tr>
 	<tr>
 		<td> Yusuf Hasan Nazila </td>
 		<td> 5025211225</td>
 	</tr>
	 <tr>
		 <td> Farhan Dwi Putra </td>
 		<td> 5025211093</td>
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
```
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
