# Instrukcja wgrania strony na WordPress

## Co zawiera ten pakiet

| Plik/folder | Opis |
|---|---|
| `strona-wordpress.html` | Gotowa strona HTML z CSS – otwórz w przeglądarce, żeby zobaczyć podgląd |
| `GRAFIKI BIEGI/` | Folder z wszystkimi obrazami PNG |

---

## Metoda A – Gotowa strona HTML (najprostsza)

Jeśli masz wtyczkę **WPCode**, **Elementor**, **Divi** lub **Full Site Editing**, możesz wkleić kod HTML bezpośrednio.

### Krok 1 – Wgraj grafiki do WordPress

1. W panelu WP wejdź w **Media → Dodaj nowe**
2. Wgraj **wszystkie pliki PNG** z folderu `GRAFIKI BIEGI`:
   - `logo_biegi-01.png`
   - `logo_biegi-02.png`
   - `15.png` do `29.png` (brakuje 26 – to normalne)
3. Po wgraniu każdego pliku **skopiuj jego URL** (widoczny w panelu Media po kliknięciu na plik → "Kopiuj URL do schowka")

### Krok 2 – Podmień URL-e w pliku HTML

Otwórz `strona-wordpress.html` w notatniku (Notepad++, VS Code) i zamień:

| Szukaj | Zastąp |
|---|---|
| `images/logo_biegi-01.png` | URL logo-01 z WP |
| `images/logo_biegi-02.png` | URL logo-02 z WP |
| `images/15.png` | URL pliku 15.png z WP |
| `images/16.png` | URL pliku 16.png z WP |
| *(itd. dla 17–29)* | |

### Krok 3 – Wstaw na stronę WordPress

#### Opcja 1 – Blok Custom HTML (Gutenberg)
1. Utwórz nową stronę: **Strony → Dodaj nową**
2. Kliknij **+** → wyszukaj „Custom HTML"
3. Wklej całą zawartość pliku HTML (od `<!DOCTYPE html>` do `</html>`)
4. Opublikuj

> ⚠️ Uwaga: niektóre motywy WP mogą nadpisać style. Wtedy użyj Opcji 2.

#### Opcja 2 – Wtyczka WPCode (zalecana)
1. Zainstaluj wtyczkę **WPCode** (darmowa)
2. Wejdź w **WPCode → Dodaj nowy snippet**
3. Wybierz typ: HTML
4. Wklej kod i przypisz go do wybranej strony

#### Opcja 3 – Elementor / Divi
1. Edytuj stronę wtyczką
2. Dodaj widget **HTML** lub **Code**
3. Wklej kod

---

## Dodanie linku do rejestracji

W kodzie HTML znajdź wszystkie wystąpienia:
```
href="#"
```
I zamień `#` na właściwy link do rejestracji (np. `https://twoj-formularz.pl/rejestracja`).

Są **4 przyciski** z takim linkiem:
- Hero (górny baner)
- Sekcja "O wydarzeniu"
- Karta "Szmaragd Borów"
- Karta "Kręgi Mocy"
- Finalny CTA (dolny baner)

---

## Podgląd przed wgraniem

Otwórz `strona-wordpress.html` lokalnie w przeglądarce (Chrome/Firefox) – **grafiki nie będą widoczne** do czasu podmienienia URL-ów, ale układ i kolory będą widoczne.
