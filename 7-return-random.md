# return, srand, rand

- return w funkcji main służy głównie do pokazania, czy wystąpił jakiś błąd.
- 0 oznacza ok.
- użycie return oznacza zatrzymanie programu.
- Przykład:
```cpp
int main() {
  ...
  if (...) {
    std::cout << "Error: ...\n";
    return 1; 
  }
  ...
  return 0;
}
```

---

- `srand` ustawia seed do losowania, najczęściej `time(NULL)` czyli poprustu czas który jest.
- jeśli seed będzie taki sam, to wylosowane liczby też będą takie same (jak świat w grach)
- `rand` losuje liczbe, wystarczy użyć `srand` jeden raz na nieskonczenie wiele `rand`
- Przykład:
```cpp
srand(12345);
int random = rand();
std::cout<<"liczba z seed 12345: "<<random<<"\n";
srand(time(NULL));
random = rand();
std::cout<<"bardziej losowa liczba: "<<random<<"\n";
```
