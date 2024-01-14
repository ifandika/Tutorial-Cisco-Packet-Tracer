## Konfigurasi DHCP Server

#### DHCP
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




