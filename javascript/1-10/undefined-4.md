# 반복문과 배열의 활용

## 21화 반복문\(Loop\)

{% hint style="info" %}
반복문은 while \(\){}
{% endhint %}

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



## 22화 배열과 반복

```markup
    <h1>Loop & Array</h1>
    <script>
        var coworkers = ['AAA', 'BBB', 'CCC','DDD'];
    </script>
    <h2>Co workers</h2>
    <ul>
        <script>
            var i = 0;
            //배열명.length 이런식으로 많이 씀.
            while (i < coworkers.length) {
                document.write('<li>' + coworkers[i]+'</li>');
                i = i + 1;
            }
        </script>
    </ul>
```



## 23화 배열과 반복문의 활

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
```

