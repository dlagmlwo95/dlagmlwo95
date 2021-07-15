# 문자열 메소드

html 코드는 ' '로 하는 것이 편하다.  
영어로된 문장은는 " "가 편하다.  
\` 은 여러줄을 가능.  


```javascript
let desc = `오늘은 맑고화창한
날씨가 계속.`;

let desc = '오늘은 맑고 화창한/n날씨가 계속.';

```

### length

```javascript
let desc = '안녕하세요';
desc.length //6
```

### toUpperCase\(\) 대문자

### toLowerCase\(\) 소문자

### str.indexOf\(\) : 문자가 몇번째 위치인지 알려줌.

```javascript
let desc = "Hi guys. Nice to meet you";
desc.indexOf(to) // 14 
desc.indexOf('man') // 찾는 문자가 없으면 -1 로 나옴.

//if 문을 쓸때는 이렇게 ( indexOf는 0 이기 때문에 false나옴. 그래서 > -1 추)
if(desc.indexOf('Hi' > -1) ){
    console.log('Hi가 포함된 문장입니다.');
}
```

### str.slice\(n, m\) : n은 시작점. m은 생략가능\(문자열끝까지\)

```javascript
 
let desc = "abcdefg";
desc.slice(2) // cdefg
desc.slice(0,5) // abcde
desc.slice(2,-2) // cde
```

### str.substring\(n,m\) : n과 m사이 문자열을 반환.

```javascript
let desc = "abcdefg";
desc.substr(2,4) // cdef
desc.substr(-4,2) // de
```

### str.trim\(\) : 앞 뒤 공백 제거

### str.repeat\(\) : 반복

```javascript
let desc='hi';
desc.repeat(3)// hihihi
```

### 문자열 비교

아스키번호.

