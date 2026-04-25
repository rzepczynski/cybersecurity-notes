# Windows Fundamentals Part 1 — SOC Perspective

## Wprowadzenie

W tej części zapoznałem się z podstawami systemu operacyjnego Windows, jednak w podejściu ukierunkowanym na cyberbezpieczeństwo i pracę analityka SOC.

Skupiłem się nie tylko na tym *czym są* poszczególne komponenty systemu, ale również:

* jakie mają znaczenie w analizie incydentów,
* jak mogą być wykorzystywane przez atakujących,
* jakie artefakty i ślady pozostawiają w systemie.

---

## Edycje systemu Windows

Poznałem podstawowe edycje Windows:

* Home
* Pro
* Enterprise
* Education

### SOC perspective

* Edycje Enterprise i Pro są najczęściej spotykane w środowiskach firmowych, czyli tam, gdzie pracuje SOC.
* Różnice w funkcjach (np. Group Policy, BitLocker, Remote Desktop) wpływają na powierzchnię ataku.
* Brak funkcji security w edycjach Home może ograniczać monitoring i kontrolę.

---

## Pulpit i interfejs graficzny

Poznałem podstawowe elementy GUI Windows:

* Start Menu
* Taskbar
* File Explorer
* System tray

### SOC perspective

* GUI jest często pierwszym miejscem interakcji użytkownika z potencjalnie złośliwym oprogramowaniem.
* File Explorer może być używany do uruchamiania malware (np. ukryte rozszerzenia plików).
* Taskbar i autostart mogą zawierać persistence mechanizmy.

---

## Podstawy działania Windows

Zrozumiałem podstawowe funkcje systemu operacyjnego:

* zarządzanie procesami
* zarządzanie pamięcią
* obsługa sprzętu
* interakcja z użytkownikiem

### SOC perspective

* Procesy są kluczowe w analizie malware (process tree, parent-child relationships).
* Zarządzanie pamięcią ma znaczenie przy analizie exploitów.
* System jako warstwa pośrednia może ukrywać aktywność atakującego.

---

## System plików NTFS

Poznałem strukturę NTFS:

* pliki i katalogi
* atrybuty plików
* uprawnienia ACL
* struktura dysków

### SOC perspective

* Nieprawidłowe uprawnienia mogą umożliwić eskalację uprawnień.
* ACL abuse może być wykorzystany do persistence.
* NTFS może ukrywać dane (hidden files, alternate data streams).

---

## Katalog System32

Poznałem zawartość katalogu System32:

* pliki systemowe
* biblioteki DLL
* narzędzia administracyjne

### SOC perspective

* System32 zawiera legalne narzędzia, które mogą być nadużywane (Living Off The Land Binaries - LOLBins).
* Atakujący często wykorzystują wbudowane narzędzia Windows (np. cmd, powershell, rundll32).
* Analiza uruchomień z System32 jest ważna w detekcji malware.

---

## Konta użytkowników i uprawnienia

Poznałem:

* konta lokalne i Microsoft
* grupy użytkowników
* role i uprawnienia

### SOC perspective

* Eskalacja uprawnień często zaczyna się od konta standardowego.
* Konta administratora są głównym celem atakujących.
* Nietypowe logowania mogą wskazywać na kompromitację konta.

---

## UAC (User Account Control)

Zrozumiałem mechanizm UAC:

* kontrola uprawnień administracyjnych
* wymaganie potwierdzeń działań

### SOC perspective

* UAC może być obchodzony przez malware (bypass techniques).
* Podniesione uprawnienia są często celem ataków.
* Monitoring elevation requests może wskazywać na podejrzaną aktywność.

---

## Panel sterowania i Ustawienia

Poznałem narzędzia konfiguracji systemu:

* Control Panel
* Windows Settings

### SOC perspective

* Zmiany konfiguracji mogą wskazywać na działania atakującego.
* Wyłączenie zabezpieczeń (np. Defender) jest częstą techniką malware.
* SOC analizuje zmiany systemowe jako potencjalne IOC.

---

## Task Manager

Poznałem narzędzie do monitorowania systemu:

* procesy
* wydajność
* aplikacje startowe

### SOC perspective

* Analiza procesów pozwala wykryć malware (np. nietypowe child processes).
* High CPU/memory usage może wskazywać na cryptomining.
* Startup programs są częstym miejscem persistence.

---

## Podsumowanie

W tej części zdobyłem podstawową wiedzę o systemie Windows, jednak w podejściu ukierunkowanym na cyberbezpieczeństwo:

* zrozumiałem kluczowe komponenty systemu,
* przeanalizowałem ich znaczenie z perspektywy SOC,
* zacząłem łączyć funkcje systemu z potencjalnymi technikami ataków.

---

## Wnioski końcowe

Windows Fundamentals Part 1 stanowi fundament do dalszej nauki w obszarze cyberbezpieczeństwa i pracy w SOC. Pozwala zrozumieć, jak system działa, oraz w jaki sposób może być analizowany pod kątem incydentów bezpieczeństwa, śladów aktywności użytkownika oraz potencjalnych działań atakujących.
