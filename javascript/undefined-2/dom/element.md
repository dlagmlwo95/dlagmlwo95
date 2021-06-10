# Element 객체

![](../../../.gitbook/assets/image%20%285%29.png)



**식별자**

문서내에서 특정한 엘리먼트를 식별하기 위한 용도로 사용되는 API

* Element.classList
* Element.className
* Element.id
* Element.tagName

**조회**

엘리먼트의 하위 엘리먼트를 조회하는 API

* Element.getElementsByClassName
* Element.getElementsByTagName
* Element.querySelector
* Element.querySelectorAll

**속성**

엘리먼트의 속성을 알아내고 변경하는 API

* Element.getAttribute\(name\)
* Element.setAttribute\(name, value\)
* Element.hasAttribute\(name\);
* Element.removeAttribute\(name\);

## 식별자 API

### Element.tagName

```markup
<ul>
    <li>html</li>
    <li>css</li>
    <li id="active" class="important current">JavaScript</li>
</ul>
<script>
console.log(document.getElementById('active').tagName) //읽기전용임.
</script>
```

### Element.id

```markup
<script>
var active = document.getElementById('active');
console.log(active.id);  //active
active.id = 'deactive';  //여기서 deactive로 바ㅏ꿈.
console.log(active.id);  //deactive
</script>
```

### Element.className

```markup
<script>
//불편함.
var active = document.getElementById('active');
// class 값을 변경할 때는 프로퍼티의 이름으로 className을 사용한다.
active.className = "important current";  //이름바꾸기.
console.log(active.className);

// 클래스를 추가할 때는 아래와 같이 문자열의 더한다.
active.className += " readed"
</script>
```

### Element.classList

```markup
<script>
function loop(){
    for(var i=0; i<active.classList.length; i++){
        console.log(i, active.classList[i]);
    }
}
// 클래스를 추가
active.classList.add('추가할이름');
// 클라스 제거
active.classList.add('제할이름');
// 추가했다가 지웠다가 반복
.active.classList.toggle('이름');
</script>
```

## 조회 API

```markup
<ul>
    <li class="marked">html</li>
    <li>css</li>
    <li id="active">JavaScript
        <ul>
            <li>JavaScript Core</li>
            <li class="marked">DOM</li>
            <li class="marked">BOM</li>
        </ul>
    </li>
</ul>
<script>
    var list = document.getElementsByClassName('marked');
    console.group('document');
    for(var i=0; i<list.length; i++){
        console.log(list[i].textContent);
    }
    console.groupEnd();//html DOM BOM
     
     //active라는 그룹으로 묶고 active를 조회함.
    console.group('active');
    var active = document.getElementById('active');     
    var list = active.getElementsByClassName('marked');
    for(var i=0; i<list.length; i++){
        console.log(list[i].textContent);
    }
    console.groupEnd();//DOM BOM
</script>
```

## 속성 API

```markup
<a id="target" href="http://opentutorials.org">opentutorials</a>
<script>
var t = document.getElementById('target');
console.log(t.getAttribute('href')); // http://opentutorials.org

//속성을 바꿈.
t.setAttribute('title', 'opentutorials.org'); // title 속성의 값을 설정한다.

//속성을 지움.
t.removeAttribute('title'); // title 속성을 제거한다.

//title이 있는지 없는지 확인.
console.log(t.hasAttribute('title')); // true, title 속성의 존재여부를 확인한다.

</script>
```

```javascript
//    두개가 거의 같음.
    var target = document.getElementById('target');
    // attribute 방식
    target.setAttribute('class', 'important');
    // property 방식
    target.className = 'important';
    
```

atrribute방식                                                                      property

| class | className |
| :--- | :--- |
| readonly | readOnly |
| rowspan | rowSpan |
| colspan | colSpan |
| usemap | userMap |
| frameborder | frameBorder |
| for | htmlFor |
| maxlength | maxLength |

