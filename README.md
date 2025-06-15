Nama kelompok

      Nama-nama member 
      
1. Alfiyana Fadillah Ashari - 241401024
2. Cindy Aulia - 241401033
3. Jeconia Farica sirotus - 2414o1108
4. Kayla Andhara - 241401081
5. Olivia Gabriela Silitonga - 241401051
   

      Our Program ->  " TEBAK ANGKA "


#include <iostream>
#include <cstdlib>  // Untuk rand() dan srand()
#include <ctime>    // Untuk time()

using namespace std;

int main() {
    srand(static_cast<unsigned int>(time(0)));
    int angka_rahasia = rand() % 100 + 1; 
    int tebakan;
    int max_kesempatan = 10;

    cout << "===============================" << endl;
    cout << "  Game Tebak Angka (1 - 100)   " << endl;
    cout << "  Kamu punya 10 kesempatan     " << endl;
    cout << "===============================" << endl;

    for (int i = 1; i <= max_kesempatan; i++) {
        cout << "\nTebakan ke-" << i << ": ";
        cin >> tebakan;

        if (tebakan == angka_rahasia) {
            cout << " Selamat! Tebakan kamu benar!" << endl;
            return 0;
        } else if (tebakan > angka_rahasia) {
            cout << "Angka terlalu besar.";
        } else {
            cout << "Angka terlalu kecil.";
        }

        if (i < max_kesempatan) {
            cout << " Sisa kesempatan: " << (max_kesempatan - i) << endl;
        } else {
            cout << "\n Kesempatan habis. Angka yang benar adalah: " << angka_rahasia << endl;
        }
    }

    return 0;
}

Untuk s
