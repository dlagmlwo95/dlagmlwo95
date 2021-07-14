# Number, Math

## toString\(\)

```javascript
//10진수 -> 2진수/16진수

let num = 10;
num.toString(); // "10" 숫자 -> 문자
num.toString(2); // "1010" 숫자를 2진수로 나타냄

let num2 = 255;
num2.toString(16); // "ff"
```

### Math.ceil\(\) : 올림

### Math.floor\(\) : 내림

### Math.round\(\) : 반올림

### toFixed\(\) : 소수점 

```javascript
//문제: 소수점 둘째자리 까지 표현(셋째 자리에서 반올림)
let userRate = 30.1234;

// 1 답
Math.round(userRate * 100)/100  //30.12
// 2 답
userRate.toFixed(2); //30.12
```

