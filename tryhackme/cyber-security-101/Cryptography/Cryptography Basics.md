# Cryptography Basics

## Cel

Celem pokoju było poznanie podstaw kryptografii oraz sposobów ochrony danych przy użyciu szyfrowania.

Omówiono podstawowe pojęcia związane z:

- szyfrowaniem danych
- poufnością informacji
- szyframi historycznymi
- kryptografią symetryczną i asymetryczną
- podstawami matematyki wykorzystywanej w kryptografii

---

## Środowisko

- Platforma: TryHackMe
- Tematyka: Cryptography
- Zakres: podstawy kryptografii i szyfrowania

---

## Wprowadzenie do kryptografii

Kryptografia służy do ochrony danych przed nieautoryzowanym dostępem.

Główne cele kryptografii:

- poufność danych
- integralność informacji
- uwierzytelnianie użytkowników
- bezpieczeństwo komunikacji

Kryptografia jest wykorzystywana m.in. w:

- HTTPS
- VPN
- SSH
- bankowości internetowej
- systemach logowania

---

## Plaintext i Ciphertext

### Plaintext

Plaintext to oryginalna, czytelna wiadomość przed zaszyfrowaniem.

Przykład:

```plaintext
Hello World
```

---

### Ciphertext

Ciphertext to zaszyfrowana forma wiadomości, która bez klucza jest trudna do odczytania.

Przykład:

```plaintext
U2FsdGVkX1...
```

Proces szyfrowania zamienia plaintext w ciphertext przy użyciu algorytmu kryptograficznego.

---

## Historyczne szyfry

Omówiono podstawowe historyczne metody szyfrowania:

### Caesar Cipher

Szyfr Cezara polega na przesuwaniu liter alfabetu o określoną liczbę pozycji.

Przykład:

```plaintext
A → D
B → E
C → F
```

---

### Vigenère Cipher

Szyfr Vigenère wykorzystuje słowo kluczowe do szyfrowania tekstu.

Był znacznie bezpieczniejszy od prostych szyfrów podstawieniowych.

---

## Rodzaje szyfrowania

### Szyfrowanie symetryczne

Ten sam klucz służy do:

- szyfrowania
- odszyfrowywania danych

Przykłady:

- AES
- DES

Zalety:

- szybkie działanie
- wydajność

Wady:

- problem bezpiecznego przekazywania klucza

---

### Szyfrowanie asymetryczne

Wykorzystuje dwa klucze:

- publiczny
- prywatny

Przykłady:

- RSA
- ECC

Zastosowania:

- HTTPS
- SSH
- podpis cyfrowy

---

## Podstawy matematyki w kryptografii

Kryptografia wykorzystuje matematykę do ochrony danych.

W pokoju omówiono m.in.:

- działania modulo
- liczby pierwsze
- podstawowe operacje matematyczne wykorzystywane w szyfrowaniu

Matematyka stanowi fundament nowoczesnych algorytmów kryptograficznych.

---

## Znaczenie w cyberbezpieczeństwie

Kryptografia jest kluczowym elementem cyberbezpieczeństwa.

Znajomość podstaw kryptografii pomaga zrozumieć:

- działanie HTTPS
- bezpieczną komunikację
- uwierzytelnianie użytkowników
- ochronę danych
- podpisy cyfrowe

---

## Podsumowanie

Podczas pokoju przećwiczono:

- podstawowe pojęcia kryptograficzne
- różnice między plaintext i ciphertext
- historyczne szyfry
- szyfrowanie symetryczne i asymetryczne
- podstawowe zagadnienia matematyczne związane z kryptografią

Pokój stanowi podstawę do dalszej nauki bezpieczeństwa komunikacji oraz nowoczesnych metod szyfrowania.

