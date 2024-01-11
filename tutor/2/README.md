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

**3. end**
```Txt
Router(config)# end
//Contoh
Router(config)# end
Router#
```
Keluar dari mode **Global Configuration**.

**4. show running-config**
```Txt
Router# show running-config
//Contoh
Router# show running-config
...
```

### Konfigurasi Interface
**1. interface**
```Txt
Router(config)# interface "interface|no/no"
//Contoh
Router(config)# interface fa0/0 //Interface FastEthernet
Router(config-if)#
Router(config)# interface gig0/0 //Interface GigabitEthernet
Router(config-if)#
Router(config)# interface gig0/8 //GigabitEthernet Untuk WAN (gig0/8)
Router(config-if)#
```
Masuk ke interface.

**2. ip address**
```Txt
Router(config-if)# ip address "ip_address" "netmask"
//Contoh
Router(config)# interface fa0/0
Router(config-if)# ip address 192.168.10.10 255.255.255.0
```

**3. no shutdown**
```Txt
Router(config-if)# no shutdown
//Contoh
Router(config)# interface fa0/1
Router(config-if)# ip address 192.168.10.10 255.255.255.0
Router(config-if)# no shutdown
```
Menghidupkan interface itu, bawaan Cisco interface masih mati maka perlu dihidupkan manual.

**4. exit**
```Txt
Router(config-if)# exit
//Contoh
Router(config-if)# exit
Router(config)#
```
Keluar dari mode ***Global Configuration*** pada sebuah interface.

### Konfigurasi Routing Statis
Konfigurasi ***static route*** pada sebuah interface, untuk perintah routing **ip route**.
```Txt
Router(config)# ip route "prefix|ip_network" "netmask" "ip_address"
//Contoh
Router(config)# ip route 192.168.1.0 255.255.0.0 10.10.10.2
```

### Konfigurasi Routing Dinamis
Konfigurasi ***dynamic route*** pada sebuah interface, untuk perintah routing **route rip**.
```Txt
Router(config)# router rip
Router(config-router)# version "1|2"
Router(config-router)# network "ip_address|ip_network"
Router(config-router)# no auto-summary
//Contoh
Router(config)# router rip
Router(config-router)# version 1 //Pilih versi RIP v1 atau v2
Router(config-router)# network 192.168.10.0 //IP Network
Router(config-router)# no auto-summary
Router(config-router)# end
Router(config) exit
Router# show running-config
router rip
version 2
network 10.0.0.0
network 192.168.1.0
no auto-summary
```


