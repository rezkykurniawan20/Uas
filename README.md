# Uas
package muhammad_rezky_kurniawan_2410010277;
import java.util.Scanner;
class Atlet {
private String nama; // [Poin 3: Atribut] & [Poin 7: Encapsulation]
private String npm;
public Atlet(String nama, String npm) {
this.nama = nama;
this.npm = npm;
}
public String getNama() { return nama; }
public String getNpm() { return npm; }
public void setNama(String nama) { this.nama = nama; } 
public void info() {
System.out.println("Nama Atlet : " + nama);
System.out.println("NPM        : " + npm);
}
}
class Powerlifter extends Atlet {
double[] angkatan = new double[3]; // [Poin 13: Array]
public Powerlifter(String nama, String npm) {
super(nama, npm);
}
@Override
public void info() {
super.info();
double total = angkatan[0] + angkatan[1] + angkatan[2];
System.out.println("Total Lift : " + total + " kg");
if (total >= 500) {
System.out.println("Kategori   : Kelas Berat (Elite)");
} else {
System.out.println("Kategori   : Kelas Ringan/Menengah");
}
}
}
public class Muhammad_Rezky_Kurniawan_2410010277 {
public static void main(String[] args) {
Scanner in = new Scanner(System.in);
try {
System.out.print("Masukkan Nama Atlet: ");
String namaInput = in.nextLine();
System.out.print("Masukkan NPM Atlet : ");
String npmInput = in.nextLine();
Powerlifter p = new Powerlifter(namaInput, npmInput);
System.out.println("\n=== INPUT DATA ANGKATAN ===");
String[] jenis = {"Squat", "Bench Press", "Deadlift"};
for (int i = 0; i < 3; i++) {
System.out.print("Masukkan berat " + jenis[i] + " (kg): ");
p.angkatan[i] = in.nextDouble();
}
System.out.println("\n--- HASIL PERHITUNGAN ---");
p.info();
} catch (Exception e) {
System.out.println("Error: Input wajib berupa angka untuk berat angkatan!");
}
}
}
