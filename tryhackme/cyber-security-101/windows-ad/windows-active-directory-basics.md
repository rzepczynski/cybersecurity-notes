# Active Directory Basics

## Wprowadzenie

Active Directory jest jedną z najważniejszych usług katalogowych wykorzystywanych w środowiskach korporacyjnych opartych o system Windows. Umożliwia centralne zarządzanie użytkownikami, komputerami, zasobami oraz politykami bezpieczeństwa w całej organizacji.

Ukończenie tego modułu pozwoliło mi zrozumieć podstawową architekturę Active Directory oraz jego kluczową rolę w administracji i cyberbezpieczeństwie.

---

## Domeny Windows

Domena to logiczna grupa komputerów i użytkowników zarządzana centralnie przez kontroler domeny.

### Najważniejsze cechy domeny

- centralne uwierzytelnianie użytkowników,
- jednolite zarządzanie uprawnieniami,
- łatwiejsza administracja zasobami,
- możliwość stosowania polityk bezpieczeństwa.

### Znaczenie praktyczne

Domeny stanowią podstawę infrastruktury w większości średnich i dużych przedsiębiorstw.

---

## Active Directory

Active Directory przechowuje informacje o wszystkich obiektach znajdujących się w domenie.

### Przykładowe obiekty

- użytkownicy,
- komputery,
- grupy,
- drukarki,
- jednostki organizacyjne (OU).

### Główne zadania AD

- uwierzytelnianie,
- autoryzacja,
- zarządzanie zasobami,
- egzekwowanie polityk bezpieczeństwa.

---

## Zarządzanie użytkownikami w Active Directory

Konta użytkowników są podstawowym elementem każdej domeny.

### Możliwe operacje

- tworzenie nowych kont,
- resetowanie haseł,
- blokowanie i odblokowywanie kont,
- przypisywanie do grup.

### Znaczenie w cyberbezpieczeństwie

Nieprawidłowe zarządzanie kontami użytkowników jest jedną z najczęstszych przyczyn incydentów bezpieczeństwa.

---

## Zarządzanie komputerami w Active Directory

Komputery dołączone do domeny są centralnie zarządzane przez administratorów.

### Możliwości

- dodawanie urządzeń do domeny,
- organizowanie komputerów w OU,
- wdrażanie konfiguracji,
- zarządzanie uprawnieniami.

---

## Group Policy (GPO)

Group Policy umożliwia centralne zarządzanie konfiguracją systemów i użytkowników.

### Przykładowe zastosowania

- wymuszanie polityki haseł,
- blokowanie urządzeń USB,
- konfiguracja zapory sieciowej,
- automatyczna instalacja oprogramowania.

### Znaczenie

GPO jest jednym z najpotężniejszych narzędzi administracyjnych w środowisku Windows.

---

## Metody uwierzytelniania

Active Directory wykorzystuje różne protokoły uwierzytelniania.

### Najważniejsze

- Kerberos,
- NTLM.

### Kerberos

Domyślny i preferowany mechanizm uwierzytelniania w nowoczesnych domenach Windows.

### NTLM

Starszy protokół, nadal spotykany w niektórych środowiskach.

---

## Drzewa, Lasy i Relacje Zaufania

Zaawansowane struktury umożliwiające skalowanie środowiska.

### Tree

Zbiór domen o wspólnej przestrzeni nazw.

### Forest

Najwyższy poziom struktury Active Directory.

### Trusts

Relacje zaufania pomiędzy domenami lub lasami.

---

## Zastosowanie w Cyberbezpieczeństwie

Znajomość Active Directory jest kluczowa dla specjalistów bezpieczeństwa.

### Dlaczego?

- większość ataków w środowiskach korporacyjnych dotyczy AD,
- błędna konfiguracja może prowadzić do eskalacji uprawnień,
- AD jest częstym celem ataków typu lateral movement.

---

## Podsumowanie

W ramach tego modułu poznałem:

- architekturę domen Windows,
- podstawowe komponenty Active Directory,
- zarządzanie użytkownikami i komputerami,
- działanie Group Policy,
- metody uwierzytelniania,
- strukturę lasów i relacji zaufania.

---

## Zdobyte Umiejętności

Po ukończeniu modułu potrafię:

- wyjaśnić działanie domeny Windows,
- rozpoznać kluczowe komponenty Active Directory,
- zrozumieć rolę GPO w organizacji,
- opisać podstawowe metody uwierzytelniania,
- wskazać znaczenie AD w cyberbezpieczeństwie.

---

## Wnioski Końcowe

Active Directory stanowi fundament większości środowisk korporacyjnych opartych na systemach Windows. Zrozumienie jego działania jest niezbędne zarówno dla administratorów, jak i analityków bezpieczeństwa.

Jest to jedna z najważniejszych technologii, które powinien znać każdy przyszły SOC Analyst, Security Analyst lub Pentester.
