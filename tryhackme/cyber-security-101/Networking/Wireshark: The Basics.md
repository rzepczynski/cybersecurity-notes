# Wireshark: The Basics

## Cel

Celem było poznanie podstaw programu Wireshark oraz nauka analizy ruchu sieciowego i pakietów sieciowych.

---

## Wprowadzenie

Wireshark to jedno z najpopularniejszych narzędzi do analizy ruchu sieciowego.

Pozwala:

- przechwytywać pakiety sieciowe  
- analizować protokoły  
- filtrować ruch  
- diagnozować problemy sieciowe  
- wykrywać podejrzaną aktywność  

Wireshark jest powszechnie używany przez:

- analityków SOC  
- administratorów sieci  
- pentesterów  
- specjalistów cyberbezpieczeństwa  

---

## Podstawy działania Wireshark

Program przechwytuje ruch sieciowy w czasie rzeczywistym i prezentuje pakiety w czytelnej formie.

Każdy pakiet zawiera informacje takie jak:

- adres źródłowy i docelowy  
- używany protokół  
- zawartość danych  
- szczegóły komunikacji sieciowej  

---

## Packet Dissection

Wireshark pozwala analizować strukturę pakietów oraz ich zawartość.

Możliwe jest sprawdzanie:

- warstw modelu TCP/IP  
- nagłówków protokołów  
- szczegółów transmisji danych  

Znaczenie w cyberbezpieczeństwie:

- analiza pakietów pomaga wykrywać ataki sieciowe  
- umożliwia identyfikację podejrzanego ruchu  
- pomaga diagnozować incydenty bezpieczeństwa  

---

## Packet Navigation

Wireshark umożliwia wygodne poruszanie się pomiędzy pakietami i analizę całych sesji komunikacyjnych.

Możliwe jest:

- śledzenie komunikacji  
- analiza kolejnych pakietów  
- filtrowanie ruchu według określonych parametrów  

---

## Packet Filtering

Filtrowanie pakietów pozwala szybko znaleźć interesujący ruch sieciowy.

Przykładowe filtry:

```plaintext
http
dns
tcp
ip.addr == 192.168.1.1
```

Filtrowanie znacząco ułatwia analizę dużych ilości danych sieciowych.

<img width="960" height="817" alt="filter" src="https://github.com/user-attachments/assets/c4acf507-ae97-4b7d-9495-2070c43f7f28" />

Znaczenie w cyberbezpieczeństwie:

- pomaga wykrywać złośliwy ruch  
- umożliwia analizę komunikacji malware  
- wspiera monitorowanie incydentów bezpieczeństwa  

---

## Follow Streams

Wireshark umożliwia śledzenie całych rozmów sieciowych pomiędzy hostami.

Funkcja „Follow Stream” pozwala analizować:

- komunikację HTTP  
- sesje TCP  
- przesyłane dane  

<img width="958" height="821" alt="follow" src="https://github.com/user-attachments/assets/8ca6e6da-ef3c-4a01-9142-9342312f7c09" />

---

## Statistics

Wireshark posiada funkcje statystyczne umożliwiające analizę ruchu sieciowego.

Możliwe jest sprawdzanie:

- ilości pakietów  
- używanych protokołów  
- aktywności hostów  
- obciążenia sieci  

<img width="959" height="962" alt="statistics" src="https://github.com/user-attachments/assets/54822d7b-95c7-4662-8404-1ee4333784f8" />

---

## Warnings i analiza problemów

Program potrafi wykrywać potencjalne problemy w ruchu sieciowym.

Przykłady:

- retransmisje TCP  
- błędy komunikacji  
- nieprawidłowe pakiety  
- podejrzane zachowania sieciowe  

<img width="954" height="818" alt="warnings" src="https://github.com/user-attachments/assets/e3782804-0e4d-481a-8780-0835d6e32de3" />

---

## Analiza daty i czasu pakietów

Wireshark umożliwia analizę czasu przechwycenia pakietów.

Pozwala to:

- analizować chronologię zdarzeń  
- wykrywać anomalie czasowe  
- badać przebieg komunikacji sieciowej  

<img width="957" height="815" alt="date" src="https://github.com/user-attachments/assets/938fecce-d15e-4114-ba4b-329df09faf70" />

---

## Podsumowanie

W ramach modułu poznano:

- podstawy działania Wireshark  
- analizę pakietów sieciowych  
- filtrowanie ruchu  
- analizę sesji komunikacyjnych  
- podstawowe funkcje statystyczne  

Poznano również zastosowanie Wireshark w analizie bezpieczeństwa sieciowego.

---

## Zastosowanie w cyberbezpieczeństwie

Wireshark jest jednym z podstawowych narzędzi używanych w cyberbezpieczeństwie.

Znajomość programu pomaga w:

- analizie incydentów bezpieczeństwa  
- monitorowaniu ruchu sieciowego  
- wykrywaniu podejrzanej aktywności  
- analizie malware  
- diagnostyce problemów sieciowych  

Jest to ważne narzędzie w pracy:

- SOC Analyst  
- Blue Team  
- Pentester  
- Network Security Engineer  
