# 객체

## 29-32화 객체

```markup
    <h1>Object</h1>
    <h2>Create</h2>
    <script>
        var coworkers = {
            "programmer": "egoing",
            "designer": "leezche"
        };
        document.write("programmer : " + coworkers.programmer + "<br>");
        document.write("designer : " + coworkers.designer + "<br>");
        coworkers.bookkeeper = "duru";
        document.write("bookkeeper : " + coworkers.bookkeeper + "<br>");
        coworkers["data scientist"] = "taeho";
        document.write("data scientist : " + coworkers["data scientist"] + "<br>");
    </script>


    <h2>Iterate</h2>
    <script>
        for (var key in coworkers) {
            document.write(key + ' + ' + coworkers[key] + '<br>')
        }
        // key : var coworkers 안에있는 programmer, designer등... coworkers[key] : "egoing, leezche등"
    </script>


    <h2>Property & Method</h2>
    <script>
        coworkers.showAll = function () {
            for (var key in this) {
                document.write(key + ' + ' + this[key] + '<br>')
            }
        }
        coworkers.showAll();
        // coworkers.showAll = function(){} 이거와
        // function showAll (){}  두개 같은 것
    </script>
```

{% hint style="info" %}
메소드 : 객체에 소속된 함수  
프로퍼티 : 객체에 소속된 변 수  
{% endhint %}

## 33화 객체활용

```javascript
        var Links = {
            setColor: function (color) {
                var alist = document.querySelectorAll('a');
                var i = 0;
                while (i < alist.length) {
                    alist[i].style.color = color;
                    i = i + 1;
                }
            }
        }
        var Body = {
            setColor: function (color) {
                document.querySelector('body').style.color = color;
            },
            setBackgroundColor: function (color) {
                document.querySelector('body').style.backgroundColor = color;
            }
        }
        
        
        변경
        ---------------------------------------------------------------
        변경전
        
        
            function LinksSetColor(color) {
            var alist = document.querySelectorAll('a');
            var i = 0;
            while (i < alist.length) {
                alist[i].style.color = color;
                i = i + 1;
            }
        }

        
        function BodySetColor(color){
            document.querySelector('body').style.color = color;
        }
        function BodySetBackgroundColor(color){
            document.querySelector('body').style.backgroundColor = color;
        }
```



