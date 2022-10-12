# Transformers
BY !KHAMD

<p align="center">
  <img height="50" height="auto" src="https://www.tfsc.io/doc/img/logo.svg">
</p>

# Tutorial TFSC node Pharse 2

**Dokumen Official :**
> [Node TFSC](https://www.tfsc.io/doc/learn/run-rpc-node)

**Explorer :**
> [Explorer TFSC](https://explorer.tfsc.io/)

**Discord :**
> [Discord TFSC](https://discord.gg/FCXpvHSq)

## Perangkat Keras

|  Komponen |  Persyaratan Minimum |
| ------------ | ------------ |
| CPU  | Intel Core i7-8700 Hexa-Core  |
| RAM | DDR4 16 GB  |
| Penyimpanan  | 500GB |
| koneksi | Port 1 Gbit/dtk |

## Perangkat Lunak

|Komponen | Persyaratan Minimum |
| ------------ | ------------ |
| OS |  Ubuntu 20 , CentOS 7 | 


## 1. Update Tools Yang di Perlukan
```
sudo apt-get update && sudo apt install git && sudo apt install screen
```
```
sudo apt-get install -y make bzip2 automake libbz2-dev libssl-dev doxygen graphviz libgmp3-dev \
autotools-dev libicu-dev python2.7 python2.7-dev python3 python3-dev \
autoconf libtool curl zlib1g-dev sudo ruby libusb-1.0-0-dev \
libcurl4-gnutls-dev pkg-config patch llvm-7-dev clang-7 vim-common jq libncurses5
```
## 2. Buat direktori baru dan masuk ke direktori folder
```
mkdir $HOME/tfsc && cd tfsc
```
## 3. Download Programs
```
wget https://uscloudmedia.s3.us-west-2.amazonaws.com/transformers/test/ttfs_v0.8.1_003950f_devnet
```
## 4. Beriakses
```
chmod +x ttfs_v0.8.1_003950f_devnet
```
## 5. Beri Izin File
```
./ttfs_v0.8.1_003950f_devnet -c
```
## 6. Jalankan node nya
```
screen -S tfsc
```
```
./ttfs_v0.8.1_003950f_devnet -m
```
Tunggu sampai node berhasil tersingkronisasi
## 7.Untuk mengonfigurasi node dengan informasi IP server Anda
```
cd tfsc
```
```
nano config.json
```
Isi dibagian IP (baris ke tiga) Dengan IP ADDRES node mu
Kamu juga bisa menambahkan nama di bagian "name"
Contoh seperti dibawah
```
{
    "http_callback": {
        "ip": "",
        "path": "",
        "port": 0
    },
    "http_port": 41517,
    "info": {
        "logo": "",
        "name": "<NAMA_NODEMU>"
    },
    "ip": "<IP_VPSMU>",
    "log": {
        "console": false,
        "level": "OFF",
        "path": "./logs"
    },
    "server": [
        "52.52.118.136",
        "13.52.162.66",
        "223.113.164.228",
        "223.113.164.226",
        "223.113.164.229",
        "223.113.164.230",
        "223.113.167.250",
        "223.113.167.246",
        "36.153.133.250"
    ],
    "server_port": 41516,
    "sync_data": {
        "count": 200,
        "interval": 10
    },
    "thread_num": 0,
    "version": "1.0"
}
```

## 7. Mulai Protocol Blockchain
Mulai ulang node anda
```
./ttfs_v0.8.1_003950f_devnet -m
```
atau bila sudah di screen anda bisa mengetikan
```
screen -Rd <NAMA_SCREENMU>
```
## 8. BYPASS data.db jika node tidak kunjung sync!!!
Ikuti cara ini 
NB!! data.db selalu update jadi terus ikuti di discord agar tidak tertinggal!!

masuk ke folder tfsc
```
cd tfsc
```
hapus data.db terlebih dahulu
```
rm -rf data.db
```
Download DB terbaru!! KAMU BISA DOWNLOAD LANGSUNG DI HP/PC MU LALU EKSTRAK DAN PINDAH DI NODE MU ATAU LANGSUNG DOWNLOAD LAGSUNG DI NODE!!
```
wget https://cdn.discordapp.com/attachments/993852538531090493/1029305973959041064/data.db_30116.tar.xz
```
EKSTRAK
```
tar -xf nama_file.tzr.xz
```
COBA JALANKAN KEMBALI TUNGGU SAMPAI SYNC!!!
## 9. CARA INVEST MANDIRI KE WALLET KAMU
Hubungkan ke sesi Layar saat ini dan hentikan program melalui item menu 0.Exit:
```
cd $HOME/tfsc && screen -r tfsc
```
Selanjutnya, Anda perlu mengganti nama folder dengan private key (cert) dari dompet Anda A:
```
mv cert bak_cert
```
Sekarang jalankan program, setelah memulai program akan secara otomatis menghasilkan dompet B baru:
```
./ttfs_v0.8.1_003950f_devnet -m
```
##Salin alamat dompet B dari menu, buka 🚰｜faucets di discord dan minta faucet.
```
!faucet <Address>
```
Setelah Anda menerima 5001 tTFSC (biasanya masuk dalam kurun waktu -+10 menit)
Anda perlu mendelegasikannya (untuk melakukan investasi) untuk wallet A Anda
untuk ini pilih item menu 4.Invest dan kemudian masukkan data seperti berikut:

AddrList:
```
<Disini wallet B sudah terisi otomatis> [default]
```
Please enter your addr:
```
<Masukan address wallet B (wallet kedua untuk invest mandiri)>.
```
Please enter the addr you want to invest to:
```
<Masukan address wallet A (wallet utama)>.
```
Please enter the amount to invest:
```
5000
```
enter Pleaseinvest type: (0: NetLicence) 
```
0
```
## DONE 
Silakan cek namamu di exploler kalau ada berarti dah kelar dan tunggu step selanjutnya...
