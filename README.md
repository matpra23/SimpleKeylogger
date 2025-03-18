# Simple Keylogger

## Opis
Prosty keylogger napisany w Pythonie wykorzystujący bibliotekę `pynput`. Program zapisuje wszystkie naciśnięte klawisze do pliku tekstowego wraz z dokładnym czasem ich wystąpienia.

## Wymagania
- Python 3.x
- Biblioteka pynput (`pip install pynput`)

## Struktura projektu
```python
main.py          # Główny plik
keyLogs.txt      # Plik wyjściowy z zapisem klawiszy
```

## Instalacja
1. Sklonuj repozytorium lub pobierz plik `main.py`
2. Zainstaluj wymagane zależności:
```bash
pip install pynput
```

## Użycie
1. Uruchom program komendą:
```bash
python main.py
```
2. Program będzie działał w tle, zapisując wszystkie naciśnięte klawisze do pliku `keyLogs.txt`
3. Aby zakończyć działanie programu, użyj kombinacji Ctrl+C

## Szczegóły implementacji

### Komponenty
- `logging` - moduł do zapisywania logów
- `pynput.keyboard` - moduł do przechwytywania zdarzeń klawiatury

### Główne funkcje

#### `on_press(key)`
Funkcja callback wywoływana przy każdym naciśnięciu klawisza.
- Parametr `key` - naciśnięty klawisz
- Zapisuje informację o naciśniętym klawiszu do pliku logów

### Format logów
Każde zdarzenie jest zapisywane w formacie:
RRRR-MM-DD GG:MM:SS,mmm: <klawisz>
