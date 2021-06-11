# 프로퍼티 리스너, addEventListener\(\)

프로퍼티 리스너 \(권장x\)  


```markup
<input type="button" id="target" value="button" />
<script>
    var t = document.getElementById('target');
    t.onclick = function(){
        alert('Hello world');
    }
</script>
```

## addEventListener\(\)

```markup
<input type="button" id="target" value="button" />
<script>
    var t = document.getElementById('target');
    t.addEventListener('click', function(event){
        alert('Hello world, '+event.target.value);
    });
    // ie8 전버전은 addEventListener 대신 attachEvent 로 사용해야함.(onclick)
</script>
```



