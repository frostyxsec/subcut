# SubCut

**subcut** adalah script bash untuk memfilter URL, menghapus domain utama, dan mempertahankan hanya subdomain.  
Cocok digunakan saat melakukan pengolahan daftar URL hasil crawling atau scraping.

---

## 🚀 Fitur
- Menghapus domain utama dari daftar URL
- Mempertahankan hanya subdomain
- Menampilkan ringkasan hasil proses (jumlah URL yang dihapus & dipertahankan)
- Preview hasil (10 baris pertama)
- Error handling untuk input file kosong atau tidak ditemukan

---

## 📦 Instalasi
Clone repository atau unduh script `subcut`:

```bash
git clone https://github.com/frostyxsec/subcut/
cd repo
chmod +x subcut
````

---

## 🔧 Penggunaan

```bash
./subcut -i input_file -o output_file -d domain
```

### Opsi

| Opsi | Deskripsi                                                 |
| ---- | --------------------------------------------------------- |
| `-i` | File input yang berisi daftar URL                         |
| `-o` | File output untuk menyimpan hasil filter                  |
| `-d` | Domain utama yang akan difilter (contoh: `example.go.id`) |
| `-h` | Menampilkan bantuan                                       |

---

## 📖 Contoh

### Input (`urls.txt`)

```
https://example.go.id
http://www.example.go.id
https://api.example.go.id
sub.example.go.id
https://www.admin.example.go.id
```

### Command

```bash
./subcut -i urls.txt -o filtered.txt -d example.go.id
```

### Output (`filtered.txt`)

```
https://api.example.go.id
sub.example.go.id
https://www.admin.example.go.id
```

---

## ✅ URL yang Dihapus

* `example.go.id`
* `https://example.go.id`
* `http://www.example.go.id`
* `www.example.go.id`

## ✅ URL yang Dipertahankan

* `https://api.example.go.id`
* `sub.example.go.id`
* `https://www.admin.example.go.id`

---

## 📜 Lisensi

Proyek ini dirilis di bawah lisensi **MIT**.
Silakan gunakan, modifikasi, dan distribusikan sesuai kebutuhan.
