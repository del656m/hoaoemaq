
- funkcje usuwają repetycje w kodzie.
Przykład:
```
#include <iostream>

int err(int id) {
  std::cout<<"Error with id "<<id<<"\n";
  std::cout<<" more info\n";
  return id % 0b1000;
}

int main() {
  if (true) {
    int ret = err(0x10F)
    return ret;
  }

  return 0;
}
```
Wyjaśnienie:
- `int err(` - start definicji funkcji, `int` to typ danych, która funckja zwraca (`void` gdy niemają zostać zwrócone żadne dane). `err` to nazwa funkcji, tak samo jak zanwy zmiennych mogą być nazwane jak sie chce.
- `(int id)` - parametry funckji, czyli dane do których funkcja ma dostęp.
- `{...}` - kod funckji
- `return ...;` - zwrócenie liczby z funckji, po użyciu return funkcja zakończy swoje działanie, i odda kontrole funkcji, która ją użyła
- `return id % 0b1000;` - przykładowa kalkulacja, wynik modulo pomiędzy `id` a liczbą 8 (1000 w systemie binarnym)
- `int main` - funckja od kturej program zaczyna, zwraca ona integer, nie bierze parametrów.
- `if (true)` - przykład, żeby funkcja `err` zawsze była używana przez ten program.
- `int ret = err(0x10F)` - przykładowe użycie stworzonej funkcji, (argument kiedy używa się funckji, parametr kiedy sie ją definiuje, ale są tym samym) jako argument bierze przykładową liczbę 10F w systemie hex. Rezultat funkcji jest zapisywany do zmiennej `ret`.
- można byłoby również napisać `return err(0x10F);` zamiast dwuch linijek.
- zmienne nie są dostępne pomiędzy funkcjami

Przykład 2:
```
#include <iostream>

int something(int a, int b) {
  return a+(b*2);
}

int main() {
  int x = 0;
  int y = 6;
  int a = something(x, y);
  int b = something(y, a)
  int c = a+something(x, b)
  std::cout << "c="<<c<<"\n";
}
```

Przykład 3:
```
#include <iostream>

int fib(int n) {
  if (n<=1) return n;
  return fib(n-1)+fib(n-2);
}

int main() {
  for (int i = 0; i < 10; i++) {
    std::cout << "fib("<<i<<") = "<<fib(i)<<"\n";
  }
}
```
Wyjaśnienie:
- `int fib(int n)` to znana w programowaniu matematyczna funkcja "Fibonacci". Wyjaśnienie czym ona jest, można zobaczyć z kodu lub (lepiej) w google.
- `if (n<=) return n;` liczby 0 i 1 zwracają siebie.
- `return ...` - używanie funkcji fib w sobie, nie jest to polecane gdy jest ona używana dużo, ale i tak można.
- `for (int i ...` - pętla, która wyliczy fib dla n od 0 do 9.
- `std::cout<< ...` - liczy i wyświetla wynik

Zadania:
1. program, który
- od użytkownika zabiera 5 liczb typu double.
- dla kazdej kombinacji z nich, liczy ich: dodawanie, odejmowanie, mnożenie, dzielenie, modulo, potęga, pierwiastek ich sum, logarytm o podstawie 2 z ich sum.
- kombinacje: 25 - aa, ab, ac, ad, ae, ba, bb, bc, bd, be, ca, cb, cc, cd, ce, da, db, dc, dd, de, ea, eb, ec, ed, ee
- użyj funkcji, bez kopiowania kodu 25 razy, ale wykonanie funkcji 25 razy jest dozwolone
- wszystkie 5 liczb można albo ustawić samemu, albo losowo
2. zadanie pierwsze, ale użyj array jako liczby, ilość liczb powinna być możliwa do zmienienia jedną linijką, np. `const int NUMBERS = 7;`, wraz z słowem `const`, i `int nums[NUMBERS]`.
3. funkcja która zwróci losową liczbe, i automatycznie użyje srand oraz rand.
