# 문서 로딩



```markup
<html>
    <body>
        <p id="target">Hello</p>
        <script>
        var t = document.getElementById('target');
        console.log(t);
        </script>
    </body>
</html>
```

## 

```markup
// DOMContentLoaded 문서에서 스크립트 작업을 할 수 있을 때
// 실행되기 때문에 이미지 다운로드를 기다릴 필요가 없다.
<html>
    <head>
        <script>
            window.addEventListener('load', function(){
                console.log('load');
            })
            window.addEventListener('DOMContentLoaded', function(){
                console.log('DOMContentLoaded');
            })
        </script>
    </head>
    <body>
        <p id="target">Hello</p>
    </body>
</html>
```

