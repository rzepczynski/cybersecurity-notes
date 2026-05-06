# Networking Essentials

## Cel

Celem było poznanie podstawowych protokołów sieciowych oraz zrozumienie, w jaki sposób urządzenia komunikują się w sieci.

---

## Wprowadzenie

Sieci komputerowe umożliwiają komunikację między urządzeniami poprzez przesyłanie danych w postaci pakietów.  
Aby komunikacja była możliwa, wykorzystywane są różne protokoły sieciowe.

---

## DHCP (Dynamic Host Configuration Protocol)

DHCP automatycznie przydziela urządzeniom w sieci:

- adres IP  
- maskę podsieci  
- bramę domyślną  
- serwery DNS  

Dzięki temu użytkownik nie musi ręcznie konfigurować ustawień sieciowych.

Znaczenie w cyberbezpieczeństwie:
- ataki typu DHCP spoofing mogą przejąć ruch sieciowy  
- analiza DHCP pozwala wykrywać nieautoryzowane urządzenia w sieci  

---

## ARP (Address Resolution Protocol)

ARP służy do mapowania adresu IP na adres MAC w sieci lokalnej.

Proces:
1. urządzenie wysyła zapytanie ARP  
2. urządzenie docelowe odpowiada swoim adresem MAC  

Znaczenie w cyberbezpieczeństwie:
- podatny na ataki ARP spoofing  
- używany w atakach typu Man-in-the-Middle (MITM)  

---

## ICMP (Internet Control Message Protocol)

ICMP służy do diagnostyki sieci.

Najczęściej używany w:
- `ping`
- `traceroute`

Pozwala sprawdzić:
- czy host jest dostępny  
- opóźnienia w sieci  

Znaczenie w cyberbezpieczeństwie:
- używany do rekonesansu sieci  
- może być wykorzystywany w atakach (np. ICMP flood)  

---

## Routing

Routing to proces przekazywania pakietów między sieciami.

Router:
- analizuje adres docelowy  
- wybiera najlepszą trasę  

Znaczenie w cyberbezpieczeństwie:
- błędna konfiguracja może prowadzić do przejęcia ruchu  
- routing może być manipulowany przez atakującego  

---

## NAT (Network Address Translation)

NAT umożliwia wielu urządzeniom korzystanie z jednego publicznego adresu IP.

Działa poprzez:
- zamianę adresów prywatnych na publiczne  

Znaczenie w cyberbezpieczeństwie:
- ukrywa strukturę sieci wewnętrznej  
- utrudnia bezpośredni dostęp do urządzeń  
- może utrudniać analizę ruchu  

---

## Podsumowanie

W ramach tego modułu poznano:

- podstawowe protokoły sieciowe  
- sposób komunikacji w sieci  
- działanie DHCP, ARP, ICMP, Routing i NAT  

Zrozumienie tych mechanizmów jest kluczowe w analizie ruchu sieciowego oraz wykrywaniu potencjalnych zagrożeń.

---

## Zastosowanie w cyberbezpieczeństwie

Znajomość podstaw sieci jest niezbędna w pracy:

- analityka SOC  
- pentestera  
- specjalisty ds. bezpieczeństwa  

Pozwala na:
- analizę ruchu sieciowego  
- wykrywanie anomalii  
- identyfikację ataków sieciowych  
