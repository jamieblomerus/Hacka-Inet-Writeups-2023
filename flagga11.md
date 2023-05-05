# Flagga 11 - *Medelsvår*
Beskrivning: *Du får ingen hjälp*

Url: *https://hackainet.se/flag11*

## Writeup
När vi öppnar sidan får vi upp detta felmeddelande:
> {"fel":"Den här sidan är inte tillgänglig från en webbläsare"}

Vi testar att läsa in sidan från terminalen:
```bash
curl https://hackainet.se/flag11
```

Detta lyckades och vi fick svaret:
> {"flag":"inet_alltid_i_framkant"}

Flaggan är alltså `inet_alltid_i_framkant`
