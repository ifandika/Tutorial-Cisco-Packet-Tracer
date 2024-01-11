## Konfigurasi Dasar Router
Perintah konfigurasi pada Router, seperti konfigurasi Hostname, IP, DHCP, dsb.

## Perintah
### Konfigurasi Umum
**1. configure terminal**
```Txt
Router# configure terminal
// Contoh
Router> enable
Router# configure terminal
Router(config)#
```
Untuk masuk ke mode ***Global Configuration***.

**2. hostname**
```Txt
Router(config)# hostname "nama"
// Contoh
Router(config)# hostname ISP
ISP(config)#
```
Untuk merubah nama hostname.

### Konfigurasi Interface
**1. interface**
```Txt
Router(config)# interface "interface|no/no"
//Contoh
Router(config)# interface fa0/0 //Interface FastEthernet
Router(config)# interface gig0/0 //Interface GigabitEthernet
Router(config)# interface gig0/8 //GigabitEthernet Untuk WAN (gig0/8)
```
Masuk ke interface.

**2. ip address**
```Txt
Router(config)# ip address "ip_address" "netmask"
//Contoh
Router(config)# interface fa0/0
Router(config)# ip address 192.168.10.10 255.255.255.0
```

**3. no shutdown**
```Txt
Router(config)# no shutdown
//Contoh
Router(config)# interface fa0/1
Router(config)# ip address 192.168.10.10 255.255.255.0
Router(config)# no shutdown
```
Menghidupkan interface itu, bawaan Cisco interface masih mati maka perlu dihidupkan manual.










