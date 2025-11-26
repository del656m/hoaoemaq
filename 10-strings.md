## std::string, std::wstring, const char*

- optional
- z jakiś powodów sposobów na tekst w c++ jest o wiele za dużo. z czego windows ma z 15. tutaj będą tylko 3.
- std::string - tekst w ASCII lub UTF-8.
- std::wstring - tekst w UTF-16 na windows, UTF-32 na linux.
- const char* - bardziej podstawowa wersja string.

Jak stworzyć każde z nich:
- `std::string` i `const char*` w ten sam spruób, pimiędzy dwoma znakami `"`.
- `std::wstring` podoble, ale z literą `L` przed, np. `L"Hello, π!"`

`cout` dla wstring to `wcout`

W Windows, używane jest głównie wstring, a na linux string.
