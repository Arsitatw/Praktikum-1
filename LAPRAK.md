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


# Referensi
[1] Afrizal Zein Emi Sita Eriana, Algoritma dan Struktur Data. Responsitory unpam, 2022.
