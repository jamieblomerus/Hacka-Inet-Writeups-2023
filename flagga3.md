# Flagga 3 - *Lätt*
Beskrivning: *Klarar du den tredje flaggan?*

Url: *https://hackainet.se/flag3*

## Writeup
När vi först går in på sidan möts vi av ett autentiseringsformuler, som kräver lösenord för att ge oss flaggan.
![Skärmdump](https://user-images.githubusercontent.com/34009701/236374546-88b8ae8a-7d28-4ca0-aacd-a479795ef2f1.png)

Vi testar att kolla på sidans källkod och finner då detta inline-skript.

``` html
<script>
function check_password() {
  var correct_password = 'sommar2023';
  var the_flag = 'inet_gillar_sommaren';
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

I detta skript finner vi både lösenordet och flaggan som variablar deklarerade i klartext.

Flaggan är alltså `inet_gillar_sommaren
