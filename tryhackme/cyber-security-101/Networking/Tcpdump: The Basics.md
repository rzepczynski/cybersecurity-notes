# Tcpdump: The Basics

## Cel

Celem było poznanie podstaw narzędzia Tcpdump oraz nauka przechwytywania i filtrowania ruchu sieciowego z poziomu terminala Linux.

---

## Wprowadzenie

Tcpdump to narzędzie działające w terminalu służące do przechwytywania i analizy pakietów sieciowych.

Pozwala:

- monitorować ruch sieciowy  
- filtrować pakiety  
- analizować protokoły  
- diagnozować problemy sieciowe  
- wykrywać podejrzaną aktywność  

Tcpdump jest często wykorzystywany przez:

- administratorów sieci  
- analityków SOC  
- pentesterów  
- specjalistów cyberbezpieczeństwa  

---

## Podstawowe przechwytywanie pakietów

Przechwycono ruch sieciowy z interfejsu `ens5`.

Użyta komenda:

```bash
sudo tcpdump -i ens5 -c 5 -n
```

Opis parametrów:

- `-i ens5` → wybór interfejsu sieciowego  
- `-c 5` → przechwycenie 5 pakietów  
- `-n` → wyłączenie tłumaczenia nazw hostów  

<img width="944" height="640" alt="resolving" src="https://github.com/user-attachments/assets/e118b6cb-30ec-4340-ae90-7ec411083df1" />

Znaczenie w cyberbezpieczeństwie:

- analiza ruchu pozwala wykrywać nietypową aktywność  
- monitorowanie pakietów pomaga diagnozować problemy sieciowe  
- podstawowa analiza ruchu jest ważna w SOC i Blue Team  

---

## Filtrowanie pakietów i analiza PCAP

Przeanalizowano pakiety zapisane w pliku `traffic.pcap`.

Użyte komendy:

```bash
sudo tcpdump -r traffic.pcap icmp -n | wc
sudo tcpdump -r traffic.pcap arp and host 192.168.124.137
sudo tcpdump -r traffic.pcap port 53 -A
```

Wykonano:

- analizę pakietów ICMP  
- filtrowanie ruchu ARP dla konkretnego hosta  
- analizę ruchu DNS na porcie 53  

<img width="940" height="290" alt="2" src="https://github.com/user-attachments/assets/38ec5062-93b5-4086-9ff2-da0ccd35513e" />

Znaczenie w cyberbezpieczeństwie:

- analiza DNS pomaga wykrywać złośliwe domeny  
- analiza ARP może pomóc wykryć spoofing  
- filtrowanie ruchu jest podstawą analizy sieciowej  

---

## Zaawansowane filtrowanie TCP

Przeanalizowano pakiety TCP zawierające flagę RST oraz duże pakiety sieciowe.

Użyte komendy:

```bash
sudo tcpdump -r traffic.pcap 'tcp[tcpflags] == tcp-rst' | wc -l
sudo tcpdump -r traffic.pcap 'greater 15000' -n
```

Wykonano:

- analizę pakietów TCP RST  
- wyszukiwanie dużych pakietów sieciowych  

<img width="939" height="693" alt="3" src="https://github.com/user-attachments/assets/a77a61f6-f478-4b2a-bca3-0450d6836106" />

Znaczenie w cyberbezpieczeństwie:

- analiza flag TCP pomaga wykrywać anomalie sieciowe  
- duża liczba pakietów RST może wskazywać na skanowanie sieci  
- nietypowo duże pakiety mogą sugerować podejrzaną aktywność  

---

## Wyświetlanie adresów MAC

Przeanalizowano pakiety ARP wraz z nagłówkami Ethernet.

Użyta komenda:

```bash
sudo tcpdump -r traffic.pcap arp -e
```

Opis parametru:

- `-e` → wyświetlenie nagłówka Ethernet oraz adresów MAC  

<img width="939" height="178" alt="4" src="https://github.com/user-attachments/assets/630e48c0-54d3-413e-bcbe-192396ace49d" />

Znaczenie w cyberbezpieczeństwie:

- analiza adresów MAC pomaga identyfikować urządzenia w sieci  
- umożliwia wykrywanie spoofingu MAC  
- wspiera analizę komunikacji lokalnej  

---

## Podsumowanie

W ramach modułu poznano:

- podstawy działania Tcpdump  
- przechwytywanie pakietów  
- filtrowanie ruchu sieciowego  
- analizę DNS, ARP i ICMP  
- analizę flag TCP  
- analizę plików PCAP  

Poznano również praktyczne zastosowanie Tcpdump w analizie bezpieczeństwa sieciowego.

---

## Zastosowanie w cyberbezpieczeństwie

Tcpdump jest jednym z podstawowych narzędzi używanych podczas analizy ruchu sieciowego.

Znajomość Tcpdump pomaga w:

- monitorowaniu sieci  
- analizie incydentów bezpieczeństwa  
- wykrywaniu podejrzanej aktywności  
- analizie malware  
- diagnostyce problemów sieciowych  

Narzędzie jest często wykorzystywane przez:

- SOC Analyst  
- Blue Team  
- Pentester  
- Network Security Engineer  
