---
name: 'install-rstudio-ubuntu'
title: Install R Studio On Ubuntu
year: 24 Sept 2020
color: '#edece7'
isTextColorDark: true
noMainImage: false
extraComponent: 'Datatable'
id: 'install-rstudio-ubuntu'
description: |
  Bagaimana sih cara install R studio di ubuntu? apa susah installnya? Tenang aja disini kita akan belajar bagaimana cara menginstall Rstudio dengan cepat dan tentunya sangat sangat mudah. SO lets Read it
---

## Opening...

Assalamualaikum wr.wb

Guys disini saya akan membagikan tutorial bagaimana cara menginstall software R studio pada Operasi sistem linux distro ubuntu. Nah kebetulan kali ini saya menggunakan Lubuntu distro yang menggunakan Desktop Environment Lxde yang merupakan DE paling ringan yang ada di Linux. 

<image-responsive
    imageURL="blog/install-rstudio-ubuntu/neofetch.png"
    width="100%"
    alt="Neofetch terminal"
/>

Tutorial ini saya buat dengan 2 Metode, metode pertama menggunakan full Terminal, metode yang kedua menggunakan GUI(Grphical User Interface). Jadi simak baik baik ya :D
Oke langsung saja kita kebagian installasinya.

## Full Terminal Method

### Step 1: Tambah dulu Reponya

okey langkah pertama yang harus kita lakukan adalah menambahkan repository R studio ke terminal. Hal ini kita lakukan agar terminal kita dapat membaca perintah kita saat menginstall software R studio nanti.

ketik perintah ini pada terminal anda
```console
sudo apt update
sudo apt -y upgrade
```

### Step 2: Install R base package

lalu kita memerlukan package R base untuk pengoptimalan penggunaan R studio nanti
```console
sudo apt -y install r-base
```

### Step 3: Download dan Install R studio

langkah terakhir, tentu saja kita harus menginstall software R studionya dong. Jalankan perintah berikut di terminal kalian.

```console
sudo apt -y install wget
wget https://download1.rstudio.org/desktop/bionic/amd64/rstudio-1.2.5042-amd64.deb
sudo apt install ./rstudio-1.2.5042-amd64.deb
```

selesai deh, sekarang kalian dapat menggunakan R studio dan menjalankannya di app menu kalian atau bisa juga menggunakan terminal berikut:

```console
rstudio
```

## GUI Method

Oke kali ini kita akan menggunakan cara grafik bahasa umumnya tinggal klik-klik.

### Step 1: Buka dulu website resminya

Kalian bisa membuka website resminya dan langsung mendownloadnya, untuk linya disini [Rstdio](https://rstudio.com/products/rstudio/download/) . Dan download sampai selesai

### Step 2: Install dong packagenya

Kemudian install package kalian tadi yang berekstensikan .deb . Kalian dapat menggunakan software pihak ketiga seperti gdebi atau software bawaan kalian untuk menginstall package ini


## Conclusion

Bagaimana mudah bukan? saya sendiri lebih suka menggunakan terminal daripada menggunakan metode GUI. Sekian tutorial dari saya kurang lebihnya mohon maaf

Terima kasih

Wassalamualaikum wr.wb