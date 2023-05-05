# Flagga 8 - *Medelsvår*
Beskrivning: *Genvägar är inte alltid senvägar*

Url: *https://hackainet.se/flag8*

## Writeup
När vi först går in på sidan möts vi av ett autentiseringsformulär, som kräver lösenord för att ge oss flaggan. 
![Skärmdump](https://user-images.githubusercontent.com/34009701/236502188-e4d6d3f8-3315-4908-836d-64ffb4c6de5e.png)

Vi testar att kolla på sidans källkod och finner då denna kod.
```html
<script src="js/flag8-obfuscated.js"></script>
<script>
function check_password() {
  var user_input = document.getElementById('thepassword').value;
  var result_obj = document.getElementById('theresult');
  result_obj.classList.remove('fade-in');
  void result_obj.offsetWidth;
  if (user_input == correct_password) {
    result_obj.innerHTML = 'Grattis! Flaggan du letar efter är: ' + the_flag;
  } else {
    result_obj.innerHTML = 'Fel lösenord!';
  }
  result_obj.classList.add('fade-in');
  return false;
}
</script>
```

Nu ser vi att det inkluderas ett skript som heter `flag8-obfuscated.js`. Då vi redan ser i namnet att den är obfuskerad, kan vi välja genvägen att istället hämta innehållet av `the_flag` från konsolen.

Vi inspekterar sidan, öppnar konsolen och exekverar `the_flag` som ger svaret:
> "inet_heroes_never_dies"

Flaggan är alltså `inet_heroes_never_dies`.
