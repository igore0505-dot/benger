# Oryginalne wnętrze + Twój garaż — FIX 4

**[Pobierz FIX 4 do MTA](https://github.com/igore0505-dot/benger/raw/refs/heads/main/oryginal_garaz_FIX4_MTA.zip)**

[ZIP na GitHubie — Download raw file](oryginal_garaz_FIX4_MTA.zip)

## Co poprawiono

- Oddzielono nieruchome szkło od pełnych ścian i wyposażenia. Tryb przezroczystości jest włączony wyłącznie dla szkła oraz przeszklonych drzwi.
- Wyłączono wymuszone rysowanie obu stron. Źródłowe rośliny i lampy mają już osobne przednie i tylne powierzchnie; ich UV i kolory pozostają zachowane.
- Usunięto zakryte warstwy ścian bazowych pod oryginalnymi okładzinami, bez zmiany wystroju.
- Dodano kolizję trzech donic, półki z przegródkami i gaśnicy. Zachowano kolizje monitora, racków, rozdzielni, palet i kartonów.
- Podgląd tymczasowo wyłącza strefy okluzji domyślnej mapy GTA i przywraca wcześniejszy stan po usunięciu lub zatrzymaniu resource, jeśli klient udostępnia odpowiednie API.
- Nowa komenda `/bengerfix` nie uruchamia dawnych handlerów `/benger`. Oznaczenie czatu to **[Benger FIX 4]**.

Twój przesłany garaż, jego tekstury, dopasowanie podłogi i drzwi pozostały bez zmian. Poprawki dotyczą renderowania oraz kolizji. Podgląd jest lokalny dla gracza.

## Wymiana poprzedniej wersji

Rozpakuj folder `benger_original_garaz_fix` do `resources`. W konsoli serwera zatrzymaj wszystkie wcześniejsze paczki:

```text
stop benger_garage
stop benger_garage_v2
stop benger_original_garaz
stop benger_original_garaz_fix
refresh
start benger_original_garaz_fix
```

W grze wpisz **`/bengerfix`**. Czat powinien pokazać `[Benger FIX 4]`.
`/bengerinfo` wyświetla wersję i liczbę sześciu wczytanych modeli, `/bengerdrzwi` przełącza tryb drzwi, `/bengerusun` usuwa podgląd. Nie uruchamiaj równocześnie starszego resource: jego istniejące obiekty mogą nakładać się na nowe.

## Sprawdzenie

Przechodzi 67 prób widocznych ścian i 42 próby kolizji donic, półki, gaśnicy, przejścia oraz podłogi. Zweryfikowano ramy, sfery, indeksy, binmesh i zachowanie UV/kolorów/materiałów. Testy Lua 5.1 z atrapami API obejmują flagi renderowania, TXD/COL, drzwi, awarie, usuwanie podglądów i przywracanie okluzji.

MTA nie było uruchamiane w tej maszynie. Ostateczny test obrotu kamery i chodzenia wokół wyposażenia trzeba wykonać w grze. Raporty są w paczce.

[Edytowalny plik Blendera FIX 4](https://github.com/igore0505-dot/benger/raw/refs/heads/main/Oryginal_plus_Twoj_garaz_FIX4.blend)

[Wygląd przejścia](oryginal_drzwi_garaz.png) · [Przesłany garaż](zalaczony_garaz.png) · [Połączenie modeli](oryginal_polaczenie.png)

Obrazy przedstawiają render projektu w Blenderze; nie są dowodem działania renderera MTA.
