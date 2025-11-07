# README ASAL BUAT <3

# T4n-Manpy (VUR Helper)

T4n-Manpy adalah tool CLI yang berfungsi sebagai helper untuk mengelola paket dari VUR (Void User Repo). Tool ini mempermudah proses instalasi, pembaruan, penghapusan, hingga pembuatan dan pengiriman paket ke repositori komunitas.

---

## Tujuan

* Mengurangi kerumitan penggunaan `xbps-src` secara manual.
* Memberikan workflow yang konsisten untuk user dan maintainer.
* Mempercepat proses kontribusi ke VUR.

---

## Fitur Utama

* Install paket langsung dari VUR.
* Build paket otomatis dari source.
* Update paket dengan sinkronisasi template terbaru.
* Submit paket baru ke repositori VUR.
* Validasi dependensi dan environment build.

---

## Cara Menggunakan

### **Menginstall Paket**

```
t4n-manpy install <nama-paket>
```

Tool akan:

1. Menarik template paket dari VUR
2. Melakukan build otomatis
3. Menginstall ke sistem menggunakan `xbps-install`

### **Menghapus Paket**

```
t4n-manpy remove <nama-paket>
```

### **Update Paket**

```
t4n-manpy update <nama-paket>
```

### **Build Paket Tanpa Install**

```
t4n-manpy build <nama-paket>
```

Output hasil build berada di:

```
hostdir/binpkgs/
```

### **Submit Paket Baru ke VUR**

```
t4n-manpy submit <nama-paket>
```

Persyaratan sebelum submit:

* `template` valid
* Build tidak error
* Checksum dan source valid

---

## Struktur Direktori T4n-Manpy

```
~/.local/share/t4n-manpy/
 ├── cache/       # cache paket
 ├── logs/        # log build
 └── config.toml  # konfigurasi user
```

---

## Konfigurasi

Edit file:

```
~/.local/share/t4n-manpy/config.toml
```

Contoh:

```
[vur]
path = "/home/user/vur"
repo_url = "https://github.com/t4n-os/vur.git"
```

---

## Filosofi

* **Transparan**: Semua proses terlihat, tidak ada magic.
* **Kendali Penuh**: User selalu tahu apa yang sedang dibuild.
* **Efisien**: Memotong langkah repetitif tanpa menyembunyikan detail.

---

## Catatan

Tool ini bukan pengganti `xbps-src`, melainkan pembantu workflow agar pengalaman VUR semakin nyaman.

---

**T4n-Manpy — Bukan hanya helper. Tapi jembatan antara pengguna dan komunitas.**
