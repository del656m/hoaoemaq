## `if`, `else if`, `else`

- dokra wiadomość, można po tym zrobic to menu wyboru
- trzeba rozumiec typ boolean żeby cokolwiek zrobić
- if robi coś jeśli coś jest true (siem, bardzo pomocne)
- if, umożliwia wykonywanie kodu, jeśli podana wartość bool jest równa `true`
Przykład (jeśli 2 liczby są równe, coś zrub):
```
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
- jeśli niewiesz co rubi cout lub cin, to niewiem co robisz w if, lepiej przeczytać i zrozumieć to co jest a `1-printing-variables.md`
- `if (num1 == num2)` - if znaczy jeżeli. `==` znaczy czy są równe. w połączeniu: `jeżeli są równe`. to tyle.
- if potrzebuje wiedziec to wtedy ma zrobić jak to co znajdule sie w `()` jest true. żeby mu to powiedzieć, wszystko co się ma wtedy stać musi być w znakach `{}`. to jest dokładnie tak samo jak w `int main()`, te same znaki muwią co ma robić. tylko że w int main jest to informacja gdzie jest kod, a w if jest to, co zrobic.
- w tym przypadku, jeżeli num1 jest równe num2, c++ wykona wszystkie instrukcje pomiędzy znakiem `{` a `}`. Jeśli jednego z tych znaków nie znajdzie, pojawi sie błąd ``
