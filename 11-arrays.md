## []

- array działa jak lista, która nie zmienia listy elementów.
- elementy w array zaczynają się od 0. czyli pierwszym elementem będzie element z index 0, czyli o 1 miejszym.
- przykład:
```cpp
int scores[5] = {82, 70, 21, 98, 88};
scores[4] = 64;

std::cout<<"score 1: "<<scores[0]<<"\n";
std::cout<<"score 2: "<<scores[1]<<"\n";
std::cout<<"score 3: "<<scores[2]<<"\n";
std::cout<<"score 4: "<<scores[3]<<"\n";
std::cout<<"score 5: "<<scores[4]<<"\n";

int sum = 0;
// pętla for będzie dopiero w nr 13
for (int i = 0; i < 5; ++i) {
  sum = sum + scores[i];
  std::cout<<"score "<<i+1<<": "<<scores[i]<<"\n";
}
float average = sum / 5.0;
std::cout<<"srednia wynikow: "<<average<<"\n";
```
wyjasnienie:
- `int scores[5]` - zmienna o nazwie 'scores' z array z `5` elementami (od 0 do 4), gdzie elementy mają typ `int`
- `{82, 70, 21, 98, 88}` - ustaw wartości elementów
- `scores[4] = 64` - zmień ostatni element na 64
- 5x cout - manualne wyświetlenie elementów
- `int sum = 0` - potem policzona będzie suma wyników nazwana `sum` o typie int, która zaczyna sie od 0
- `for` - będzie puźniej, jak narazie wystarczy wiedzieć że robi coś 5 razy
- `sum = sum + scores[i]` - ustaw sum, jako sum + wartość elementu w miejscu który jest w liczbie `i` (for będzie w nr 13)
- 1x cout w for - bardziej automatyczne pokazanie wyników, przez to że array zaczyna się od 0, a my chcemy wyświetlić od 1, dodajemy 1.
- `float average = sum / 5.0` - średnia
