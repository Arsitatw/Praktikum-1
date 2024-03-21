# <h1 align="center">Laporan Praktikum Modul Tipe Data</h1>
<p align="center"> Arsita Wiwit Tiyaswening </p>

# Dasar Teori
Tipe data adalah adalah sebuah pengklasifikasian data berdasarkan jenis data tersebut. Tipe data dibutuhkan agar kompiler dapat mengetahui bagaimana sebuah 
data akan digunakan. Adapun tipe data yang akan dipelajari adalah tipe data Primitif, tipe data Abstrak, dan tipe data Koleksi.

# Tipe data Primitif
Tipe data primitif adalah tipe data yang didefinisikan dalam bahasa pemrograman, yang dapat dibuat secara langsung tanpa membutuhkan alokasi memori yang ekstra. Contoh tipe data primitif dalam C++ adalah:
- 'char' = karakter
- 'int' = integer atau bilangan bulat
- 'float' = untuk bilangan desimal
- 'bool' = boolean atau benar dan salah
  
# Tipe data Abstrak
Tipe data abstrak (ADT) adalah model matematika dari objek data yang menyempurnakan tipe data dengan cara mengaitkannya dengan fungsi-fungsi yang beroperasi pada data yang bersangkutan. ADT hanya menyebutkan operasi apa yang akan dilakukan, tetapi tidak menyebutkan bagaimana operasi ini akan dilakukan. Ini disebut "abstraksi" karena memberikan tampilan yang tidak bergantung pada implementasi. Contoh tipe data abstrak dalam C++ adalah kelas, struct, union, dan enumerasi[1]. 

# Tipe data Koleksi
Tipe data koleksi adalah jenis tipe data yang mengumpulkan beberapa nilai dalam satu variabel. Contoh tipe data koleksi dalam C++ adalah array, string, dan list. Tipe data koleksi dapat berisi nilai dari berbagai jenis tipe data, seperti bilangan bulat, karakter, dan boolean

# Guided

## Tipe Data Primitif
```C++
#include <iostream>
using namespace std;
// Main program
int main()
{
    char op;
    float num1, num2;
    cout<<"Masukan Operator: ";
    cin>>op;
    cout<<"\nMasukan Bilangan ke-1 dan ke-2: ";
    cin>>num1>>num2;

    switch(op)
    {
    case '+':
        cout<< num1 + num2;
        break;
    case '-':
        cout<< num1 - num2;
    case '*':
        cout<< num1 * num2;
    case '/':
        cout<< num1 / num2;
    default:
        cout<< "Error! operator is not correct";
        
    }

return 0;
}
```
Kode diatas merupakan kode untuk operasi penjumlahan, pengurangan, perkalian dan pembagian. Saat kode dijalankan operator awalnya akan diminta untuk menginput operasi aritmatika yang ingin dijalankan. Setalahnya menginput angka yang akan di lakukan operasi, jika operator salah dalam menginput program akan otomatis menampilkan pesan eror.

## Tipe Data Abstrak
```C++
#include <iostream>
#include <stdio.h>
using namespace std; 


struct Mahasiswa 
{
    const char *name;
    const char *address;
    int age; 
};
int main()
{
    // menggunakan struct 
    Mahasiswa mhs1, mhs2;

    mhs1.name = "Tata";
    mhs1.address = "Banjarnegara";
    mhs1.age = 18;
    mhs2.name = "Jeti"; 
    mhs2.address = "Jember";
    mhs2.age = 18; 

    cout<<"Mahasiswa 1\n";
    cout<<"Nama: "<< mhs1.name <<endl;
    cout<<"Alamat: " <<mhs1.address <<endl;
    cout<<"Umur: "  << mhs1.age <<endl;

    cout <<"\nMahasiswa 2\n"; 
    cout << "Nama: " << mhs2.name <<endl;
    cout << "Alamat: "<< mhs2.address <<endl;
    cout << "Umur: "<< mhs2.age <<endl; 

    return 0;
}
```
Kode diatas merupakan tipe data abstrak yaitu struck. Pada kode tersebut menggunakan struct Mahasiswa yang memuat tiga nilai yaitu name, addres dengan tipe data character dan age dengan tipe data integer. Lalu terdapat const pada name dan addres untuk menyatakan objek atau variable. Setelahnya digunakan Mahasiswa mhs1, mhs2 untuk medeklarasikan dua variable bertipe Mahasiswa yaitu mhs1 dan mhs2. Menggunakan objek cout untuk mencetak output.

