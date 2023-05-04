# Flagga 2 - *Lätt*
Beskrivning: *Lite svårare att lösa*

Url: *https://hackainet.se/flag2*

## Writeup
Precis som på förra ser vi en text som informerar oss att vi måste finna flaggan på den sidan.
![Skärmdump](https://user-images.githubusercontent.com/34009701/236289221-87760312-41e6-4b4a-810a-317d63907113.png)

På förra utmaningen hittade vi flaggan i källkoden. Vi testar att kolla där igen.

När vi läser igenom källkoden hittar vi denna HTML-kommentar längst upp:
```html
<!--

Den här är svårare, flaggan är typ krypterad!

Flaggan är: lqhw_hw_wx_kdfnduh

Veni, vidi, vici.

-->
```

Denna flagga verkar dock vara krypterad eller liknande men bevarar rätt format för en flagga. Kan detta möjligen vara ceasar cipher?

Vi testar att avkoda det med [en lämplig avkodare](https://www.dcode.fr/caesar-cipher). Detta ger oss upptäckten att det sannerligen är ceasar cipher och att förskjutningen är 3 bokstäver.

Flaggan är alltså `inet_et_tu_hackare`.
