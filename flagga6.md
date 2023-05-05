# Flagga 6 - *Medelsvår*
Beskrivning: *Var gömmer sig flaggan?*

Url: *https://hackainet.se/flag6*

## Writeup
När vi först går in på sidan ser vi enbart en bild. Undra om flaggan gömmer sig där i?
![Skärmdump](https://user-images.githubusercontent.com/34009701/236379397-8a584e80-1b6d-4e29-aa63-5449dd8b580a.png)

Vi testar att läsa in filen som rådata i Burp Suite:
![Skärmdump](https://user-images.githubusercontent.com/34009701/236379807-352ad008-7352-43df-9049-80e1c2d0de51.png)

Nu kan vi se att bilden innehåller texten `inet_likes_their_doctor` vilket även är våran flagga.

Flaggan är alltså `inet_likes_their_doctor`.