## Tipe Data Koleksi
```C++
#include <iostream>
#include <array>
using namespace std;

int main() 
{
    
    int nilai[5];
    nilai[0] = 20;
    nilai[1] = 25;
    nilai[2] = 30;
    nilai[3] = 6;
    nilai[4] = 3;

    
    cout << "Isi array pertama : " << nilai[0] << endl;
    cout << "Isi array kedua : " << nilai[1] << endl;
    cout << "Isi array ketiga : " << nilai[2] << endl;
    cout << "Isi array keempat : " << nilai[3] << endl;
    cout << "Isi array kelima : " << nilai[4] << endl;
    return 0;
}
```
Menggunakan using namespace std; agar tidak perlu menggunakan std:: setiap menambahkan fungsinya. Pendeklarasian menggunakan array bernama nilai dengan panjang 5. Mengisi nilai nilai ke dalam array nilai menggunkaan indeks array. Kemudian untuk menampilkan nilai nilai dari array nilai menggunakan objek cout dan operator <<.

# Unguided
## 1.  Buatlah program menggunakan tipe data primitif minimal dua fungsi dan bebas. Menampilkan program, jelaskan program tersebut dan ambil kesimpulan dari materi tipe data primitif

```C++
#include <iostream>
#include <cmath> 
using namespace std;

// Fungsi untuk menghitung luas segitiga
double hitungLuasSegitiga(double alas, double tinggi) {
    return 0.5 * alas * tinggi;
}

// Fungsi untuk menghitung keliling segitiga
double hitungKelilingSegitiga(double sisi1, double sisi2, double sisi3) {
    return sisi1 + sisi2 + sisi3;
}

int main() {
    double alas, tinggi, sisi1, sisi2, sisi3;

    // Masukkan panjang alas dan tinggi segitiga
    cout << "Masukkan panjang alas segitiga: ";
    cin >> alas;
    cout << "Masukkan tinggi segitiga: ";
    cin >> tinggi;

    // Masukkan panjang sisi-sisi segitiga
    cout << "Masukkan panjang sisi pertama segitiga: ";
    cin >> sisi1;
    cout << "Masukkan panjang sisi kedua segitiga: ";
    cin >> sisi2;
    cout << "Masukkan panjang sisi ketiga segitiga: ";
    cin >> sisi3;

    // Hitung dan tampilkan luas segitiga
    cout << "Luas segitiga: " << hitungLuasSegitiga(alas, tinggi) << endl;

    // Hitung dan tampilkan keliling segitiga
    cout << "Keliling segitiga: " << hitungKelilingSegitiga(sisi1, sisi2, sisi3) << endl;

    return 0;
}
```
Outputnya :

![alt text](https://github.com/Arsitatw/Praktikum-1/blob/master/Screenshot%202024-03-21%20235623.png?raw=true)

## 2. Jelaskan fungsi dari class dan struct secara detail dan berikan contoh programnya

```C++
#include <iostream>
#include <string>
using namespace std;

// Deklarasi struct Mahasiswa
struct MahasiswaStruct {
    string nama;
    int umur;
    
    // Method untuk menampilkan data mahasiswa
    string tampilkanData() {
        string data = "Nama : " + nama + "\n";
        data += "Umur : " + to_string(umur) + "\n";
        return data;
    }
};

// Deklarasi class Mahasiswa
class MahasiswaClass {
private:
    string nama;
    int umur;
    
public:
    // Constructor untuk inisialisasi objek
    MahasiswaClass(string n, int u) : nama(n), umur(u) {}

    // Method untuk menampilkan data mahasiswa
    string tampilkanData() {
        string data = "Nama : " + nama + "\n";
        data += "Umur : " + to_string(umur) + "\n";
        return data;
    }
};

int main() {
    // Menggunakan struct
    MahasiswaStruct mhs1Struct;
    mhs1Struct.nama = " Tata ";
    mhs1Struct.umur = 18;
    cout << mhs1Struct.tampilkanData();

    // Menggunakan class
    MahasiswaClass mhs1Class(" Tata ", 18);
    cout << mhs1Class.tampilkanData();

    return 0;
}
```
Outputnya :

![alt text](https://github.com/Arsitatw/Praktikum-1/blob/master/Screenshot%202024-03-22%20000541.png?raw=true)


## 3. Buat dan jelaskan program menggunakan fungsi map dan jelaskan perbedaan dari array dengan map

```C++
#include <iostream>
#include <map>
#include <string>

using namespace std;

int main() {
    
    map<string, int> mahasiswa;

    
    mahasiswa["Tata"] = 18;
    mahasiswa["Lika"] = 18;
    mahasiswa["Ana"] = 19;

    
    cout << "Data Mahasiswa:\n";
    for (auto it = mahasiswa.begin(); it != mahasiswa.end(); ++it) {
        cout << "Nama: " << it->first << ", Umur: " << it->second << endl;
    }

    return 0;
}
```

Outputnya :

![alt text](https://github.com/Arsitatw/Praktikum-1/blob/master/Screenshot%202024-03-22%20000627.png?raw=true)

# Referensi
[1] Afrizal Zein Emi Sita Eriana, Algoritma dan Struktur Data. Responsitory Unpam, 2022.
