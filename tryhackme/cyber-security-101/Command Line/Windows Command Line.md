# Windows Command Line

## Wprowadzenie

Pokój **Windows Command Line** na platformie TryHackMe wprowadza do podstaw pracy z wierszem poleceń systemu Windows. CMD jest jednym z najważniejszych narzędzi administratora systemów, analityka SOC oraz specjalisty cyberbezpieczeństwa. Pozwala na szybkie wykonywanie operacji administracyjnych, diagnostykę systemu, analizę procesów oraz zarządzanie plikami bez konieczności korzystania z interfejsu graficznego.

Znajomość CMD jest niezbędna podczas pracy w środowiskach korporacyjnych, analizy incydentów bezpieczeństwa oraz reagowania na zagrożenia.

---

## Cele pokoju

- Poznanie podstawowych poleceń wiersza poleceń Windows
- Uzyskiwanie informacji o systemie operacyjnym
- Diagnostyka połączeń sieciowych
- Zarządzanie plikami i katalogami
- Monitorowanie oraz kończenie procesów

---

## Sprawdzanie wersji systemu

Jednym z podstawowych poleceń administracyjnych jest sprawdzenie wersji systemu operacyjnego.

```cmd
ver
```

Polecenie wyświetla aktualną wersję zainstalowanego systemu Windows.



---

## Wyświetlanie zawartości plików

Polecenie `type` pozwala na odczytanie zawartości pliku tekstowego bezpośrednio w konsoli.

```cmd
type C:\Treasure\Hunt\flag.txt
```

W praktyce jest ono bardzo przydatne podczas analizy plików konfiguracyjnych, logów oraz artefaktów bezpieczeństwa.



---

## Zarządzanie procesami

### Wyświetlanie procesów

Polecenie umożliwia filtrowanie listy uruchomionych procesów.

```cmd
tasklist /FI "imagename eq notepad.exe"
```

Pozwala szybko sprawdzić, czy wskazany proces jest aktywny.

### Kończenie procesu

```cmd
taskkill /PID 1516
```

Polecenie kończy proces na podstawie jego identyfikatora PID. Jest to niezwykle przydatne podczas reagowania na podejrzaną aktywność lub zamykania zawieszonych aplikacji.



---

## Diagnostyka sieci

Podstawowe narzędzia diagnostyczne dostępne w CMD:

```cmd
ipconfig
ping
tracert
nslookup
```

### Zastosowanie

- **ipconfig** – wyświetla konfigurację interfejsów sieciowych
- **ping** – testuje łączność z hostem
- **tracert** – analizuje trasę pakietów
- **nslookup** – umożliwia rozwiązywanie nazw DNS

Narzędzia te są codziennie wykorzystywane w administracji oraz cyberbezpieczeństwie.

---

## Zarządzanie plikami i katalogami

Najczęściej używane polecenia:

```cmd
dir
cd
copy
move
del
mkdir
rmdir
```

Pozwalają na:

- przeglądanie zawartości katalogów
- nawigację po systemie plików
- kopiowanie i przenoszenie danych
- usuwanie plików i folderów
- tworzenie nowych katalogów

---

## Znaczenie w cyberbezpieczeństwie

Windows Command Line jest podstawowym narzędziem w pracy:

- Junior SOC Analyst
- Security Analyst
- Incident Responder
- System Administrator
- Blue Team Specialist

Umiejętność sprawnego korzystania z CMD pozwala na szybką analizę systemów, zbieranie artefaktów oraz reagowanie na incydenty bezpieczeństwa.

---

## Zdobyte umiejętności

Po ukończeniu pokoju potrafię:

- poruszać się po systemie plików za pomocą CMD
- uzyskiwać informacje o systemie
- diagnozować podstawowe problemy sieciowe
- monitorować aktywne procesy
- kończyć niepożądane procesy
- efektywnie wykorzystywać narzędzia administracyjne systemu Windows

---

## Podsumowanie

Pokój **Windows Command Line** dostarczył praktycznych podstaw pracy z konsolą systemu Windows. Jest to jedna z najważniejszych umiejętności wymaganych zarówno w administracji systemami, jak i w cyberbezpieczeństwie.

Znajomość CMD stanowi solidny fundament do dalszej nauki PowerShell, Active Directory, analizy incydentów oraz pracy w zespole SOC.
