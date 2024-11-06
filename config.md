Konfigurasi R1 (Router KHI)

hostname R1
interface GigabitEthernet0/0
 ip address 192.168.25.1 255.255.255.0
 no shutdown

interface GigabitEthernet0/1
 ip address 13.13.13.1 255.255.255.0
 no shutdown

interface GigabitEthernet0/2
 ip address 192.168.26.1 255.255.255.0
 no shutdown

router rip
 version 2
 network 192.168.25.0
 network 13.13.13.0
 network 192.168.26.0

Konfigurasi R2 (Router KJ)

hostname R2
interface GigabitEthernet0/0
 ip address 192.168.20.1 255.255.255.0
 no shutdown

interface GigabitEthernet0/1
 ip address 13.13.13.2 255.255.255.0
 no shutdown

interface GigabitEthernet0/2
 ip address 12.12.12.1 255.255.255.0
 no shutdown

interface GigabitEthernet0/3
 ip address 192.168.21.1 255.255.255.0
 no shutdown

router rip
 version 2
 network 192.168.20.0
 network 13.13.13.0
 network 12.12.12.0
 network 192.168.21.0

Konfigurasi R3 (Router CR)

hostname R3
interface GigabitEthernet0/0
 ip address 192.168.10.1 255.255.255.0
 no shutdown

interface GigabitEthernet0/1
 ip address 12.12.12.2 255.255.255.0
 no shutdown

interface GigabitEthernet0/2
 ip address 192.168.11.1 255.255.255.0
 no shutdown

router rip
 version 2
 network 192.168.10.0
 network 12.12.12.0
 network 192.168.11.0

Konfigurasi RIP: Setiap router dikonfigurasi menggunakan RIP versi 2 untuk routing dinamis. Perintah network digunakan untuk menentukan jaringan yang akan diiklankan oleh masing-masing router.
Alamat IP: Setiap antarmuka diberi alamat IP sesuai dengan topologi yang ditunjukkan, dengan subnet yang sesuai.
