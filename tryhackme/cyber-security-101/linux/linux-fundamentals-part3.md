# Linux Fundamentals Part 3

## Wprowadzenie

W tej części kontynuowałem naukę systemu Linux, skupiając się na edytorach tekstu, użytecznych narzędziach systemowych, zarządzaniu procesami, automatyzacji oraz analizie logów. Wszystkie ćwiczenia wykonywałem samodzielnie na maszynie wirtualnej.

---

## Edycja plików w Nano

Poznałem podstawy pracy z terminalowym edytorem tekstu Nano.

### Użyte polecenia

```bash
ls
nano
nano /home/tryhackme/task3
```

### Co zrobiłem

- wyświetliłem zawartość katalogu,
- uruchomiłem edytor Nano,
- otworzyłem wskazany plik do edycji.

Dowód:

<img width="959" height="961" alt="1" src="https://github.com/user-attachments/assets/6ff41559-044b-4fa1-9793-5e3223158ef7" />

### Wnioski

- Nano pozwala szybko edytować pliki bez środowiska graficznego.
- Jest często wykorzystywany podczas pracy na serwerach Linux.

---

## Prosty serwer HTTP i pobieranie plików

Uruchomiłem lokalny serwer HTTP oraz pobrałem plik z wykorzystaniem narzędzia `wget`.

### Użyte polecenia

```bash
python3 -m http.server
wget http://10.112.162.119:8000/.flag.txt
ls -l
cat .flag.txt
```

### Co zrobiłem

- uruchomiłem serwer HTTP w bieżącym katalogu,
- pobrałem plik z innego hosta,
- zweryfikowałem pobrany plik,
- wyświetliłem jego zawartość.

Dowód:

<img width="958" height="960" alt="2" src="https://github.com/user-attachments/assets/19ff9051-0b2e-4a8c-ab8c-3b426eb77039" />

### Wnioski

- Python umożliwia szybkie uruchomienie prostego serwera HTTP.
- `wget` jest bardzo przydatny podczas pobierania plików w środowisku terminalowym.

---

## Monitorowanie procesów

Sprawdziłem aktualnie uruchomione procesy w systemie.

### Użyte polecenia

```bash
ps
ps aux
```

### Co zrobiłem

- wyświetliłem procesy aktualnej sesji,
- przeanalizowałem wszystkie aktywne procesy w systemie.

Dowód:

<img width="957" height="961" alt="3" src="https://github.com/user-attachments/assets/469015d9-66e8-44f4-9e15-0c67beb50edf" />

### Wnioski

- `ps` pokazuje podstawowe informacje o procesach.
- `ps aux` dostarcza pełny widok wszystkich uruchomionych usług i użytkowników.

---

## Dynamiczne monitorowanie systemu

Do monitorowania zasobów wykorzystałem narzędzie `top`.

### Użyte polecenie

```bash
top
```

### Co zrobiłem

- obserwowałem obciążenie procesora,
- sprawdzałem zużycie pamięci RAM,
- analizowałem najbardziej zasobożerne procesy.

📸 Dowód:

<img width="957" height="967" alt="4" src="https://github.com/user-attachments/assets/85e97914-aa55-4af2-845d-484ffcefe77b" />

### Wnioski

- `top` umożliwia monitorowanie systemu w czasie rzeczywistym.
- To podstawowe narzędzie diagnostyczne administratora.

---

## Automatyzacja z Cron

Poznałem podstawy planowania zadań cyklicznych.

### Użyte polecenie

```bash
crontab -e
```

### Co zrobiłem

- otworzyłem harmonogram zadań użytkownika,
- zapoznałem się z konfiguracją automatycznych zadań.

Dowód:

<img width="957" height="964" alt="5" src="https://github.com/user-attachments/assets/1751a63e-f00a-4811-86e1-ccf334428518" />

### Wnioski

- Cron pozwala automatyzować rutynowe zadania.
- Jest powszechnie wykorzystywany w administracji systemami.

---

## Analiza logów Apache

Przeanalizowałem logi serwera Apache.

### Użyte polecenia

```bash
cd /var/log/apache2
ls
ls -l
less access.log.1
```

### Co zrobiłem

- przeszedłem do katalogu z logami Apache,
- sprawdziłem dostępne pliki logów,
- przeanalizowałem zawartość archiwalnego logu dostępowego.

Dowód:

<img width="956" height="963" alt="6" src="https://github.com/user-attachments/assets/63585f1e-8190-4a02-b70e-8c0cf4eaac59" />

### Wnioski

- logi są kluczowe podczas analizy incydentów bezpieczeństwa.
- Umiejętność ich interpretacji jest niezbędna w cyberbezpieczeństwie.

---

## Podsumowanie

W tej części zdobyłem praktyczne umiejętności w zakresie:

- edycji plików w terminalu,
- udostępniania i pobierania plików,
- analizy procesów,
- monitorowania wydajności systemu,
- automatyzacji zadań,
- analizy logów serwera WWW.

---

## Wnioski końcowe

Linux Fundamentals Part 3 pozwolił mi lepiej zrozumieć codzienną pracę administratora systemów oraz specjalisty cyberbezpieczeństwa. Zdobyte umiejętności mają bezpośrednie zastosowanie w analizie systemów, reagowaniu na incydenty oraz testach bezpieczeństwa.
````

