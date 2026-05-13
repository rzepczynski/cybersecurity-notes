# Nmap: The Basics

## Cel

Celem pokoju było poznanie podstaw działania narzędzia Nmap wykorzystywanego do:

- wykrywania aktywnych hostów
- skanowania portów
- identyfikacji usług sieciowych
- analizy dostępnych usług w sieci

---

## Środowisko

- Platforma: TryHackMe
- Narzędzie: Nmap
- System: Linux AttackBox

---

## Host Discovery

Nmap pozwala wykrywać aktywne hosty w sieci.

Wykonano skanowanie zakresu adresów IP:

```bash
nmap -sL 192.168.0.1/27
```

Opcja `-sL` wyświetla listę hostów bez wykonywania pełnego skanowania.

<img width="960" height="725" alt="1" src="https://github.com/user-attachments/assets/458152d0-5645-4e71-82e1-cebaf3aa2021" />

---

## Port Scanning

Wykonano pełne skanowanie portów hosta:

```bash
nmap -p- 10.112.185.239
```

Opcja `-p-` skanuje wszystkie porty TCP (1–65535).

Podczas analizy wykryto otwartą usługę HTTP działającą na porcie `8008`.

Następnie otwarto usługę w przeglądarce:

```plaintext
http://10.112.185.239:8008/
```

<img width="943" height="937" alt="2" src="https://github.com/user-attachments/assets/8b94629c-640f-4817-a06d-582f710122ef" />

---

## Najważniejsze informacje

### Host Discovery

- identyfikacja hostów w sieci
- enumeracja adresów IP
- szybkie rozpoznanie środowiska

### Port Scanning

- wykrywanie otwartych portów
- identyfikacja usług sieciowych
- analiza dostępnych serwisów

---

## Znaczenie w cyberbezpieczeństwie

Nmap jest jednym z podstawowych narzędzi używanych przez:

- Pentesterów
- SOC Analystów
- Administratorów sieci
- Blue Team
- Red Team

Narzędzie umożliwia szybkie rozpoznanie infrastruktury sieciowej oraz identyfikację potencjalnych usług dostępnych dla użytkowników i atakujących.

---

## Podsumowanie

Podczas pokoju przećwiczono:

- wykrywanie hostów
- skanowanie portów
- identyfikację usług sieciowych
- podstawową enumerację sieci

Pokój stanowi podstawę do dalszej nauki rekonesansu oraz analizy usług sieciowych.

