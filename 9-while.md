## while

- dodatkowe
- pozwala powtużyć kod bez go kopiowania i wklejania 2 biliony razy (ta liczba nie jest zmyślona)
- troche podobna do if. wykonuje kod przypisany do niego, jeśli kondycja jest true, tylko zamiast robienia tego raz zobi to dopuki nie będzie ona wynośić false.
- Przykład:
```
bool running = true
int a = 1;
int b = 2;
while (running) {
  a = a + b;
  b = b + 1;
  if (a > 1000*1000*1000) {
    running = false;
  }
  std::cout << "next: a="<<a<<" b="<<b<<"\n";
}
std::cout << "Finished!\n";
```
Wyjaśnienie
- program liczy liczby w pętli.
- jeśli a jest większe od 1 biliona (2 biliony to limit dla typu int), zmienna running zmieni się na false, a while przestanie wykonywać kod (dopiero po tym, w kturym wartość została zmieniona na false)

Zadanie:
1. Zrub program który do końca życia tego programu będzie liczyc setki kalkulacji (np. sqrt). Przestać jego działanie przez ctrl+c w windows.
