# for

- pętla for, jest podobna do while.
- używana żeby zrobić coś daną ilość razy.
- przykład:
```
for (int i = 0; i < 5; ++i) {
  std::cout<<"Iteracja: "<<i<<"\n";
}
```
wyjaśnienie:
- `for` tak samo jak w if oraz while ma argument, ale niejest to bool.
- `int i = 0` w pierwszej części oddzielonej znakiem `;`, jest coś co ma sie stać na początku, np. stworzyć zmienną która będzie używana jako licznik.
- `i < 5` - kondycja, liczona przed każdym razem kod w for jest wywołany, jeśli wynośi true, kod zostanie wykonany, a jeśli wynośi false, kod nie zostanie wykonany, a c++ zacznie wykonywać kolejne insteukcje po niej
- `++i` - powiększa liczbe i o 1 (to samo co `i = i+1`), jest to wykonywane po kodzie pętli.
- `{...}` - kod pętli for, to co ma zostać wyonane za każdym razem.
- cout wyświetla i (ang. iteration)
- typ `int` można zmienić na inny.
- nazwe `i` można zmienić na inną.
- liczbe `0` to liczba, od której pętla zacznie
- kondycje można zmienić
- `++i` można zmienić na np. `--i` żeby ją zmienszać o 1 zamiast zwiększać


Zadania:
1. pętla for, która wyświetla liczby 0-12
2. pętla która wyświetla liczby 1-3
3. wyświetla liczby od -1 do 6
4. wyświetla liczby od 7 do 5 (od większej do mniejszej
5. wyświetla wiadomości (pętla for która nie używa zmiennej i, tylko generune inną zmienną). zmienna i niema być używana poza definicją pętli (definicja jako pomiędzy `for(` a `)`
