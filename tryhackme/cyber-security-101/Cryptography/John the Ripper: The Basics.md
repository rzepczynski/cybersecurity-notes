# John the Ripper: The Basics

## Opis

Notatki z pokoju **John the Ripper: The Basics** na platformie TryHackMe.  
Pokój wprowadza do podstaw password crackingu oraz wykorzystania narzędzia John the Ripper do łamania hashy i odzyskiwania haseł.

John the Ripper jest jednym z najpopularniejszych narzędzi wykorzystywanych podczas:

- testów penetracyjnych  
- audytów bezpieczeństwa  
- analiz powłamaniowych  
- oceny siły haseł  
- działań Red Team i Blue Team  

---

## Środowisko

- Platforma: TryHackMe  
- System: Linux AttackBox  
- Narzędzia:
  - John the Ripper
  - hash-id.py
  - rockyou.txt

---

# Zakres materiału

Podczas wykonywania pokoju poznano:

- podstawowe pojęcia związane z password crackingiem  
- rozpoznawanie typów hashy  
- łamanie hashy MD5 oraz SHA512  
- wykorzystanie wordlist  
- analizę hashy systemów Linux  
- podstawy odzyskiwania haseł  

---

# Zadania

## Task 1 — Introduction

Wprowadzenie do narzędzia John the Ripper oraz podstaw password crackingu.

Omówiono zastosowanie narzędzia podczas testów bezpieczeństwa oraz analiz bezpieczeństwa haseł.

---

## Task 2 — Basic Terms

Poznano podstawowe pojęcia związane z hashingiem oraz password crackingiem:

- hash  
- salt  
- wordlist  
- dictionary attack  
- brute force  

---

## Task 3 — Setting Up Your System

Przygotowano środowisko pracy oraz narzędzia potrzebne do analizy hashy.

Rozpoznanie typu hasha:

```bash
python3 hash-id.py
```

Screenshot:

<img width="1236" height="486" alt="1" src="https://github.com/user-attachments/assets/20d11f47-b573-4af1-9c59-56b24957cf4f" />

### Znaczenie w cyberbezpieczeństwie

Identyfikacja typu hasha jest kluczowa przed rozpoczęciem password crackingu, ponieważ różne algorytmy wymagają różnych metod ataku.

---

## Task 4 — Cracking Basic Hashes

Łamanie podstawowego hasha MD5 przy użyciu słownika `rockyou.txt`.

Użyta komenda:

```bash
john --format=raw-md5 --wordlist=/usr/share/wordlists/rockyou.txt hash1.txt
```

Screenshot:

<img width="1222" height="221" alt="2" src="https://github.com/user-attachments/assets/8a81c612-83d9-4262-b8ca-d3d3ac42190f" />

### Znaczenie w cyberbezpieczeństwie

Password cracking pozwala wykrywać słabe hasła oraz oceniać bezpieczeństwo systemów uwierzytelniania.

Techniki tego typu są wykorzystywane podczas:

- audytów bezpieczeństwa  
- testów penetracyjnych  
- analiz wycieków danych  
- analiz powłamaniowych  

---

## Task 5 — Cracking Windows Authentication Hashes

Omówiono podstawy łamania hashy wykorzystywanych w systemach Windows.

Przedstawiono znaczenie bezpieczeństwa haseł użytkowników domenowych i lokalnych.

---

## Task 6 — Cracking /etc/shadow Hashes

Łamanie hashy SHA512 przechowywanych w systemie Linux.

Użyta komenda:

```bash
john --wordlist=/usr/share/wordlists/rockyou.txt hash1.txt --format=sha512crypt unshadowed.txt
```

Screenshot:

<img width="1242" height="242" alt="3" src="https://github.com/user-attachments/assets/b99d9cd4-24d4-4b81-b13e-fad75164170f" />

### Znaczenie w cyberbezpieczeństwie

Plik `/etc/shadow` zawiera hashe użytkowników systemu Linux.  
Uzyskanie dostępu do tych danych może prowadzić do przejęcia kont użytkowników oraz eskalacji uprawnień.

---

## Task 7 — Single Crack Mode

Poznano podstawy trybu Single Crack Mode wykorzystywanego do inteligentnego generowania kandydatów na hasła.

---

## Task 8 — Custom Rules

Omówiono wykorzystanie custom rules do modyfikowania słowników oraz zwiększania skuteczności password crackingu.

---

## Task 9 — Cracking Password Protected Zip Files

Poznano podstawy odzyskiwania haseł do archiwów ZIP.

---

## Task 10 — Cracking Password-Protected RAR Archives

Omówiono podstawy łamania zabezpieczeń archiwów RAR.

---

## Task 11 — Cracking SSH Keys with John

Przedstawiono możliwość odzyskiwania haseł zabezpieczających klucze SSH.

---

## Task 12 — Further Reading

Dodatkowe materiały dotyczące password crackingu oraz narzędzia John the Ripper.

---

# Wnioski

Podczas wykonywania pokoju:

- identyfikowano typy hashy  
- używano John the Ripper do password crackingu  
- analizowano bezpieczeństwo haseł  
- pracowano z hashami Linux i Windows  
- wykorzystywano wordlisty do odzyskiwania haseł  

---

# Znaczenie w cyberbezpieczeństwie

Znajomość password crackingu jest istotna podczas:

- audytów bezpieczeństwa  
- testów penetracyjnych  
- działań Red Team  
- analiz incydentów bezpieczeństwa  
- oceny polityki haseł w organizacji  

Umiejętność pracy z hashami i narzędziami typu John the Ripper pomaga wykrywać słabe zabezpieczenia oraz poprawiać bezpieczeństwo systemów.
