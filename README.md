# Proyek Akhir Pemrograman Berbasis Objek 1

Proyek ini adalah contoh sederhana aplikasi pengolahan data dan kategori atlet Powerlifting menggunakan Java sebagai tugas akhir dari mata kuliah Pemrograman Berorientasi Objek 1.

## Deskripsi

Aplikasi ini menerima input berupa nama atlet, NPM, serta beban tiga jenis angkatan (*Squat*, *Bench Press*, dan *Deadlift*). Aplikasi kemudian memberikan output berupa total beban yang berhasil diangkat dan menentukan kategori kelas atlet tersebut (*Kelas Berat/Elite* atau *Kelas Ringan/Menengah*).

Aplikasi ini mengimplementasikan beberapa konsep penting dalam Pemrograman Berorientasi Objek (OOP) seperti Class, Object, Atribut, Method Constructor, Method Mutator, Method Accessor, Encapsulation, Inheritance, Polymorphism (Overriding), Seleksi, Perulangan, IO Sederhana, Array, dan Error Handling.

## Penjelasan Kode

Berikut adalah bagian kode yang relevan dengan konsep OOP yang dijelaskan:

1. **Class** adalah template atau blueprint dari object. Pada kode ini, `Atlet`, `Powerlifter`, dan `Muhammad_Rezky_Kurniawan_2410010277` adalah contoh dari class.

```java
class Atlet { ... }
class Powerlifter extends Atlet { ... }
public class Muhammad_Rezky_Kurniawan_2410010277 { ... }

```
 2. **Object** adalah instance dari class. Pada kode ini, Powerlifter p = new Powerlifter(namaInput, npmInput); adalah contoh pembuatan object.
```java
Powerlifter p = new Powerlifter(namaInput, npmInput);

```
 3. **Atribut** adalah variabel yang ada dalam class. Pada kode ini, nama, npm, dan angkatan adalah contoh atribut.
```java
private String nama;
private String npm;
double[] angkatan = new double[3];

```
 4. **Constructor** adalah method yang pertama kali dijalankan pada saat pembuatan object. Pada kode ini, constructor ada di dalam class Atlet dan Powerlifter.
```java
public Atlet(String nama, String npm) {
    this.nama = nama;
    this.npm = npm;
}

public Powerlifter(String nama, String npm) {
    super(nama, npm);
}

```
 5. **Mutator** atau setter digunakan untuk mengubah nilai dari suatu atribut. Pada kode ini, setNama adalah contoh method mutator.
```java
public void setNama(String nama) {
    this.nama = nama;
}

```
 6. **Accessor** atau getter digunakan untuk mengambil nilai dari suatu atribut. Pada kode ini, getNama dan getNpm adalah contoh method accessor.
```java
public String getNama() { return nama; }
public String getNpm() { return npm; }

```
 7. **Encapsulation** adalah konsep menyembunyikan data dengan membuat atribut menjadi private dan hanya bisa diakses melalui method. Pada kode ini, atribut nama dan npm dienkapsulasi dan hanya bisa diakses melalui method getter dan setter.
```java
private String nama;
private String npm;

```
 8. **Inheritance** adalah konsep di mana sebuah class bisa mewarisi property dan method dari class lain. Pada kode ini, Powerlifter mewarisi Atlet dengan sintaks extends.
```java
class Powerlifter extends Atlet { ... }

```
 9. **Polymorphism** adalah konsep di mana sebuah nama dapat digunakan untuk merujuk ke beberapa tipe atau bentuk objek berbeda. Pada kode ini, method info() di Powerlifter merupakan bentuk overriding dari method info() di class Atlet.
```java
@Override
public void info() {
    super.info();
    double total = angkatan[0] + angkatan[1] + angkatan[2];
    System.out.println("Total Lift : " + total + " kg");
    ...
}

```
 10. **Seleksi** adalah statement kontrol yang digunakan untuk membuat keputusan berdasarkan kondisi. Pada kode ini, digunakan seleksi if else dalam method info() untuk menentukan kategori atlet.
```java
if (total >= 500) {
    System.out.println("Kategori   : Kelas Berat (Elite)");
} else {
    System.out.println("Kategori   : Kelas Ringan/Menengah");
}

```
 11. **Perulangan** adalah statement kontrol yang digunakan untuk menjalankan blok kode berulang kali. Pada kode ini, digunakan loop for untuk meminta input berat dari masing-masing angkatan.
```java
for (int i = 0; i < 3; i++) {
    System.out.print("Masukkan berat " + jenis[i] + " (kg): ");
    p.angkatan[i] = in.nextDouble();
}

```
 12. **Input Output Sederhana** digunakan untuk menerima input dari user dan menampilkan output ke user. Pada kode ini, digunakan class Scanner untuk menerima input dan method System.out.println untuk menampilkan output.
```java
Scanner in = new Scanner(System.in);
System.out.print("Masukkan Nama Atlet: ");
String namaInput = in.nextLine();
System.out.println("\n--- HASIL PERHITUNGAN ---");

```
 13. **Array** adalah struktur data yang digunakan untuk menyimpan beberapa nilai dalam satu variabel. Pada kode ini, double[] angkatan = new double[3]; dan String[] jenis adalah contoh penggunaan array.
```java
double[] angkatan = new double[3];
String[] jenis = {"Squat", "Bench Press", "Deadlift"};

```
 14. **Error Handling** digunakan untuk menangani error yang mungkin terjadi saat runtime. Pada kode ini, digunakan try catch untuk menangani error apabila input berat angkatan tidak berupa angka.
```java
try {
    // Jalannya program input data
} catch (Exception e) {
    System.out.println("Error: Input wajib berupa angka untuk berat angkatan!");
}

```
## Usulan nilai
| No | Materi | Nilai |
|---|---|---|
| 1 | Class | 5 |
| 2 | Object | 5 |
| 3 | Atribut | 5 |
| 4 | Constructor | 5 |
| 5 | Mutator | 5 |
| 6 | Accessor | 5 |
| 7 | Encapsulation | 5 |
| 8 | Inheritance | 5 |
| 9 | Polymorphism | 10 |
| 10 | Seleksi | 5 |
| 11 | Perulangan | 5 |
| 12 | IO Sederhana | 10 |
| 13 | Array | 15 |
| 14 | Error Handling | 15 |
|  | **TOTAL** | **100** |
## Pembuat
Nama: Muhammad Rezky Kurniawan
NPM: 2410010277
