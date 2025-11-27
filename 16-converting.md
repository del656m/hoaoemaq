
- `static_cast` - zmienia liczbe na liczbe w podobno bezpieczny sposób.
- Przykład:
```
double a = 9.4;
int b = static_cast<int>(a);
```
Wyjaśnienie:
- `<int>` - na jaki typ zamienic

---

- `std::to_string(a)` - na string
- `std::stoi(a)` - string na int
- `std::stod(a)` - string na double
