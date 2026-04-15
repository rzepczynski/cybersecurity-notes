# Nmap Scan – scanme.nmap.org

## Cel

Celem było przeskanowanie serwera w celu wykrycia otwartych portów oraz identyfikacji usług działających na tych portach.

---

## Narzędzie

* Nmap – narzędzie do skanowania sieci i rekonesansu

---

## Wykonane komendy

```bash
nmap scanme.nmap.org
nmap -sV scanme.nmap.org
nmap -sS -sV scanme.nmap.org
```

---

## Wyniki skanowania

### Port 22 – SSH

* Status: otwarty
* Opis: umożliwia zdalne logowanie do serwera

### Port 80 – HTTP

* Status: otwarty
* Opis: serwer udostępnia stronę internetową

### Port 9929

* Status: otwarty
* Opis: niestandardowa usługa (może być używana do testów)

### Port 31337

* Status: otwarty
* Opis: niestandardowy port (często używany w środowiskach testowych)

---

## Analiza (-sV)

Polecenie:

```bash
nmap -sV scanme.nmap.org
```

Pozwala określić dokładne wersje usług działających na portach.

---

## Stealth scan (-sS)

Polecenie:

```bash
nmap -sS -sV scanme.nmap.org
```

* tzw. "SYN scan"
* mniej wykrywalny niż standardowy scan
* używany w testach penetracyjnych

---

## Potencjalne ryzyka

### Port 22 (SSH)

* możliwość ataków brute-force (zgadywanie haseł)
* potencjalny dostęp do systemu po uzyskaniu danych logowania

### Port 80 (HTTP)

* możliwość znalezienia podatności webowych
* potencjalne ataki: XSS, SQL Injection

### Porty 9929 i 31337

* niestandardowe usługi mogą zawierać błędy
* często są interesujące z punktu widzenia pentestera

---

## Co to jest rekonesans (Recon)

Rekonesans to pierwszy etap testów bezpieczeństwa,
polegający na zbieraniu informacji o celu (np. otwarte porty, usługi, systemy).

---

## Czego się nauczyłem

* jak używać narzędzia Nmap
* czym są porty i usługi
* jak analizować wyniki skanowania
* czym jest rekonesans w cyberbezpieczeństwie

---

## Dowód

<img width="1319" height="749" alt="image" src="https://github.com/user-attachments/assets/1ca6cb97-7aa5-4b4c-a1bb-7d688eebf0ba" />
