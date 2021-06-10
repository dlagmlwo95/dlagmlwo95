# 함수 function

{% hint style="info" %}
function 함수명 \( \[인자 ... \[,인자\]\]\) {  
                         코드  
                         return 반환값   
}
{% endhint %}

```javascript
        function numbering(){
            document.write(1);
        }
        numbering();  // 1
/**********************************************/
        function numbering(){
            i = 0;
            while(i < 10){
                document.write(i);
                i += 1;
            }
        }
        numbering();    //0123456789
```

{% hint style="info" %}
반복문은 기계적으로 일정한 반복을 그자리에서 실행할 때 의미가 있음  
함수는 여러가지 맥락에서 반복되서 사용되는 경우 \(재사용성, 유지보수 용이,가독성 good\)
{% endhint %}

출력과 입력

```javascript
        //출력
        function get_member1(){
            return 'egoing';
        }
        function get_member2(){
            return 'egoing';
            return 'k8805';
            return 'leezche';
        }

        alert(get_member1());   // egoing
        alert(get_member2());   // egoing


        //입력
        function get_argument(arg){
            return arg * 1000;
        }

        alert(get_argument(1));  // 1000 1이 arg변수로 들어가게 됨.
        alert(get_argument(2));  // 2000
        // 여기서 arg는 매개변수(parameter)라고 부름
        // arg에 전달한 1 또는 2같은 값들은
        // 인자(argument) 라고 부름 alert(get_argument(1 <<<))

        function get_argument(arg1, arg2){
            return arg1 + arg2;
        }
        alert(get_argument(10,20));  // 30
        alert(get_argument(20,30));  // 50

```



함수의 다양한 정의 방법  


```javascript
두개가 같은 코드. 다른방법

        numbering = function (){
            i = 0;
            while(i<10){
                document.write(i);
                i += 1; 
            }
        }
        numbering();
/************같음*****************************/
        function numbering (){
            i = 0;
            while(i<10){
                document.write(i);
                i += 1; 
            }
        }
        numbering();


```

```javascript
        //익명함수
        (function numbering (){
            i = 0;
            while(i<10){
                document.write(i);
                i += 1; 
            }
        })();
```

