## ++, --, +=, -=, *=, /=, %=, <<, >>, <<=, >>=, &, &=

- połowa z tego jest łatwa, a drugiej połowy nie trzeba znać
- `++` zwiększa liczbe o 1, a `--` zmniejsza o 1. w przypadku gdy użtwa się np. array, to `arr[i++]` oznacza dostanie elementu, a dopiero potem zwiększenie i, a `arr[++i]` oznacza zwiększenie i, a potem dostanie elementu. podobnie z `--`
- `+=`, `-=`, `*=`, `/=`, `%=`, `<<=`, `>>=` oraz `&=`, umożliwiają zmienienie kodu z `x = x * 2` na `x *= 2` (`x *=` to `x = x *`). tak samo dla reszty.
- `<<` w liczbach znaczy coś innego niż w cout. stosowane na liczbach oznacza operacje `left shift` lub `right shift`. mają one sens, kiedy liczby pokaże się w systemie binarnym.
- Przykład dla shift:
```
int x = 0b10011;
int x2 = x<<2;
// x2 =  1001100
int x3 = x>>1;
//x3 =   1001
```
Czyli:
- `<<` przesuwa bity o `n` w lewo, i dodaje `n` zer po prawej
- `>>` przesuwa bity o `n` w prawi, i dodaje `n` zer po lewej

- `&` to `&&` ale dla liczb. liczy AND dla każdego bita liczby.
Przykład:
```
  1010
  1100
& ----
  1000
```

Zadania:
1. Pamiętać że istnieją
