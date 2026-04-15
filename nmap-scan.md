Nmap Scan – scanme.nmap.org

Cel

Celem było przeskanowanie serwera w celu wykrycia otwartych portów i usług.

Narzędzie

* Nmap

Wykonane komendy
- nmap scanme.nmap.org
- nmap -sV scanme.nmap.org

Wyniki

Otwarty port 22

* Usługa: SSH
* Opis: umożliwia zdalne logowanie do serwera

Otwarty port 80

* Usługa: HTTP
* Opis: serwer udostępnia stronę internetową

Otwarty port 9929

* Usługa: nieznana / niestandardowa
* Opis: może być używana do testów lub niestandardowych aplikacji

Otwarty port 31337

* Usługa: niestandardowa
* Opis: często używany port testowy / hackerski (leet)

Dodatkowa analiza (-sV)

Polecenie:
- nmap -sV scanme.nmap.org

Pozwala sprawdzić dokładne wersje usług działających na portach.

Wnioski

* Serwer posiada kilka otwartych portów
* Najważniejsze usługi to SSH i HTTP
* Dodatkowe porty mogą stanowić potencjalne ryzyko bezpieczeństwa
* Skanowanie portów to pierwszy krok w procesie rekonesansu (recon)

Czego się nauczyłem

* jak używać Nmap
* czym są porty i usługi
* jak interpretować wyniki skanowania

Potencjalne ryzyka

Port 22 (SSH)

* możliwość prób brute-force (ataków na hasło)
* dostęp do systemu jeśli dane logowania zostaną złamane

Port 80 (HTTP)

* możliwość analizy strony (np. podatności webowe)
* potencjalne ataki typu XSS / SQL Injection

Porty 9929 i 31337

* niestandardowe usługi mogą być podatne na błędy
* trudniejsze do wykrycia → często ciekawsze dla pentestera
