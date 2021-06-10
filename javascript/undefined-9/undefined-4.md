# 변수와 비교

변

```javascript
//변수 

var a = 1;   alert(a);   // 1
        
var first = 'coding'
alert(first + 'everybody');   //coding everybody

a = 100;        // a 는 변
a = a + 10;    // a : 110
a = a / 10     // a : 11
a = a - 10     // a : 1
a = a * 10     // a : 10
```



{% hint style="info" %}
bloolean\(블린\)은 true와 false
{% endhint %}



```javascript
    alert(1==2)                 //false
    alert(1==1)                 //true
    alert("one"=="two")         //false
    alert("one"=="one")         //true

    //1은 숫자 "1"은 문자
    alert(1 == "1")             //true
    alert(1 === "1")            //false 

    //null 값이 없다.(의도한것)
    //undefined 값이 정의되지 않았다.(의도하지않은것)

    alert(undefined == null);   //true
    alert(undefined === null);  //false
    alert(true == 1)            //true    true는 1로 인식함.
    alert(0 === -0)             //true
    //NaN 존재하지 않는 수
    alert(NaN === NaN)          //false   

    //!는 부정을 의미함
    alert(1!=2);                //true
    alert(1!=1);                //false
```



==는 같기만 하면 되고  
===는 값까지 같아야함.  
!는 부정의 의미를 갖고있음.

