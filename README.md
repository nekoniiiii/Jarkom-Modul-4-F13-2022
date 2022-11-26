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

Kemudian, lakukan hal yang sama pada setiap interface pada device. Berikut adalah pembagiannya.


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

#### C

#### D

#### E

#### F

#### G

#### H
