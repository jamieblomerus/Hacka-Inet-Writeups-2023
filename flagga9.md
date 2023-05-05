# Flagga 9 - *Medelsvår*
Beskrivning: *Ta dig förbi spärren*

Url: *https://hackainet.se/flag9*

## Writeup
När vi går in på sidan finner vi ett temporärt avaktiverat inloggningsformulär för e-postadress.
![Skärmdump](https://user-images.githubusercontent.com/34009701/236504927-50557164-aa0c-4caf-ae7c-17073bcddf99.png)

Då avstängningen enbart är temporär blir man nyfiken på huruvida back-end:en är uppdaterad eller om den fortfarande accepterar inloggningsförfrågningar.

Vi testar att inspektera och ta bort disabled parametrarna på samtliga avaktiverade element i formuläret och sedan skicka iväg förfrågan med påhittad e-postaddress.

Detta ger svaret:
> Bra gjort, du tog dig förbi det! Flaggan är: inet_stoppas_aldrig

Flaggan är alltså `inet_stoppas_aldrig`
