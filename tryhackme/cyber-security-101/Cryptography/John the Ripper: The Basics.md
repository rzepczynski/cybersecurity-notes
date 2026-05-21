# John the Ripper: The Basics

## Opis

Ten pokój wprowadzał do podstaw łamania haseł za pomocą narzędzia John the Ripper.  
Ćwiczenia skupiały się na identyfikacji typów hashy, przeprowadzaniu ataków słownikowych oraz zrozumieniu, w jaki sposób słabe hasła mogą zostać wykorzystane podczas testów bezpieczeństwa.

Pokój pokazał również znaczenie silnych polityk haseł oraz bezpiecznego przechowywania danych uwierzytelniających.

---

# Cele

- Zrozumienie podstaw łamania haseł
- Identyfikacja popularnych typów hashy
- Używanie John the Ripper z odpowiednimi formatami
- Przeprowadzanie ataków słownikowych przy użyciu wordlist
- Łamanie hashy systemów Linux
- Zrozumienie zagrożeń wynikających ze słabych haseł

---

# Wykorzystane narzędzia

- John the Ripper
- hash-id
- Linux CLI
- rockyou.txt

---

# Identyfikacja Hashy

Przed próbą złamania hasha ważne jest określenie, jaki algorytm został użyty do jego wygenerowania.

## Użyta komenda

```bash
python3 hash-id.py
```

## Wyjaśnienie

- Uruchamia narzędzie `hash-id`
- Próbuje rozpoznać algorytm haszujący
- Pomaga dobrać odpowiedni format dla John the Ripper

## Screenshot

<img width="1236" height="486" alt="1" src="https://github.com/user-attachments/assets/ef1c6b51-475d-4a46-8e46-e0abcc759229" />

---

# Łamanie Hashy MD5

John the Ripper umożliwia przeprowadzanie ataków słownikowych z wykorzystaniem dużych list haseł, takich jak `rockyou.txt`.

## Użyta komenda

```bash
john --format=raw-md5 --wordlist=/usr/share/wordlists/rockyou.txt hash1.txt
```

## Wyjaśnienie

- `--format=raw-md5` określa typ hasha
- `--wordlist` wskazuje listę haseł używaną podczas ataku
- `hash1.txt` zawiera docelowy hash

## Security Insight

MD5 jest obecnie uznawany za niebezpieczny algorytm do przechowywania haseł.  
Szybkie algorytmy haszujące są podatne na ataki słownikowe oraz brute-force.

## Screenshot

<img width="1222" height="221" alt="2" src="https://github.com/user-attachments/assets/f28b08ad-c377-47c5-9482-ecf8496fa3a8" />

---

# Łamanie Hashy SHA512Crypt

Systemy Linux często przechowują hasła w pliku `/etc/shadow`, wykorzystując silniejsze algorytmy takie jak SHA512Crypt.

## Użyta komenda

```bash
john --wordlist=/usr/share/wordlists/rockyou.txt --format=sha512crypt unshadowed.txt
```

## Wyjaśnienie

- Używa formatu `sha512crypt`
- Wykonuje atak słownikowy na hashe systemu Linux
- `unshadowed.txt` zawiera połączone dane z `/etc/passwd` oraz `/etc/shadow`

## Security Insight

Nawet silne algorytmy haszujące stają się podatne, gdy użytkownicy używają słabych haseł.  
Złożone hasła oraz MFA znacząco zwiększają poziom bezpieczeństwa kont.

## Screenshot

<img width="1242" height="242" alt="3" src="https://github.com/user-attachments/assets/cae976f5-76dc-4b66-8d30-09ae2e039dee" />

---

# Najważniejsze Wnioski

- Przed próbą łamania hasha należy rozpoznać jego typ
- Słabe hasła są podatne na ataki słownikowe
- MD5 nie powinien być używany do przechowywania haseł
- Linux wykorzystuje SHA512Crypt w pliku `/etc/shadow`
- Silne hasła i MFA znacząco poprawiają bezpieczeństwo
- John the Ripper jest skutecznym narzędziem do audytu bezpieczeństwa haseł

---

# Umiejętności

- Audyt bezpieczeństwa haseł
- Identyfikacja hashy
- Obsługa Linux CLI
- Ataki słownikowe
- Analiza bezpieczeństwa haseł
- Praca z narzędziami cybersecurity

---

# Podsumowanie

Pokój zapewnił praktyczne wprowadzenie do pracy z John the Ripper oraz pokazał, w jaki sposób specjaliści cybersecurity mogą testować siłę haseł przy użyciu rzeczywistych technik.

Ćwiczenia podkreśliły znaczenie:

- bezpiecznego przechowywania haseł,
- silnych polityk haseł,
- praktyk defensywnego bezpieczeństwa,
- oraz regularnego audytu haseł w środowiskach IT.
