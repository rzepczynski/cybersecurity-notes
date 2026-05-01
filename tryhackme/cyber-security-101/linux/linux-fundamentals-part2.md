# Linux Fundamentals Part 2

## Wprowadzenie
W tej części kontynuowałem naukę systemu Linux, skupiając się na praktycznym wykorzystaniu w kontekście cyberbezpieczeństwa.  
Ćwiczenia wykonywałem na maszynie wirtualnej.

---

## Połączenie przez SSH

Połączyłem się z maszyną zdalnie:

```bash
ssh tryhackme@10.114.177.166
```

Po wpisaniu hasła uzyskałem dostęp do systemu.

### Dowód:
<img width="957" height="962" alt="1" src="https://github.com/user-attachments/assets/59e0d121-643d-4213-aea4-130151954df9" />


### Wnioski:
- SSH służy do zdalnego zarządzania systemami
- połączenie jest szyfrowane
- używane w pracy administratora i pentestera

---

## Praca z poleceniami i flagami

Testowałem różne opcje polecenia `ls`:

```bash
ls -lh
ls -R
ls -lt
```
### Dowód:
<img width="958" height="929" alt="2" src="https://github.com/user-attachments/assets/7ce31c75-ab5a-4aac-90d0-1b7edfb0ffa3" />

### Wnioski:
- flagi zmieniają sposób wyświetlania danych
- znajomość flag przyspiesza pracę

---

## Analiza plików

Użyłem narzędzi do sprawdzania plików:

```bash
tree
stat file.txt
file file.txt
history
```
### Dowód:
<img width="958" height="960" alt="3" src="https://github.com/user-attachments/assets/ae3550cb-b956-487d-8cce-7d675f92a7fb" />

### Wnioski:
- można analizować pliki bez ich otwierania
- historia poleceń pokazuje działania użytkownika

---

## Użytkownicy i uprawnienia

Sprawdziłem informacje o użytkowniku:

```bash
whoami
id
```
### Dowód:
<img width="960" height="959" alt="4" src="https://github.com/user-attachments/assets/da5cad60-4e52-43e7-b48e-2741d5236ebe" />

### Wnioski:
- użytkownik i grupy określają dostęp
- ważne w kontekście privilege escalation

---

## Eksploracja systemu

Sprawdziłem ważne katalogi:

```bash
cd /var/log
ls -lh

cd /tmp
ls
```

<img width="958" height="961" alt="5" src="https://github.com/user-attachments/assets/da2e9ee6-1dca-4a5f-8d45-5101c4ece447" />

### Wnioski:
- `/var/log` zawiera logi systemowe
- `/tmp` często używany w atakach

---

## Podsumowanie

### Zdobyte umiejętności:

- korzystanie z SSH
- używanie zaawansowanych flag
- analiza plików
- sprawdzanie użytkowników i grup
- znajomość struktury systemu

---

## Wnioski końcowe

Ta część pozwoliła mi lepiej zrozumieć praktyczne działanie Linuxa oraz jego znaczenie w cyberbezpieczeństwie.

Wszystkie zadania wykonałem samodzielnie na maszynie wirtualnej.
