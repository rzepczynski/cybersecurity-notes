# Public Key Cryptography Basics

## Cel

Celem pokoju było poznanie podstaw kryptografii asymetrycznej oraz sposobów wykorzystania kluczy publicznych i prywatnych w nowoczesnych systemach bezpieczeństwa.

Omówiono działanie:

- RSA
- Diffie-Hellman
- SSH
- podpisów cyfrowych
- certyfikatów
- PGP i GPG

---

## Środowisko

- Platforma: TryHackMe
- Tematyka: Cryptography
- Zakres: kryptografia asymetryczna i klucze publiczne

---

## Kryptografia asymetryczna

Kryptografia asymetryczna wykorzystuje dwa klucze:

- klucz publiczny
- klucz prywatny

Klucz publiczny może być udostępniany innym użytkownikom, natomiast klucz prywatny powinien pozostać tajny.

Zastosowania:

- HTTPS
- SSH
- podpisy cyfrowe
- certyfikaty
- bezpieczna komunikacja

---

## RSA

RSA jest jednym z najpopularniejszych algorytmów kryptografii asymetrycznej.

Wykorzystuje:

- liczby pierwsze
- operacje matematyczne
- parę kluczy publiczny/prywatny

RSA umożliwia:

- szyfrowanie danych
- podpisywanie wiadomości
- uwierzytelnianie użytkowników

---

## Diffie-Hellman Key Exchange

Mechanizm Diffie-Hellman umożliwia bezpieczną wymianę kluczy przez niezaufaną sieć.

Pozwala dwóm stronom:

- uzgodnić wspólny sekret
- bez wcześniejszego przesyłania klucza prywatnego

Technika ta jest wykorzystywana m.in. w:

- HTTPS
- VPN
- SSH

---

## SSH

SSH (Secure Shell) umożliwia bezpieczne zdalne połączenie z systemem.

SSH wykorzystuje kryptografię asymetryczną do:

- uwierzytelniania użytkownika
- ochrony komunikacji
- szyfrowania danych przesyłanych przez sieć

Najczęściej wykorzystywane są:

- klucze RSA
- Ed25519
- ECDSA

---

## Podpisy cyfrowe i certyfikaty

Podpis cyfrowy pozwala potwierdzić:

- autentyczność nadawcy
- integralność danych

Certyfikaty cyfrowe są wykorzystywane do:

- weryfikacji tożsamości serwera
- zabezpieczania połączeń HTTPS
- budowania zaufania w sieci

---

## PGP i GPG

PGP (Pretty Good Privacy) oraz GPG (GNU Privacy Guard) służą do:

- szyfrowania wiadomości
- podpisywania danych
- ochrony komunikacji e-mail

Narzędzia te wykorzystują kryptografię asymetryczną i pary kluczy.

---

## Najważniejsze informacje

### Kryptografia asymetryczna

- wykorzystuje dwa klucze
- zapewnia bezpieczną komunikację
- jest podstawą nowoczesnych systemów bezpieczeństwa

### SSH

- umożliwia bezpieczny dostęp zdalny
- szyfruje komunikację
- wykorzystuje klucze kryptograficzne

### Certyfikaty

- potwierdzają tożsamość
- zabezpieczają połączenia HTTPS
- budują zaufanie w sieci

---

## Znaczenie w cyberbezpieczeństwie

Kryptografia asymetryczna jest kluczowym elementem bezpieczeństwa sieciowego.

Znajomość tych zagadnień pomaga zrozumieć:

- działanie HTTPS
- uwierzytelnianie użytkowników
- podpisy cyfrowe
- bezpieczeństwo SSH
- ochronę komunikacji

---

## Podsumowanie

Podczas pokoju przećwiczono:

- podstawy kryptografii asymetrycznej
- działanie RSA
- wymianę kluczy Diffie-Hellman
- działanie SSH
- podpisy cyfrowe i certyfikaty
- podstawy PGP i GPG

Pokój stanowi podstawę do dalszej nauki bezpiecznej komunikacji oraz nowoczesnych systemów kryptograficznych.

