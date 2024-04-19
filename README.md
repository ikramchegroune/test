**Configuration Settings**

* **Enable Password :**
  - `enable secret cisco` 
* **Username and Password:**
  - `username admin secret cisco` 


**Interfaces configuration**

* **GigabitEthernet 0/0**

    - `interface GigabitEthernet 0/0`
    - `description Link to ASA-DMZ-I`
    - `ip address 195.1.1.129 255.255.255.252`
    - `no shutdown`
    - `exit`

* **GigabitEthernet 0/1**

    - `interface GigabitEthernet0/1`
    - `description Link to ISP1`
    - `ip address 198.10.10.2 255.255.255.252`
    - `no shutdown`
    - `exit`

* **GigabitEthernet 0/2**

    - `interface GigabitEthernet0/2`
    - `description Link to ASAv-I`
    - `ip address 172.16.0.2 255.255.255.252`
    - `no shutdown`
    - `exit`

* **GigabitEthernet 0/3**
    - `interface GigabitEthernet0/3`
    - `description Link to ISP2`
    - `ip address 197.10.10.2 255.255.255.252`
    - `no shutdown`
    - `exit`

* **LoopBack 0**
    - `interface loopback 0`
    - `description Management`
    - `ip address 10.1.1.5 255.255.255.255`
    - `no shutdown`
    - `exit`


**NAT Configuration**
* **Standard access-list 1**
    - `access-list 1 permit 192.168.10.0 0.0.0.255`
    - `access-list 1 permit 192.168.20.0 0.0.0.255`
    - `access-list 1 permit 192.168.30.0 0.0.0.255`
    - `access-list 1 permit 192.168.40.0 0.0.0.255`
    - `access-list 1 permit 10.0.0.0 0.0.0.255`
    - `access-list 1 permit 10.1.1.0 0.0.0.255`
    - `access-list 1 permit 172.16.0.0 0.0.0.255`
    - `access-list 1 permit 172.16.50.0 0.0.0.255`
    - `access-list 1 deny any`
* **NAT pool of inside global addresses**
    - `ip nat pool 1 195.1.1.1 195.1.1.127 netmask 255.255.255.128`
* **NAT Overload**
    - `ip nat inside source list 1 pool 1 overload`
* **Inside and outside interfaces**
    
* **GigabitEthernet 0/0**

    - `interface GigabitEthernet 0/0`
    - `description Link to ASA-DMZ-I`
    - `ip address 195.1.1.129 255.255.255.252`
    - `no shutdown`
    - `exit`

* **GigabitEthernet 0/1**

    - `interface GigabitEthernet0/1`
    - `description Link to ISP1`
    - `ip address 198.10.10.2 255.255.255.252`
    - `no shutdown`
    - `exit`

* **GigabitEthernet 0/2**

    - `interface GigabitEthernet0/2`
    - `description Link to ASAv-I`
    - `ip address 172.16.0.2 255.255.255.252`
    - `no shutdown`
    - `exit`

* **GigabitEthernet 0/3**
    - `interface GigabitEthernet0/3`
    - `description Link to ISP2`
    - `ip address 197.10.10.2 255.255.255.252`
    - `no shutdown`
    - `exit`


**Security**

* **Using SSH version 2**
    - `ip ssh version 2` (Enforce SSH version 2 for more secure connections)
    - `ip domain-name companyXYZ_2.sk`
    - `crypto key generate rsa modulus 4096`
* **Restrecting remote access only to SSH**
    - `line vty 0 1500`
    - `transport input ssh`
    - `login local `
* **Message digest (MD5) authentication password**
    - `area 0 authentication message-digest`
    - `key 36 md5 key_for_md5`
    - `area 0 authentication message-digest-key 36`

**NTP Synchronization**

* Configure NTP
    - `ntp server 172.16.50.1`
    - `clock timezone UTC+2 +2`

**Loggins**

* Enable logging for network events:
    - `logging host 172.16.50.1`
    - `logging trap notifications`


