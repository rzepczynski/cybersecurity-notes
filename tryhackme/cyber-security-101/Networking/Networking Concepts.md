# Networking Concepts

## Cel

Celem było poznanie podstawowych modeli sieciowych oraz zrozumienie sposobu komunikacji urządzeń w sieci komputerowej.

---

## Wprowadzenie

Sieci komputerowe opierają się na modelach komunikacyjnych, które definiują sposób przesyłania danych między urządzeniami.

Najważniejsze modele wykorzystywane w sieciach to:

- model OSI  
- model TCP/IP  

Zrozumienie tych modeli jest podstawą analizy ruchu sieciowego oraz cyberbezpieczeństwa.

---

## Model OSI

Model OSI (Open Systems Interconnection) składa się z 7 warstw:

1. Physical  
2. Data Link  
3. Network  
4. Transport  
5. Session  
6. Presentation  
7. Application  

Każda warstwa odpowiada za określone zadania związane z komunikacją sieciową.

### Zadania poszczególnych warstw

- Physical – transmisja danych w postaci sygnałów  
- Data Link – komunikacja między urządzeniami w sieci lokalnej  
- Network – routing i adresacja IP  
- Transport – niezawodność transmisji  
- Session – zarządzanie sesjami komunikacji  
- Presentation – formatowanie i szyfrowanie danych  
- Application – komunikacja aplikacji użytkownika  

Znaczenie w cyberbezpieczeństwie:
- analiza ruchu sieciowego wymaga znajomości warstw OSI  
- ataki mogą być wykonywane na różnych warstwach modelu  
- pomaga identyfikować miejsce występowania problemów i zagrożeń  

---

## Model TCP/IP

Model TCP/IP jest praktycznym modelem używanym w Internecie.

Składa się z 4 warstw:

1. Application  
2. Transport  
3. Internet  
4. Network Access  

Model ten odpowiada za rzeczywistą komunikację urządzeń w sieciach komputerowych.

Znaczenie w cyberbezpieczeństwie:
- większość analiz ruchu sieciowego opiera się na modelu TCP/IP  
- wykorzystywany podczas monitorowania i analizy pakietów  
- pomaga zrozumieć sposób działania protokołów sieciowych  

---

## Adresy IP i podsieci

Adres IP identyfikuje urządzenie w sieci.

Wyróżnia się:
- IPv4  
- IPv6  

Maska podsieci określa:
- część sieciową adresu  
- część hosta  

Podsieci umożliwiają podział większych sieci na mniejsze segmenty.

Znaczenie w cyberbezpieczeństwie:
- analiza adresacji IP jest kluczowa podczas rekonesansu  
- błędna konfiguracja podsieci może prowadzić do problemów bezpieczeństwa  
- segmentacja sieci zwiększa poziom ochrony infrastruktury  

---

## UDP i TCP

### TCP (Transmission Control Protocol)

TCP zapewnia:
- niezawodność transmisji  
- kontrolę błędów  
- ustanawianie połączenia  

Wykorzystywany m.in. przez:
- HTTP/HTTPS  
- SSH  
- FTP  

### UDP (User Datagram Protocol)

UDP:
- działa szybciej niż TCP  
- nie zapewnia kontroli połączenia  
- używany jest tam, gdzie liczy się szybkość transmisji  

Wykorzystywany m.in. przez:
- DNS  
- VoIP  
- streaming  

Znaczenie w cyberbezpieczeństwie:
- TCP i UDP są często analizowane podczas skanowania portów  
- wiele ataków sieciowych wykorzystuje protokoły transportowe  
- analiza ruchu TCP/UDP pomaga wykrywać anomalie w sieci  

---

## Enkapsulacja

Enkapsulacja to proces dodawania informacji nagłówkowych do danych podczas przechodzenia przez kolejne warstwy modelu sieciowego.

Każda warstwa:
- dodaje własne informacje  
- przekazuje dane do następnej warstwy  

Po stronie odbiorcy dane są dekapsulowane.

Znaczenie w cyberbezpieczeństwie:
- analiza enkapsulacji jest ważna podczas przechwytywania pakietów  
- pomaga zrozumieć strukturę ruchu sieciowego  
- wykorzystywana podczas analizy w Wireshark i tcpdump  

---

## Telnet

Telnet umożliwia zdalne połączenie z urządzeniem przez sieć.

Działa w postaci nieszyfrowanej.

Zagrożenia:
- dane przesyłane są otwartym tekstem  
- login i hasło mogą zostać przechwycone  

Z tego powodu Telnet został zastąpiony przez SSH.

Znaczenie w cyberbezpieczeństwie:
- Telnet jest uznawany za niebezpieczny protokół  
- często wykrywany podczas audytów bezpieczeństwa  
- obecność Telnetu może wskazywać na słabe zabezpieczenia infrastruktury  

---

## Podsumowanie

W ramach modułu poznano:

- model OSI  
- model TCP/IP  
- adresację IP i podsieci  
- działanie TCP i UDP  
- proces enkapsulacji  
- protokół Telnet  

Zrozumienie tych zagadnień jest podstawą dalszej nauki sieci komputerowych oraz cyberbezpieczeństwa.

---

## Zastosowanie w cyberbezpieczeństwie

Znajomość podstaw sieci jest niezbędna w pracy:

- analityka SOC  
- pentestera  
- administratora bezpieczeństwa  
- specjalisty ds. bezpieczeństwa sieci  

Pozwala na:
- analizę ruchu sieciowego  
- wykrywanie anomalii  
- identyfikację podatności i zagrożeń  
- lepsze rozumienie działania ataków sieciowych  
