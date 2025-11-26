## std::fixed, std::setprecision, liczba pi

- `std::fixed` i `std::setprecision` zmieniają ilość liczb po przecinku do pokazania, dla typów float a double.
- `std::cout << std::fixed << std::setprecision(2)` powoduje, że pokazanie liczb jak '3.141' będzie skrucone do 2 liczb po przecunku, czyli '3.14'

Przykład:
```
#include <iostream>
#include <iomapip> // dla std::fixed i std::setprecision

int main() {
  double pi = 3.14159265359;
  std::cout << "pi: " << pi << "\n";
  std::cout << std::fixed;
  std::cout << std::setprecision(3);
  std::cout << "pi (3): " << pi << "\n";
}
```
Output (co powinno być pokazane w cmd):
```
pi: 3.14159265359
pi (3): 3.141
```

---

### Sposoby użycia liczby pi:
1. 

---

Jakieś zadania:
0. skopiować przykład i zobaczyć co można zmienić
1. zapisz liczbe zabraną od użytkownika, i pokaż ją do precyzji 4 liczb po przecinku.
2. pokaż wynik mnożeni `pi * pi * pi` do 5 miejsc po przecinku
