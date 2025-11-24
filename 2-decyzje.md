## Instrukcje warunkowe w C++

**if … else**  
**switch … case**

Instrukcja **if else** sprawdza, czy coś jest równe `true`, czyli czy jest prawdziwe.  
Przykład:

``` 
int number = 82;
if (number == 82) {
  std::cout << "Liczba jest równa 82\n";
} else {
  std::cout << "Liczba nie jest równa 82\n";
}
```

Instrukcja **switch** sprawdza, czy zmienna jest równa wartości.  
Głównie używana, gdy możliwych wartości jest dużo (np. 10).  
Krótki przykład:

```
int option = /* jakaś liczba z cmd */;
switch (option) {
  case 1:
    std::cout << "Opcja 1\n";
    break;
  case 2: {
    std::cout << "Opcja 2\n";
    break;
  }
  default:
    std::cout << "Opcja ?\n";
    break;
}
```

Przykładowy program 1 (bez `using namespace std`):  
Dla trzech boków trójkąta (a, b, c) sprawdza, czy tworzą trójkąt prostokątny.

``` 
#include <iostream>
#include <conio.h>

int main() {
  int a, b, c;
  std::cout << "Podaj bok a: ";
  std::cin >> a;
  if (a <= 0) {
    std::cout << "Bok a jest <= 0\n";
    return -1;
  }
  std::cout << "Podaj bok b: ";
  std::cin >> b;
  if (b <= 0) {
    std::cout << "Bok b jest <= 0\n";
    return -1;
  }
  std::cout << "Podaj bok c: ";
  std::cin >> c;
  if (c <= 0) {
    std::cout << "Bok c jest <= 0\n";
    return -1;
  }
  
  // twierdzenie Pitagorasa
  if ((a*a + b*b) == (c*c)) {
    std::cout << "Boki tworzą trójkąt prostokątny.\n";
  } else {
    std::cout << "Boki nie tworzą trójkątu prostokątnego\n";
  }
  return 0;
}
```

Można pozmieniać parę rzeczy w programie i zobaczyć, co się zmieni, jeśli czegoś się trochę nie rozumie.

---

# Zadania 2:

1. Napisz program, który:  
- Ma zmienne `a`, `b` i `c` (`a` nie może być równe 0) jako `double`  
- Oblicza deltę (`b*b - 4*a*c`)  
- Jeśli delta jest mniejsza od zera, równanie nie posiada pierwiastków rzeczywistych.  
- Jeśli delta jest równa 0, jest to pierwiastek podwójny (tylko `x1`).  
- Jeśli delta jest większa od 0, posiada `x1` i `x2`.  
- Wyświetl `x1` i `x2` wszędzie do dwóch miejsc po przecinku.
- Wzory:
- dla podwójnego pierwiastka:  
  `x1 = -b / (2 * a);`  
- dla dwóch pierwiastków:  
  `x1 = (-b - √delta) / (2 * a);`  
  `x2 = (-b + √delta) / (2 * a);`
Wyświetl `x1` i `x2` wszędzie do dwóch miejsc po przecinku.  
<details>
<summary>Wskazówki</summary>

- Sprawdź, czy `a == 0`  
- Sprawdź deltę:  
  `if (delta < 0) {...} else if (delta == 0) {...} else {...}`  
- Pierwiastek z delty: `std::sqrt(delta)`  
- Wyświetlanie do dwóch miejsc po przecinku:  
  `std::cout << std::fixed << std::setprecision(2);`  

</details>
Przykłady:  
- `a = 1, b = 5, c = 4` -> `x1 = -4, x2 = -1`  
- `a = 1, b = 4, c = 4` -> pierwiastek podwójny: `-2`  
- `a = 1, b = 2, c = 3` -> trójmian nie ma pierwiastków rzeczywistych.

---

2. Napisz program, który używając `switch`:  
- oblicza pierwiastki równania kwadratowego (to samo co wcześniej, ale z `switch`)  

<details>
<summary>Wskazówki</summary>

Ustaw zmienną `lp` w zależności od delty:  
``` 
int lp = 0;if (delta<0){lp=0;}else if(delta==0({lp=1;}else{lp = 2;}
``` 
Następnie użyj `switch` na `lp` tak jak w przykładzie na początku.

</details>

---

3. Napisz program, który:  
- Ma wartości `a`, `b`, `c` typu `double`.  
- Przekształca równanie `ax + b = c` tak, aby obliczyć `x`.  
- Oblicza `x`.  
- Wyświetla wszystkie 4 zmienne z precyzją do dwóch miejsc po przecinku.  

<details>
<summary>Wskazówka</summary>

`x = (c - b) / a;`

</details>

---

4. Napisz program, który:  
- generuje losową liczbę od 0 do 9, którą użytkownik zgaduje.  

<details>
<summary>Wskazówki</summary>

Dodaj do includes:  
`#include <random>`  

Przykład generowania:  
``  
std::random_device rd;  
std::mt19937 gen(rd()); // metoda losowania  
std::uniform_int_distribution<> dist(0, 9); // zakres 0-9  
int wylosowana = dist(gen); // losowanie liczby  
