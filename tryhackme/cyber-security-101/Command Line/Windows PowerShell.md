# Windows PowerShell

## Wprowadzenie

Pokój **Windows PowerShell** na platformie TryHackMe wprowadza do pracy z jednym z najważniejszych narzędzi w środowisku Windows. PowerShell jest nowoczesną powłoką i językiem skryptowym, który umożliwia analizę systemu, automatyzację zadań oraz szybkie reagowanie na incydenty bezpieczeństwa.

W przeciwieństwie do CMD, PowerShell operuje na obiektach, co pozwala na dokładne filtrowanie, analizę i przetwarzanie danych.

Z perspektywy cyberbezpieczeństwa jest to kluczowe narzędzie w pracy:
- SOC Analyst
- Security Analyst
- Incident Responder
- Blue Team

---

## Cele pokoju

- Poznanie podstaw PowerShell
- Praca z cmdletami
- Analiza systemu (procesy, użytkownicy, usługi)
- Monitorowanie połączeń sieciowych
- Wykorzystanie filtrowania i pipeline

---

## Podstawy PowerShell

Cmdlety w PowerShell mają strukturę:

```powershell
Verb-Noun
```

Przykłady:

```powershell
Get-Process
Get-Service
Get-LocalUser
Get-NetTCPConnection
```

Dzięki temu polecenia są czytelne i łatwe do interpretacji.

---

## Analiza użytkowników systemu

Polecenie:

```powershell
Get-LocalUser
```

Pozwala wyświetlić wszystkich lokalnych użytkowników systemu.

### Zastosowanie w cyberbezpieczeństwie

- identyfikacja nieznanych kont
- sprawdzanie aktywności użytkowników
- analiza potencjalnych backdoorów

<img width="959" height="838" alt="get-localuser" src="https://github.com/user-attachments/assets/e70a50e9-661f-43f3-86ea-3421d6049b33" />

---

## Analiza połączeń sieciowych

Polecenie:

```powershell
Get-NetTCPConnection
```

Wyświetla aktywne połączenia TCP oraz porty.

### Zastosowanie w cyberbezpieczeństwie

- wykrywanie podejrzanych połączeń
- analiza komunikacji z zewnętrznymi adresami IP
- identyfikacja nietypowych portów

<img width="902" height="690" alt="get-netTCPconnection" src="https://github.com/user-attachments/assets/6506a484-8a9d-4c87-952c-2101715f778b" />

---

## Monitorowanie procesów

Polecenie:

```powershell
Get-Process
```

Wyświetla wszystkie uruchomione procesy wraz z ich parametrami.

### Zastosowanie w cyberbezpieczeństwie

- wykrywanie podejrzanych procesów
- analiza zużycia CPU i pamięci
- identyfikacja malware działającego w tle

<img width="947" height="814" alt="get-process" src="https://github.com/user-attachments/assets/52bf53dc-bce6-41e5-8e6b-329bdddc3d39" />

---

## Filtrowanie usług

Polecenie:

```powershell
Get-Service | Where-Object {$_.DisplayName -like "*merry*"}
```

Pozwala filtrować usługi według nazwy.

### Zastosowanie

- szybkie wyszukiwanie konkretnych usług
- analiza konfiguracji systemu
- identyfikacja nietypowych usług

---

## Wybór konkretnych danych

Polecenie:

```powershell
Get-Service | Where-Object {$_.DisplayName -like "*merry*"} | Select-Object Name, Status
```

Pozwala wyświetlić tylko wybrane informacje.

### Dlaczego to ważne

- redukcja szumu danych
- tworzenie czytelnych raportów
- szybsza analiza systemu

<img width="945" height="258" alt="get-service, where-object" src="https://github.com/user-attachments/assets/a85a2cf6-7e21-415d-bd68-5e25c5c52cda" />

---

## Pipeline – przetwarzanie danych

Jedną z najważniejszych funkcji PowerShell jest pipeline (`|`).

Przykład:

```powershell
Get-Process | Sort-Object CPU -Descending | Select-Object -First 5
```

### Co robi to polecenie

- pobiera procesy
- sortuje je po użyciu CPU
- wyświetla 5 najbardziej obciążających

### Zastosowanie w praktyce

- wykrywanie podejrzanych procesów
- identyfikacja anomalii
- szybka analiza wydajności systemu

---

## Praktyczne zastosowanie (perspektywa SOC)

PowerShell może być używany do:

- enumeracji systemu
- zbierania artefaktów
- analizy procesów
- wykrywania podejrzanych połączeń
- sprawdzania użytkowników
- automatyzacji reakcji na incydenty

Pozwala szybko zebrać kluczowe informacje o systemie bez użycia GUI.

---

## Zdobyte umiejętności

Po ukończeniu pokoju potrafię:

- korzystać z cmdletów PowerShell
- analizować użytkowników systemu
- monitorować procesy i usługi
- sprawdzać aktywne połączenia sieciowe
- filtrować dane za pomocą `Where-Object`
- wykorzystywać `Select-Object`
- używać pipeline do analizy danych

---

## Podsumowanie

PowerShell jest jednym z najważniejszych narzędzi w środowisku Windows oraz cyberbezpieczeństwie.

Umożliwia szybkie zbieranie informacji, analizę systemu oraz wykrywanie potencjalnych zagrożeń. Jego znajomość jest kluczowa dla każdego, kto chce pracować jako SOC Analyst lub w Blue Team.

Stanowi fundament do dalszej nauki:
- Active Directory
- SIEM
- Incident Response
- automatyzacji i skryptów
