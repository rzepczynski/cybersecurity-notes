# Linux System Analysis

## Cel

Celem projektu była podstawowa analiza systemu Linux z perspektywy cyberbezpieczeństwa. Skupiłem się na identyfikacji użytkowników, procesów, usług oraz potencjalnych punktów analizy w systemie.

---

## Środowisko

- System: Linux (VM)
- Dostęp: lokalny terminal

---

## Analiza systemu

### Informacje o systemie

Sprawdziłem podstawowe informacje o użytkowniku i systemie:

```bash
whoami
id
hostname
pwd
```

![System info](Images/system-info.png)

---

### Użytkownicy

Przeanalizowałem listę użytkowników:

```bash
cat /etc/passwd
```

Pozwala to zidentyfikować konta systemowe oraz potencjalnie podejrzanych użytkowników.

![users](images/users.png)

---

### Uprawnienia i pliki

Sprawdziłem uprawnienia plików:

```bash
ls -la
```

Pozwala to wykryć nieprawidłowe konfiguracje dostępu.

![permissions](images/permissions.png)

---

### Procesy

Wyświetliłem wszystkie procesy:

```bash
ps aux
```

Dzięki temu można zidentyfikować podejrzane aplikacje działające w systemie.

![processes](images/processes.png)

---

### Obciążenie systemu

```bash
top
```

Pozwala zobaczyć najbardziej obciążające procesy.

![top](images/top.png)

---

### Porty i połączenia

```bash
ss -tuln
```

Sprawdziłem otwarte porty oraz usługi nasłuchujące.

![ports](images/ports.png)

---

### Logi systemowe

```bash
cat /var/log/syslog | tail
```

Logi są kluczowe w analizie incydentów bezpieczeństwa.

![logs](images/logs.png)

---

### Historia poleceń

```bash
history
```

Pozwala przeanalizować działania użytkownika.

![history](images/history.png)

---

## Wnioski

Podczas analizy systemu:

- zidentyfikowałem użytkowników systemowych  
- przeanalizowałem aktywne procesy  
- sprawdziłem otwarte porty  
- przejrzałem logi systemowe  

System nie wykazywał oczywistych oznak nieautoryzowanej aktywności, jednak powyższe kroki stanowią podstawę analizy bezpieczeństwa systemu Linux.

---

## Podsumowanie

Projekt pozwolił mi przećwiczyć podstawową analizę systemu Linux z perspektywy cyberbezpieczeństwa. Zdobyte umiejętności stanowią fundament do dalszej nauki w kierunku SOC Analyst oraz Incident Response.
