# HTMLElement, HTMLCollection

## 단수와 복수

```javascript
    var li = document.getElementById('active');
    console.log(li.constructor.name);//HTMLLIElement (li 태그)
    var lis = document.getElementsByTagName('li');
    console.log(lis.constructor.name);//HTMLCollection 유사배
```

{% hint style="info" %}
constructor.name  객체에 이름을 알 수 있는 코
{% endhint %}

```markup
<a id="anchor" href="http://opentutorials.org">opentutorials</a>
<ul>
    <li>HTML</li>
    <li>CSS</li>
    <li id="list">JavaScript</li>
</ul>
<input type="button" id="button" value="button" />
<script>
    var target = document.getElementById('list');
    console.log(target.constructor.name);//HTMLLIElement
 
    var target = document.getElementById('anchor');
    console.log(target.constructor.name);//HTMLAnchorElement
 
    var target = document.getElementById('button');
    console.log(target.constructor.name);//HTMLInputElement
 
</script>
```

## DOM Tree

![](../../../../.gitbook/assets/image%20%284%29.png)

 HTMLElement는 Element의 자식이고 Element는 Node의 자식이다. Node는 Object의 자식이다. 이러한 관계를 DOM Tree라고 한다.

## HTMLCollection

```markup
<!DOCTYPE html>
<html>
<body>
<ul>
    <li>HTML</li>
    <li>CSS</li>
    <li id="active">JavaScript</li>
</ul>
<script>
console.group('before');
var lis = document.getElementsByTagName('li');
for(var i = 0; i < lis.length; i++){
    console.log(lis[i]);
}
console.groupEnd();
console.group('after');
lis[1].parentNode.removeChild(lis[1]);   //removeChild 삭제.
for(var i = 0; i < lis.length; i++){
    console.log(lis[i]);
}
console.groupEnd();
</script>
</body>
</html>
```

