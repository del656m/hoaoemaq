## bool, ==, !, &&, ||, <, >, <=, >=

- według pdf z tego trzeba znać: `==` i to że bool istnieje jako coś co sie daje do `if`. reszta jest dodatkowo.

- bool to typ danych (jak int float i double), tylko że zawiera 1 bit informacji (true lub false, 1 lub 0)
- Przykład: `bool numbersEqual = number1 == number2`. `bool numbersEqual = ` ustawi wartosc 'numbersEqual' na to, co jest po prawej stronie znaku '='. `number1 == number2` sprawdza czy dane (liczby, boolean, tekst) są równe siebie (oddaje typ bool)
- Przykład 2: `bool failed = false`. ustawia wartość 'failed' typu 'bool' na false (0)
- `==` sprawdza czy dane są równe
- `<`, `>`, `<=`, `>=` sprawdzają czy liczby są większe czy mniejsze. `a < b` czy a jest mniejsza od b. `a > b` czy a jest większe od b. `a <= b` czy a jest mniejsze lub równe b. `a >= b` czy a jest większe lub równe b.
- nazwy 'a' i 'b' można zmienić na jakies inne.
- `&&` działa tak samo jak bramka logiczna AND, bo to jest to samo. czyli jeżeli w `a && b` gdzie a i b są bool, oba `a` i `b` mają wartość true, to and również odda wartość true.
- `||` działa tak samo jak bramka logiczna OR. jeśli w `a || b` a lub b będzie true, to OR również odda wartość true.
- `!` to bramka NOT. Przykład: `bool success = !failed`, potrzebuje ona innej wartości boolean.
- Większość innych bramek można robić przez dodawanie innych. Przykład NOR: `bool valueA = !(checkA || checkB)`. nazwy `valueA`, `checkA` oraz `checkB` można zamienić na jakiekolwiek inne. Jeśli napisało by się `bool valueA = !checkA || checkB`, to c++ najpierw wyliczyłoby NOT(checkA), i oddało wartość wyniku bramek AND(NOT(checkA), checkB), zamiast NAND(checkA, checkB).

Zadania: brak, ale polecam zobaczyć jak wszystko działa i jak sie może zepsuć. można używać chatgpt jesli konieczne.
