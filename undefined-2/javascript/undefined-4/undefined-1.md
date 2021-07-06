# 기본동작의 취소

## inline

리턴값이 false이면 기본 동작이 취소 check

```javascript
<p>
    <label>prevent event on</label><input id="prevent" type="checkbox" name="eventprevent" value="on" />
</p>
<p>
    <a href="http://opentutorials.org" onclick="if(document.getElementById('prevent').checked) return false;">opentutorials</a>
</p>
<p>
    <form action="http://opentutorials.org" onsubmit="if(document.getElementById('prevent').checked) return false;">
            <input type="submit" />
    </form>
</p>
```

## property 방식

리턴 값이 false이면 기본동작이 취소

```javascript
<script>
    document.querySelector('a').onclick = function(event){
        if(document.getElementById('prevent').checked)
            return false;
    };
     
    document.querySelector('form').onclick = function(event){
        if(document.getElementById('prevent').checked)
            return false;
    };
 
</script>
```

## addEventListener 방식

ie9 이하 버전에서는 event.returnValue를 false로 해야 한다  
preventDefault 메소드를 실행하면 기본 동작이 취소

```javascript
<script>
        document.querySelector('a').addEventListener('click', function(event){
        if(document.getElementById('prevent').checked)
            event.preventDefault();
        });
             
        document.querySelector('form').addEventListener('submit', function(event){
        if(document.getElementById('prevent').checked)
            event.preventDefault();
        });
 
</script>
```

