# 폼

## submit

submit은 폼의 정보를 서버로 전송하는 명령인 submit시에 일어난다.

```markup
<form id="target" action="result.html">
    <label for="name">name</label> <input id="name" type="name" />
    <input type="submit" />
</form>
<script>
var t = document.getElementById('target');
t.addEventListener('submit', function(event){
    if(document.getElementById('name').value.length === 0){
        alert('Name 필드의 값이 누락 되었습니다');
        event.preventDefault();
    }
});
</script>
```

## change

change는 폼 컨트롤의 값이 변경 되었을 때 발생하는 이벤트

```markup
<p id="result"></p>
<input id="target" type="name" />
<script>
var t = document.getElementById('target');
t.addEventListener('change', function(event){
    document.getElementById('result').innerHTML=event.target.value;
});
</script>
```

## blur, focus

```markup
<input id="target" type="name" />
<script>
var t = document.getElementById('target');
t.addEventListener('blur', function(event){
    alert('blur');  
});
t.addEventListener('focus', function(event){
    alert('focus'); 
});
</script>
```

