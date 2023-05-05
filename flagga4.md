# Flagga 4 - *Lätt*
Beskrivning: *Hacka sidan så den tror du är admin*

Url: *https://hackainet.se/flag4*

## Writeup
När vi först går in på sidan ser vi en text som informerar oss att vi måste vara admin för att komma vidare.
![Skärmdump](https://user-images.githubusercontent.com/34009701/236375879-959f50d2-1731-47e1-bd53-730eb96ef53f.png)

Vi ser nu i adressfältet att det automatiskt lagts till GET-parametern `admin` och dess värde är 0. Vi testar att ändra värdet till 1.

Och då får vi svaret:
> Välkommen admin! Flaggan är: inet_gillas_av_admins

Flaggan är alltså `inet_gillas_av_admins`
