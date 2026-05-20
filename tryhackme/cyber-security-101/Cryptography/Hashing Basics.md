# Hashing Basics

## Opis

Notatki z pokoju **Hashing Basics** na platformie TryHackMe.  
Celem pokoju było poznanie podstaw funkcji skrótu (hashing), bezpieczeństwa haseł oraz wykorzystania hashy w cyberbezpieczeństwie.

Hashing jest jednym z kluczowych mechanizmów wykorzystywanych w:

- przechowywaniu haseł  
- weryfikacji integralności plików  
- systemach uwierzytelniania  
- analizie incydentów bezpieczeństwa  
- wykrywaniu modyfikacji danych  

---

## Środowisko

- Platforma: TryHackMe  
- System: Linux AttackBox  
- Narzędzia:
  - sha256sum
  - hashcat
  - base64

---

# Zakres materiału

Podczas wykonywania pokoju poznano:

- działanie funkcji hashujących  
- różnice między szyfrowaniem a hashowaniem  
- zastosowanie algorytmu SHA256  
- bezpieczne przechowywanie haseł  
- rozpoznawanie typów hashy  
- podstawy password crackingu  
- sprawdzanie integralności plików  
- dekodowanie danych Base64  

---

# Zadania

## Task 1 — Introduction

Wprowadzenie do podstaw hashingu oraz jego zastosowań w cyberbezpieczeństwie.

Omówiono rolę funkcji skrótu w ochronie danych oraz weryfikacji integralności informacji.

---

## Task 2 — Hash Functions

Wygenerowano hash SHA256 dla przykładowego pliku.

Użyta komenda:

```bash
sha256sum ~/Hashing-Basics/Task-2/passport.jpg
```

Screenshot:

<img width="945" height="148" alt="ss1" src="https://github.com/user-attachments/assets/cbf2706b-2f71-447b-aa80-e64743831924" />

### Znaczenie w cyberbezpieczeństwie

Hashing umożliwia sprawdzenie, czy plik został zmodyfikowany.  
Zmiana nawet jednego bajtu powoduje wygenerowanie całkowicie innego hasha.

Mechanizm ten jest powszechnie wykorzystywany podczas:

- analizy malware  
- weryfikacji integralności plików  
- wykrywania manipulacji danymi  

---

## Task 3 — Insecure Password Storage for Authentication

Omówiono zagrożenia wynikające z przechowywania haseł w postaci plaintext.

Przedstawiono ryzyko związane z wyciekiem baz danych oraz znaczenie stosowania bezpiecznych metod przechowywania haseł.

### Potencjalne zagrożenia

- przejęcie kont użytkowników  
- credential stuffing  
- reuse password attacks  
- eskalacja uprawnień po wycieku danych  

---

## Task 4 — Using Hashing for Secure Password Storage

Poznano wykorzystanie soli (salt) oraz nowoczesnych algorytmów hashujących do bezpiecznego przechowywania haseł.

Omówiono znaczenie ochrony przed:

- rainbow tables  
- brute force attacks  
- dictionary attacks  

---

## Task 5 — Recognising Password Hashes

Analizowano charakterystyczne cechy różnych typów hashy.

Rozpoznawanie formatów hashy jest istotne podczas:

- testów penetracyjnych  
- analizy wycieków danych  
- działań red team  
- analizy incydentów bezpieczeństwa  

---

## Task 6 — Password Cracking

Przykład użycia Hashcat do łamania hasha z wykorzystaniem słownika `rockyou.txt`.

Podgląd słownika:

```bash
head -n 20 rockyou.txt
```

Screenshot:

<img width="765" height="466" alt="ss2" src="https://github.com/user-attachments/assets/0a0bcf82-9708-4ae7-ae57-c83a451b64aa" />

Uruchomienie Hashcat:

```bash
hashcat -m 3200 -a 0 ~/Hashing-Basics/Task-6/hash1.txt rockyou.txt
```

Screenshot:

<img width="942" height="682" alt="ss3" src="https://github.com/user-attachments/assets/2e6933ab-9772-43f9-8f44-dc1744462fc2" />

### Znaczenie w cyberbezpieczeństwie

Password cracking pozwala ocenić siłę haseł oraz wykrywać słabe zabezpieczenia w organizacji.

Techniki tego typu są wykorzystywane podczas:

- audytów bezpieczeństwa  
- testów penetracyjnych  
- analiz powłamaniowych  
- red teamingu  

---

## Task 7 — Hashing for Integrity Checking

Zweryfikowano integralność pliku przy użyciu SHA256.

Użyta komenda:

```bash
sha256sum ~/Hashing-Basics/Task-7/libgcrypt-1.11.0.tar.bz2
```

Screenshot:

<img width="938" height="98" alt="ss4" src="https://github.com/user-attachments/assets/46d29f08-b9aa-4612-b0c7-ab004b4a34ee" />

### Znaczenie w cyberbezpieczeństwie

Weryfikacja integralności plików pozwala wykryć:

- modyfikacje plików  
- uszkodzenie danych  
- podmianę oprogramowania  
- malware ukryte w zmodyfikowanych plikach  

---

## Task 8 — Conclusion

Dekodowanie danych zapisanych w Base64.

Użyta komenda:

```bash
base64 -d ~/Hashing-Basics/Task-8/decode-this.txt
```

Screenshot:

<img width="863" height="70" alt="ss5" src="https://github.com/user-attachments/assets/a08a41b8-f87a-4d87-a43a-1351c5a51a2e" />

### Znaczenie w cyberbezpieczeństwie

Kodowanie Base64 jest często spotykane podczas:

- analizy malware  
- analizy phishingu  
- analizy logów  
- pracy z danymi przesyłanymi przez HTTP/API  

---

# Wnioski

Podczas wykonywania pokoju:

- generowano hashe SHA256  
- analizowano bezpieczeństwo przechowywania haseł  
- używano Hashcat do password crackingu  
- sprawdzano integralność plików  
- dekodowano dane Base64  

---

# Znaczenie w cyberbezpieczeństwie

Umiejętność pracy z hashami jest istotna w rolach takich jak:

- SOC Analyst  
- Incident Responder  
- Penetration Tester  
- Blue Team  
- Digital Forensics Analyst  

Hashing stanowi podstawowy element bezpieczeństwa systemów oraz ochrony danych użytkowników.
