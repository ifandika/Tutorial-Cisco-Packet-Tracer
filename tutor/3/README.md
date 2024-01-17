## Konfigurasi DHCP Server

### DHCP
Secara sederhana DHCP adalah sistem untuk konfigurasi protokol, dibagi menjadi 2
**DHCP Server** & **DHCP Client**. Perintah untuk membuat DHCP Server.
```Txt
Router(config)# ip dhcp pool "nama"
Router(dhcp-config)# network "ip_network" "netmask"
Router(dhcp-config)# default-router "ip_gateway"
Router(dhcp-config)# exit
Router(config)#

//IP yang tidak diikutkan
Router(config)# ip dhcp excluded-address "ip"
```
### Topologi Sederhana Untuk DHCP

Untuk konfigurasi pada Router0.
```Txt
Router>enable 
Router#configure terminal 
Enter configuration commands, one per line.  End with CNTL/Z.
Router(config)#service dhcp
Router(config)#interface fastEthernet 0/0
Router(config-if)#ip dhcp pool POOL-1
Router(dhcp-config)#network 10.20.0.0 255.255.255.248
Router(dhcp-config)#default-rou
Router(dhcp-config)#default-router 10.20.0.1
Router(dhcp-config)#dns-server 8.8.8.8
Router(dhcp-config)#exit
Router(config)#ip dhcp-exl
Router(config)#ip dhcp-exc
Router(config)#ip dhcp-excl
Router(config)#ip dhcp excl
Router(config)#ip dhcp excluded-address 10.20.0.1
Router(config)#exit
```

