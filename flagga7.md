# Flagga 7 - *Medelsvår*
Beskrivning: *Military-grade encryption*

Url: *https://hackainet.se/flag7*

## Writeup
När vi först går in på sidan möts vi av texten:
> Nu vet vi hur vi skyddar oss, med TRE LAGER KRYPTERING!!1!
> 
> NmUgNmYgNjkgNzQgNzAgNzkgNzIgNjMgNmUgNjUgNWYgNzkgNzIgNjEgNzQgNjkgNmMgNjkgNmQgNWYgNzMgNjUgNzMgNzUgNWYgNzQgNjUgNmUgNjk= 

Denna sträng ser ut att vara Base64-kodad. Detta kännetecknas av den slutar med likahetstecken.

Vi testar att avkoda den med [lämplig avkodare](https://www.base64decode.org/). Nu får vi fram en ny sträng.
> 6e 6f 69 74 70 79 72 63 6e 65 5f 79 72 61 74 69 6c 69 6d 5f 73 65 73 75 5f 74 65 6e 69

Detta ser ut att vara hexadecimala bytes. Vi testar att avkoda det med [lämplig avkodare](https://cryptii.com/pipes/binary-decoder).

Nu får vi ett svar som verkar vara flaggan i fel ordning.
> noitpyrcne_yratilim_sesu_teni

Vi testar att vända det rätt.
> inet_uses_military_encryption

Flaggan är alltså `inet_uses_military_encryption`
