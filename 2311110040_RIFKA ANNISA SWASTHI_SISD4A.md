# <h1 align="center">Laporan Praktikum Modul Tipe Data</h1>
<p align="center">Rifka Annisa Swasthi</p>
<p align="center">2211110040</p>

## Dasar Teori
Tipe data disini dibagi menjadi tiga
1. Tipe data Primitif dibagi menjadi tipe byte, short, int dan long yaitu tipe data yang bersifat signed, yang merepresentasikan nilai positif dan negatif. 
2. Tipe data koleksi adalah data yang berupa rangkaian yang berindeks tipe data ini dibagi menjadi tiga yaitu array, liat dan map. 
3. Tipe data abstrak yaitu tipe data yang berupa kumpulan tipe data primitif yang dapat diciptakan secara dinamis.

## Guided 

### 1. Tipe Data Primitif
```C++
#include <iostream>
using namespace std;
// Main program
main()
{
    char op;
    float num1, num2;
    // It allows user to enter operator i.e. +, -, *, /
    cout << "masukkan operator:";
    cin >> op;
    // It allow user to enter the operands
    cout << "masukkan angka1 & 2";
    cin >> num1 >> num2;
    //switch statment begins
    switch(op)
    {
    // if user enter +
    case '+':
        cout << num1 + num2;
        break;
     //if user enter -
     case '-':
        cout << num1 - num2;
        break;
    //if user enter *
    case '*':
        cout << num1 * num2;
        break;
    //if user enter /
    case '/':
        cout << num1 / num2;
        break;
    //if the operator is other than +, -, * or /,
    //eror massage will display
    default:
        cout << "eror! operator is not correct";
    }// switch statement ends
    return 0;
}

```
#### Output:
![Screenshot 2024-03-09 152146](https://github.com/suxeno/Struktur-Data-Assignment/assets/162097297/4286acd3-7e40-41d9-b24d-c14e12b461a5)



Kode di atas digunakan untuk mencetak angka dari operasi bilangan aritmatika yang sudah diberi operator sehingga ketika run hasilnya akan berupa hasil dari proses tadi. 

#### Full code Screenshot:
![Screenshot 2024-03-09 152526](https://github.com/suxeno/Struktur-Data-Assignment/assets/162097297/4ab823c8-a507-4ab5-86b0-b13e3f5e2335)
Dengan menggunakan menggunakan function cout untuk mengeksekusi nya yang diatasnya sudah dimasukkan using name space std yang memungkinkan untuk menggunakan cout dan cin tanpa menulis std:: di awalnya. Switch statement dimasukkan ketika akan mengeksekusi operasi aritmatika karena itu ankn memudahkan daripada switch if else lainnya.


### 2. Tipe Data Abstrak

```C++
#include <stdio.h>
//Struct
struct Mahasiswa
{
    const char *name;
    const char *address;
    int age;
};
int main()
{
    //menggunaka struct
    struct Mahasiswa mhs1, mhs2;
    mhs1.name = "dian";
    mhs1.address = "mataram";
    mhs1.age = 22;
    mhs2.name = "bambang";
    mhs2.address = "surabaya";
    mhs2.age = 23;
    // mencetak isi struct
    printf("## mahasiswa 1 ##\n");
    printf("nama: %s\n", mhs1.name);
    printf("alamat:%s\n", mhs1.address);
    printf("umur: %d\n", mhs1.age);
    printf("## mahasiswa 2 ##\n");
    printf("nama: %s\n", mhs2.name);
    printf("alamat:%s\n", mhs2.address);
    printf("umur: %d\n", mhs2.age);
    return 0;
}

```
#### Output:
![Screenshot 2024-03-09 152902](https://github.com/suxeno/Struktur-Data-Assignment/assets/162097297/7ed99073-0721-49cd-a946-1230bca3ee6a)



Kode di atas digunakan untuk mencetak teks dari setiap data yang sudah dimasukkan

#### Full code Screenshot:
![Screenshot 2024-03-09 153021](https://github.com/suxeno/Struktur-Data-Assignment/assets/162097297/ea6ba189-0789-4985-8ed7-4478a6b59c21)
dilihat dari kode diatas kode dibuat dalam satu struktur yang dikelompokkan menjadi satu entitas mahasiswa jika dijalankan akan menghemat waktu karena satu masukkan mahasiswa akan mencetak berbagai data sesuai inputan.
### 3. Tipe Data Koleksi

```C++
#include <iostream>
using namespace std;

int main()
{
    //deklarasi dan inisialisasi array
    int nilai[5];
    nilai[0] = 23;
    nilai[1] = 50;
    nilai[2] = 34;
    nilai[3] = 78;
    nilai[4] = 90;

    //mencetak array
    cout << "Isi array pertama :" << nilai[0] << endl;
    cout << "Isi array kedua :" << nilai[1] << endl;
    cout << "Isi array ketiga :" << nilai[2] << endl;
    cout << "Isi array keempat :" << nilai[3] << endl;
    cout << "Isi array kelima :" << nilai[4] << endl;
    return 0;
}
```
### output
![Screenshot 2024-03-09 153243](https://github.com/suxeno/Struktur-Data-Assignment/assets/162097297/ab22b8bb-8082-4c04-95c3-0d76fb26ab23)

Kode di atas digunakan untuk mencetak nilai array yang sudah disimpan dalam nilai kemudian akan keluar satu satu nilai dari indeks 
#### Full code Screenshot:
![Screenshot 2024-03-09 153439](https://github.com/suxeno/Struktur-Data-Assignment/assets/162097297/32086a34-681a-4570-a1e3-da143c67286e)

Dengan menggunakan array, program menyimpan beberapa nilai dengan tipe data yang sama dalam satu struktur data sehingga dapat digunakan untuk memanipulasi dan mengakses nilai-nilai tersebut menggunakan indeks.
## Soal Unguided 

### 1. Buatlah program menggunakan tipe data primitif minimal dua fungsi dan bebas.
Menampilkan program, jelaskan program tersebut dan ambil kesimpulan dari
materi tipe data primitif!


```C++
#include <iostream>

using namespace std;

// Fungsi untuk menghitung luas persegi
double hitungLuasPersegi(double sisi) {
    return sisi * sisi;
}

// Fungsi untuk menghitung volume tabung
double hitungVolumeTabung(double jari_jari, double tinggi) {
    const double PI = 3.14159;
    return PI * jari_jari * jari_jari * tinggi;
}

int main() {
    // Input untuk persegi
    double sisiPersegi;
    cout << "Masukkan panjang sisi persegi: ";
    cin >> sisiPersegi;

    // Hitung dan cetak luas persegi
    double luasPersegi = hitungLuasPersegi(sisiPersegi);
    cout << "Luas persegi: " << luasPersegi << endl;

    // Input untuk tabung
    double jariJari, tinggiTabung;
    cout << "Masukkan jari-jari tabung: ";
    cin >> jariJari;
    cout << "Masukkan tinggi tabung: ";
    cin >> tinggiTabung;

    // Hitung dan cetak volume tabung
    double volumeTabung = hitungVolumeTabung(jariJari, tinggiTabung);
    cout << "Volume tabung: " << volumeTabung << endl;

    return 0;
}
```
#### Output:
![image](https://github.com/suxeno/Struktur-Data-Assignment/assets/162097297/6294624a-22f3-4765-b8ca-154fb578813e)



Kode di atas digunakan untuk menghitung nilai dari volume tabugn dengan memasukkan jari-jari dan tinggi tabung.

#### Full code Screenshot:
![Screenshot 2024-03-09 154144](https://github.com/suxeno/Struktur-Data-Assignment/assets/162097297/d0a09226-4382-4a9a-af02-b73a1d48ab8b)
Dalam kode diatas menggunakan fungsi antara logika dengan memisahkan fungsi input output sehingga lebih mudah untuk dipahami. memasukkan data dengan cin dan memberikan hasil dengan cout.
kesimpulan dari materi tipe data primitif adalah tipe data yang sudah ada di pemprograman yang digunakan untuk membuat kode yang lebih kompleks.
### 2. Jelaskan fungsi dari class dan struct secara detail dan berikan contoh programnya
Class

```C++
#include <iostream>
using namespace std;

class Person {
    private:
        string name;
        int age;

    public:
        // Constructor
        Person(string n, int a) {
            name = n;
            age = a;
        }

        // Method untuk menampilkan informasi
        void displayInfo() {
            cout << "Name: " << name << endl;
            cout << "Age: " << age << endl;
        }
};

int main() {
    // Membuat objek dari class Person
    Person person1("John", 30);

    // Memanggil method untuk menampilkan informasi
    person1.displayInfo();

    return 0;
}


```
### Penjelasan Class dan Struct
Class adalah  tipe data mempunyai prototipe yang mendefinisikan variabel dari sebuah objek.beda class denga tipe lain yaitu tipe lain digunakan untuk mendeklarasikan variabel normal dan class digunakan utnuk mendeklarasikan variabel yagn berupa objek.
Struct adalah konstruksi dari bahasa pemprograman yaang memungkinkan untuk membuat tipe data beru dari yang terdiri dari sejumlah elemen yang berbeda
#### Output:
![Screenshot 2024-03-09 152146](https://github.com/suxeno/Struktur-Data-Assignment/assets/162097297/59b8cf4c-001f-459e-8e77-92c56d62c27d)
#### Full code Screenshot:
![Screenshot 2024-03-09 155238](https://github.com/suxeno/Struktur-Data-Assignment/assets/162097297/8237d6f2-23b2-4b0d-b2c0-efb137db4d29)

Struct
```C++
#include <iostream>
using namespace std;

struct Person {
    string name;
    int age;
};

int main() {
    // Membuat objek dari struct Person
    Person person1;
    person1.name = "Dina";
    person1.age = 12;

    // Menampilkan informasi
    cout << "Name: " << person1.name << endl;
    cout << "Age: " << person1.age << endl;

    return 0;
}
```
#### Output:
![Screenshot 2024-03-10 145118](https://github.com/RifkaASwasthi/Praktikum-Struktur-Data-Assignment/assets/162097297/5d04d881-f122-4518-a2d1-4e707338c09c)

#### Full code Screenshot:

![Screenshot 2024-03-10 145335](https://github.com/RifkaASwasthi/Praktikum-Struktur-Data-Assignment/assets/162097297/47a3e021-761e-477d-89d6-c23e29cc37de)

### 3. Buat dan jelaskan program menggunakan fungsi map dan jelaskan perbedaan dari
array dengan map.


```C++
#include <iostream>
#include <vector>
#include <algorithm>
#include <functional>

int main() {
    // Membuat vector
    std::vector<int> numbers = {1, 2, 3, 4, 5};

    // Menentukan angka untuk dikalikan
    int multiplier = 2;

    // Menggunakan fungsi map untuk mengalikan setiap elemen dengan multiplier
    std::transform(numbers.begin(), numbers.end(), numbers.begin(), std::bind(std::multiplies<int>(), std::placeholders::_1, multiplier));

    // Menampilkan hasil
    std::cout << "Hasil perkalian: ";
    for (const auto& num : numbers) {
        std::cout << num << " ";
    }
    std::cout << std::endl;

    return 0;
}
```
### Perbedaan Array dan Map
Array dalam mengakses menggunakan indeks sementara map dalam mengakses mengguanakan kunci
#### Output:
![Screenshot 2024-03-10 145603](https://github.com/RifkaASwasthi/Praktikum-Struktur-Data-Assignment/assets/162097297/d7d3372c-d96a-46ee-a637-d635c71593ac)




#### Full code Screenshot:
![Screenshot 2024-03-10 145650](https://github.com/RifkaASwasthi/Praktikum-Struktur-Data-Assignment/assets/162097297/622a67b2-d06b-4db1-81e2-99fc2805fa9b)

program diatad adalah contoh dari map dimana dalam mnegakses dibtuthlan kunci std::

## Kesimpulan
Dari berbagai tipe data yang sudah dipelajari mempunyai fungsi masing-masing seperti dalam penggunaanya tipe data abstrak yang lebih efektif jika digunakan untuk membuat obyek baru tanpa susah untuk menginput satu persatu data, tinggal disesuaikan dengan data yang dimiliki kemudian meneksekuisi sesuai dengan kode yang dibutuhkan. 

## Referensi
[1] dwitha fajri,2017, "LAPORAN PRAKTIKUM I
TIPE DATA PRIMITIF, ABSTRAK DAN KOLEKSI",MALANG,academia.edu.