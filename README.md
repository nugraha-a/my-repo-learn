# MY REPO LEARN
Learn using laravel 8

## Requirement
<!-- * nodejs latest lts version 14.15.*^ -->
* laravel 8 (included)
* composer

## instalasi
1. silahkan clone repo ini
2. composer install
<!-- 3. yarn install -->

### Ketentuan
* branch master hanya untuk commit final untuk siap release (tiap release membuat branch version)
* gunakan branch dev untuk development
* jika ingin melakukan experiment silahkan membuat branch baru pada branch dev
* jangan pernah membuat modul secara langsung pada branch dev dan master
* untuk experimental silahkan bebas membuatnya di pada branch dev
* merge ke branch dev saat modul anda selesai di testing
##### 1. commit
* Commit dilakukan perbundle, atau perbaikan bug dsb. 
* diusahakan sedetail mungkin agar tracking mudah Contoh: 
```
git commit -m "membuat fitur pembayaran"
git commit -m "memperbaiki bug pada modul pembayaran" -m "bug pada pengkodisian pada file abc.js" 
```
##### 2. branch
* Jangan pernah membuat modul secara langsung pada branch dev dan master (jika ingin membuat modul silahkan buat branch baru yang menginduk pada branch dev)
* Branch dilakukan untuk fitur experimental dan penambahan modul
##### 3. merge
* Jika modul sudah selesai dan sudah di test maka silahkan merge ke dev
* Jika semua (team atau keseluruhan) modul sudah selesai silahkan merge ke master untuk di release
##### 4. menyusul 
## Panduan dasar
#### 1. panduan branch dari commit tertentu
![](https://4.bp.blogspot.com/-ygY_7uRflA4/WLvKgowOChI/AAAAAAAAEOg/pv6WngsMPYkYjGXuV2FOVHLNJnfsYiLawCPcB/s1600/membuat%2Bcabang%2Bbaru%2Bdari%2Bcommit%2Bmasa%2Blalu.png)
```
git checkout -b nama_cabang <nomer_commit>
```

#### 2. panduan revert (kembali ke commit yang diinginkan dan mengkomit didepan dari komit terakhir)
![](https://1.bp.blogspot.com/-p1Hts6bga0Q/WLvqvSAOYHI/AAAAAAAAEQc/eQzgyZfu5OoEN0jkS1FPX2AGN1-za7M-wCPcB/s1600/git-revert-petanikode.png)
```
git revert <nomer_commit>
git commit -m "pesan"
```

#### 3. panduan reset (pehatian jika melakukan reset maka commit yang diloncati(di depannya) akan hilang)
![](https://3.bp.blogspot.com/-BRpPbv9rlKo/WLvVCr4npTI/AAAAAAAAEPY/5TTifioVF-0LccoQx9gIYc_a8A5fB9LogCPcB/s1600/dampak%2Bgit%2Breset.png)
```
git reset --hard <nomer_commit>
git reset --soft HEAD
git commit -m "Reverting to the state of the project at f414f31"
```
penjelasan mode reset dibawah :
```
Contoh simulasi kamu punya comit kerjaan seperti ini , Asumsi kita sedang di C
- A - B - C (master)
```
* git reset --soft
Kalau kamu punya kerjaan yang sudah distage (git add). Pada saat menjalankan command ini, dia akan mengganti HEADnya. Menjalankan git reset --soft B, sekarang dia menunjuk ke B, tapi statusnya tetap yang sudah kamu lakukan sebelumnya (tidak berubah). Tinggal git commit hasilnya berarti balik lagi ke C

* git reset --mixed
Berganti saat di mixed, bukan hanya HEADnya yang terganti, tapi juga statusnya berubah, perlu di git add . lagi sebelum commit

* git reset --hard
Hard sama seperti mixed, bedanya kerjaan kamu di text-editor akan ikut berubah, kembali ke point yang kamu tunjuk. Kalau mixed kerjaan kamu sekarang di text-editor tidak terganti

## Tambahan
keterangan posisi head
```
$ git log --oneline

3fad532  Last commit   (HEAD)
3bnaj03  Commit before HEAD   (HEAD~1)
vcn3ed5  Two commits before HEAD   (HEAD~2)
```
Credit :
* http://petanikode.com/
* https://sekolahkoding.com/

Baca Lebih Lanjut :
* https://github.com/bantenprov/cara-penggunaan-github
