## switch + case

- podobne do if
- zamiast sprawdzac kondycje, dprawdza on liczbe
pzrykład:
```
int type = 2;
switch (type) {
case 0: {
  std::cout << "Usuwanie folderu System32...\n";
  break;
}
case 1: {
  std::cout << "Liczba pi != 92\n"
  break;
}
case 2: {
  std::cout << "Fake: ";
}
default: {
  std::cout << "Nieznana opcja!\n";
}
}
std::cout << "Koniec programu\n";
```
- jeżeli type bendzie 0, wykona sie kod przypisany do case 0. jeśli type to 1, wykona się kod przypisany do case 1. i tak dalej.
- `break;` muwi, że to jest już koniec switcha. Brak break spowoduje wykonanie `default`
- default jest używane, gdy switch niema jak czegoś zrobić (np. type będzie 10 a switch nie będzie miał case dla liczby 10. `default` zostanie również wykonane gdy w case, nie było break.
- w tym przypadku, switch znajdzie informacje, co ma zrobić gdy wartość będzie 2, i to zrobi. Ponieważ w case 2 niema break, switch wykola case 2, oraz default.
- w tym przypadku powinna pojawić się wiadomość "Fake: Nieznana opcja!".
