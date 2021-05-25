---
description: 핵심 33개!
---

# 노마드

1화  
콜스택 \(call stack\) : 자바스크립트가 함수를 실행하는 핸들 방법  
하나씩 차근차근 하는 것  
리스트가 존재하고 함수는 리스트에 추가된다. 실행이 완료되면 함수는 리스트에서 제거된다.

2화  
기초타입?\(Primitive type\)  
String : " " or ' '  
Number : 정수 or 소수점  
Undefined : 정의가 되지 않음  
Null : 존재하지 않음으로 정의 됨  
NaN \(Not A Number\) : 숫자와 문자\(?\)가 계산식 오류인 것

```text
console.log(hello === undefined)           ->  true
console.log(hello === null)                ->  false
```

3화  


```text
Value   :string,number,boolean,NaN,undefined,null 에서 가

let a = 50;
let b = a;
a = 10;
console.log(b);           -> 50




reference : array,object,function 에서 사

const sexy = ["kimchi", "potato"]
const pretty = sexy;
sexy.push("hello");
console.log(pretty)                  -> "kimchi", "potato", "hello"


const sexy = ["kimchi", "potato"]
const pretty = sexy;
sexy.push("hello");
pretty.push("lalala");
console.log(sexy)                     ->"kimchi", "potato", "hello","lalala"
```

4화

```text
console.log(4 + "hello");            -> 4hello
console.log(4 + 4 + "hello");        -> 8hello
console.log("" == true);             -> false
console.log(1 == true);              -> true
console.log(66 + true);              -> 67
console.log(66 + false);             -> 0


type conversion -> 자바스크립트가 값을 강제적으로 변환시킨다
console.log(66 + true); 에서 true를 1로 변환시켜 값이 67이 된다.

```

