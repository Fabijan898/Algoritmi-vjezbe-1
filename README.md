# Algoritmi-vjezbe-1
#include <iostream>
#include <stdlib.h>
#include <cmath>
#include <string>
#include <algorithm>

using namespace std;

//int main()
//Binarno pretrazivanje
/* {
    int a[] = { 1,2,3,4,5,6,7,8,9,10 };
    int trazeni_broj = 1;
    int gornja, donja, sredina, index;
    gornja = 0;
    donja = trazeni_broj;
    index = -1;
    while (gornja <= donja)
    {
        sredina = gornja + (donja - gornja) / 2;
        if (a[sredina] == trazeni_broj)
        {
            index = sredina;
            break;
        }
        else if (a[sredina] < trazeni_broj)
        {
            gornja = sredina + 1;

        }
        else
        {
            donja = sredina - 1;
        }
    }
    if (index != -1)
    {
        cout << "broj " << trazeni_broj << " =1" << endl;
    }
    else
    {
        cout << "broj " << trazeni_broj << " =0" << endl;
    }
    cout << endl << endl;
}
*/
//Dijagonale
/* {
    {
        int polje[10][10];
        cout << "   nesortirano  " << endl;
        for (int i = 0; i < 10; i++) {
            for (int j = 0; j < 10; j++) {
                polje[i][j] = rand() % 10;
                cout << polje[i][j] << " ";
            }
            cout << endl<<endl;
        }
        for (int i = 0; i < 9; i++) {
            for (int j = 0; j < 9; j++) {
                if (polje[j][j] > polje[j + 1][j + 1]) {
                    int temp = polje[j][j];
                    polje[j][j] = polje[j + 1][j + 1];
                    polje[j + 1][j + 1] = temp;
                }
            }
        }
        for (int i = 0; i < 9; i++) {
            int min = i;
            for (int j = i + 1; j < 10; j++) {
                if (polje[j][9 - j] < polje[min][9 - min]) {
                    min = j;
                }
            }
            int temp = polje[i][9 - i];
            polje[i][9 - i] = polje[min][9 - min];
            polje[min][9 - min] = temp;
        }
        cout << endl << "    sortirano  " << endl;
        for (int i = 0; i < 10; i++) {
            for (int j = 0; j < 10; j++) {
                cout << polje[i][j] << " ";
            }
            cout << endl<<endl;
        }
        return 0;
    }


}*/
// Nesortirano polje u kojemu se traži nalazili se taj broj u njemu
    /* {
        int a[]={4,2,7,1,5,9,6,8 };
        int trazeni_broj = 10;
        int veličina_polja = 8;

        bool traži = false;

        for (int i = 0; i < veličina_polja; ++i) {
            if (a[i] == trazeni_broj) {
                traži = true;
                break;
            }
        }

        if (traži) {
            std::cout << "broj " << trazeni_broj << " = 1 " << std::endl;
        }
        else {
            std::cout << "broj " << trazeni_broj << " = 0 " << std::endl;
        }
        cout << endl << endl;

        return 0;
    }*/
    //Selection sort
    /*{
        int a[] = { 9,2,4,8,1,3 };
        int veličina_polja = 6;

        for (int i = 0; i < veličina_polja - 1; i++) {
            int min = i;

            for (int j = i + 1; j < veličina_polja; j++) {
                if (a[j] < a[min])
                    min = j;
            }
            int temp = a[min];
            a[min] = a[i];
            a[i] = temp;
        }


        for (int i = 0; i < veličina_polja; i++) {


            cout << a[i] ;
        }
        cout << endl << endl;
        return 0;
    }*/
    //Bubble sort
     /*{
        int a[] = { 6,8,4,3,6};
        int veličina_polja= 5;

        for (int i = 0; i < veličina_polja - 1; i++) {
            for (int j = 0; j < veličina_polja - i - 1; j++) {
                if (a[j] > a[j + 1]) {

                    int temp = a[j];
                    a[j] = a[j + 1];
                    a[j + 1] = temp;
                }
            }
        }


        for (int i = 0; i < veličina_polja; i++)
           cout << a[i] ;

        return 0;
    }*/
    //Sortiranje parnih od manjeg do većeg i neparnih od većeg do manjeg
 /* {
            int a[] = {8,4,6,2,3,11,5,7 };
            int veličina_polja = 8;

            for (int i = 0; i < veličina_polja - 1; i++) {
                for (int j = 0; j < veličina_polja - i - 1; j++) {
                    if (a[j] % 2 == 0 && a[j + 1] % 2 == 0 && a[j] > a[j + 1]) {

                        int temp = a[j];
                        a[j] = a[j + 1];
                        a[j + 1] = temp;

                    }
                }

            }

            for (int i = 0; i < veličina_polja - 1; i++) {
                for (int j = 0; j < veličina_polja - i - 1; j++) {
                    if (a[j] % 2 != 0 && a[j + 1] % 2 != 0 && a[j] < a[j + 1]) {

                        int temp = a[j];
                        a[j] = a[j + 1];
                        a[j + 1] = temp;
                    }
                }
            }


            for (int i = 0; i < veličina_polja; i++)
                cout << a[i] ;

            return 0;
        }

}*/
// Sortiranje polja od većeg do manjeg i obrnuto
/*{
    const int red  = 3;
    const int stupac = 5;
    int a[red][stupac] = {
        {3,1,5,7,8},
        {5,8,22,3,6,},
        {3,7,9,11,56}
    };
    for (int i = 0; i < stupac - 1; i++) {
        for (int j = 0; j < stupac - i - 1; j++) {
            if (a[0][j] < a[0][j + 1]) {
                int temp = a[0][j];
                a[0][j] = a[0][j + 1];
                a[0][j + 1] = temp;
            }
        }
    }
    for (int i = 0; i < stupac - 1; i++) {
        for (int j = 0; j < stupac - i - 1; j++) {
            if (a[1][j] > a[1][j + 1]) {
                int temp = a[1][j];
                a[1][j] = a[1][j + 1];
                a[1][j + 1] = temp;
            }
        }
    for (int i = 0; i < red; i++) {
        for (int j = 0; j < stupac; j++) {
            cout << a[i][j] ;
        }
        cout << endl;
    }

    return 0;
}*/
// za unesene sate minute i sekunde ispise ukupne sekunde

