# Flagga 5 - *Medelsvår*
Beskrivning: *Nu börjar det bli lite krångligare*

Url: *https://hackainet.se/flag5*

## Writeup
När vi först går in på sidan möts vi av ett autentiseringsformuler, som kräver lösenord för att ge oss flaggan.
![Skärmdump](https://user-images.githubusercontent.com/34009701/236377852-ba393fe2-d750-4f0d-86d8-f59ff318b311.png)

Vi testar att kolla på sidans källkod och finner då denna kod.

``` html
<script src="js/flag5.js"></script>
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

Vi ser att `correct_password` och `the_flag` är deklarerade som variablar. Och att det inkluderas ett skript som heter `flag5.js`. Vi testar att kolla innehållet av `js/flag5.js`.

Innehållet av detta skript är:

```js
var correct_password = 'junkrat';
var the_flag = 'inet_not_now_ratjunk';
``` 

Flaggan är alltså `inet_not_now_ratjunk`
