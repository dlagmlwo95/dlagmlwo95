# 제로초

1-3화  
\( \) : parentheses  
{ } : braces  
\[ \] : brackets

2-2화  
typeof로 문자열인지 확인 할 수 있다.  
ex\) typeof "asdf"     // typeof 0x1a1   // 



2-4화  
parseInt\('123'\) 문자를 숫자\(정수\)로 바꾸는 명령어

2-5화 불값\(boolean\)  
== : 같다\(값\)  
!= : 같지않다.  
=== : 같다\(자료형, 값\)  
!== : 같지않다.  
  
ex\)  '1' === 1;       -&gt; false  
       1 === true     -&gt; false  
       1 != '1'            -&gt; false  
       1 !== '1'           -&gt; true



2-10화 변수명짓기  
특수문자는 $ \_ 두개만 된다.  
숫자는 맨 앞에 나오면 안된다.  
띄어쓰기 안된다.



2-11화 변수 수정하기  
let number = 16  
number /=4           // number = number / 4    -&gt; 4



2-12화 상수  
let 외에도 변수를 선언하는 예약어로는 const 와 var이 있다.  
최근에 let을 더 많이 쓰는 추세,  
var은 옛 코  


2-14화 else,else if, switch  
  
if\(조건식\){  
   동작문;  
} else if \(조건식\){  
   동작문  
} else {  
   동작문;  
}  
switch문은 영상 참조.



2-15화 조건부 연산자  
조건식 ? 참일 때 실행되는 식 : 거짓일 때 실행되는 식



2-16화 반복문\(while\)  
무한반복문을 하면 에러남.  
i = i + 1   // i += 1  //  i++

```text
let i = 0;
while(i<100) {
  console.log('hello');
  i++;
}
```



2-17화 반복문\(for\)  
for \(시작; 조건식; 종료식\)  
     동작문  
  
for문은 실행할때 시작 , 조건식 , 동작문, 종료식 순으로 실행한다.  
for문의 시작, 조건식, 종료식은 생략할 수 있다.  


```text
for(let i = 0; i < 100; i++){
console.log('hello');
}
```

```text
while문과 for문 비교 (같음)

let i = 0;
while(i < 100){
  console.log('hello');
  i++;
}

for(let i = 0; i < 100; i++;){
  console.log('hello');
}
```



2-18화 break와 continue

```text
break

let i = 0;
while(true){
  if ( i === 5) break;
  i++;
}
console.log(i);
```

```text
continue

let i = 0;
while (i < 10) {     // 홀수만 console.log
  i++;
  if ( i % 2 === 0) {     // i % 2 = 짝수   (i를 2로 나눠서 나머지가 0이 나오는 수)
  continue
}
console.log(i);
```



2-19화 중첩 반복문\(어려움, 잘 모름\) 

```text
for (let i = 0; i < 10; i++){
  for (let j = 0; j < 10; j++){
    console.log(i,j);
  }
}

0 0
0 1
...
0 9
1 0
1 1
1 2
...
9 9

-------------------------------------------

for (let i = 0; i < 5; i++){
  if(i % 2 === 0) continue;
  for ( let j = 0; j < 5; j++){
    if ( j % 2 === 0) continue;
    for ( let k = 0; k < 5; k++){
      if ( k % 2 === 0 ) continue;
      console.log(i, j, k);
    }
  }
}

// i==0 continue
// i==1 j==0 continue
// i==1 j==1 k==0 continue
// i==1 j==1 k==1 console.log(1, 1, 1)
// i==1 j==1 k==2 continue
// i==i j==1 k==3 console.log(1, 1, 3)
// i==1 j==1 k==4 continue
// i==1 j==1 k==5 조건x
// i==1 j==2 continue
// i==1 j==3 k==0 continue
// i==1 j==3 k==1 console.log(1, 3, 1)
......
```

2-21 배열 기본  
const fruits = \['사과','오렌지','포도'\]  
console.log\(fruits\[1\]\);         -&gt; 오렌지  
  
배열 안에는 배열을 넣을 수 있다  
const arrayOfArray = \[\[1,2,3\], \[4,5\]\]  
arrayOfArray\[0\];    //\[1,2,3\]  
  
1.요소가 몇개인지 궁금할 때  
console.log\(이름.length\);  
2.마지막 요소를 찾을 때  
console.log\(findLastElement\[findLastElement.length - 1\]\);  
3.맨 앞에 추가 할 때  
이름.unshift\('내용'\)                          shift &lt;-&gt; unshift  
4.맨 뒤에 추가 할 때  
이름.push\('내용'\)                             push &lt;-&gt; pop  
  
  
  
이름.splice\(1,2\)                   //1은 몇번째인지 알려주는 것, 2는 1번째에서 뒤에 2개를 지운다.  
이름.splice\(1\)                      // 1번째부터 다 지운다.  
이름.splice\(1, 3, '가', '나'\)   // 1번째부터 3개를 지우고 그 자리에 '가' '나' 를 채워넣는다.  
  
5.검색기능  
const result = 이름.includes\('내용'\)  
const에는 새로운 값을 대입하지 못한다.  
6. 몇번째 있는 지 검색  
const result = 이름.indexOf\('내용'\)          // 없으면 -1  
const result = 이름.lastindexOf\('내용'\)   //뒤에서부터



2-24화 함수 기본  
function\(\) {}  
\(\) =&gt; {}  
  
이름 붙이기  
function a \(\){}                       함수선언문  
const b = function\(\) {};        함수표현식  
const c = \(\) =&gt; {};  
함수는 return undefined 가 생략 됨.

2-25화 매개변수와 인수  
function a\(parameter\){  
  console.log\(parameter\);  
}  
a\('argument'\)  
선언 parameter 매개변수 ,호출 argument 인 

```text
function a(w, x, y, z){
  console.log(w, x, y, z);
  console.log(arguments);
}
a('Hello', 'Parameter', 'Argument')

// 실행결과 //
Hello Parameter Argument undefined
Arguments(3) ['Hello', 'Parameter', 'Argument']
```

  
2-26화 객체 리터널 기본  
배열 대신에 객체 리터널을 쓰는 이유는 값의 이름이 각 각 있다.  
const 객체 = {  
  속성 1 이름: 속성1값,  
  속성 2 이름: 속성2값,  
  속성 3 이름: 속성3값,  
}

```text
const zerocho = {
  name : '조현영',
  year : 1994,
  date : 12,
  gender : 'M',
};
console.log(zerocho.name);
console.log(zerocho['name']);
```

객체 안에 있는 함수는 메소드라고 부른다.



2-27화 객체의 비교\(어려움, 잘 모름\)  
객체끼리는 비교하면 서로 false가 나온다

