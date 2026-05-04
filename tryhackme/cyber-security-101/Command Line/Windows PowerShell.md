# Windows PowerShell

## Wprowadzenie

Pokój **Windows PowerShell** na platformie TryHackMe wprowadza do podstaw pracy z zaawansowanym narzędziem administracyjnym systemu Windows. PowerShell jest znacznie bardziej rozbudowany niż klasyczny CMD i pozwala na automatyzację zadań, analizę systemu oraz zarządzanie środowiskiem w sposób obiektowy.

Znajomość PowerShell jest kluczowa w pracy administratora systemów, analityka SOC oraz specjalisty cyberbezpieczeństwa, szczególnie w środowiskach korporacyjnych i Active Directory.

---

## Cele pokoju

- Poznanie podstaw działania PowerShell
- Nauka pracy z cmdletami
- Analiza użytkowników i procesów systemowych
- Monitorowanie usług i połączeń sieciowych
- Wprowadzenie do filtrowania i przetwarzania danych

---

## Podstawowe informacje o PowerShell

PowerShell opiera się na tzw. **cmdletach**, które mają strukturę:

```powershell
Verb-Noun
```

Przykłady:

- `Get-Process`
- `Get-Service`
- `Get-LocalUser`

Dzięki temu polecenia są czytelne i logiczne.

---

## Wyświetlanie użytkowników systemu

Polecenie pozwala na wyświetlenie lokalnych użytkowników systemu.

```powershell
Get-LocalUser
```

Jest to przydatne podczas analizy kont użytkowników oraz w kontekście bezpieczeństwa systemu.

<img width="959" height="838" alt="get-localuser" src="https://github.com/user-attachments/assets/aacb71d0-12f3-46c8-ac58-a01b073a6c0d" />

---

## Analiza połączeń sieciowych

Polecenie umożliwia sprawdzenie aktywnych połączeń TCP w systemie.

```powershell
Get-NetTCPConnection
```

Pozwala to na identyfikację podejrzanych połączeń oraz analizę aktywności sieciowej.

<img width="902" height="690" alt="get-netTCPconnection" src="https://github.com/user-attachments/assets/9ff1f9c5-d92d-4cd4-baef-6374c11c2925" />

---

## Monitorowanie procesów

Polecenie wyświetla aktualnie uruchomione procesy.

```powershell
Get-Process
```

Jest to odpowiednik polecenia `tasklist` z CMD, ale oferuje znacznie więcej możliwości analizy.

<img width="947" height="814" alt="get-process" src="https://github.com/user-attachments/assets/65d5d75c-159e-4a44-a055-55d608cbc6c8" />

---

## Analiza usług systemowych (filtrowanie)

PowerShell pozwala na zaawansowane filtrowanie wyników.

```powershell
Get-Service | Where-Object {$_.DisplayName -like "*merry*"}
```

Polecenie wyszukuje usługi zawierające w nazwie określony ciąg znaków.

Można również wybrać konkretne właściwości:

```powershell
Get-Service | Where-Object {$_.DisplayName -like "*merry*"} | Select-Object
```

Dzięki temu możliwa jest dokładna analiza usług działających w systemie.

<img width="945" height="258" alt="get-service, where-object" src="https://github.com/user-attachments/assets/818ab77e-22d3-4576-883d-7393f8a45792" />

---

## Praca z danymi i pipeline

Jedną z najważniejszych funkcji PowerShell jest **pipeline (`|`)**, który pozwala przekazywać dane między poleceniami.

Przykład:

```powershell
Get-Service | Where-Object {$_.Status -eq "Running"}
```

Dzięki temu można:

- filtrować dane
- sortować wyniki
- wybierać konkretne informacje
- automatyzować analizę systemu

---

## Znaczenie w cyberbezpieczeństwie

PowerShell jest jednym z najważniejszych narzędzi w pracy:

- Junior SOC Analyst
- Security Analyst
- Incident Responder
- System Administrator
- Blue Team Specialist

Jest często wykorzystywany zarówno przez administratorów, jak i przez atakujących, dlatego jego znajomość jest kluczowa w analizie incydentów.

---

## Zdobyte umiejętności

Po ukończeniu pokoju potrafię:

- korzystać z podstawowych cmdletów PowerShell
- analizować użytkowników systemu
- sprawdzać aktywne połączenia sieciowe
- monitorować procesy i usługi
- filtrować dane za pomocą pipeline
- wykorzystywać PowerShell w analizie systemu

---

## Podsumowanie

Pokój **Windows PowerShell** dostarczył podstaw do pracy z jednym z najważniejszych narzędzi administracyjnych systemu Windows.

PowerShell znacząco rozszerza możliwości klasycznego CMD i jest niezbędny w nowoczesnych środowiskach IT oraz cyberbezpieczeństwie.

Stanowi solidny fundament do dalszej nauki automatyzacji, Active Directory oraz pracy w środowisku SOC.
