# Jarkom-Modul-4-F13-2022

## Penyelesaian Soal Praktikum Modul 4 Jaringan Komputer

* Muhammad Andi Akbar Ramadhan (5025201264)
* Natya Madya Marciola	(5025201238)
* Neisa Hibatillah Alif	(5025201170)

## Topologi
![soal shift 4 1](https://user-images.githubusercontent.com/91374949/204077653-535e7221-0642-4e4d-884d-076b5f461ff6.png)
Soal shift dikerjakan pada Cisco Packet Tracer dan GNS3 menggunakan metode perhitungan CLASSLESS yang berbeda. Bila di CPT menggunakan VLSM, maka di GNS3 menggunakan CIDR atau sebaliknya.

## VLSM
### Subnetting
Dari topologi di atas, tentukan jumlah subnet yang ada di dalam topologi tersebut.
![image](https://user-images.githubusercontent.com/91374949/204084424-38d91c9f-c98a-4509-b1fd-e751134e55c0.png)
Terdapat 18 subnet di dalam topologi. Lalu tentukan jumlah alamat IP yang dibutuhkan oleh tiap subnet dan lakukan labelling netmask berdasarkan jumlah IP yang dibutuhkan.
| Subnet | Jumlah IP | Netmask |
|--|--|--|
| A1 | 1001 | /22 |
| A2 | 2 | /30 |
| A3 | 251 | /24 |
| A4 | 2 | /30 |
| A5 | 2 | /30 |
| A6 | 51 | /26 |
| A7 | 2 | /30 |
| A8 | 121 | /25 |
| A9 | 211 | /24 |
| A10 | 2 | /30 |
| A11 | 2 | /30 |
| A12 | 2 | /30 |
| A13 | 2 | /30 |
| A14 | 501 | /23 |
| A15 | 2 | /30 |
| A16 | 271 | /23 |
| A17 | 71 | /25 |
| A18 | 121 | /25 |
| **Total** | **2617** | **/20** |

Berdasarkan total IP dan netmask yang dibutuhkan, diperoleh hasil total IP yang digunakan sebanyak 2617, sehingga netmask yang digunakan adalah /20.
Dari tabel subnetting sebelumnya, dilakukan pembagiann IP berdasarkan NID dan netmask menggunakan pohon seperti gambar di bawah sampai semua subnet yang diminta pada topologi mendapat bagiannya.

![image](https://user-images.githubusercontent.com/91374949/204085043-5a6ac236-d52c-440e-9494-4b66d6d97e72.png)

Kemudian, dari pohon tersebut akan didapat pembagian IP sebagai berikut.

![image](https://user-images.githubusercontent.com/91374949/204085189-ab21038c-904d-4534-b599-3202a280e31a.png)

Berdasarkan pembagian tadi, atur IP untuk masing-masing interface yang ada di setiap device. Berikut contoh mengatur IP pada subnet A7 dan juga A6.
- Atur IP pada interface The Resonance yang mengarah ke The Order
![image](https://user-images.githubusercontent.com/91374949/204085466-844016c5-ada7-478c-a3f1-0aef86c56170.png)

- Atur IP pada interface The Order yang mengarah ke The Resonance
![image](https://user-images.githubusercontent.com/91374949/204085473-871b1d69-dc61-46aa-b86b-e29914ad5cb2.png)

- Atur IP pada interface The Order yang mengarah ke client Ashaf
![image](https://user-images.githubusercontent.com/91374949/204085598-819d5559-d820-453e-9ede-90aca9917048.png)

- Atur IP pada client Ashaf <br>
![image](https://user-images.githubusercontent.com/91374949/204085649-3de2a982-50f3-4b88-a04b-3294b3411ffc.png)

Kemudian, lakukan hal yang sama pada setiap interface pada device. Berikut adalah pembagiannya. </br>

**Subnet A7**
- Resonance - The Order
```
IP Address 10.35.0.13
Subnet Mask 255.255.255.252
```
- The Order - Resonance
```
IP Address 10.35.0.14/30
Subnet Mask 255.255.255.252
```

**Subnet A6**
- The Order - Ashaf
```
IP Address 10.35.0.65
Subnet Mask 255.255.255.192
```
- Ashaf - The Order
```
IP Address 10.35.0.66
Subnet Mask 255.255.255.192
Gateaway 10.35.0.65
```

**Subnet A5**
- The Order -The Minister
```
IP Address 10.35.0.9
Subnet Mask 255.255.255.252
```
- The Minister - The Order
```
IP Address 10.35.0.10
Subnet Mask 255.255.255.252
```

**Subnet A1**
- The Minister - Guideau
```
IP Address 10.35.8.1
Subnet Mask 255.255.252.0
```
- Guideau - The Minister
```
IP Address 10.35.8.2
Subnet Mask 255.255.252.0
Gateaway 10.35.8.1
```
**Subnet A2**
- The Minister - The Dauntless
```
IP Address 10.35.0.1
Subnet Mask 255.255.255.252
```
The Dauntless - The Minister
```
IP Address 10.35.0.2
Subnet Mask 255.255.255.252
```
**Subnet A3**
- The Dauntless - Johan dan Phanora
```
IP Address 10.35.2.1
Subnet Mask 255.255.255.0
```
- Johan - The Dauntless
```
IP Address 10.35.2.2
Subnet Mask 255.255.255.0
Gateaway 10.35.2.1
```
- Phanora - The Dauntless
```
IP Address 10.35.2.3
Subnet Mask 255.255.255.0
Gateaway 10.35.2.1
```
**Subnet A12**
- The Resonance -The Instrument
```
IP Address 10.35.0.25
Subnet Mask 255.255.255.252
```
- The Instrument -The Resonance
```
IP Address 10.35.0.26
Subnet Mask 255.255.255.252
```
**Subnet A8**
- The Instrument - Matt Cugat
```
IP Address 10.35.0.129
Subnet Mask 255.255.255.128
```
- Matt Cugat - The Instrument
```
IP Address 10.35.0.130
Subnet Mask 255.255.255.128
Gateaway 10.35.0.129
```

**Subnet A13**
- The Instrument -The Firefist
```
IP Address 10.35.0.29
Subnet Mask 255.255.255.252
```
- The Firefist menuju The Instrument
```
IP Address 10.35.0.30
Subnet Mask 255.255.255.252
```

**Subnet A9**
- The Firefist menuju Keith dan The Queen
```
IP Address 10.35.3.1
Subnet Mask 255.255.255.0
```
- Keith menuju The Firefist
```
IP Address 10.35.3.2
Subnet Mask 255.255.255.0
Gateaway 10.35.3.1 
```
- The Queen menuju The Firefist
```
IP Address 10.35.3.3
Subnet Mask 255.255.255.0
```

**Subnet A4**
- The Queen menuju The Witch
```
IP Address 10.35.0.5
Subnet Mask 255.255.255.252
```
- The Witch menuju The Queen
```
IP Address 10.35.0.6
Subnet Mask 255.255.255.252
Gateaway 10.35.0.5
```

**Subnet A14**
- The Firefist menuju Oakleave
```
IP Address 10.35.4.1
Subnet Mask 255.255.254.0
```
- Oakleave menuju The Firefist
```
IP Address 10.35.4.2
Subnet Mask 255.255.254.0 
Gateaway 10.35.4.1
```

**Subnet A15**
- The Instrument menuju The Profound
```
IP Address 10.35.0.33
Subnet Mask 255.255.255.252
```
- The Profound menuju The Instrument
```
IP Address 10.35.0.34
Subnet Mask 255.255.255.252
```

**Subnet A17**
- The Profound menuju Helga
```
IP Address 10.35.1.1
Subnet Mask 255.255.255.128
```
- Helga menuju The Profound
```
IP Address 10.35.1.2
Subnet Mask 255.255.255.128
Gateaway 10.35.1.1
```

**Subnet A18**
- The Profound menuju Spendrow
```
IP Address 10.35.1.129
Subnet Mask 255.255.255.128
```
- Spendrow menuju The Profound
```
IP Address 10.35.1.130
Subnet Mask 255.255.255.128
Gateaway 10.35.1.129
```

**Subnet A11**
- The Resonance menuju The Magical
```
IP Address 10.35.0.21
Subnet Mask 255.255.255.252
```
- The Magical menuju The Resonance
```
IP Address 10.35.0.22
Subnet Mask 255.255.255.252
```

**Subnet A16**
- The Magical menuju Coverkt dan Haines
```
IP Address 10.35.6.1
Subnet Mask 255.255.254.0
```
- Coverkt menuju The Magical
```
IP Address 10.35.6.2
Subnet Mask 255.255.254.0
Gateaway 10.35.6.1
```
- Haines menuju The Magical
```
IP Address 10.35.6.3
Subnet Mask 255.255.254.0
Gateaway 10.35.6.1
```

**Subnet A10**
- The Resonance - The Beast
```
IP Address 10.35.0.17
Subnet Mask 255.255.255.252
```
- The Beast - The Resonance
```
IP Address 10.35.0.18
Subnet Mask 255.255.255.252
Gateaway 10.35.0.17
```

### Routing
Routing dapat dilakukan pada menu Config > Routing > Static pada Router. Contohnya pada gambar berikut:
![static](https://user-images.githubusercontent.com/72701806/204090853-dd9cf5d2-68ce-4153-b7c9-01ea0b4b3cd0.png)


Berikut list Static Route yang digunakan: </br>


**The Resonance**
```
10.35.0.64/26 via 10.35.0.14
10.35.0.8/30 via 10.35.0.14
10.35.8.0/22 via 10.35.0.14
10.35.0.0/30 via 10.35.0.14
10.35.2.0/30 via 10.35.0.14
10.35.0.128/25 via 10.35.0.26
10.35.0.28/30 via 10.35.0.26
10.35.0.4/30 via 10.35.0.26
10.35.4.0/23 via 10.35.0.26
10.35.0.32/30 via 10.35.0.26
10.35.1.0/25 via 10.35.0.26
10.35.1.128/25 via 10.35.0.26
10.35.6.0/23 via 10.35.0.22
```
**The Order**
```
0.0.0.0/0 via 10.35.0.13
10.35.8.0/22 via 10.35.0.10
10.35.0.0/30 via 10.35.0.10
10.35.2.0/30 via 10.35.0.10
```
**The Minister**
```
0.0.0.0/0 via 10.35.0.9
10.35.2.0/24 via 10.35.0.2
```
**The Daundless**
```
0.0.0.0/0 via 10.35.0.1
```
**The Instrument**
```
0.0.0.0/0 via 10.35.0.25
10.35.0.4/30 via 10.35.0.30
10.35.4.0/23 via 10.35.0.30
10.35.1.0/25 via 10.35.0.34
10.35.1.128/25 via 10.35.0.34
```
**The Firefist**
```
0.0.0.0/0 via 10.35.0.29
10.35.0.4/30 via 10.35.3.3
```
**The Queen**
```
0.0.0.0/0 via 10.35.3.1
```
**The Magical**
```
0.0.0.0/0 via 10.35.0.21
```
**The Profound**
```
0.0.0.0/0 via 10.35.0.33
```
## CIDR
### Subnetting
#### A

![image](https://user-images.githubusercontent.com/80830860/204086761-e1d2c6dd-807d-4cbf-8d63-41c09484882b.png)

| Subnet | #1 | #2 | Netmask |
|--|--|--|--|
| A1 | Guideau | The Minister | /22 |
| A2 | The Dauntless | Johan, Phanora | /24 |
| A3 | The Minister | The Dauntless | /30 |
| A4 | The Minister | The Order | /30 |
| A5 | Ashaf | The Order | /26 |
| A6 | The Order | The Resonance | /30 |
| A7 | The Witch | The Queen | /30 |
| A8 | Keith | The Firefist | /24 |
| A9 | Oakleave | The Firefist | /23 |
| A10 | The Firefist | The Instrument | /30 |
| A11 | Helga | The Profound | /25 |
| A12 | Spendrow | The Profound | /25 |
| A13 | The Profound | The Instrument | /30 |
| A14 | Matt Cugat | The Instrument | /25 |
| A15 | The Instrument | The Resonance | /30 |
| A16 | The Beast | The Resonance | /30 |
| A17 | The Magical | The Resonance | /30 |
| A18 | Haines, Corvekt | The Magical | /23 |

#### B

![image](https://user-images.githubusercontent.com/80830860/204087762-262ea643-90f5-4929-925c-a5c27b6a0335.png)

| Subnet | #1 | #2 | Netmask |
|--|--|--|--|
| B1 | A2 /24 | A3 /30 | /23 |
| B2 | A7 /30 | A8 /24 | /23 |
| B3 | A17 /30 | A18 /23 | /22 |
| B4 | A11 /25 | A12 /25 | /24 |

#### C

![image](https://user-images.githubusercontent.com/80830860/204088113-7e206fb9-5b1b-4e11-8b23-d77fca99bc9e.png)

| Subnet | #1 | #2 | Netmask |
|--|--|--|--|
| C1 | B1 /23 | A1 /22 | /21 |
| C2 | B2 /23 | A9 /23 | /22 |
| C3 | B3 /22 | A16 /30 | /21 |
| C4 | B4 /24 | A13 /30 | /23 |

#### D

![image](https://user-images.githubusercontent.com/80830860/204088171-5f0666f0-f555-460d-9945-4110c51087ae.png)

| Subnet | #1 | #2 | Netmask |
|--|--|--|--|
| D1 | C1 /21 | A4 /30 | /20 |
| D2 | C2 /22 | A10 /30 | /21 |
| D3 | C4 /23 | A14 /25 | /22 |

#### E

![image](https://user-images.githubusercontent.com/80830860/204088261-e0a37a16-882d-4aa4-8f86-cac56f4503e4.png)

| Subnet | #1 | #2 | Netmask |
|--|--|--|--|
| E1 | D1 /20 | A5 /26 | /19 |
| E2 | D2 /21 | D3 /22 | /20 |

#### F

![image](https://user-images.githubusercontent.com/80830860/204088307-6d9a2226-6cfd-484d-91d4-70a9c3449c8f.png)

| Subnet | #1 | #2 | Netmask |
|--|--|--|--|
| F1 | E1 /19 | A6 /30 | /18 |
| F2 | E2 /20 | A15 /30 | /19 |

#### G

![image](https://user-images.githubusercontent.com/80830860/204088362-1765eec9-f247-4f5f-b1d7-53b0b3df6a61.png)

| Subnet | #1 | #2 | Netmask |
|--|--|--|--|
| G1 | F2 /19 | C3 /21 | /18 |

#### H

![image](https://user-images.githubusercontent.com/80830860/204088401-32ec4027-8718-4e3a-946e-568e947971f9.png)

| Subnet | #1 | #2 | Netmask |
|--|--|--|--|
| H1 | G1 /18 | F1 /18 | /17 |

#### CIDR's Tree

![image](https://user-images.githubusercontent.com/80830860/204088424-cf272d11-ef0e-4e4f-a451-8ce3e40aa969.png)

### Configuration

The Resonance
```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
    address 10.35.98.1
    netmask 255.255.255.252

auto eth2
iface eth2 inet static
    address 10.35.32.1
    netmask 255.255.255.252

auto eth3
iface eth3 inet static
    address 10.35.100.1
    netmask 255.255.252.0

auto eth4
iface eth4 inet static
    address 10.35.80.1
    netmask 255.255.255.252
```

The Order
```
auto eth0
iface eth0 inet static
    address 10.35.32.2
    netmask 255.255.255.252
    gateway 10.35.80.1

auto eth1
iface eth1 inet static
    address 10.35.16.1
    netmask 255.255.255.192

auto eth2
iface eth2 inet static
    address 10.35.8.1
    netmask 255.255.255.252
```

Ashaf 
```
auto eth0
iface eth0 inet static
    address 10.35.16.2
    netmask 255.255.255.192
    gateway 10.35.16.1
```

The Minister
```
auto eth0
iface eth0 inet static
    address 10.35.8.2
    netmask 255.255.255.252
    gateway 10.35.8.1

auto eth1
iface eth1 inet static
    address 10.35.4.1
    netmask 255.255.252.0

auto eth2
iface eth2 inet static
    address 10.35.1.1
    netmask 255.255.255.252
```

Guideau
```
auto eth0
iface eth0 inet static
    address 10.35.4.2
    netmask 255.255.252.0
    gateway 10.35.4.1
```

The Dauntless
```
auto eth0
iface eth0 inet static
    address 10.35.1.2
    netmask 255.255.255.252
    gateway  10.35.1.1

auto eth1
iface eth1 inet static
    address 10.35.0.1
    netmask 255.255.255.0

```
Johan 
```
auto eth0
iface eth0 inet static
    address 10.35.0.2
    netmask 255.255.255.0
    gateway 10.35.0.1
```

Phanora (150 host)
```
auto eth0
iface eth0 inet static
    address 10.35.0.3
    netmask 255.255.255.0
    gateway 10.35.0.1
```
The Instrument
```
auto eth0
iface eth0 inet static
    address 10.35.80.2
    netmask 255.255.255.252
    gateway 10.35.32.1

auto eth1
iface eth1 inet static
    address 10.35.68.1
    netmask 255.255.255.252

auto eth2
iface eth2 inet static
    address 10.35.73.1
    netmask 255.255.255.252

auto eth3
iface eth3 inet static
    address 10.35.74.1
    netmask 255.255.255.128
```
Matt Cugat (120 host)
```
auto eth0
iface eth0 inet static
    address 10.35.74.2
    netmask 255.255.255.128
    gateway 10.35.74.1
```

The Firefist
```
auto eth0
iface eth0 inet static
    address 10.35.68.2
    netmask 255.255.255.252
    gateway 10.35.68.1

auto eth1
iface eth1 inet static
    address 10.35.66.1
    netmask 255.255.248.0

auto eth2
iface eth2 inet static
    address 10.35.64.1
    netmask 255.255.255.0
```

Keith 
```
auto eth0
iface eth0 inet static
    address 10.35.64.2
    netmask 255.255.255.0
    gateway 10.35.64.1
```

The Queen
```
auto eth0
iface eth0 inet static
    address 10.35.64.3
    netmask 255.255.255.0
    gateway 10.35.64.1

auto eth1
iface eth1 inet static
    address 10.35.65.1
    netmask 255.255.255.252
```

The Witch
```
auto eth0
iface eth0 inet static
    address 10.35.65.2
    netmask 255.255.255.252
    gateway 192.190.65.1
```
Oakleave 
```
auto eth0
iface eth0 inet static
    address 10.35.66.2
    netmask 255.255.248.0
    gateway 10.35.66.1
```

The Profound
```
auto eth0
iface eth0 inet static
    address 10.35.73.2
    netmask 255.255.255.252
    gateway 10.35.73.1

auto eth1
iface eth1 inet static
    address 10.35.72.129
    netmask 255.255.255.128

auto eth2
iface eth2 inet static
    address 10.35.72.1
    netmask 255.255.255.128
```

Helga 
```
auto eth0
iface eth0 inet static
    address 10.35.72.130
    netmask 255.255.255.128
    gateway 10.35.72.129
```
Spendrow 
```
auto eth0
iface eth0 inet static
    address 10.35.72.2
    netmask 255.255.255.128
    gateway 10.35.72.1
```

The Magical
```
auto eth0
iface eth0 inet static
    address 10.35.98.2
    netmask 255.255.255.252
    gateway 10.35.98.1

auto eth1
iface eth1 inet static
    address 10.35.96.1
    netmask 255.255.254.0
```
Coverkt 
```
auto eth0
iface eth0 inet static
    address 10.35.96.2
    netmask 255.255.254.0
    gateway 10.35.96.1
```

Haines 
```
auto eth0
iface eth0 inet static
    address 10.35.96.3
    netmask 255.255.254.0
    gateway 10.35.96.1
```

The Beast
```
auto eth0
iface eth0 inet static
    address 10.35.100.2
    netmask 255.255.252.0
    gateway 10.35.100.1
 ```
