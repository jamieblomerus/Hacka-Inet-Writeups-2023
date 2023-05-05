# Flagga 10 - *Medelsvår*
Beskrivning: *Få sidan att tro att du är admin*

Url: *https://hackainet.se/flag10*

## Writeup
När vi först går in på sidan ser vi en text som informerar oss att vi måste vara admin för att komma vidare. 
![Skärmdump](https://user-images.githubusercontent.com/34009701/236506792-1593cf0a-4c6a-46b9-9f1d-c72c33eeb2a1.png)

Vi testar att fånga in förfrågan i Burp Suite för att analysera den och finna sårbarheter.
![Skärmdump](https://user-images.githubusercontent.com/34009701/236508944-dc4d5ccd-5b81-4e0e-8697-b49f12394c93.png)

Här ser vi att den skickar med kakan `is_admin` som har värdet `0`. Vi testar att ändra värdet till `1` och skicka förfrågan igen.

Detta fungerade och vi får nu svaret:
> Välkommen admin! Flaggan är: inet_kakor_vs_pingviner

Flaggan är alltså `inet_kakor_vs_pingviner`.
