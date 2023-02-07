# TEST REPORT -PINTEREST

| Test case specification |  |
| --- | --- |
| Author | Anna Nowak |
| Document version | 1.0 |
| Creation date | 07.02.2023 12:15 |
| Application /link | https://pl.pinterest.com/ |
| Testing enviroment | OS<br/>Windows 10 Home (64 bit);<br/>Browsers<br/>Firefox ver 109.0.1 (64 bit),<br/>Chrome ver 109.0.5414.120 (64-bit) |
| Duration time | Testing: 4h
Creating report: 2h |

| No. | Test case | Expected result | Obtained result | Comments |
| --- | --- | --- | --- | --- |
| 1 | Login attempt: correct login & password | The user successfully logged into system. | The user successfully logged into system. |  |
| 2 | Login attempt: correct login & incorrect password | The user did not log into system. Validation message appears. | The user did not log into system. Message appears: “Wprowadzone hasło jest nieprawidłowe. Spróbuj jeszcze raz lub wykonaj następujące działanie: zresetuj hasło.” |  |
| 3 | Login attempt: non existence in base login & password | The user did not log into system. Validation message appears. | The user did not log into system. Two messages appears: “Podany e-mail nie należy do żadnego konta” and “Wyświetl zachowane dane logowania”. |  |
| 4 | Login attempt: empty fields e-mail and password. | The user did not log into system. Validation message appears. | The user did not log into system. Validation message appears: “Czegoś tu brakuje! Nie zapomnij dodać swojego adresu e-mail.” |  |
| 5 | Login attempt: correct login & password, checking password security | Entered password appeared as covered by symbols. | Entered password appeared as covered by symbols: “ . . . . “. |  |
| 6 | Login attempt: correct login & incorrect password entered 3 times in a row. | The user did not log into system. Validation message appears. | The user did not log into system. Validation box with messages appears: “Wygląda na to, że masz problemy z zalogowaniem. Na adres example@gmail.com wysłaliśmy email, który pomoże Ci się ponownie zalogować.” Also: buttons with “Wyślij ponownie e-mail”, “Kontynuuj przez Facebooka”, “Kontynuuj jako example@gmail.com” and “Rozumiem”. | Screenshot 1 |
| 7 | Login attempt: correct login & incorrect password entered 5 times in a row. | The user did not log into system. Validation message appears. Page blocked option for log in for a specific time.  | The user did not log into system. Validation box with messages appears: “Ups! Zbyt wiele prób logowania. Osiągnięto maksymalną liczbę prób logowania. Spróbuj ponownie za 30 minut.” Message box still appears after another login attempts.  | Screenshot 2 |
| 8 | Trying to save pinterest pin without being logged in.  | The user can’t save pin without being logged in. Validation message appears. | The user can’t save pin without being logged in. Validation message in a box appears: “Dołącz do Pinteresta, aby zapisać ten pomysł”. | Screenshot 3 |
| 9 | Clicking “Zapisz” to save pin on main page to your boards (logged user). | Pin is saved on boards. Validaion message appears. | Pin is saved on boards. Validaion message appears: “Zapisano na tablicy [board name]” and link to the undo option “Cofnij”. |  |
| 10 | Clicking “Zapisz” to save pin on main page to your boards (logged user) after you saved it earlier.  | Pin is deleted from boards. Validaion message appears. | Pin is deleted from boards. Validaion message appears: “Usunięto z tablicy”. |  |
| 11 | Clicking enter while “Search” box is empty. | Validation message appears. | Nothing is happened.  | BUG 001 |
| 12 | In box for searching pins text is written in english, not polish, after approx 1 second. Logged user. | Searching box title is translated from beggining to polish “Wyszukaj” and stays like that. | After approx one second searching box title changed from polish “Wyszukaj” to english “Search”. Chosen language in settings is polish.  | BUG 002 |

| BUG | Steps to recreate bug | Expected result | Obtained result | Comments | Priority |
| --- | --- | --- | --- | --- | --- |
| 001 | 1. Log in to the page https://pl.pinterest.com/
2. Click in and leave the “Search” box empty
3. Click Enter  | Validation message appears eg. “Write anything” | Nothing happened. | Suggestion -validation message should appear. | Low |
| 002 | 1. Log in to the page https://pl.pinterest.com/
2. Choose polish language in Ustawienia → Dane osobowe
3. Refresh page to see changing translation | Searching box title is translated from beggining to polish “Wyszukaj” and stays like that. | After approx one second searching box title changed from polish “Wyszukaj” to english “Search”. Chosen language in settings is polish.  | Screenshot 4 | Low |

![Screenshot 1](TEST%20REPORT%20-PINTEREST%20805c23fceabf41d687c593542610d70c/Screenshot_2.png)

Screenshot 1

![Screenshot 2](TEST%20REPORT%20-PINTEREST%20805c23fceabf41d687c593542610d70c/Screenshot_1.png)

Screenshot 2

![Screenshot 3](TEST%20REPORT%20-PINTEREST%20805c23fceabf41d687c593542610d70c/Screenshot_3.png)

Screenshot 3

![Screenshot 4](TEST%20REPORT%20-PINTEREST%20805c23fceabf41d687c593542610d70c/Screenshot_4.png)

Screenshot 4

[GitHub - Octarine-cat/Testing: Testowanie](https://github.com/Octarine-cat/Testing)
