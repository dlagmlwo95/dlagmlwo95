# 문자열로 노드 제어

{% hint style="info" %}
innerHTML \(자주사용\) 자기의 자식들  
outerHTML 자기포함
{% endhint %}

```markup
<ul id="target">
    <li>HTML</li>
    <li>CSS</li>
</ul>
<input type="button" onclick="get();" value="get" />
<input type="button" onclick="set();" value="set" />
<script>
    function get(){
        var target = document.getElementById('target');
        alert(target.innerHTML);
    }
    //결과 :     <li>HTML</li>    <li>CSS</li>
    function set(){
        var target = document.getElementById('target');
        target.innerHTML = "<li>JavaScript Core</li><li>BOM</li><li>DOM</li>";
    }
    // 결과 html 코드가 바뀜.
    function get(){
        var target = document.getElementById('target');
        alert(target.outerHTML);
    }
    // <ul id="target"> <li>HTML</li> <li>CSS</li> </ul> 
    
    
</script>
```

{% hint style="info" %}
innerText  태그는 안나옴.  
outerText
{% endhint %}

## insertAdjacentHTML\(\)

```markup
<!-- beforebegin-->
<ul id="target">
<!--afterbegin -->
    <li>CSS</li>
<!-- beforeend -->
</ul>
<!--afterend -->
<input type="button" onclick="beforebegin();" value="beforebegin" />
<input type="button" onclick="afterbegin();" value="afterbegin" />
<input type="button" onclick="beforeend();" value="beforeend" />
<input type="button" onclick="afterend();" value="afterend" />
<script>
    function beforebegin(){
        var target = document.getElementById('target');
        target.insertAdjacentHTML('beforebegin','<h1>Client Side</h1>');
    }
    function afterbegin(){
        var target = document.getElementById('target');
        target.insertAdjacentHTML('afterbegin','<li>HTML</li>');
    }
    function beforeend(){
        var target = document.getElementById('target');
        target.insertAdjacentHTML('beforeend','<li>JavaScript</li>');
    }
    function afterend(){
        var target = document.getElementById('target');
        target.insertAdjacentHTML('afterend','<h1>Server Side</h1>');
    }
</script>
```

