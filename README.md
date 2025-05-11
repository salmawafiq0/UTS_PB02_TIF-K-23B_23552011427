# UTS Pemrograman Berorientasi Obyek 2
<ul>
  <li>Mata Kuliah: Pemrograman Berorientasi Obyek 2</li>
  <li>Dosen Pengampu: <a href="https://github.com/Muhammad-Ikhwan-Fathulloh">Muhammad Ikhwan Fathulloh</a></li>
</ul>

## Profil
<ul>
  <li>Nama: {Wafiq Salma Aulia}</li>
  <li>NIM: {23552011427}</li>
  <li>Studi Kasus: {Sistem Kasir}</li>
</ul>

## Judul Studi Kasus
<p>Sistem Kasir Restoran.</p>

## Penjelasan Studi Kasus
<p>Sistem Kasir Restoran adalah aplikasi yang dirancang untuk mengelola pemesanan dan pembayaran makanan dan minuman di sebuah restoran. Aplikasi ini memungkinkan pengguna untuk membuat pesanan baru, melihat daftar pesanan, dan memproses pembayaran.
  
=> Fitur Utama
    - Manajemen Menu (Makanan dan Minuman)
    - Pembuatan Pesanan
    - Perhitungan Total Harga
    - Proses Pembayaran dan Cetak Struk</p>

## Penjelasan 4 Pilar OOP dalam Studi Kasus

### 1. Inheritance
<p>Inheritance diimplementasikan dengan hierarki kelas Menu sebagai parent class, serta Makanan dan Minuman sebagai child class.
javapublic abstract class Menu {
    protected int id;
    protected String nama;
    protected double harga;
    protected String jenis;
    // ...
}

public class Makanan extends Menu {
    private boolean spesial;
    // ...
}

public class Minuman extends Menu {
    private boolean dingin;
    // ...
}
Kelas Makanan dan Minuman mewarisi atribut dan method dari kelas Menu seperti id, nama, harga, dan jenis. Dengan inheritance, kode dapat diorganisir dengan lebih baik dan menghindari duplikasi.</p>

### 2. Encapsulation
<p>Enkapsulasi diimplementasikan dengan penggunaan access modifier (private, protected, public) dan metode getter/setter untuk mengontrol akses ke data.
javapublic class Pesanan {
    private int id;
    private int nomorMeja;
    private String status;
    private Date tanggalPesanan;
    private List<DetailPesanan> detailPesanan;
    
    // Getter dan Setter
    public int getId() {
        return id;
    }
    
    public void setId(int id) {
        this.id = id;
    }
    
    // Method lainnya...
}
Dengan enkapsulasi, data disembunyikan dan hanya dapat diakses melalui method yang disediakan, sehingga menjaga integritas data.</p>

### 3. Polymorphism
<p>Polimorfisme diimplementasikan melalui method hitungHarga() yang di-override oleh kelas turunan.
java// Di abstract class Menu
public abstract double hitungHarga();

// Di class Makanan
@Override
public double hitungHarga() {
    // Makanan spesial mendapatkan tambahan 10% dari harga dasar
    if (spesial) {
        return harga * 1.1;
    }
    return harga;
}

// Di class Minuman
@Override
public double hitungHarga() {
    // Minuman dingin mendapatkan tambahan Rp 2000
    if (dingin) {
        return harga + 2000;
    }
    return harga;
}
Dengan polimorfisme, sistem dapat memanggil method hitungHarga() pada objek Menu, dan implementasi yang sesuai akan dipanggil berdasarkan tipe objeknya (Makanan atau Minuman).</p>

### 4. Abstract
<p>Abstraksi diimplementasikan melalui abstract class Menu dan abstract method hitungHarga().
javapublic abstract class Menu {
    // ...
    
    // Abstract method yang akan diimplementasikan oleh subclass
    public abstract double hitungHarga();
    
    // ...
}
Abstraksi memungkinkan pembuatan blueprint untuk kelas-kelas turunan dan menyembunyikan implementasi detail dari pengguna.</p>

## Demo Proyek
<ul>
  <li>Github: <a href="">Github</a></li>
  <li>Youtube: <a href="">Youtube</a></li>
</ul>
