## std::cout, std::cin, float, double, int

- trzeba przeczytać całość żeby to zrozumieć, nie pominonć wszystko i odrazu do zadań

---

- bez używania `using namespace std` przed wszystkim co pochodzi od std, trzeba dodać `std::` (zamiast `cout` będzie `std::cout`, ale np. `float` sie nie zmieni)
- `std::cout` wyświetla tekst to okna cmd.
przykład: `std::cout << "Wiadomość\n"`
- `\n` jako tekst oznacza znak `Enter` (nowa linia)
- tekst musi zaczynać i kończyć się znakiem `"`
- `std::cout` używa się przez dodanie do niego elementów znakami `<<`, można do niego dodawać nie tylko tekst, a równierz wiele wodzajów liczb.

### Przykład 1:
```
// iostream daje nam dostęp do std::cout
#include <iostream>

// często `int main() {}` uznacza miejsce, kiedy kod się rozpocznie
int main() {
  // wyświetla wiadomość
  std::cout << "Hello, World\n";
}
```

### Przykład 2 (z błędem):
```
#include <iostream>

int main() {
  std::cout << "Informacja pierwsza";
  std::cout << "Informacja druga";
}
```
bez znaków `\n` tekst zostanie wyświetlony w tej samej lini

---

- `int` to liczba całkowita (np. -40, 37914, 1), nie może być to np. 1,5
- `float` to liczba rzeczywista (np. 1,5; 25; 0.01; 100.95) z dokładnością do około 7 liczb (całkowitych i po przecinku)
- `double` jest podobna do float, tylko z większą dokładnością (około 15-17 liczb)
- limit liczb float i double może być większy od 7 lub 17, traci on tylko dokładność.

Przykład 3:
```
#include <iostream>

int main() {
  // n1 n2 i n3 to nazwy, które można zmieniać
  int n1 = 25;
  float n2 = 4.5;
  double n3 = 1234.5678;
  // wyświetl wszystkie liczby w oknie cmd
  std::cout << "liczba 1: "<<n1<<"\n";
  std::cout << "liczba 2: "<<n2<<"\n";
  std::cout << "liczba 3: "<<n3<<"\n";
  // każdą z tych lini można rozłożyć w taki sposób:
  std::cout << "liczba 1: "; // pierwsza informacja jako tekst
  std::cout << n1; // wyświetlanie liczby zapisanej w n1
  std::cout << "\n"; // znak nowej linii, żeby kolejny komunikat nie połączył się z tym
  // lepiej jest jednak połączyć je w większe fragmenty, żeby kod był bardziej czytelny
  // zmienianie liczby pierwszej na sume wszystkich liczb
  n1 = n1+n2+n3;
  std::cout << "nowa liczba 1: " << n1 << "\n";
  // n1 powinno zawierać liczbe 1264 albo podobną, ponieważ n1 to liczba całkowita (int)
  // suma liczb, ale jako liczba rzeczywista
  double sum = n1+n2+n3;
  std::cout << "suma: " << sum << "\n";
}
```
Po uruchomieniu tego kodu powinno pojawić się:
```
liczba 1: 25
liczba 2: 4.5
liczba 3: 1234.5678
liczba 1: 25
nowa liczba 1: 1264
suma: 1264.0678
```
Pokazanie drugo raz liczby 1 jako `25` to ta dłuższa wersja, a `nowa liczba 1` to suma liczb n1 n2 n3 jako liczba całkowita.

- jeśli zdefiniowało się jakąc zmienną (np. `int test`), nie można jej zdefiniować ponownie (każde `float test`, `int test`, lib z jakimkolwiek innym typem danych poprostu da błąd.

---

- `std::cin` jest używane do zabrania liczby od użytkownik.
- używa się znaków `>>` (od), nie `<<` (do).
przykład:
```
float number;
std::cout << "Liczba: ";
std::cin >> number;
std::cout << "Wprowadzono liczbe: "<<number<<"\n";
```
Wyjaśnienie przykładu:
- `float number;` muwi c++, że ma stworzyć coś o nazwie `number` i o typie `float`, która ma być pusta
- `std::cout << "Liczba: "` wyświetla komunikat dla użytkownika że może wpisać liczbe. Jest to opcjonalne ale lepiej to mieć.
- `std::cin >> number` czeka na to, aż użytkownik wpisze liczbe do okna cmd, i tą liczbe wkłada do `number`
- `std::cout ` wyświetla tą liczbe

---

Jakieś zadania:

0. jeśli coś jest niezrozumiałe, można zobaczyć w google (ChatGPT albo inne ai lub edge lepiej nie)

0. skopiować przykłady, zobaczyć co można zmienić i co to zrobi. również jakie błędy co oznaczają.

1. wyświetl dowojny tekst składający się z 3 linii, używając jednego std::cout. (znaku `\n` nie trzeba używać tylko na koncu tekstu)
2. wyświetl mnożenie liczb 4.5 i 21 jako liczba całkowita
3. wyświetl mnożenie liczb, gdzie pierwsza i druga liczba są zabrane od użytkownika
4. oblicz x=a+(b/2)+(c*2). liczby `a`, `b` i `c` powinny być wpisane przez użytkownika. wszystkie liczby powinny być rzeczywiste, ilość precyzji niejest tu ważna.

jakieś problemy albo coś to ja mam dużo wolnego czasu, można jakoś napisac to odpisze jak bende mugl
