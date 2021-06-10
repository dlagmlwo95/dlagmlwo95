# 함수, 매개변수, 인자, return

## 24-27화 함수\(function\) 매개변수, 인자, return

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

-------------------------------------------------------------
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

-------------------------------------------------------------
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

## 28화 함수의 활용 

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



