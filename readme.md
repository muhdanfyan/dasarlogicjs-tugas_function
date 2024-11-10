

# 🚀 **Sistem Kasir Sederhana dengan JavaScript**

Selamat datang di repositori **Sistem Kasir Sederhana**! Proyek ini dirancang untuk membantu Anda memahami dan mempraktikkan konsep-konsep fungsi (**function**) dalam JavaScript dengan pendekatan **Project-Based Learning**. Anda akan membangun aplikasi kasir sederhana sambil mempelajari:

- Membuat dan menjalankan function.
- Menggunakan parameter dan argument.
- Memahami scope variabel.
- Melakukan refactoring.
- Menerapkan rekursif.
- Memahami perbedaan declaration vs. expression.

---

## 📋 **Tujuan Pembelajaran**

Dengan menyelesaikan proyek ini, Anda akan mampu:
1. Menggunakan fungsi untuk menulis kode yang modular dan efisien.
2. Memahami dan mengimplementasikan parameter, argument, dan return value.
3. Menggunakan scope variabel dengan benar.
4. Menerapkan rekursif untuk masalah yang relevan (opsional).
5. Memahami perbedaan antara function declaration dan expression.

---

## 🛠️ **Instruksi Tugas**

Ikuti langkah-langkah di bawah ini untuk menyelesaikan tugas:

### **1. Membuat Struktur Dasar Program**
- Buatlah fungsi `main` untuk menjadi entry point dari program.
- Di dalam `main`, tampilkan menu pilihan berikut:
  1. Tambahkan barang.
  2. Hitung total.
  3. Keluar.

Contoh:
```javascript
function main() {
    console.log("Selamat datang di Sistem Kasir!");
    console.log("1. Tambahkan barang");
    console.log("2. Hitung total");
    console.log("3. Keluar");

    // Logika untuk memanggil fungsi berdasarkan pilihan
}
main();
```

---

### **2. Membuat dan Menjalankan Function**
Buat fungsi `tambahBarang` untuk menambahkan barang ke dalam keranjang belanja.

**Tugas:**
1. Definisikan array kosong bernama `keranjangBelanja`.
2. Buat fungsi `tambahBarang(nama, harga)` yang menambahkan barang ke dalam array tersebut.
3. Panggil `tambahBarang` dari dalam fungsi `main`.

---

### **3. Menggunakan Parameter dan Argument**
Gunakan parameter dan argument untuk menangani input pengguna.

**Tugas:**
1. Tambahkan prompt untuk memasukkan nama dan harga barang.
2. Kirim nama dan harga barang sebagai argument ke fungsi `tambahBarang`.

Contoh:
```javascript
tambahBarang("Sabun", 5000); // Output: Barang Sabun berhasil ditambahkan.
```

---

### **4. Refactoring**
Refactor kode Anda agar lebih modular dan mudah dibaca.

**Tugas:**
1. Pindahkan logika penghitungan total harga ke dalam fungsi `hitungTotal`.
2. Pastikan fungsi `main` hanya memanggil fungsi lain tanpa logika langsung.

Contoh Sebelum Refactoring:
```javascript
let total = 0;
for (let item of keranjangBelanja) {
    total += item.harga;
}
console.log(total);
```

Contoh Setelah Refactoring:
```javascript
function hitungTotal() {
    let total = 0;
    for (let item of keranjangBelanja) {
        total += item.harga;
    }
    return total;
}
```

---

### **5. Memahami Scope Variabel**
Gunakan scope variabel dengan benar:
- Variabel global (`keranjangBelanja`) harus dapat diakses oleh semua fungsi.
- Variabel lokal seperti `total` hanya boleh berada dalam fungsi `hitungTotal`.

**Tugas:**
Periksa apakah semua variabel memiliki scope yang sesuai.

---

### **6. Rekursif (Opsional)**
Gunakan rekursif untuk menampilkan isi keranjang belanja.

**Tugas:**
1. Buat fungsi `tampilkanKeranjang(index)` yang menggunakan rekursif untuk menampilkan barang satu per satu.
2. Pastikan program berhenti saat semua barang telah ditampilkan.

Contoh:
```javascript
function tampilkanKeranjang(index) {
    if (index >= keranjangBelanja.length) return;
    console.log(`${index + 1}. ${keranjangBelanja[index].nama} - Rp${keranjangBelanja[index].harga}`);
    tampilkanKeranjang(index + 1);
}
```

---

### **7. Declaration vs. Expression**
Gunakan **function declaration** dan **function expression** dengan bijak:
- Gunakan **declaration** untuk fungsi utama, seperti `tambahBarang`.
- Gunakan **expression** untuk fungsi yang hanya dipanggil sekali.

Contoh:
```javascript
const keluar = function() {
    console.log("Terima kasih telah menggunakan Sistem Kasir.");
};
```

---

## 📌 **Kriteria Penilaian**
1. **Fungsi Berjalan Sesuai Harapan**:
   - Program dapat menambahkan barang, menghitung total harga, dan memberikan diskon dengan benar.
2. **Penggunaan Parameter dan Argument**:
   - Semua fungsi menggunakan parameter dan argument secara efektif.
3. **Struktur Kode yang Modular**:
   - Refactoring dilakukan, dan fungsi memiliki tugas spesifik.
4. **Scope Variabel yang Benar**:
   - Variabel global dan lokal digunakan sesuai kebutuhan.
5. **(Opsional) Rekursif**:
   - Daftar barang ditampilkan menggunakan rekursif.
6. **Penerapan Declaration dan Expression**:
   - Perbedaan penggunaan function declaration dan expression diterapkan dengan tepat.
7. **Masing-masing Silahkan memberikan penamaan variabel dan fungsi yang sesuai**:
   - Jangan menggunakan nama variabel dan fungsi yang mirip
8. **Buat Repo dan Video Penjelasan cara kerja kodingan, dan cara kerja aplikasi yang sudah dibuat**:
   - Jelaskan semua bahan yang dipelajari dalam kodingan seperti function yang digunakan, scope variabel, dan refactoring, rekursif, dan perbedaan declaration dan expression lalu tampilkan bagaiama itu berguna dalam aplikasi yang dibuat..
9. **Ketika selesai, silahkan memberikan link repo github, jelaskan pemaparan tersebut di hadapan mentor dan akademik**
   - Menghadap ke mentor dan akademik, serta jelaskan cara kerja sistem. Jangan lupa untuk menguji kode Anda secara menyeluruh. 


---

## 🚀 **Output Akhir**
Berikut adalah contoh output yang diharapkan saat program dijalankan:

```
Selamat datang di Sistem Kasir!
1. Tambahkan barang
2. Hitung total
3. Keluar
Pilih menu: 1
Masukkan nama barang: Sabun
Masukkan harga barang: 5000
Barang berhasil ditambahkan!

1. Tambahkan barang
2. Hitung total
3. Keluar
Pilih menu: 2
Total belanja Anda: Rp5000
```

---

Selamat belajar dan semoga berhasil menyelesaikan tugas ini! Jangan lupa untuk menguji kode Anda secara menyeluruh. 🎉

--- 

**README.md** ini siap digunakan di GitHub untuk membantu pelajar memahami dan mengaplikasikan **function** dalam JavaScript melalui **Project-Based Learning**.