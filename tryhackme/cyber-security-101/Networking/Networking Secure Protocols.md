# Networking Secure Protocols

## Cel

Celem było poznanie bezpiecznych protokołów sieciowych wykorzystywanych do szyfrowania komunikacji oraz ochrony danych przesyłanych przez sieć.

---

## Wprowadzenie

Bezpieczne protokoły sieciowe zapewniają:

- poufność danych  
- integralność komunikacji  
- uwierzytelnienie użytkowników i serwerów  

Są one kluczowe w nowoczesnych systemach informatycznych oraz cyberbezpieczeństwie.

---

## TLS (Transport Layer Security)

TLS to protokół odpowiedzialny za szyfrowanie komunikacji sieciowej.

Zapewnia:

- szyfrowanie danych  
- ochronę przed podsłuchem  
- integralność przesyłanych informacji  

TLS jest następcą starszego protokołu SSL.

Znaczenie w cyberbezpieczeństwie:

- chroni dane przed przechwyceniem  
- zabezpiecza loginy, hasła i dane użytkowników  
- jest podstawą bezpiecznej komunikacji internetowej  

---

## HTTPS

HTTPS to bezpieczna wersja HTTP wykorzystująca TLS.

Dzięki HTTPS:

- komunikacja z serwerem jest szyfrowana  
- dane użytkownika są chronione  
- możliwe jest potwierdzenie tożsamości strony internetowej  

Znaczenie w cyberbezpieczeństwie:

- chroni przed atakami typu Man-in-the-Middle  
- zabezpiecza dane logowania i płatności  
- pomaga wykrywać fałszywe strony internetowe  

---

## SMTPS, POP3S i IMAPS

Są to bezpieczne wersje protokołów pocztowych wykorzystujące szyfrowanie TLS.

### SMTPS

Służy do bezpiecznego wysyłania wiadomości e-mail.

### POP3S

Pozwala bezpiecznie pobierać wiadomości z serwera pocztowego.

### IMAPS

Umożliwia bezpieczną synchronizację poczty między urządzeniami.

Znaczenie w cyberbezpieczeństwie:

- chronią wiadomości e-mail przed podsłuchem  
- zabezpieczają dane logowania użytkowników  
- zmniejszają ryzyko przejęcia kont pocztowych  

---

## SSH (Secure Shell)

SSH umożliwia bezpieczne zdalne połączenie z systemem.

Najczęściej wykorzystywany jest do:

- administracji serwerami  
- zdalnego wykonywania poleceń  
- bezpiecznego transferu danych  

Przykład połączenia:

```bash
ssh user@host
```

Znaczenie w cyberbezpieczeństwie:

- szyfruje komunikację z serwerem  
- zastępuje niebezpieczny Telnet  
- pozwala bezpiecznie zarządzać systemami Linux i serwerami  

---

## SFTP i FTPS

### SFTP

SFTP działa przez SSH i umożliwia bezpieczny transfer plików.

### FTPS

FTPS wykorzystuje TLS do zabezpieczenia klasycznego FTP.

Oba rozwiązania:

- szyfrują dane  
- chronią loginy i hasła  
- zwiększają bezpieczeństwo transferu plików  

Znaczenie w cyberbezpieczeństwie:

- eliminują problem przesyłania danych otwartym tekstem  
- są wykorzystywane w bezpiecznych środowiskach firmowych  
- pomagają chronić poufne pliki  

---

## VPN (Virtual Private Network)

VPN tworzy zaszyfrowany tunel pomiędzy urządzeniem użytkownika a siecią.

VPN pozwala:

- ukryć adres IP  
- zabezpieczyć ruch sieciowy  
- bezpiecznie korzystać z publicznych sieci Wi-Fi  

Znaczenie w cyberbezpieczeństwie:

- chroni ruch przed podsłuchem  
- zwiększa prywatność użytkownika  
- pomaga zabezpieczyć zdalną pracę  

---

## Podsumowanie

W ramach modułu poznano:

- TLS  
- HTTPS  
- SMTPS  
- POP3S  
- IMAPS  
- SSH  
- SFTP  
- FTPS  
- VPN  

Poznano również ich zastosowanie w ochronie komunikacji sieciowej.

---

## Zastosowanie w cyberbezpieczeństwie

Bezpieczne protokoły sieciowe są podstawą nowoczesnego bezpieczeństwa IT.

Znajomość tych technologii jest istotna w pracy:

- analityka SOC  
- administratora systemów  
- specjalisty ds. bezpieczeństwa  
- pentestera  

Pozwalają one:

- zabezpieczać komunikację  
- chronić dane użytkowników  
- analizować bezpieczny ruch sieciowy  
- wykrywać błędne konfiguracje bezpieczeństwa  
