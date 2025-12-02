# int main(int argc, char* argv[])

- argumenty są przydatne, jeśli program niechce użytac cin, tylko chce informacje w argumentach.
- przykładem programów kture biorą argumenty są instalatory programów. Często jednym z dostępnych argumentów jest `/S`, `/silent`, `/qn`, które instalują program bez pytania i bez okna.
- Przykład:
```cpp
int main(int argc, char* argv[]) {
  std::cout << "Ilosc argumentow: "<<argc<<"\n";
  std::cout << "Sciezka programu: "<<argv[0]<<"\n";
  if (argc > 1) {
    std::cout << "Pierwszy argument: "<<argv[1]<<"\n";
  }
}
```
Komenda: `program.exe argTest`
Output:
```
Ilocs argumentow: 2
Sciezka programu: program.exe
Pierwszy argument: argTest
```
Wyjaśnienie:
- argc to ilość argumentów
- prawdziwie perwszym argumenter jest nazwa/scieżka pliku (argument pierwszy czyli 0, argv czyli lista argumentów to array, czyli lista, która zaczyna się od zerowego a NIE pierwszego indexu)
- reszta argumentów zaczyna sie od numeru 1
- wszystkie argumenty są tekstem typu 'char*', który jest podobly do 'const char*' ale inny. można je poruwnywać tak samo jak liczby przez `==`, np. `argv[1] == "/S"`