/*

    int sekunde(int a, int b, int c)
    {

        int ukupne_vrijeme_u_sekundama=((a * 3600) + (b * 60) + c);
        return ukupne_vrijeme_u_sekundama;

    }

    int main()
    {
        int sat, min, sec;

        cout << "Unesite sate ";
        cin >> sat;

        cout << "Unesite minute ";
        cin >> min;

        cout << "Unesite sekunde ";
        cin >> sec;

       int ukupne_vrijeme_u_sekundama = sekunde(sat, min, sec);

        cout << ukupne_vrijeme_u_sekundama << endl;

        return 0;
    }
    */
    //vrati jeli broj parni

  /** bool parni_broj(int a)
{
    if (a % 2 == 0)
        return 1;
    else
        return 0;
}

int main()
{
    int a;
    cin >> a;
    cout << parni_broj(a) << endl;
    return 0;
}*/
// vrati jeli broj prosti
/*bool prosti(int a) {
    if (a % 2 == 1)
        return 1;
    else if (a == 2)
        return 1;
    else
        return 0;


}
int main()
{
    int a;
    cin >> a;
    cout << prosti(a) << endl;
    return 0;
}*/
// vrati jeli broj veći od 0
/*bool većiodnula(int a) {
    if (a > 0)
        return 1;
    else
        return 0;
}
int main()
{
    int a;
    cin >> a;
    if (većiodnula(a))
        cout << "broj " << a << " je veci on nula";
    else
        cout << "broj " << a << " je manji od nula";
    return 0;
}*/
//vrati jeli znak slovo
/*
bool slovo(char znak) {
    if ((znak >= 'a' && znak <= 'z') || (znak >= 'A' && znak <= 'Z'))
        return 1;
    else
        return 0;

}
int main()
{
    char znak;
    cin >> znak;
    cout << slovo(znak);
    return 0;
}
*/
// ciklički vezano
/*
char sljedeceslovo(char a,int b){
    int is = a;
    is = is - 'a';
    is += b;
    is = is % 26;
    is = is + 'a';
    return is;

}
int main()
{
    char a;
    cin >> a;
    cout << sljedeceslovo('g',233);
    return 0;
}*/
//ispiše sve proste broje u nekom intervalu brojeva
/*
    bool prosti(int a){
        bool p = true;
        for (int i = 2; i < a; i++)
            if (a % i == 0)
                p = false;
        return p;
}


void ispissvihprostih(int a, int b) {
    for (int i = a; i <= b; i++)
        if (prosti(i)) {
            cout << i;
       }

}
int main()
{
    int a, b;
    cin >> a >> b;
   ispissvihprostih(a,b);
    return 0;
}
*/
// jeli uneseno slovo veliko
/*
bool veelikoslovo(char a)
{
    if (a >= 'A' && a <= 'Z')
        return 1;
    else
        return 0;
}
int main()
{
    char a;
    cin >> a;
    cout << veelikoslovo(a);
    return 0;
}*/


