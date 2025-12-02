## `if`, `else if`, `else`

- dokra wiadomość, można po tym zrobic to menu wyboru
- trzeba rozumiec typ boolean żeby cokolwiek zrobić
- if robi coś jeśli coś jest true (siem, bardzo pomocne)
- if, umożliwia wykonywanie kodu, jeśli podana wartość bool jest równa `true`
Przykład (jeśli 2 liczby są równe, coś zrub):
```cpp
float num1 = 42;
float num2;
std::cout << "Liczba: ";
std::cin >> num2;
if (num1 == num2) {
  std::cout << "abc\n";
  std::cout << "123\n";
}
```
Wyjaśnienie:
- jeśli niewiesz co robi cout lub cin, to niewiem co robisz w if, lepiej przeczytać i zrozumieć to co jest a `1-printing-variables.md`
- `if (num1 == num2)` - if znaczy jeżeli. `==` znaczy czy są równe. w połączeniu: `jeżeli są równe`. to tyle.
- if potrzebuje wiedziec to wtedy ma zrobić jak to co znajdule sie w `()` jest true. żeby mu to powiedzieć, wszystko co się ma wtedy stać musi być w znakach `{}`. to jest dokładnie tak samo jak w `int main()`, te same znaki muwią co ma robić. tylko że w int main jest to informacja gdzie jest kod, a w if jest to, co zrobic.
- w tym przypadku, jeżeli num1 jest równe num2, c++ wykona wszystkie instrukcje pomiędzy znakiem `{` a `}`. Jeśli jednego z tych znaków nie znajdzie.

- `else` to informacja dla `if`a, muwiąca co zrobić jeśli wartość zawarta w ifie syniosła false, czyli pierwszy blok kodu nie został wykonany.
Przykład:
```cpp
if (9+10 == 21) {
  std::cout << "Was?\n";
} else {
  std::cout << "9+1 nie jest równe 21\n";
}
```
- jest to dość prosty przykład który zawsze wykona ten drugi blok kodu ktury nalezy do ifa.
- `else` wpisuje się po ifie, najczęściej odrazu po znaku `}`, nigdy nie przed.

- ostatnie jest `else if`. Bez niego byłoby o wiele wiencej pisania. Przykład (pierwszy z else if, drugi robi to samo ale bez niego):
```cpp
int num = 4;
if (num == 1) {
  std::cout << "1\n";
} else if (num == 2) {
  std::cout << "2\n";
} else if (num == 3) {
  std::cout << "3\n";
} else {
  std::cout << "inna liczba\n";
}
```

```cpp
int num = 3;
if (num == 1) {
  // print 1
} else {
  if (num == 2) {
    // print 2
  } else {
    if (number == 3) {
      // print 3
    } else {
      // print inna liczba
    }
  }
}
```
- użyłem komentaży bo mi sie niechce tych pisac na telefonie.
- widać że else if jest lepsze niż wersja bez niego.
else if to tak naprawde else i if.
`else if(condition) {...}` = 
```cpp
else {
  if(condition) {
    ...
  } else {
    // jeśli if ma więcej `else if` albo `else`, byłoby dodane tutj
  }
}
```
gdzie `condition` to wartość boolean, a `...` to kod.


Zadania:
1. menu wyboru czegoś do zrobienia
2. Nwm, niemam pomysłów
