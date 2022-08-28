---
author: "Faruq 1935"
draft: false
date: 2022-08-27T18:25:16+07:00
description: ""
title: "Cara Install Dan Konfigurasi Zsh"
slug: cara-install-dan-konfigurasi-shell-zsh
featured_image: "sinauriyen-zsh.png"
cascade:
    banner: 
    -

categories:
    -

bahasa:
    -

topik:


---

Pastinya kalian mungkin sudah bosan dengan tampilan terminal linux yang itu itu aja dengan zsh kalian bisa merubah tampilan terminal linux kalian menjadi lebih cantik.

Shell zsh ini bisa dikostumisasi sesuka kalian langsung saja kita install.

### 1.  Proses instalasi zsh
&nbsp;&nbsp;&nbsp;&nbsp;Buka terminal kalian dengan menekan tombol kombinasi `ctrl+alt+t`. Untuk Debian, Ubuntu dan turunannya ketikan perintah:
```shell
sudo apt update && apt install zsh
```
> Jika kalian menggunakan distro linux yang berbeda dengan saya kalian bisa lihat [disini](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH "zsh")

### 2. Mengkonfigurasi zsh sebagai shell utama pengganti bash
&nbsp;&nbsp;&nbsp;&nbsp;Jika sudah terpasang kalian bisa langsung menjalankan zsh dengan mengetik perintah `zsh` diterminal.
Untuk mengubah sehell bash ke zsh:
```shell
chsh $(whoami) -s $(which zsh)
```
Setelah mengetikan perintah diatas kalian bisa logout user lalu login kembali,
buka kembali terminal maka akan tampil sperti ini:

> Pilih nomor 2, (2) Populate your ~/.zshrc with the configuration recomemded by the system adminstarator and exit (you will need to edit the file by hand, if so desired).

![b](/assets/img/tutor-zsh/zshsudah.png "zshsudah")
&nbsp;&nbsp;&nbsp;&nbsp;

### 3. Memperacntik zsh
&nbsp;&nbsp;&nbsp;&nbsp;Nah kalian bisa mngubah tema yang disediakan oleh zsh loh kalian bisa memasang **oh my zsh**. Pastikan git sudah terinstall di sitem kalian.
dengan perintah:
```shell
sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

![b](/assets/img/tutor-zsh/ohmyzsh.png "ohmyzsh")
&nbsp;&nbsp;&nbsp;&nbsp;

kemudian kalian edit file `~/.zshrc`
```shell
nano ~/.zshrc
```

edit di baris `ZSH_THEME=""`

![b](/assets/img/tutor-zsh/filekonfigurasi.png "filekonfigurasi")
&nbsp;&nbsp;&nbsp;&nbsp;

> Untuk kumpulan thema zsh kalian bisa kunjungi [Theme oh my zsh](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes#agnoster "zsh")

jika sudah simpan dan keluar **ctrl + x** lalu tekan **y** dan **enter**.

Ketikan perintah:
```shell
source ~/.zshrc
```
> Untuk merestart file ~/.zshrc

Maka tampilannya akan seperti ini:

![b](/assets/img/tutor-zsh/hasilzsh.png "hasilzsh")
&nbsp;&nbsp;&nbsp;&nbsp;

Nah kurang lebihnya seperti itu jika ada yang mau dipertanyakan silahkan tulis dikolom komentar.

Referensi artikel ini:
* [https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH ](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH "zsh")
* [https://github.com/ohmyzsh/ohmyzsh/wiki/Themes#agnoster](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes#agnoster "zsh")