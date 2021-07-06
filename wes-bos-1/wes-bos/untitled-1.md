# KONAMI CODE

![](../../.gitbook/assets/image%20%2825%29.png)

```markup
<script src="http://www.cornify.com/js/cornify.js"></script>
<script>
    const pressed = [];
    const secretCode = 'konami';
    window.addEventListener('keyup',(e) => {
        console.log(e.key);
        pressed.push(e.key);
        pressed.splice(-secretCode.length - 1, pressed.length - secretCode.length);
        if(pressed.join('').includes(secretCode)){
            console.log('ding ding');
            cornify_add();
        }
        console.log(pressed);
    });
</script>
```

