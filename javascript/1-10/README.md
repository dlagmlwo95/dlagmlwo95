---
description: 생활코딩자바스크립트
---

# WEB2 JAVASCRIPT

## 2화 수업의 목

  
html의 웹브라우저에는 onclick 다음에 자바스크립트가 와야함. \(클릭 시 어떤식으로 동작할지.\)  
  
1.자바스크립트는 사용자와 상호작용하는 언어  
2. 웹브라우저는 화면에 출력되면 바꿀수 없음. 하지만 자바스크립트로 스타일을 바꿀 수 있음

## 12화 제어할 태그 선택하기

```markup
    <input type="button" value="night" onclick="
    document.querySelector('body').style.backgroundColor = 'black';
    document.querySelector('body').style.color = 'white';
    ">
    <input type="button" value="day" onclick="
    document.querySelector('body').style.backgroundColor = 'white';
    document.querySelector('body').style.color = 'black';
    ">
    
    <ol>
        <li><a href="#">HTML</a></li>
        <li><a href="#">CSS</a></li>
        <li><a href="#">JAVASCRIPT</a></li>
    </ol>
    <h2>Javascript</h2>
    <p>asklflksajd fdslkjf lsadfjioasvn calnvlksad dsf</p>
    
    검색법 : javascript select tag by css selector
    검색 : javascript element style
```

  
  
18화 리팩토링\(refactoring\)  
리팩토링 : 코드를 깔끔하게 만드는 

```markup
    <input id="night_day" type="button" value="night" onclick="
    if(document.querySelector('#night_day').value === 'night'){
        document.querySelector('body').style.backgroundColor = 'black';
        document.querySelector('body').style.color = 'white';
        document.querySelector('#night_day').value = 'day'
    } else {
        document.querySelector('body').style.backgroundColor = 'white';
        document.querySelector('body').style.color = 'black';
        document.querySelector('#night_day').value = 'night';
     }
    ">
------------------------------------------------------------------------    
    <input type="button" value="night" onclick="
    var target = document.querySelector('body');
    if(this.value === 'night'){
        target.style.backgroundColor = 'black';
        target.style.color = 'white';
        this.value = 'day';
    } else {
        target.style.backgroundColor = 'white';
        target.style.color = 'black';
        this.value = 'night';
     }
    ">
```



20화 배

```markup
    <h1>Array</h1>
    <h2>Syntax</h2>
    <script>
        var coworkers = ["egoing","leezche"];
    </script>

    <h2>get</h2>
    <script>
        document.write(coworkers[0]);    //-> egoing
    </script>

    <h2>add</h2>    
    <script>    // push 배열뒤 추가
        coworkers.push('duru');
        coworkers.push('taeho');
    </script>

    <h2>count</h2>
    <script>
        document.write(coworkers.length);       // ->2개
    </script>

    검색법 javascript array
```



21화 반복

```markup
    <h1>Loop</h1>
    <ul>
        <script>
            document.write('<li>1</li>');
            var i = 0;
            while (i < 3) {
                document.write('<li>2</li>');
                document.write('<li>3</li>');
                i = i + 1;
            }
            document.write('<li>4</li>');

            // while(){} -> (true)인 동안은 {}안에있는게 반복적으로 실행됨. 
            //              (false)가 되면 {}바깥쪽에 있는 코드가 실행됨.
        </script>
    </ul>
```



22화 배열과 반복

```markup
    <h1>Loop & Array</h1>
    <script>
        var coworkers = ['AAA', 'BBB', 'CCC','DDD'];
    </script>
    <h2>Co workers</h2>
    <ul>
        <script>
            var i = 0;
            while (i < coworkers.length) {
                document.write('<li>' + coworkers[i]+'</li>');
                i = i + 1;
            }
        </script>
    </ul>
```



23화 배열과 반복문의 활

```markup
    <input type="button" value="night" onclick="
    var target = document.querySelector('body');
    if(this.value === 'night'){
        target.style.backgroundColor = 'black';
        target.style.color = 'white';
        this.value = 'day';
        
        var alist = document.querySelectorAll('a');
        var i = 0;
        while(i < alist.length){
        alist[i].style.color='powderblue';
        i = i + 1;
        }
    } else {
        target.style.backgroundColor = 'white';
        target.style.color = 'black';
        this.value = 'night';
        
        var alist = document.querySelectorAll('a');
        var i = 0;
        while(i < alist.length){
        alist[i].style.color='blue';
        i = i + 1;
        }
     }
    ">
    
    ------------------------------------------------------------------
    
    
```

24-27화 함수\(function\) 매개변수, 인자, return

```markup
    <h1>Function</h1>
    <h2>Basic</h2>
    <ul>
        <script>
            function two() {
                document.write('<li>2-1</li>');
                document.write('<li>2-2</li>');
            }
            document.write('<li>1</li>');
            two();
            document.write('<li>3</li>');
            two();
        </script>
    </ul>


    <h2>Parameter(매개변수) & Argument(인자)</h2>
    <script>
        function onePlusOne() {
            document.write(1 + 1+'<br>');
        };
        onePlusOne();
        
        function sum(left, right) {
            document.write(left + right + '<br>');
        }
        sum(2, 3); // 5
        sum(3, 4); // 7
        
        /*function sum(매개변수left, right){
            document.write(left + right + '<br>')
        }
        sum(인자 2,3)*/
    </script>


    <h2>Return</h2>
    <script>
        function sum2(left, right) {
            return left + right;
        }
        document.write(sum2(2, 3) + '<br>');
        document.write('<div style="color:red;">' + sum2(2, 3) + '</div>');
        document.write('<div style="font-size:3rem">' + sum2(2, 3) + '</div>');
    </script>
```

28화 함수의 활

```markup
    <script>
        function nigthDayHandler(self){
        var target = document.querySelector('body');
        if (self.value === 'night') {
            target.style.backgroundColor = 'black';
            target.style.color = 'white';
            self.value = 'day';

            var alist = document.querySelectorAll('a');
            var i = 0;
            while (i < alist.length) {
                alist[i].style.color = 'powderblue';
                i = i + 1;
            }
        } else {
            target.style.backgroundColor = 'white';
            target.style.color = 'black';
            self.value = 'night';

            var alist = document.querySelectorAll('a');
            var i = 0;
            while (i < alist.length) {
                alist[i].style.color = 'blue';
                i = i + 1;
            }
        }
    }
    </script>

    <input type="button" value="night" onclick="
        nigthDayHandler(this);
    ">
    
    <!-- input onclick안에 있던 코드를 밖으로 빼서 function으로 묶어줌.
    nigthDayHandler(this)
    this => 자신이 속한 태그 -->
```



29-32화 객체

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
        // coworkers.showAll = function(){}      function showAll (){}  두개 같은 것
        // 메소드 : 객체에 소속된 함수.
        // 프로퍼티 : 객체에 소속된 변수
    </script>
```

33화 객체활용

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



34화 파일로 쪼개서 정리정돈하기  
&lt;script src=""&gt; 파일을 만들어서 정리하기  
  
library : jquery 같은 것   
UI : User Interface \(사용자 장치\)  
API : Application Programming Interface \(프로그래밍 장치\)

