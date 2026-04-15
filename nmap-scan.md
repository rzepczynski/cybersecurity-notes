Skanowanie nmap

Co zrobiłem:
- zainstalowałem nmap
- wykonałem skan scanme.nmap.org

Wyniki:
- port 22 (SSH) – otwarty
- port 80 (HTTP) – otwarty
- port 9929 – otwarty
- port 31337 – otwarty

Wnioski:
Serwer posiada kilka otwartych portów, które mogą umożliwiać różne usługi

Kolejny skan:

Użyłem komendy: 
- nmap -sV scanme.nmap.org

Wniosek:
Można sprawdzić jakie dokładnie usługi działają na portach