// ispisuje samoglasnike ako se unese suglasnik trazi ponovni unos
/*bool slovo(char a) {
    if (a == 'a' || a == 'e' || a == 'i' || a == 'o' || a == 'u' || a == 'A' || a == 'E' || a == 'I' || a == 'O' || a == 'U')
        return 1;
    else
        return 0;
}
int main()
{
    char a;
    bool samoglasnik = false;
    while (!samoglasnik) {
        cin >> a;
        if (slovo(a)) {
            samoglasnik = true;// ==0 ako ocemo sam suglasnike
            cout << "slovo je samoglasnik";

        }
        else {
            cout << "slovo je suglasnik unesi ponovo";
        }
    }
    return 0;
}*/
// određuje na kojem mjestu se nalazi slovo u abecedi
/*int mjesto(char a) {
    if(a>='a'&&a<='z')
        return  a - 'a' + 1;
    else
        return -1;
}
int main()
{
    char a;
    cin >> a;
    cout << mjesto(a);
    return 0;
}*/
// vrati jesu li apsolutne vrijednosti iste
/*bool apsolutne_vrijednosti(int a, int b)
{
    if (abs(a) == abs(b))
        return 1;
    else
        return 0;
    }
int main()
{
    int a, b;
    cin >> a >> b;
    cout << apsolutne_vrijednosti(a, b);
    return 0;
}*/
// vrati zbeoj znamenaka broj
/*int zbroj_znamenik(int a)
{
    int brZnm = 0;
    while (a > 0) {
        brZnm += a % 10;
       a = a / 10;
    }
    return brZnm;
    }
int main()
{
    int a;
    cin >> a;
    cout << zbroj_znamenik(a);
    return 0;
}*/
//vrati broj zanmennki
/*
int vartibroj(int a) {
    int b = 0;
    while (a > 0)
    {
        a = a / 10;
        b++;
    }
    return b;

}
int main()
{
    int a;
    cin >> a;
    cout << vartibroj(a);
    return 0;

}*/
//jednaki su ako su zbroj znamenki jednaki ako nisu onda nisu jednaki
/*int zbroj_znamenik(int a)
{
    int brZnm = 0;
    while (a > 0) {
        brZnm += a % 10;
        a = a / 10;
    }
    return brZnm;
}
bool jednak(int a, int b) {
    return (zbroj_znamenik(a) == zbroj_znamenik(b));

}
int main()
{
    int a, b;
    cin >> a >> b;
    if (jednak(a, b))
    {
        cout << "brojevi su jednaki";
   }
    else {
        cout << "brojevi nisu jednaki";
    }
    return 0;
}*/
//vrati jeli trokut pravokutan
/*int trokut(int a, int b, int c) {
    if (a * a + b * b == c * c || a * a + c * c == b * b || b * b + c * c == a * a)
        return 1;
    else
        return 0;
}
int main()
{
    int a, b, c;
    cin >> a >> b >> c;
    cout << (trokut(a, b, c));
    return 0;
}*/
// vrai povrsinu upisane kruznice
/*int povrsinupisanog(int a, int b)
{

        int dijagonala = static_cast<int>(sqrt(a * a + b * b));
        int radius = dijagonala / 2;
        int povrsina = 3 * radius * radius;

        return povrsina;

}
int main()
{
    int a, b;
    cin >> a >> b;
    int povrsina = povrsinupisanog(a, b);
    cout << povrsina;
    return 0;
}*/
//vrati to samo za opisanu

