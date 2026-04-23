# Linux Fundamentals Part 2

## Wprowadzenie

W tej części kontynuowałem naukę systemu Linux w kontekście cyberbezpieczeństwa. Skupiłem się na pracy zdalnej (SSH), analizie systemu oraz eksploracji katalogów istotnych z punktu widzenia bezpieczeństwa.

---

## Połączenie z maszyną przez SSH

Połączyłem się z maszyną zdalnie używając SSH:

```bash
ssh username@ip_address
```

Po wpisaniu hasła uzyskałem dostęp do systemu.

### Czego się nauczyłem:

* SSH umożliwia zdalne zarządzanie serwerem
* połączenie jest szyfrowane
* jest to standard w pracy administratorów i w pentestach

---

## Analiza poleceń i flag

Sprawdzałem rozszerzone opcje poleceń:

```bash
ls -lh
ls -R
ls -lt
```

Dodatkowo użyłem:

```bash
man ls
```

### Wnioski:

* `-h` → czytelne rozmiary plików
* `-R` → przeglądanie całej struktury katalogów
* `-t` → sortowanie po czasie

### Czego się nauczyłem:

* znajomość flag przyspiesza pracę
* dokumentacja (`man`) to podstawowe źródło wiedzy

---

## Analiza systemu plików

Użyłem narzędzi do analizy plików:

```bash
tree
stat file.txt
file file.txt
history
```

### Co zrobiłem:

* zobaczyłem strukturę katalogów (`tree`)
* sprawdziłem szczegóły pliku (`stat`)
* określiłem typ pliku (`file`)
* przeanalizowałem historię poleceń (`history`)

### Wnioski:

* można analizować pliki bez ich otwierania
* historia poleceń może być użyta do analizy działań użytkownika

---

## Użytkownicy i uprawnienia

Sprawdziłem informacje o użytkowniku:

```bash
whoami
id
```

### Co zrobiłem:

* sprawdziłem aktualnego użytkownika
* zobaczyłem grupy użytkownika

### Wnioski:

* dostęp do systemu zależy od użytkownika i grup
* ważne w kontekście privilege escalation

---

## Eksploracja systemu

Przeglądałem kluczowe katalogi:

```bash
cd /var/log
ls -lh

cd /etc
ls

cd /tmp
ls
```

### Co zauważyłem:

* `/var/log` → zawiera logi systemowe
* `/etc` → pliki konfiguracyjne
* `/tmp` → pliki tymczasowe

### Wnioski (cybersecurity):

* logi są kluczowe w analizie incydentów
* `/tmp` może być używany przez malware
* konfiguracja systemu często zawiera wrażliwe dane

---

## Zastosowanie w cyberbezpieczeństwie

Wykorzystanie tych umiejętności:

* analiza systemu po uzyskaniu dostępu
* szukanie podatności
* analiza logów
* wykrywanie podejrzanych działań

---

## Podsumowanie

### Umiejętności:

* zdalne łączenie się przez SSH
* używanie zaawansowanych opcji poleceń
* analiza plików i systemu
* rozumienie użytkowników i uprawnień
* eksploracja katalogów systemowych

---

## Wnioski końcowe

Ta część pomogła mi zrozumieć:

* jak działa Linux w praktyce
* gdzie znajdują się ważne dane systemowe
* jak analizować system z perspektywy bezpieczeństwa

---

