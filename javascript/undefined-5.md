# 반복문

{% hint style="info" %}
반복문 loop iterate  
반복문은 while문 for문 가 있다

while\(조건\){반복해서 실행할 코드}
{% endhint %}

{% hint style="info" %}
프로그램은 숫자를 셀 때 0부터 센다.
{% endhint %}

```javascript
        var i = 0;
        while(i<10){
            document.write('hello <br />')
            i = i + 1;
        }
/*------------------둘이 같음-------------------------- */
        for (var i = 0; i < 10; i = i + 1) {
            document.write('hello <br />')
        }
```

{% hint style="info" %}
i = i + 1; 은 i++; ++i;는 거의 같다  
i = 0; alert\(i++\); 는 0한번 실행시키고 1 2 3 이렇게간다  
i = 0; alert\(++i\); 는 1 2 3 4 이렇게감.  
i++를 많이 씀.
{% endhint %}

```javascript
 //반복문의 제
           
           for(var i = 0; i < 10; i++){
               if(i === 5){
                   break;
                }
                document.write('hello' + i +'<br />') 
            }
            // 0 1 2 3 4 에서 멈춤

            for(var i = 0; i < 10; i++){
               if(i === 5){
                   continue;
                }
                document.write('hello' + i +'<br />')
            }
            // 5만 빠짐
```



