# Flagga 1 - *Lätt*
Beskrivning: *Den enklaste flaggan, börja här*

Url: *https://hackainet.se/flag1*

## Writeup
När vi först går in på sidan ser vi en text som informerar oss att vi måste finna flaggan på den sidan.
![Skärmdump](https://user-images.githubusercontent.com/34009701/236286253-293e24ff-2ede-487a-8069-62939a3bae3b.png)

Detta får en att bli nyfiken på sidans HTML-kod. Vi kollar in dess källkod.

När vi läser igenom källkoden hittar vi denna HTML-kommentar längst upp:
```html
<!--

Grattis, du hittade hit!
Flaggan är: inet_gillar_flaggor

Det blir svårare sen ;D

-->
```

Flaggan är alltså `inet_gillar_flaggor`.
