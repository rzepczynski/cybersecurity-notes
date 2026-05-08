# Networking Core Protocols

## Cel

Celem było poznanie podstawowych protokołów sieciowych wykorzystywanych w komunikacji internetowej oraz zrozumienie ich zastosowania w praktyce.

---

## Wprowadzenie

Protokoły sieciowe odpowiadają za wymianę danych pomiędzy urządzeniami w sieci.

Każdy protokół pełni określoną funkcję, np.:

- przesyłanie stron internetowych  
- transfer plików  
- komunikację e-mail  
- tłumaczenie nazw domenowych  

Znajomość tych protokołów jest kluczowa w analizie ruchu sieciowego oraz cyberbezpieczeństwie.

---

## DNS (Domain Name System)

DNS tłumaczy nazwy domen na adresy IP.

Przykład:

```plaintext
twitter.com → adres IP
```

Bez DNS użytkownik musiałby wpisywać adresy IP zamiast nazw stron.

Znaczenie w cyberbezpieczeństwie:

- DNS jest często wykorzystywany podczas rekonesansu  
- ataki DNS spoofing mogą przekierowywać użytkowników na fałszywe strony  
- analiza zapytań DNS pomaga wykrywać złośliwą aktywność  

---

## WHOIS

WHOIS pozwala uzyskać informacje o domenie, takie jak:

- właściciel  
- rejestrator  
- serwery DNS  
- daty rejestracji  

Przykładowe użycie:

```bash
whois twitter.com
```

<img width="916" height="897" alt="whois" src="https://github.com/user-attachments/assets/d9f2b9e0-00bc-4e0b-a220-86ba5d15585c" />

Znaczenie w cyberbezpieczeństwie:

- używany podczas rekonesansu OSINT  
- pomaga zbierać informacje o infrastrukturze celu  
- często wykorzystywany podczas testów penetracyjnych  

---

## HTTP i HTTPS

HTTP oraz HTTPS służą do komunikacji z serwerami WWW.

### HTTP

- dane przesyłane są otwartym tekstem  
- brak szyfrowania  

### HTTPS

- wykorzystuje szyfrowanie TLS/SSL  
- zapewnia poufność i integralność danych  

Znaczenie w cyberbezpieczeństwie:

- HTTPS chroni przed przechwyceniem danych  
- błędna konfiguracja HTTPS może prowadzić do podatności  
- analiza ruchu HTTP/HTTPS jest ważna podczas monitorowania sieci  

---

## FTP (File Transfer Protocol)

FTP służy do przesyłania plików pomiędzy klientem a serwerem.

Przykładowe polecenia:

```bash
ftp 10.112.191.46
ls
get flag.txt
```

W projekcie:

- połączono się z serwerem FTP  
- wyświetlono pliki komendą `ls`  
- pobrano plik `flag.txt`  

<img width="916" height="707" alt="ftp" src="https://github.com/user-attachments/assets/c40c9305-cb9c-4897-a552-bdc953911212" />

Znaczenie w cyberbezpieczeństwie:

- klasyczny FTP przesyła dane bez szyfrowania  
- login i hasło mogą zostać przechwycone  
- często analizowany podczas audytów bezpieczeństwa  

---

## SMTP (Simple Mail Transfer Protocol)

SMTP odpowiada za wysyłanie wiadomości e-mail.

Wykorzystywany jest pomiędzy:

- klientem poczty a serwerem  
- serwerami pocztowymi  

Znaczenie w cyberbezpieczeństwie:

- często wykorzystywany w phishingu i spamie  
- błędna konfiguracja może umożliwiać open relay  
- analiza SMTP pomaga wykrywać złośliwe wiadomości  

---

## POP3

POP3 służy do pobierania wiadomości e-mail z serwera.

Po pobraniu wiadomości:

- mogą zostać usunięte z serwera  

Znaczenie w cyberbezpieczeństwie:

- starszy protokół pocztowy  
- brak szyfrowania może prowadzić do przechwycenia danych  

---

## IMAP

IMAP umożliwia synchronizację wiadomości e-mail między urządzeniami.

W przeciwieństwie do POP3:

- wiadomości pozostają na serwerze  

Znaczenie w cyberbezpieczeństwie:

- często używany w nowoczesnych systemach pocztowych  
- wymaga bezpiecznej konfiguracji szyfrowania  

---

## Podsumowanie

W ramach modułu poznano:

- DNS  
- WHOIS  
- HTTP/HTTPS  
- FTP  
- SMTP  
- POP3  
- IMAP  

Poznano również podstawowe zastosowania tych protokołów oraz ich znaczenie w komunikacji sieciowej.

---

## Zastosowanie w cyberbezpieczeństwie

Znajomość podstawowych protokołów sieciowych jest ważna w pracy:

- analityka SOC  
- pentestera  
- administratora bezpieczeństwa  
- specjalisty ds. bezpieczeństwa sieci  

Pozwala na:

- analizę ruchu sieciowego  
- wykrywanie podatności  
- identyfikację niebezpiecznych usług  
- lepsze zrozumienie działania ataków sieciowych  