/*int povrsinupisanog(int a, int b)
{

    int dijagonala = static_cast<int>(sqrt(a * a + b * b));
    int radius = dijagonala / 2;
    int povrsina = 4 * radius * radius;

    return povrsina;

}
int main()
{
    int a, b;
    cin >> a >> b;
    int povrsina = povrsinupisanog(a, b);
    cout << povrsina;
    return 0;
}*/
//mini kalkulator
/*int izracunaj(int operand1, int operand2, char operacija) {
    int rezultat;
    switch (operacija) {
    case '+':
        rezultat = operand1 + operand2;
        break;
    case '-':
        rezultat = operand1 - operand2;
        break;
    case '*':
        rezultat = operand1 * operand2;
        break;
    case '/':
        if (operand2 != 0) {
            rezultat = operand1 / operand2;
        }
        else {
            rezultat = 0;
        }
        break;
    default:
            cout <<  operacija ;
        rezultat = 0;
        break;
    }
    return rezultat;
}

int main() {
    int operand1, operand2;
    char operacija;

    cin >> operand1 >> operand2 >> operacija;

    int rezultat = izracunaj(operand1, operand2, operacija);

    cout << rezultat ;

    return 0;
}
*/
// binarni u dekatski
/*void dekadski_binarni(int broj) {
    if (broj == 0) {
        return;
    }

    int binarni[32];

    int indeks = 0;
    while (broj > 0) {
        binarni[indeks] = broj % 2;
        broj /= 2;
        indeks++;
    }

    if (indeks == 0) {
        return;
    }

    for (int i = indeks - 1; i >= 0; i--) {
        cout << binarni[i];
    }

}

int main() {
    int dekadskiBroj;

    cin >> dekadskiBroj;

    dekadski_binarni(dekadskiBroj);

    return 0;
}*/
//sekunde u sve ostalo
/*void pretvoriSekunde(int Sekunde, int& sati, int& minute, int& sekunde) {
    sati = Sekunde / 3600;
    Sekunde %= 3600;
    minute = Sekunde / 60;
    sekunde = Sekunde % 60;
}

int main() {
    int Sekunde, sati, minute, sekunde;
    cin >>Sekunde;
    pretvoriSekunde(Sekunde, sati, minute, sekunde);
    cout  <<  sati   <<  minute  <<  sekunde  ;
    return 0;
}*/


//računa površinu kružnog isječka
/*int stupnjeviURadijane(int stupnjevi) {
    return (stupnjevi * 22) / 7;

}
int povrsinaKruzniIsjecak(int centralniKut, int radijus) {
    int theta = stupnjeviURadijane(centralniKut);
    return (theta * radijus * radijus) / 360;
}

int main() {
    int centralniKut, radijus;
   cin >> centralniKut>> radijus;
    int povrsinaIsjeka = povrsinaKruzniIsjecak(centralniKut, radijus);
    cout << povrsinaIsjeka  ;
    return 0;
}*/


