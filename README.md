# k-drive
(Pronounced Key Drive) is a HMS-supportive web project.
![](https://i.insider.com/61d1c0e2aa741500193b2d18?width=450)
Przyszłe logo jako baner

### Cel
Implementacja aplikacji webowej do bezpiecznego przechowywania plików
tzw. Secure vault z użyciem możliwości oferowanych przez HSM

#### Technologię użyte w projekcie wybrane przez grupę:
	- Node.js
	- React.js
	- MongoDB albo alternatywy
	- Serwer Apache (WWW)
	- Serwer e-mail - jeszcze nie wybrany
	- Docker

## Założenia cyber security:
#### Odporność
- [ ] brute force - Cloudfare
- [ ] DDoS - Cloudfare
- [ ] spam - REcaptcha od Google albo alternatywa
- [ ] Kryptografia dzieki integracji modułu HSM

## Frontend (część wizualna):
#### Strona startowa
##### Panel logowania
 - [ ] pole "username"
 - [ ] pole "password"
 - [ ] przycisk "login"

![](https://i.insider.com/61d1c0e2aa741500193b2d18?width=450)	
Widok panelu logowania

##### Strona pomocy z logowaniem
 - [ ] pole "First name"
 - [ ] pole "Second name"
 - [ ] pole "e-mail lub username"
 - [ ] pole "Description"
		- Opis problemu
 - [ ] przycisk "Send request"

![](https://i.insider.com/61d1c0e2aa741500193b2d18?width=450)
Strona pomocy z logowaniem

##### Strona odzyskiwania hasła
- [ ] Pole "e-mail lub username"
	Po podaniu e-maila lub nazwy użytkownika na e-mail przyjdzie link z resetowaniem hasła Jak 2FA jest aktywne na koncie dana czynność zostanie zastąpiąna informacją o tym, aby zalogowac się kodem z np. Google Authenticator
- [ ] Przycisk "Send request"

![](https://i.insider.com/61d1c0e2aa741500193b2d18?width=450)
Strona odzyskiwania hasła

#### Strona aktywacji konta
Link zostaje przesłany przez serwer e-mail na polecenie administratora:
- [ ] pole "First name"
- [ ] pole "Second Name"
- [ ] pole "username"
- [ ] pole "password"
- [ ] przycisk "Create Account"

![](https://i.insider.com/61d1c0e2aa741500193b2d18?width=450)
Strona aktywacji konta

#### Strona resetowania hasła
- [ ] pole "new password"
- [ ] pole "new password"
- [ ] wskaźnik mocy i poprawności hasła
- [ ] przycisk "Change password")

![](https://i.insider.com/61d1c0e2aa741500193b2d18?width=450)
Strona resetowania hasła

## Strona administratora
### Dashboard
- [ ] Statysyki o zajętym miejscu
- [ ] Statystyki o użytkowników (akcje użytkowników / aktywnie zalogowani / zablokowani użytkownicy / nieaktywowani)

![](https://i.insider.com/61d1c0e2aa741500193b2d18?width=450)
Widok Dashboard

### Zakładki
#### Users (posortowani według czasu dodania do systemu):

|numer użytkownika :heavy_check_mark:|Stan uzytkownika :heavy_check_mark:|First Name :heavy_check_mark:|Second Name :heavy_check_mark:|Username :heavy_check_mark:|E-mail :heavy_check_mark:|Zajete miejsce/Zarezerwowane miejsce :heavy_check_mark:|Edit :heavy_check_mark:|Lock :heavy_check_mark:|Delete :heavy_check_mark:|
|--|--|--|--|--|--|--|--|--|--|
|1|200|Peter|Spiderman|xoxopp241|mail@mail.com| 200 MB / 500 MB|EDIT|LOCK|DELETE|
|2|100|Loid|Superman|asfasdfacx|mail@mail.com| 430 MB / 600 MB|EDIT|LOCK|DELETE|
|3|200|Damian|Icetea|hgdadfr241|mail@mail.com| 155 MB / 1400 MB|EDIT|LOCK|DELETE|

### Kody statusu użytkownika
|Code|Status|Description|
|--|--|--|
|100|INIT|Użytkownik został zaproszony, ale jeszcze nie odpowiedział na link aktywacyjny|
|200|OK|Uzytkownik odpowiedział na link aktywacyjny i ma dostęp do platformy|
|401|DISSABLED|Konto użytkownika zostało tymczasowo zablokowane przez administratora|
|403|LOCKED|Konto użytkownika jest atakowane|
|404|DELETED|Konta użytkownika zostało oznaczone do usunięcia przez administratora - tylko administrator może zarządzać kontem a dla poprzedniego użytkownika jest niedostępne do logowania |

![](https://i.insider.com/61d1c0e2aa741500193b2d18?width=450)
Zakładka Users

#### Drive
- [ ] Pole tekstowe z dozwolonomi rozszerzeniami
- [ ] Standardowe ustawienie maksymalnego czau sesji użytkownika

![](https://i.insider.com/61d1c0e2aa741500193b2d18?width=450)
Zakładka Drive

#### Helpdesk
- [ ] Lista zgłoszeń posortowana według czasu oraz priorytetu

|nr zgłoszenia|priorytet zgłoszenia|data zgłoszenia|otwórz zgłoszenie|
|--|--|--|--|
|1|top|21.03.2054 18:34|Open|

- [ ] Rozmowa ze zgłaszającym problem
- [ ] Dodawanie notatek do zgłoszenia
- [ ] Możliwość zamknięcia zgłoszenia

![](https://i.insider.com/61d1c0e2aa741500193b2d18?width=450)
Zakładka Zgłoszeń

![](https://i.insider.com/61d1c0e2aa741500193b2d18?width=450)
Okienko z problem

## Strona użytkownika główna

### Zakładki

#### Moje pliki
- [ ] Struktura plików użytkownika - foldery i pliki
- [ ] Wykres liniowy zajętego miejsca
- [ ] Udostępnianie plików
- [ ] Zmiana nazwy pliku
- [ ] Podgląd plików
	Standardowe formaty do podglądu
	- [ ] jpg, png, gif - Image formats
	- [ ] mp3, ogg - Music formats
	- [ ] mp4, avi, mkv - Movie formats
	- [ ] word, power point, excel, odt, pdf, txt - Document formats
- [ ] Edycja poszczególnych plików (plan na po zakończenie projektu)
- [ ] Usuwanie plików
- [ ] Kopiowanie plików
- [ ] Przenoszenie plików
- [ ] Wyświetlanie informacji o pliku
	- [ ] Typ pliku
	- [ ] Rozmiar Pliku
	- [ ] Czy plik jest udostępniony
	- [ ] Czy plik jest w koszu (widoczne tylko w koszu ale status do implementacji)
	- [ ] Czy plik jest ulubiony (komu i gdzie)
	- [ ] Data wrzucenia / Data utworzenia?
- [ ] Wyświetlanie ścieżki obecnego katalogu (z możliwością powrotu do poprzednich)
- [ ] Pobieranie plików/folderów jako zip

![Wstawić schemat](https://i.insider.com/61d1c0e2aa741500193b2d18?width=450)
Zakładka moje pliki

#### Ulubione
- [ ] Pokazywanie plików ulubionych w zakładce Ulubione
- [ ] Oznaczanie plików jako ulubione

![Wstawić schemat](https://i.insider.com/61d1c0e2aa741500193b2d18?width=450)
Zakładka ulubione

#### Udostepnione
- [ ] Wyświetlanie udostępnionych plików (posortowane według nazwy)
- [ ] Kopiowanie plików na swoje prywatne zasoby
- [ ] Możliwość pobrania pliku

![Wstawić schemat](https://i.insider.com/61d1c0e2aa741500193b2d18?width=450)
Zakładka udostępnione

#### Kosz
- [ ] Usuwanie plików
- [ ] Automatyczne usuwanie plików
- [ ] Przywracanie plików do poprzedniego miejsca

![](https://i.insider.com/61d1c0e2aa741500193b2d18?width=450)
Zakładka kosz

#### Ustawienia
- [ ] Możliwość skonfigurowania 2FA
- [ ] Możliwość zmiany hasła
- [ ] - Ustawienie automatycznego usuwania 

![](https://i.insider.com/61d1c0e2aa741500193b2d18?width=450)
Zakładka Ustawienia

# Ściąga MARKDOWN:
## Small heading
### Smallerrrr
###### Smallest

Strona do edycji pliku markdown: [link](https://stackedit.io/app#)

:white_check_mark: Zielony znaczek
:heavy_check_mark: Szary znaczek

\!\[Podpis](link) - Wstawianie obrazka ![](https://i.insider.com/61d1c0e2aa741500193b2d18?width=50)

- [ ] Checkbox
- [x] Oznaczony Checkbox

Tabelka
|1|2|
|-|-|
|3|4|
