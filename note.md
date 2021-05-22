# 생활코딩

## 생활코딩 자바스크립트 노트

2화 수업의 목적  
1.자바스크립트는 사용자와 상호작용하는 언어  
2. 웹브라우저는 화면에 출력되면 바꿀수 없음. 하지만 자바스크립트로 스타일을 바꿀 수 있음

4화 HTML과 JS의 만남:이벤트  
이벤트 onclick 뒤엔 자바스크립트가 와야함, 

5화 HTML과 JS의 만남\(콘솔 console\)  
length 문자의 갯수를 알려주는 코드   
  
6화 데이터타입 - 문자열과 숫자  
'문자열'

12화 제어할 태그 선택하기  
onclick= "document.querySelector\('body'\).style.background-color = 'black'; "

14화 조건문 예고  
if else

15화 비교 연산자와 블리언  
Number String\(문자열\) Boolean\(true,false\)  
true false 를 블리언이라고 함.

16화 조건문  
if\(\){}  
else{}

18화 리팩토링 중복의 제거  
리팩토링 : 코딩을 효율적으로 만드는 것

20화 배열  
배열은 \[ \] \(대괄호\)  
검색 javascript array 해서 알아보기 \(push 등등\)

21화 반복문\(Loop\)  
while\(\)

```text
22화 배열과 반복문

<h1>Loop & Array</h1>
<script>
    var coworkers = ['egoing','leezche','duru','taeho'];
</script>
<h2>Co workers</h2>
<ul>
    <script>
        var i = 0;
        while(i < cowork29ers.length ){
        document.write('<li>'+coworkers[i]+'</li>');
        i = i + 1;
        }
    </script>
    
    
    
```

24화 함수예고 25화 함수  
function nightDayHandler\(self\){ }  함수를 사용하여 묶음.  
사용시 nightDayHandler\(this\) &lt;-함수명만 사용하면 됨.  
function two\(\){}         
사용시 two\(\);

```text
26화 함수 : 매개변수와 인자
Parameter(매개변수) & Argument(인자) 
sum(매개변수 left, right)
sum(인자 2,3)


        function onePlusOne(){
            document.write(1+1+'<br>');
        }
        onePlusOne();
        function sum(left, right){
            document.write(left+right+'<br>');
        }
        sum(2,3);    //5
        sum(3,4);    //7
```

#### 27화 함수\(리턴\)  이해가 되지 않음! 

29화 객체 예고  
function BodySetColor\(color\){document.querySelector\('body'\).style.color = color ; } 함수로 묶은 다음  
밑에 함수에 BodySetColor\('red'\) // 또는 Body.setColor\('red'\) 이런식으로 바꾼다   
  
document.querySelector\('body'\).style.color = color 에서    
객체 : document.    메소드: 객체안에있는함수는 querySelector\('body'\).style.color = color ;

```text
30화 객체 쓰기와 읽기
객체 : ex) var coworkers = ['egoing' , 'leezche']; 
는 순서대로 저장되지만 순서대로 없이 저장되는것이 객체       
        
        
        
        
          var coworkers = {
            "programmer" : "egoing",
            "designer" : "leezche"
        };
        document.write("programmer : " + coworkers.programmer + "<br>");
        coworkers.bookkeeper = "duru";
        document.write("bookkeeper : " + coworkers.bookkeeper + "<br>");
        
        
여기에서 띄어쓰기는 coworkers뒤에 점을 빼고 대괄호[] 후에 ""
        coworkers["data scientist"] = "taeho";
        document.write("data scientist : " + coworkers["data scientist"] + "<br>");
```

객체에 소속된 함수를 메소드라고 한