// ispiše slova od kud mu zadam do kud ma zadam da završi
/*void ispisiAbecedu(char pocetak, char kraj) {
    if (pocetak < 'a' || pocetak > 'z' || kraj < 'a' || kraj > 'z') {
        return;
    }
    for (char c = pocetak; c <= kraj; c++) {
       cout << c ;
    }
}

int main() {
    char pocetak, kraj;
    cin >> pocetak >> kraj;
    ispisiAbecedu(pocetak, kraj);
    return 0;
}*/
//ispise unesenu recenicu do \0
/*
int main() {
    char polje[20];
    gets_s(polje);
    for (int i = 0; polje[i] != '\0'; i++)
        cout << polje[i];
    return 0;
}*/
// ispise broj rijeci u  recenici
/*
int main() {
    int br = 0;
    char polje[100];
    gets_s(polje);

    for (int i = 0; polje[i] != '\0'; i++) {
        if (polje[i] == ' ')
            br++;
    }

    cout << br ;

    return 0;
}*/

//kod provjeri jeli recenica ispravno napoisana
/*
int main() {
    char polje[100];
    int i;
    gets_s(polje);


    bool poljei = true;


    for (i = 0; polje[i] != '\0'; i++) {

        if (i == 0 && polje[i] >= 'a' && polje[i] <= 'z') {
            poljei = false;
            break;
        }


        if (polje[i] == '.' && polje[i + 1] == ' ') {
            i += 2;
            if (polje[i] >= 'a' && polje[i] <= 'z') {
                poljei = false;
                break;
            }
        }


    }


    if (poljei) {
        cout << "Recenica je  ispravna" ;
    }
    else {
        cout << "Recenica nije ispravn" ;
    }

    return 0;
}*/
// ispise jeli recenica anagram broj slova i jeli simedricna anavolimilovana
/*
bool isAnagram(const string& recenica) {
    string obrnuta_recenica = recenica;
    reverse(obrnuta_recenica.begin(), obrnuta_recenica.end());
    return recenica == obrnuta_recenica;
}

int main() {
    string recenica;
    getline(cin, recenica);

    if (isAnagram(recenica)) {
        cout << "Rečenica je anagram  " ;
    }
    else {
        cout << "Rečenica nije anagram  " ;
    }

    int broj_slova = recenica.length();
    cout << broj_slova << endl;

    bool simetricna = true;
    for (int i = 0; i < broj_slova / 2; i++) {
        if (recenica[i] != recenica[broj_slova - i - 1]) {
            simetricna = false;
            break;
        }
    }

    if (simetricna) {
        cout << "Rečenica je simetrična" ;
    }
    else {
        cout << "Rečenica nije simetrična" ;
    }

    return 0;
}
*/
//povrsina pravokutnika
/*
int povrsina(int a, int b) {
    int P;
    P = a * b;
    return P;
}
int main() {
    int a, b;
    cin >> a >> b;
    cout << povrsina(a,b);
    return 0;
}*/
// nađe broji različitih slova u riječi
/*
int brojslova(string recenica) {
    int brojac = 0;
    int i = 0;

    while (recenica[i] != '\0') {
        char znak = recenica[i];
        if ((znak >= 'a' && znak <= 'z') || (znak >= 'A' && znak <= 'Z')) {
            bool ima = false;
            int j = 0;
            while (j < i) {
                if (recenica[j] == znak || recenica[j] == znak + 32 || recenica[j] == znak - 32) {
                  ima = true;
                    break;
                }
                j++;
            }
            if (!ima) {
                brojac++;
            }
        }
        i++;
    }

    return brojac;
}

int main() {
    string recenica;
    cin >> recenica;
    cout<<brojslova(recenica);
    return 0;
}
*/
