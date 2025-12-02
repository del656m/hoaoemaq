## switch + case

- podobne do if
- zamiast sprawdzac kondycje, dprawdza on liczbe
pzrykład:
```cpp
int type = 2;
switch (type) {
case 0: {
  std::cout << "Usuwanie folderu System32...\n";
  break;
}
case 1: {
  std::cout << "Liczba pi != 92\n";
  break;
}
case 2: {
  std::cout << "Fake: ";
}
default: {
  std::cout << "Nieznana opcja!\n";
  break;
}
}
std::cout << "Koniec programu\n";
```
- jeżeli type będzie 0, wykona się kod przypisany do case 0. jeśli type to 1, wykona się kod przypisany do case 1. i tak dalej.
- `break;` mówi, że to jest już koniec switcha. Brak break spowoduje wykonanie kolejnych caseów aż do napotkania break lub końca switcha, nie ważne czy wartość w `case X` się zgadza. Najlepiej jest zawsze dodawać case.
- default jest używane, gdy switch nie ma jak czegoś zrobić (np. type będzie 10, a switch nie będzie miał case dla liczby 10). `default` zostanie również wykonane, gdy w case nie było break.
- w tym przypadku, switch znajdzie informację, co ma zrobić gdy wartość będzie 2, i to zrobi. Ponieważ w case 2 nie ma break, switch wykona case 2 oraz default.
- w tym przypadku powinna pojawić się wiadomość "Fake: Nieznana opcja!".
- przez to że w case 2 niema break, przy dodawaniu kolejnego case może być problem. Najlepiej dodawać break zawsze.
